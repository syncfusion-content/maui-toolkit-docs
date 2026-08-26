---
layout: post
title: Pane Customization in .NET MAUI Grid Splitter | Syncfusion®
description: Learn how to customize pane sizes using the Syncfusion® .NET MAUI Grid Splitter control for flexible, resizable user interfaces.
platform: maui-toolkit
control: SfGridSplitter
documentation: UG
---

# Pane Customization in .NET MAUI Grid Splitter

The [SplitterPane]() class represents an individual pane within the [SfGridSplitter]() control. Each pane can host custom content and provides several properties to control its appearance and behavior.

The following sections describe the pane customization options available in the Grid Splitter control.

## Content

The `Content` property allows you to display any .NET MAUI view inside a pane. A pane can host controls such as labels, images, layouts, charts, data grids, editors, or any custom view.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SplitterPane>
    <VerticalStackLayout Padding="16">
        <Label Text="Customer Details"
               FontSize="20"
               FontAttributes="Bold" />
        <Label Text="View and manage customer information." />
    </VerticalStackLayout>
</gridSplitter:SplitterPane>

{% endhighlight %}

{% highlight c# %}

SplitterPane pane = new SplitterPane()
{
    Content = new VerticalStackLayout()
    {
        Children =
        {
            new Label
            {
                Text = "Customer Details"
            },
            new Label
            {
                Text = "View and manage customer information."
            }
        }
    }
};

{% endhighlight %}
{% endtabs %}

## Background

The `Background` property customizes the pane background using a `Brush`.

### Set a solid background color

{% tabs %}
{% highlight xaml %}

<gridSplitter:SplitterPane Background="LightBlue">
    <Label Text="Pane Content"/>
</gridSplitter:SplitterPane>

{% endhighlight %}

{% highlight c# %}

SplitterPane pane = new SplitterPane()
{
    Background = Brush.LightBlue
};

{% endhighlight %}
{% endtabs %}

### Use a gradient background

{% tabs %}
{% highlight xaml %}

<gridSplitter:SplitterPane>
    <gridSplitter:SplitterPane.Background>
        <LinearGradientBrush
            StartPoint="0,0"
            EndPoint="1,1">
            <GradientStop Color="#6750A4"
                          Offset="0.0"/>
            <GradientStop Color="#D0BCFF"
                          Offset="1.0"/>
        </LinearGradientBrush>
    </gridSplitter:SplitterPane.Background>
</gridSplitter:SplitterPane>

{% endhighlight %}
{% endtabs %}

---

## IsCollapsible

The `IsCollapsible` property determines whether a pane can be expanded or collapsed by the user.

The default value is `false`.

When enabled, an expand/collapse icon is displayed on the associated separator.

### Enable collapse support

{% tabs %}
{% highlight xaml %}

<gridSplitter:SplitterPane IsCollapsible="True">
    <Label Text="Collapsible Pane"/>
</gridSplitter:SplitterPane>

{% endhighlight %}

{% highlight c# %}

SplitterPane pane = new SplitterPane()
{
    IsCollapsible = true
};

{% endhighlight %}
{% endtabs %}

### Multiple collapsible panes

In this example, the first two panes can be collapsed or expanded through their corresponding separators.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter>
    <gridSplitter:SplitterPane IsCollapsible="True"/>
    <gridSplitter:SplitterPane IsCollapsible="True"/>
    <gridSplitter:SplitterPane />
</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

---

## IsResizable

The `IsResizable` property controls whether a pane can participate in drag-based resizing.

The default value is `true`.

When this property is set to `false`, the separator associated with the pane ignores resize gestures.

### Disable pane resizing

{% tabs %}
{% highlight xaml %}

<gridSplitter:SplitterPane IsResizable="False">
    <Label Text="Fixed Pane"/>
</gridSplitter:SplitterPane>

{% endhighlight %}

{% highlight c# %}

SplitterPane pane = new SplitterPane()
{
    IsResizable = false
};

{% endhighlight %}
{% endtabs %}

### Create a fixed navigation pane

The following example shows a non-resizable navigation pane with a resizable content pane.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter>

    <gridSplitter:SplitterPane
            IsResizable="False"
            Background="#ECECEC">
        <Label Text="Navigation"/>

    </gridSplitter:SplitterPane>

    <gridSplitter:SplitterPane>
        <Label Text="Content Area"/>

    </gridSplitter:SplitterPane>

</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

This is useful when certain regions must maintain a fixed layout while allowing other panes to resize.

---

## IsCollapsed

The `IsCollapsed` property specifies whether a pane is currently collapsed.

The default value is `false`.

A collapsed pane occupies no layout space and can be expanded later either by user interaction or programmatically.

### Collapse a pane initially

{% tabs %}
{% highlight xaml %}

<gridSplitter:SplitterPane IsCollapsible="True"
                           IsCollapsed="True">
    <Label Text="Initially Collapsed"/>
</gridSplitter:SplitterPane>

{% endhighlight %}

{% highlight c# %}

SplitterPane pane = new SplitterPane()
{
    IsCollapsible = true,
    IsCollapsed = true
};

{% endhighlight %}
{% endtabs %}

### Collapse and expand panes programmatically

You can collapse or expand panes using the GridSplitter methods.

{% tabs %}
{% highlight c# %}

gridSplitter.CollapsePane(1);

gridSplitter.ExpandPane(1);

{% endhighlight %}
{% endtabs %}

### Two-way data binding

The `IsCollapsed` property supports two-way binding, allowing the pane state to be synchronized with a view model.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SplitterPane
    IsCollapsible="True"
    IsCollapsed="{Binding IsPaneCollapsed, Mode=TwoWay}" />

{% endhighlight %}
{% endtabs %}

---

## Combined pane customization

The following example demonstrates multiple pane customization options together.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter
    Orientation="Horizontal">

        <gridSplitter:SplitterPane
            Background="#E8DEF8"
            IsCollapsible="True"
            Size="1">

            <VerticalStackLayout Padding="16">

                <Label Text="Navigation"
                       FontAttributes="Bold"/>

            </VerticalStackLayout>

        </gridSplitter:SplitterPane>

        <gridSplitter:SplitterPane
            Background="#F7F2FA"
            IsResizable="True"
            Size="2">

            <VerticalStackLayout Padding="16">

                <Label Text="Content Area"
                       FontAttributes="Bold"/>

            </VerticalStackLayout>

        </gridSplitter:SplitterPane>

</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

In this example:

* The first pane uses a custom background color.
* The first pane can be collapsed and expanded.
* The second pane contains custom content.
* Both panes participate in layout sizing through the splitter.
* Users can resize the panes using the separator between them.