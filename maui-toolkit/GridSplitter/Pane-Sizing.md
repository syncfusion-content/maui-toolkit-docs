---
layout: post
title: Pane Sizing in .NET MAUI Grid Splitter | Syncfusion®
description: Learn how to control pane sizing in the Syncfusion® .NET MAUI Grid Splitter control using Size, MinimumSize, and MaximumSize properties.
platform: maui-toolkit
control: SfGridSplitter
documentation: UG
---

# Pane Sizing in .NET MAUI Grid Splitter

The `.NET MAUI Grid Splitter` control provides flexible sizing options through the `Size`, `MinimumSize`, and `MaximumSize` properties of the `SplitterPane` class. These properties help define the initial pane size and control how far a pane can be resized at runtime.

## Size

The `Size` property specifies the initial size of a pane and determines how available space is distributed among adjacent panes.

The default value is `1*`.

A pane with a larger size value occupies more space relative to panes with smaller values.

### Equal-sized panes

The following example creates three panes with equal widths.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter>

    <gridSplitter:SplitterPane Size="1*">
        <Label Text="Pane 1"/>
    </gridSplitter:SplitterPane>

    <gridSplitter:SplitterPane Size="1*">
        <Label Text="Pane 2"/>
    </gridSplitter:SplitterPane>

    <gridSplitter:SplitterPane Size="1*">
        <Label Text="Pane 3"/>
    </gridSplitter:SplitterPane>

</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

### Proportional pane sizing

You can assign different size values to allocate space proportionally.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter>

    <gridSplitter:SplitterPane Size="1*">
        <Label Text="Pane 1"/>
    </gridSplitter:SplitterPane>

    <gridSplitter:SplitterPane Size="2*">
        <Label Text="Pane 2"/>
    </gridSplitter:SplitterPane>

    <gridSplitter:SplitterPane Size="3*">
        <Label Text="Pane 3"/>
    </gridSplitter:SplitterPane>

</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

In this example, the panes are distributed in a ratio of 1*:2*:3*.

---

## MinimumSize

The `MinimumSize` property specifies the smallest size to which a pane can be resized.

The default value is `0`.

When a user drags a separator, the pane cannot be resized below its minimum size.

### Restrict pane shrinking

The following example prevents a pane from shrinking below 120 device-independent units.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SplitterPane MinimumSize="120">
    <Label Text="Minimum Size = 120"/>
</gridSplitter:SplitterPane>

{% endhighlight %}
{% highlight c# %}

SplitterPane pane = new SplitterPane()
{
    MinimumSize = 120
};

{% endhighlight %}
{% endtabs %}

### Multiple panes with minimum size constraints

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter>
    <gridSplitter:SplitterPane Size="1*"
                               MinimumSize="100"/>
    <gridSplitter:SplitterPane Size="2*"
                               MinimumSize="150"/>
</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

When resizing, each pane stops shrinking once its configured minimum size is reached.

---

## MaximumSize

The `MaximumSize` property specifies the largest size a pane can occupy.

The default value is `double.PositiveInfinity`.

When resizing, the pane cannot grow beyond the configured maximum size.

### Restrict pane expansion

{% tabs %}
{% highlight xaml %}

<gridSplitter:SplitterPane MaximumSize="300">
    <Label Text="Maximum Size = 300"/>
</gridSplitter:SplitterPane>

{% endhighlight %}
{% highlight c# %}

SplitterPane pane = new SplitterPane()
{
    MaximumSize = 300
};

{% endhighlight %}
{% endtabs %}

### Multiple panes with maximum size constraints

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter>
        <gridSplitter:SplitterPane Size="1*"
                                   MaximumSize="250"/>
        <gridSplitter:SplitterPane Size="2*"
                                   MaximumSize="400"/>
</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

In this scenario, pane sizes cannot exceed their configured maximum values, even when additional space is available.

---

## Use MinimumSize and MaximumSize together

You can combine both properties to define a valid resizing range for a pane.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SplitterPane Size="2*"
                           MinimumSize="100"
                           MaximumSize="400">

    <Label Text="Resizable between 100 and 400"/>

</gridSplitter:SplitterPane>

{% endhighlight %}
{% endtabs %}

The pane can now be resized only within the range of **100 to 400 device-independent units**.

---

## Dynamic size updates

The `Size` property supports two-way updates. When a user resizes a pane, the updated size is reflected in the `Size` property.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SplitterPane Size="{Binding PaneSize, Mode=TwoWay}" />

{% endhighlight %}
{% endtabs %}

This allows pane sizes to be tracked and persisted using MVVM.

---

## Sizing behavior during resize

When a separator is dragged:

* The size of the two adjacent panes is updated.
* `MinimumSize` prevents panes from becoming smaller than the configured limit.
* `MaximumSize` prevents panes from growing beyond the configured limit.
* Other panes in the Grid Splitter are not affected.
* Layout integrity is maintained automatically.

---

## Combined sizing example

The following example demonstrates all sizing properties together.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter >
    <gridSplitter:SplitterPane Size="1*"
                               MinimumSize="120"
                               MaximumSize="250"
                            Background="#E8DEF8">
        <Label Text="Navigation Pane"/>
    </gridSplitter:SplitterPane>
    <gridSplitter:SplitterPane Size="2*"
                            MinimumSize="250"
                            Background="#F7F2FA">
        <Label Text="Content Pane"/>
    </gridSplitter:SplitterPane>
    <gridSplitter:SplitterPane Size="1*" 
                               MinimumSize="150" 
                               MaximumSize="350"
                               Background="#D0BCFF">
        <Label Text="Details Pane"/>
    </gridSplitter:SplitterPane>
</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

In this example:

* The panes are initially distributed using a **1:2:1** size ratio.
* Each pane defines its own resizing limits.
* Users can resize panes while respecting the configured minimum and maximum size constraints.
* The Grid Splitter automatically maintains a valid layout throughout the resize operation.