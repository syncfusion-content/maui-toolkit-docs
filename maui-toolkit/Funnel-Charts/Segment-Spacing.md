---
layout: post
title: Segment Spacing in .NET MAUI Funnel Chart Control | Syncfusion
description: Learn how to customize segment spacing in Syncfusion® .NET MAUI Funnel Chart (SfFunnelChart) control and its elements.
platform: maui-toolkit
control: SfFunnelChart
documentation: ug
keywords: .net maui funnel chart, segment spacing, chart customization, gap ratio, funnel chart elements
---

# Segment Spacing in .NET MAUI Funnel Chart

You can customize the gap between segments in the funnel chart by using the [GapRatio](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfFunnelChart.html#Syncfusion_Maui_Toolkit_Charts_SfFunnelChart_GapRatio) property. The default value is `0`, and it can range from `0` to `1`. A higher value creates more space between segments.

{% tabs %}

{% highlight xml %}
<chart:SfFunnelChart GapRatio="0.2">
    . . .
</chart:SfFunnelChart>
{% endhighlight %}

{% highlight c# %}
SfFunnelChart chart = new SfFunnelChart();
. . .
chart.GapRatio = 0.2; // Set gap ratio between funnel segments
. . .
this.Content = chart;
{% endhighlight %}

{% endtabs %}

![Segment spacing in MAUI Funnel Chart](Segment_Spacing_images/MAUI_spacing_chart.png)