---
layout: post
title: Axis line in .NET MAUI Chart control | Syncfusion
description: Learn here all about the chart axis line and its customization in Syncfusion® .NET MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
keywords: .net maui chart axis line, .net maui chart axis customization, .net maui chart axisline guide, maui chart axis line settings, syncfusion maui chart axis line, .net maui chart axis styling, customize axis line .net maui chart.
---

# Axis line in .NET MAUI Chart

## Customization

Cartesian chart axis provides support to customize the style of the axis line by defining the [AxisLineStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html#Syncfusion_Maui_Toolkit_Charts_ChartAxis_AxisLineStyle) property as shown in the code snippet below.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    . . .
    <chart:SfCartesianChart.XAxes>
        <chart:NumericalAxis>
            <chart:NumericalAxis.AxisLineStyle>
                <chart:ChartLineStyle StrokeWidth="2"
                                      Stroke="Red"/>
            </chart:NumericalAxis.AxisLineStyle>
        </chart:NumericalAxis>
    </chart:SfCartesianChart.XAxes>
    . . .
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
. . .
NumericalAxis primaryAxis = new NumericalAxis();
// Define the style for the axis line
ChartLineStyle axisLineStyle = new ChartLineStyle()
{
    Stroke = Colors.Red,
    StrokeWidth = 2,
};
primaryAxis.AxisLineStyle = axisLineStyle; // Apply the defined axis line style to the primary axis
chart.XAxes.Add(primaryAxis);
. . .
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Axis line customization support in MAUI Chart](Axis_images/maui_chart_axis_linestyle.jpg)

## Offset

The padding to the axis line can be defined using the [AxisLineOffset](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html#Syncfusion_Maui_Toolkit_Charts_ChartAxis_AxisLineOffset) property.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    . . .
    <chart:SfCartesianChart.XAxes>
        <chart:NumericalAxis AxisLineOffset="25">
            <chart:NumericalAxis.AxisLineStyle>
                <chart:ChartLineStyle StrokeWidth="2"
                                      Stroke="Red"/>
            </chart:NumericalAxis.AxisLineStyle>
        </chart:NumericalAxis>
    </chart:SfCartesianChart.XAxes>
    . . .
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
. . .
NumericalAxis primaryAxis = new NumericalAxis();
primaryAxis.AxisLineOffset = 25; // Set the axis line offset to position the axis line away from the plotted area
ChartLineStyle axisLineStyle = new ChartLineStyle()
{
    Stroke = Colors.Red,
    StrokeWidth = 2,
};
primaryAxis.AxisLineStyle = axisLineStyle;
chart.XAxes.Add(primaryAxis);
. . .
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Padding support for axis line in .NET MAUI Chart](Axis_images/maui_chart_axis_line_offset.jpg)