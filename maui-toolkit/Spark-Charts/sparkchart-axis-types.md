---
layout: post
title: Axis types in .NET MAUI Spark Chart Control | Syncfusion
description: Learn here all about Axis types supported in Syncfusion® .NET MAUI Spark Charts (SfSparkChart) control and more.
platform: maui-toolkit
control: SfSparkChart
documentation: ug
keywords: maui spark chart axis, spark chart numeric axis, spark chart category axis, spark chart datetime axis, maui sparkline axis types, spark chart axis customization
---

# Axis types in .NET MAUI Spark Charts

Spark charts consist of two axes for measuring and categorizing data: a vertical (Y) axis and a horizontal (X) axis. The Y-axis always uses a numerical scale to measure data values, while the X-axis provides flexibility to change its type using the `AxisType` property, supporting Numeric, Category, and DateTime scales.

##  XBindingPath Property

The `XBindingPath` property specifies the data source property that contains the X-axis values. It binds your collection’s data to the horizontal axis of the spark chart.

## AxisType Property

The `AxisType` property of the spark charts determines how the chart interprets the X-axis values. Its default value is `SparkChartAxisType.Numeric`. It accepts the following SparkChartAxisType enum values

* `Category` - Treats X‑axis values as discrete categories. Use this for text or labels where each point represents a distinct group.

* `DateTime` - Treats X‑axis values as dates/times. Use this to highlight trends and changes over time.

* `Numeric` - Treats X‑axis values as numbers. Use this for quantities, indices, or other continuous numeric data.

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkColumnChart ItemsSource="{Binding Data}" 
                               YBindingPath="Value"
                               XBindingPath="OrderName" 
                               AxisType="Category">
</sparkchart:SfSparkColumnChart>

{% endhighlight %}

{% highlight c# %}

SfSparkColumnChart sparkchart = new SfSparkColumnChart()
{
    ItemsSource = new SparkChartViewModel().Data,
    YBindingPath = "Value",
    XBindingPath = "OrderName",
    AxisType = SparkChartAxisType.Category
};
this.Content = sparkchart;

{% endhighlight %}

{% endtabs %}

