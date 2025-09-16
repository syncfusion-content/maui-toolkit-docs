---
layout: post
title: Axis line in .NET MAUI Polar Chart control | Syncfusion
description: Learn here all about the chart axis line and its customization in the Syncfusion® .NET MAUI Chart (SfPolarChart) control.
documentation: ug
platform: maui-toolkit
control: SfPolarChart
keywords: .net maui polar chart, axis line customization, axis line style, axis line offset, axis customization, maui toolkit
---

# Axis Line in .NET MAUI Polar Chart

## Customization

The polar chart axis provides support for customizing the style of the axis line by defining the [AxisLineStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html#Syncfusion_Maui_Toolkit_Charts_ChartAxis_AxisLineStyle) property, as shown in the code sample below.

N> The customization of axis lines using the AxisLineStyle property can only be applied to the secondary axis.

{% tabs %}

{% highlight xaml %}

<chart:SfPolarChart>
    . . .
    <chart:SfPolarChart.SecondaryAxis>
        <chart:NumericalAxis>
            <chart:NumericalAxis.AxisLineStyle>
                <chart:ChartLineStyle StrokeWidth="2" Stroke="Red"/>
            </chart:NumericalAxis.AxisLineStyle>
        </chart:NumericalAxis>
    </chart:SfPolarChart.SecondaryAxis>
</chart:SfPolarChart>

{% endhighlight %}

{% highlight c# %}

SfPolarChart chart = new SfPolarChart();
. . .
NumericalAxis secondaryAxis = new NumericalAxis();
// Define the style for the axis line of the secondary axis
ChartLineStyle axisLineStyle = new ChartLineStyle()
{
    Stroke = Colors.Red,
    StrokeWidth = 2,
};
// Apply the defined line style to the secondary axis
secondaryAxis.AxisLineStyle = axisLineStyle;
chart.SecondaryAxis = secondaryAxis;
. . .
this.Content = chart;

{% endhighlight %}

{% endtabs %}

## Offset

The padding to the axis line is defined by using the [AxisLineOffset](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html#Syncfusion_Maui_Toolkit_Charts_ChartAxis_AxisLineOffset) property.

{% tabs %}

{% highlight xaml %}

<chart:SfPolarChart>
    . . .
    <chart:SfPolarChart.SecondaryAxis>
        <chart:NumericalAxis AxisLineOffset="25">
            <chart:NumericalAxis.AxisLineStyle>
                <chart:ChartLineStyle StrokeWidth="2" Stroke="Red"/>
            </chart:NumericalAxis.AxisLineStyle>
        </chart:NumericalAxis>
    </chart:SfPolarChart.SecondaryAxis>
</chart:SfPolarChart>

{% endhighlight %}

{% highlight c# %}

SfPolarChart chart = new SfPolarChart();
. . .
NumericalAxis secondaryAxis = new NumericalAxis();
secondaryAxis.AxisLineOffset = 25; // Set the offset of the axis line from its default position
ChartLineStyle axisLineStyle = new ChartLineStyle()
{
    Stroke = Colors.Red,
    StrokeWidth = 2
};
secondaryAxis.AxisLineStyle = axisLineStyle;
chart.SecondaryAxis = secondaryAxis;
. . .
this.Content = chart;

{% endhighlight %}

{% endtabs %}