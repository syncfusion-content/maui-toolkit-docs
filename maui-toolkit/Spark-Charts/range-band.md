---
layout: post
title: Range Band in .NET MAUI Spark Chart Control | Syncfusion
description: Learn here all about the Range Band support in Syncfusion® .NET MAUI Spark Charts (SfSparkChart) control and more.
platform: maui-toolkit
control: SfSparkChart
documentation: ug
---

# Range Band in .NET MAUI Spark Charts

Range bands are used to highlight a particular region in the spark chart along the Y-axis, making it easy to identify specific value ranges or thresholds.

* `RangeBandStart` - Specifies the starting Y-axis value where the range band begins.
* `RangeBandEnd` - Specifies the ending Y-axis value where the range band ends.
* `RangeFill` - Specifies the fill color for the range band. This color is applied to the area between RangeBandStart and RangeBandEnd values on the Y-axis.

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkLineChart ItemsSource="{Binding Data}" 
                             YBindingPath="Value"
                             RangeBandStart="10" 
                             RangeBandEnd="30" 
                             RangeFill="LightBlue">
. . . 
</sparkchart:SfSparkLineChart>

{% endhighlight %}

{% highlight c# %}

SfSparkLineChart sparkchart = new SfSparkLineChart()
{
    ItemsSource = new SparkChartViewModel().Data,
    YBindingPath = "Value",
    RangeBandStart = 10,
    RangeBandEnd = 30,
    RangeFill =  new SolidColorBrush(Colors.LightBlue)
};

this.Content = sparkchart;

{% endhighlight %}

{% endtabs %}

![Spark Line Chart With Range Band](range_band_images/MAUI_range_band.png)

