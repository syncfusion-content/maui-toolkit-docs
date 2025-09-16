---
layout: post
title: Axis Tick Line in .NET MAUI Cartesian Chart control | Syncfusion
description: Learn here all about chart axis tick line and its customization in Syncfusion® .NET MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
keywords: .net maui chart tick lines, .net maui chart tick customization, .net maui chart tickline guide, syncfusion maui chart tick lines, cartesian chart tick lines maui, .net maui chart axis tick lines, customize tick lines .net maui chart.
---

# Tick Lines in .NET MAUI Chart

Tick lines are small lines drawn on the axis line representing the axis labels. By default, tick lines are drawn outside of the axis.

Minor tick lines can also be added to the axis by defining the [MinorTicksPerInterval](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RangeAxisBase.html#Syncfusion_Maui_Toolkit_Charts_RangeAxisBase_MinorTicksPerInterval) property. This property adds minor tick lines to every interval based on the specified value.

N> Minor tick lines are not applicable for category axis since it is rendered based on index positions.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    . . .
    <chart:SfCartesianChart.XAxes>
        <chart:NumericalAxis MinorTicksPerInterval="4"/>
    </chart:SfCartesianChart.XAxes>

    <chart:SfCartesianChart.YAxes>
        <chart:NumericalAxis/>
    </chart:SfCartesianChart.YAxes>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
. . .
NumericalAxis primaryAxis = new NumericalAxis()
{
    MinorTicksPerInterval = 4 // Set the number of minor ticks between major tick marks
};
chart.XAxes.Add(primaryAxis);

NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

this.Content = chart;
{% endhighlight %}

{% endtabs %}

## Positioning the ticks

The tick lines can be positioned inside or outside the chart area using the [TickPosition](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html#Syncfusion_Maui_Toolkit_Charts_ChartAxis_TickPosition) property. The default value of [TickPosition](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html#Syncfusion_Maui_Toolkit_Charts_ChartAxis_TickPosition) is `AxisElementPosition.Outside`.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    . . .  
    <chart:SfCartesianChart.XAxes>
        <chart:CategoryAxis/>
    </chart:SfCartesianChart.XAxes>

    <chart:SfCartesianChart.YAxes>
        <chart:NumericalAxis TickPosition="Inside"/>
    </chart:SfCartesianChart.YAxes>
</chart:SfCartesianChart>


{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
CategoryAxis primaryAxis = new CategoryAxis();
NumericalAxis secondaryAxis = new NumericalAxis()
{
    TickPosition = AxisElementPosition.Inside // Set the tick position to display inside the chart area.
};

chart.XAxes.Add(primaryAxis);
chart.YAxes.Add(secondaryAxis);
this.Content = chart;
{% endhighlight %}

{% endtabs %}

![Axis ticks inside position in .NET MAUI Chart.](axis_images/maui_chart_inside_ticks.png)

## Customization

Both major and minor tick lines can be customized using the [MajorTickStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html#Syncfusion_Maui_Toolkit_Charts_ChartAxis_MajorTickStyle) and [MinorTickStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RangeAxisBase.html#Syncfusion_Maui_Toolkit_Charts_RangeAxisBase_MinorTickStyle) properties respectively. These properties provide options to change the [StrokeWidth](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxisTickStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartAxisTickStyle_StrokeWidth), [TickSize](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxisTickStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartAxisTickStyle_TickSize), and [Stroke](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxisTickStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartAxisTickStyle_Stroke) of tick lines. By default, minor tick lines are not visible.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    . . .
    <chart:SfCartesianChart.XAxes>
        <chart:NumericalAxis MinorTicksPerInterval="4">
            <chart:NumericalAxis.MajorTickStyle>
                <chart:ChartAxisTickStyle Stroke="Red" StrokeWidth="1" TickSize="10"/>
            </chart:NumericalAxis.MajorTickStyle>
            
            <chart:NumericalAxis.MinorTickStyle>
                <chart:ChartAxisTickStyle Stroke="Red" StrokeWidth="1"/>
            </chart:NumericalAxis.MinorTickStyle>
        </chart:NumericalAxis>
    </chart:SfCartesianChart.XAxes>

    <chart:SfCartesianChart.YAxes>
        <chart:NumericalAxis/>
    </chart:SfCartesianChart.YAxes>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
. . .
NumericalAxis primaryAxis = new NumericalAxis()
{
    MinorTicksPerInterval = 4,
    // Style configuration for major ticks
    MajorTickStyle = new ChartAxisTickStyle()
    {
        Stroke = Colors.Red,
        StrokeWidth = 1,
        TickSize = 10
    },
    // Style configuration for minor ticks
    MinorTickStyle = new ChartAxisTickStyle()
    {
        Stroke = Colors.Red,
        StrokeWidth = 1
    }
};

chart.XAxes.Add(primaryAxis);

NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

this.Content = chart;
{% endhighlight %}

{% endtabs %}

![Axis tick lines customization support in .NET MAUI Chart](Axis_images/maui_chart_axis_tickline_customization.jpg)
