---
layout: post
title: Customize Data Points in .NET MAUI Spark Chart Control | Syncfusion
description: Learn here all about how to customize data points in Syncfusion .NET MAUI Spark Charts (SfSparkChart) control and more.
platform: maui-toolkit
control: SfSparkChart
documentation: ug
---

# Customize Data Points in .NET MAUI Spark Charts

Color of the first, last, high, low, and negative data points can be customized using the following properties.

* `FirstPointFill` - Used to highlight the first point.
* `LastPointFill` - Used to highlight the last point.
* `HighPointFill` - Used to highlight the highest point.
* `LowPointFill` - Used to highlight the lowest point.
* `NegativePointsFill` - Used to highlight the negative points.

{% tabs %}

{% highlight xaml %}

<chart:SfSparkLineChart ItemsSource="{Binding Data}" 
                    YBindingPath="Value"
                    FirstPointFill="Green"
                    LastPointFill="Blue"
                    HighPointFill="Purple"
                    LowPointFill="Red"
                    ShowMarkers="True">
. . .
</chart:SfSparkLineChart>

{% endhighlight %}

{% highlight c# %}

SfSparkLineChart chart = new SfSparkLineChart()
{
    ItemsSource = new SparkDataViewModel().Data,
    YBindingPath = "Value",
    FirstPointFill = new SolidColorBrush(Colors.Green),
    LastPointFill = new SolidColorBrush(Colors.Blue),
    HighPointFill = new SolidColorBrush(Colors.Purple),
    LowPointFill = new SolidColorBrush(Colors.Red),
    ShowMarkers = true
};
this.Content = chart;

{% endhighlight %}

{% endtabs %}

N> `NegativePointsColor` is applicable for `SfColumnSparkline` and `SfWinLossSparkline` alone.
