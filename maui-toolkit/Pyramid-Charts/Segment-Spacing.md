---
layout: post
title: Segment Spacing in .NET MAUI Pyramid Chart Control | Syncfusion
description: Learn here all about segment spacing customization in Syncfusion® .NET MAUI Pyramid Chart (SfPyramidChart) control and more.
platform: maui-toolkit
control: SfPyramidChart
documentation: ug
keywords: .net maui pyramid chart, segment spacing, gapratio, pyramid chart customization, segment gap, chart configuration, maui toolkit
---

# Segment Spacing in .NET MAUI Pyramid Chart

The gap between each segment in the pyramid chart can be customized using the [GapRatio](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPyramidChart.html#Syncfusion_Maui_Toolkit_Charts_SfPyramidChart_GapRatio) property. The default value of the `GapRatio` property is `0`, and its value ranges from `0` to `1`.

{% tabs %}

{% highlight xaml %}

<chart:SfPyramidChart GapRatio="0.2">
    <!-- Chart configuration -->
</chart:SfPyramidChart>

{% endhighlight %}

{% highlight c# %}

SfPyramidChart chart = new SfPyramidChart();
// Chart configuration
chart.GapRatio = 0.2; // Set gap ratio between pyramid segments
// Additional configuration
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Segment spacing in .NET MAUI Pyramid Chart](Segment_Spacing_images/MAUI_spacing_chart.png)