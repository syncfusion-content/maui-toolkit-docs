---
layout: post
title: Segment spacing in .NET MAUI Chart control Syncfusion
description: Learn here all about segment spacing customization in .NET MAUI Chart (SfFunnelChart), its elements and more.
platform: maui-toolkit
control: SfFunnelChart
documentation: ug
---

# Segment spacing in .NET MAUI Funnel Chart

The gap between each segment in the funnel chart can be set using the [GapRatio](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfFunnelChart.html#Syncfusion_Maui_Toolkit_Charts_SfFunnelChart_GapRatio) property is `0` and its value ranges from `0 to 1`.

{% tabs %}

{% highlight xml %}

<chart:SfFunnelChart GapRatio="0.2">
    . . .
</chart:SfFunnelChart>

{% endhighlight %}

{% highlight c# %}

SfFunnelChart chart = new SfFunnelChart();
. . .
chart.GapRatio = 0.2; // Set gap ratio between funnel segments.
. . .
this.Content = chart;
{% endhighlight %}

{% endtabs %}

![Segment spacing in MAUI Chart](Segment_Spacing_images/MAUI_spacing_chart.png)
