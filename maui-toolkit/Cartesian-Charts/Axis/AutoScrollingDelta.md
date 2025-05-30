---
layout: post
title: Auto scrolling in .NET MAUI Chart control | Syncfusion
description: Learn here all about auto scrolling and its features in Syncfusion® .NET MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
keywords: .net maui chart auto scrolling, .net maui chart scrolling customization, .net maui chart auto scroll feature, syncfusion maui chart auto scrolling, cartesian chart auto scroll maui, .net maui chart dynamic scrolling, enable auto scrolling .net maui chart.
---

# Auto scrolling in .NET MAUI Chart

The auto-scrolling of [SfCartesianChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html) ensures that the specified range of data is always visible in the chart. It always shows the recently added data points at the end, and scrolling will be reset to the end of the range whenever a new point is added. The [AutoScrollingDelta](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html#Syncfusion_Maui_Toolkit_Charts_ChartAxis_AutoScrollingDelta) property of the chart axis can be used to set the number of data points to be always visible in the chart.

By adding [ChartZoomPanBehavior](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartZoomPanBehavior.html) to the chart, you can scroll to see the previous data points.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    . . .
    <chart:SfCartesianChart.XAxes>
        <chart:CategoryAxis AutoScrollingDelta="3"/>
    </chart:SfCartesianChart.XAxes>

    <chart:SfCartesianChart.ZoomPanBehavior>
        <chart:ChartZoomPanBehavior EnablePanning="True"/>
    </chart:SfCartesianChart.ZoomPanBehavior>
    . . .
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
. . .
CategoryAxis primaryAxis = new CategoryAxis()
{
    AutoScrollingDelta = 3,
};
chart.XAxes.Add(primaryAxis);

// Create a ChartZoomPanBehavior to manage zooming and panning interactions
ChartZoomPanBehavior zooming = new ChartZoomPanBehavior()
{
    EnablePanning = true,
};
chart.ZoomPanBehavior = zooming; // Assign the zoom and pan behavior to the chart
. . .
this.Content = chart;
{% endhighlight %}

{% endtabs %}

## AutoScrollingMode

[AutoScrollingMode](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html#Syncfusion_Maui_Toolkit_Charts_ChartAxis_AutoScrollingMode) property can be used to determine whether the axis should be scrolled from start position or end position. The default value of [AutoScrollingMode](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html#Syncfusion_Maui_Toolkit_Charts_ChartAxis_AutoScrollingMode) is `End`.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    . . .
    <chart:SfCartesianChart.XAxes>
        <chart:CategoryAxis AutoScrollingDelta="3" AutoScrollingMode="Start"/>
    </chart:SfCartesianChart.XAxes>
    . . .
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
. . .
CategoryAxis primaryAxis = new CategoryAxis()
{
    // Set the AutoScrollingDelta to 3, which determines the number of data points the chart will auto-scroll by.
    AutoScrollingDelta = 3,
    // Set the AutoScrollingMode to Start, indicating that auto-scrolling begins from the start of the dataset.
    AutoScrollingMode = ChartAutoScrollingMode.Start,
};
chart.XAxes.Add(primaryAxis);
. . .
this.Content = chart;
{% endhighlight %}

{% endtabs %}

## AutoScrollingDeltaType

In [DateTimeAxis](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DateTimeAxis.html), you can apply auto scrolling delta value in [Years](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DateTimeIntervalType.html#Syncfusion_Maui_Toolkit_Charts_DateTimeIntervalType_Years), [Months](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DateTimeIntervalType.html#Syncfusion_Maui_Toolkit_Charts_DateTimeIntervalType_Months), [Days](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DateTimeIntervalType.html#Syncfusion_Maui_Toolkit_Charts_DateTimeIntervalType_Days), [Hours](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DateTimeIntervalType.html#Syncfusion_Maui_Toolkit_Charts_DateTimeIntervalType_Hours), [Minutes](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DateTimeIntervalType.html#Syncfusion_Maui_Toolkit_Charts_DateTimeIntervalType_Minutes), [Seconds](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DateTimeIntervalType.html#Syncfusion_Maui_Toolkit_Charts_DateTimeIntervalType_Seconds) and [Milliseconds](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DateTimeIntervalType.html#Syncfusion_Maui_Toolkit_Charts_DateTimeIntervalType_Milliseconds) by setting [AutoScrollingDeltaType](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DateTimeAxis.html#Syncfusion_Maui_Toolkit_Charts_DateTimeAxis_AutoScrollingDeltaType) property. The default value of this property is [Auto](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DateTimeIntervalType.html#Syncfusion_Maui_Toolkit_Charts_DateTimeIntervalType_Auto), and the delta will be calculated automatically based on range.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    . . .
    <chart:SfCartesianChart.XAxes>
        <chart:DateTimeAxis AutoScrollingDelta="3" AutoScrollingDeltaType="Days"/>
    </chart:SfCartesianChart.XAxes>
    . . .
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
. . .
DateTimeAxis primaryAxis = new DateTimeAxis()
{
    AutoScrollingDelta = 3,
    AutoScrollingDeltaType = DateTimeDeltaType.Days,  // Setting the type of the scrolling delta to Days, meaning the axis will scroll by 3 days.
};
chart.XAxes.Add(primaryAxis);
. . .
this.Content = chart;
{% endhighlight %}

{% endtabs %}