---
layout: post
title: Limit axis labels using MaximumLabels in .NET MAUI Chart control | Syncfusion
description: Learn how to control the number of axis labels displayed in Syncfusion® .NET MAUI Chart (SfCartesianChart) control using the MaximumLabels property.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
keywords: .net maui chart maximum labels, axis labels count .net maui, syncfusion maui chart labels per 100 pixels, limit axis labels .net maui, customize axis label density .net maui chart.
---

# Maximum labels per 100 pixels in .NET MAUI Chart

The [MaximumLabels]() property in ChartAxis allows users to control the number of axis labels rendered for every 100 pixels of the chart axis. This feature helps maintain better label spacing and improves readability.

By default, a maximum of `3 labels` are displayed per 100 pixels of axis. This ensures that the chart remains clean and readable without manual configuration. You can override this behavior by explicitly setting the MaximumLabels property to your desired density.

**XAML**

{% highlight xaml %}

    <chart:SfCartesianChart>

    . . .

    <chart:NumericalAxis MaximumLabels="1" />
    . . .

    </chart:SfCartesianChart>

{% endhighlight %}

N> This property only applies during automatic interval calculation. It will have no effect if the Interval property is manually set on the axis.