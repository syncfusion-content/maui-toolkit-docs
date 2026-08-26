---
layout: post
title: Splitter Customization in .NET MAUI Grid Splitter | Syncfusion®
description: Learn how to customize the appearance and behavior of the Syncfusion® .NET MAUI Grid Splitter control.
platform: maui-toolkit
control: SfGridSplitter
documentation: UG
---

# Splitter Customization in .NET MAUI Grid Splitter

The [.NET MAUI Grid Splitter]() control provides several customization options that allow you to modify the layout behavior and appearance of splitter separators. You can control pane arrangement, separator thickness, colors, resize icons, and right-to-left layout behavior.

## Orientation

The `Orientation` property determines how the panes are arranged within the Grid Splitter.

The `GridSplitterOrientation` enum contains the following values:

| Value | Description |
|---------|---------|
| `Horizontal` | Arranges panes side-by-side from left to right. Resizing changes pane widths. |
| `Vertical` | Arranges panes from top to bottom. Resizing changes pane heights. |

### Horizontal orientation

By default, the Grid Splitter uses horizontal orientation.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter Orientation="Horizontal">
    <gridSplitter:SplitterPane />
    <gridSplitter:SplitterPane />
</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

### Vertical orientation

The following example arranges panes vertically in Grid Splitter.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter Orientation="Vertical">
    <gridSplitter:SplitterPane />
    <gridSplitter:SplitterPane />
</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

## SeparatorSize

The `SeparatorSize` property specifies the thickness of the separator displayed between adjacent panes. The default value is `8`.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter SeparatorSize="10">
    <gridSplitter:SplitterPane />
    <gridSplitter:SplitterPane />
</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

## SeparatorBackground

The `SeparatorBackground` property allows you to customize the appearance of the separator between panes.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter SeparatorBackground="LightGray">
    <gridSplitter:SplitterPane />
    <gridSplitter:SplitterPane />
</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

You can use any solid color, dynamic resource, or theme resource to style the separator.

### Using AppThemeBinding

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter
    SeparatorBackground="{AppThemeBinding Light=#E0E0E0, Dark=#3C3C3C}" />

{% endhighlight %}
{% endtabs %}

## ResizeIconColor

The `ResizeIconColor` property customizes the color of the built-in resize indicator displayed in the separator.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter ResizeIconColor="Blue">
    <gridSplitter:SplitterPane />
    <gridSplitter:SplitterPane />
</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

## ExpandCollapseIconColor

The `ExpandCollapseIconColor` property customizes the color of the expand and collapse icon displayed on collapsible panes.

The icon is displayed only when the associated pane has its `IsCollapsible` property set to `True`.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter ExpandCollapseIconColor="Red">
        <gridSplitter:SplitterPane IsCollapsible="True" />
        <gridSplitter:SplitterPane />
</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

## ResizeIconTemplate

The `ResizeIconTemplate` property allows you to replace the default resize icon with custom content.

The template is applied to all separators created by the GridSplitter.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter>
    <gridSplitter:SfGridSplitter.ResizeIconTemplate>
        <DataTemplate>
            <Image Source="resize_handle.png"
                   HeightRequest="16"
                   WidthRequest="16" />
        </DataTemplate>
    </gridSplitter:SfGridSplitter.ResizeIconTemplate>

    <gridSplitter:SplitterPane />
    <gridSplitter:SplitterPane />

</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

### Custom resize icon using shapes

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter>
    <gridSplitter:SfGridSplitter.ResizeIconTemplate>
        <DataTemplate>
            <HorizontalStackLayout Spacing="2"
                                   HorizontalOptions="Center"
                                   VerticalOptions="Center">
                <BoxView WidthRequest="2"
                         HeightRequest="12"
                         olor="Gray" />
                <BoxView WidthRequest="2"
                         HeightRequest="12"
                         Color="Gray" />
                <BoxView WidthRequest="2"
                         HeightRequest="12"
                         Color="Gray" />
            </HorizontalStackLayout>
        </DataTemplate>
    </gridSplitter:SfGridSplitter.ResizeIconTemplate>
</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

## Right-to-left (RTL)

The Grid Splitter supports right-to-left layouts through the `FlowDirection` property.

When RTL is enabled:

* Pane arrangement flows from right to left.
* Separator interactions are mirrored automatically.
* Expand and collapse icons are rendered on the opposite side of the separator.
* Resize behavior remains consistent with the application layout direction.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter FlowDirection="RightToLeft">
        <gridSplitter:SplitterPane>
            <Label Text="Pane 1"/>
        </gridSplitter:SplitterPane>
        <gridSplitter:SplitterPane>
            <Label Text="Pane 2"/>
        </gridSplitter:SplitterPane>
</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

## Combined customization example

The following example demonstrates several customization properties together.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter Orientation="Horizontal"
                             SeparatorSize="8" 
                             SeparatorBackground="#E0E0E0" 
                             ResizeIconColor="#6750A4" ExpandCollapseIconColor="#6750A4">
        <gridSplitter:SplitterPane IsCollapsible="True"
                                   Background="LightBlue">
            <Label Text="Pane 1"/>
        </gridSplitter:SplitterPane>
        <gridSplitter:SplitterPane Background="LightGreen">
            <Label Text="Pane 2"/>
        </gridSplitter:SplitterPane>
</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

In this example, the Grid Splitter uses a custom separator thickness, customized separator appearance, custom icon colors, and pane collapse support to create a personalized splitter layout.