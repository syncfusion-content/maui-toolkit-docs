---
layout: post
title: Segment Spacing in .NET MAUI Chart Control | Syncfusion
description: Learn about segment spacing customization in Syncfusion® .NET MAUI Chart (SfFunnelChart) control and its implementation.
platform: maui-toolkit
control: SfFunnelChart
documentation: ug
---

# Segment Spacing in .NET MAUI Funnel Chart

The gap between each segment in the funnel chart can be set using the [GapRatio](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfFunnelChart.html#Syncfusion_Maui_Toolkit_Charts_SfFunnelChart_GapRatio) property. The default value of GapRatio is `0`, and its value ranges from `0 to 1`.

{% tabs %}

{% highlight xml %}

<chart:SfFunnelChart GapRatio="0.2">
    <!-- Other chart configurations -->
</chart:SfFunnelChart>

{% endhighlight %}

{% highlight c# %}

SfFunnelChart chart = new SfFunnelChart();
// Other chart configurations
chart.GapRatio = 0.2; // Set gap ratio between funnel segments.
// Other chart configurations
this.Content = chart;
{% endhighlight %}

{% endtabs %}

![Segment spacing in MAUI Chart](Segment_Spacing_images/MAUI_spacing_chart.png)

