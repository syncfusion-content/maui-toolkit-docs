---
layout: post
title: Axis labels in .NET MAUI Cartesian Chart control | Syncfusion
description: Learn here all about axis labels and their customization in Syncfusion® .NET MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
keywords: .net maui chart axis labels, axis labels customization .net maui, syncfusion maui chart axis labels, cartesian chart axis labels maui, customize axis labels .net maui chart.
---

# Axis Labels in .NET MAUI Cartesian Chart

Axis labels are used to display units, measurements, or category values on an axis to help users visualize data more effectively. Labels are generated based on the axis range and the values bound to the [XBindingPath](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartSeries.html#Syncfusion_Maui_Toolkit_Charts_ChartSeries_XBindingPath) or [YBindingPath](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.XYDataSeries.html#Syncfusion_Maui_Toolkit_Charts_XYDataSeries_YBindingPath) properties of the series.

## Positioning the labels

The [LabelsPosition](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html#Syncfusion_Maui_Toolkit_Charts_ChartAxis_LabelsPosition) property is used to position axis labels inside or outside the chart area. The default value is `AxisElementPosition.Outside`.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    . . .
    <chart:SfCartesianChart.XAxes>
        <chart:CategoryAxis/>
    </chart:SfCartesianChart.XAxes>

    <chart:SfCartesianChart.YAxes>
        <chart:NumericalAxis LabelsPosition="Inside"/>
    </chart:SfCartesianChart.YAxes>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
CategoryAxis primaryAxis = new CategoryAxis();
NumericalAxis secondaryAxis = new NumericalAxis()
{
    LabelsPosition = AxisElementPosition.Inside  // Set the position of the axis labels to be inside the plot area
};

chart.XAxes.Add(primaryAxis);
chart.YAxes.Add(secondaryAxis);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Axis label inside position in .NET MAUI Chart.](axis_images/maui_chart_inside_label.png)

## Label Rotation

The [LabelRotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html#Syncfusion_Maui_Toolkit_Charts_ChartAxis_LabelRotation) property is used to define the angle for the label content.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    . . .
    <chart:SfCartesianChart.XAxes>
        <chart:CategoryAxis LabelRotation="90"/>
    </chart:SfCartesianChart.XAxes>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
. . .
CategoryAxis primaryAxis = new CategoryAxis()
{
    LabelRotation = 90 // Set the label rotation of the axis to 90 degrees
};
chart.XAxes.Add(primaryAxis);

this.Content = chart;
{% endhighlight %}

{% endtabs %}

## Label customization

The [LabelStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html#Syncfusion_Maui_Toolkit_Charts_ChartAxis_LabelStyle) property of the axis provides options to customize the font-family, font-size, font-attributes, and text color of axis labels. The axis labels can be customized using the following properties:

* `Background` - Gets or sets the background color of the labels.
* `CornerRadius` - Gets or sets a value that defines the rounded corners for labels.
* `FontAttributes` - Gets or sets the font style for the label.
* `FontFamily` - Gets or sets the font family name for the label.
* `FontSize` - Gets or sets the font size for the label.
* `Margin` - Gets or sets the margin of the label to customize the appearance of label. 
* `Stroke` - Gets or sets the border stroke color of the labels.
* `StrokeWidth` - Gets or sets the border thickness of the label.
* `TextColor` - Gets or sets the color for the text of the label.
* `LabelFormat` - Gets or sets the label format. This property is used to set numeric or date-time format to the chart axis label.
* `LabelAlignment` - Gets or sets the axis label at start, end, and center positions.
* `MaxWidth` - Gets or sets the wrap width of the axis labels.
* `WrappedLabelAlignment` - Gets or sets the horizontal rendering position of the wrapped axis labels. The default value is `Start`, other available values are `Center` and `End`.

## Edge Labels Drawing Mode

Chart axis provides support to customize the rendering position of edge labels using the [EdgeLabelsDrawingMode](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html#Syncfusion_Maui_Toolkit_Charts_ChartAxis_EdgeLabelsDrawingMode) property. The default value is `Shift`.

| Action | Description |
|--|--|
| Center | Indicates that the edge label should appear at the center of its GridLines. |
| Fit | Indicates that the edge labels should be fit within the area of SfCartesianChart. |
| Hide | Indicates that the edge labels will be hidden. |
| Shift | Indicates that edge labels should be shifted to either left or right so that they come within the area of Chart. |

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    . . .
    <chart:SfCartesianChart.XAxes>
        <chart:DateTimeAxis EdgeLabelsDrawingMode="Center"/>
    </chart:SfCartesianChart.XAxes>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
. . . 
DateTimeAxis primaryAxis = new DateTimeAxis()
{
    EdgeLabelsDrawingMode = EdgeLabelsDrawingMode.Center // Align edge labels to the center
};
chart.XAxes.Add(primaryAxis);

this.Content = chart;
{% endhighlight %}

{% endtabs %}

![Axis edge label positioning support in .NET MAUI Chart.](axis_images/net-maui-chart-axis-edge-labels-drawing.jpg)

## Edge Labels Visibility
 
The visibility of the edge labels of the axis can be controlled using the [EdgeLabelsVisibilityMode](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RangeAxisBase.html#Syncfusion_Maui_Toolkit_Charts_RangeAxisBase_EdgeLabelsVisibilityMode) property. The default value is `Default`, which displays the edge label based on auto interval calculations.

**Always Visible**

The `AlwaysVisible` option in [EdgeLabelsVisibilityMode](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RangeAxisBase.html#Syncfusion_Maui_Toolkit_Charts_RangeAxisBase_EdgeLabelsVisibilityMode) is used to view the edge labels even when the chart area is zoomed.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    . . .
    <chart:SfCartesianChart.XAxes>
        <chart:NumericalAxis EdgeLabelsVisibilityMode="AlwaysVisible"/>
    </chart:SfCartesianChart.XAxes>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
. . .
NumericalAxis primaryAxis = new NumericalAxis()
{
    EdgeLabelsVisibilityMode = EdgeLabelsVisibilityMode.AlwaysVisible
};
chart.XAxes.Add(primaryAxis);

this.Content = chart;
{% endhighlight %}

{% endtabs %}

**Visible**

The `Visible` option is used to display the edge labels irrespective of the auto interval calculation until zooming (i.e., in normal state).

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    . . .
    <chart:SfCartesianChart.XAxes>
        <chart:NumericalAxis EdgeLabelsVisibilityMode="Visible"/>
    </chart:SfCartesianChart.XAxes>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
. . .
NumericalAxis primaryAxis = new NumericalAxis()
{
    EdgeLabelsVisibilityMode = EdgeLabelsVisibilityMode.Visible
};
chart.XAxes.Add(primaryAxis);

this.Content = chart;
{% endhighlight %}

{% endtabs %}

## Smart Axis Labels

Axis labels may overlap with each other based on chart dimensions and label size. The [LabelsIntersectAction](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html#Syncfusion_Maui_Toolkit_Charts_ChartAxis_LabelsIntersectAction) property of axis is used to avoid overlapping of axis labels. The default value is `Hide`, other available values are `MultipleRows`, `None`, and `Wrap`.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    . . .
    <chart:SfCartesianChart.XAxes>
       <chart:CategoryAxis LabelsIntersectAction="MultipleRows"/>
    </chart:SfCartesianChart.XAxes>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
. . .
CategoryAxis primaryAxis = new CategoryAxis()
{
    // Set the labels intersect action to "MultipleRows", allowing labels to be positioned on multiple rows to avoid overlap
    LabelsIntersectAction = AxisLabelsIntersectAction.MultipleRows,
};
chart.XAxes.Add(primaryAxis);
 
this.Content = chart;
{% endhighlight %}

{% endtabs %}

![Smart axis label support in .NET MAUI SfCartesianChart.](axis_images/maui_chart_smart_axis_labels.png)

N> If the [LabelsIntersectAction](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html#Syncfusion_Maui_Toolkit_Charts_ChartAxis_LabelsIntersectAction) is set to Wrap, you should set the width of the wrap using the [MaxWidth](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxisLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartAxisLabelStyle_MaxWidth) property. You can align the wrapped axis label using the [WrappedLabelAlignment](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxisLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartAxisLabelStyle_WrappedLabelAlignment) property.
