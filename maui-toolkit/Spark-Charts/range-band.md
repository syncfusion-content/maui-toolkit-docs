---
layout: post
title: Range Band in .NET MAUI Spark Chart Control | Syncfusion
description: Learn here all about the Range Band support in Syncfusion® .NET MAUI Spark Charts (SfSparkChart) control and more.
platform: maui-toolkit
control: SfSparkChart
documentation: ug
keywords: .NET MAUI spark chart range band, MAUI range band, range band customization, Syncfusion MAUI spark chart range band, .NET MAUI shaded region spark chart, spark chart Y-axis range band, .NET MAUI range band highlight region
---

# Range Band in .NET MAUI Spark Charts

Range bands are used to highlight a particular region in the spark chart along the Y-axis, making it easy to identify specific value ranges or thresholds.

* [RangeBandStart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkChart.html#Syncfusion_Maui_Toolkit_SparkCharts_SfSparkChart_RangeBandStart) - Specifies the starting Y-axis value where the range band begins.
* [RangeBandEnd](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkChart.html#Syncfusion_Maui_Toolkit_SparkCharts_SfSparkChart_RangeBandEnd) - Specifies the ending Y-axis value where the range band ends.
* [RangeBandFill](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkChart.html#Syncfusion_Maui_Toolkit_SparkCharts_SfSparkChart_RangeBandFill) - Specifies the fill color for the range band. This color is applied to the area between RangeBandStart and RangeBandEnd values on the Y-axis.

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkLineChart ItemsSource = "{Binding Data}" 
                             YBindingPath = "Value"
                             RangeBandStart = "10" 
                             RangeBandEnd = "30" 
                             RangeBandFill = "LightBlue">
</sparkchart:SfSparkLineChart>

{% endhighlight %}

{% highlight c# %}

SfSparkLineChart sparkchart = new SfSparkLineChart()
{
    ItemsSource = new SparkChartViewModel().Data,
    YBindingPath = "Value",
    RangeBandStart = 10,
    RangeBandEnd = 30,
    RangeBandFill  =  new SolidColorBrush(Colors.LightBlue)
};

this.Content = sparkchart;

{% endhighlight %}

{% endtabs %}

![Spark Line Chart With Range Band](range_band_images/MAUI_range_band.png)

