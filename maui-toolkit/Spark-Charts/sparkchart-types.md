---
layout: post
title: Chart types in .NET MAUI Spark Charts | Syncfusion
description: Learn here all about chart types supported in Syncfusion .NET MAUI Spark Charts (SfSparkChart) control and more.
platform: maui
control: SfSparkChart
documentation: ug
---

# Chart types in .NET MAUI Spark Charts

The SfSparkChart control supports four different types of series: Line, Column, Area, and Win-loss. The series type can be set by using the `Type` property. The default series type is `Line`.

## Line Spark chart

The `SfSparkLineChart` chart is used for identifying patterns and trends in the data such as seasonal effects, large changes and turning points over a period of time.

The following properties are used to customize the appearance:

{% tabs %}

{% highlight xaml %}

<chart:SfSparkLineChart ItemsSource="{Binding Data}" 
                    YBindingPath="Value">
. . .
</chart:SfSparkLineChart>

{% endhighlight %}

{% highlight c# %}

SfSparkLineChart crt = new SfSparkLineChart()
{
    ItemsSource = new SparkDataViewModel().Data,
    YBindingPath = "Value",
};

this.Content = chart;

{% endhighlight %}

{% endtabs %}

## Column Spark chart

The `SfSparkColumnChart` uses vertical bars to show the comparison between the different data.

{% tabs %}

{% highlight xaml %}

<chart:SfSparkColumnChart ItemsSource="{Binding Data}" 
                    YBindingPath="Value">
. . .
</chart:SfSparkColumnChart>

{% endhighlight %}

{% highlight c# %}

SfSparkColumnChart chart = new SfSparkColumnChart()
{
    ItemsSource = new SparkDataViewModel().Data,
    YBindingPath = "YValue",
};
this.Content = chart;

{% endhighlight %}

{% endtabs %}

## Area Spark chart

The `SfSparkAreaChart` is used to emphasize a change in values. This is primarily used when the magnitude of the trend is to be communicated rather than individual data values.

{% tabs %}

{% highlight xaml %}

<chart:SfSparkAreaChart ItemsSource="{Binding Data}" 
                    YBindingPath="Value">
. . .
</chart:SfSparkAreaChart>

{% endhighlight %}

{% highlight c# %}

SfSparkAreaChart chart = new SfSparkAreaChart()
{
    ItemsSource = new SparkDataViewModel().Data,
    YBindingPath = "Value",
};

this.Content = chart;

{% endhighlight %}

{% endtabs %}

## Win-Loss Spark chart

The `SfSparkWinLossChart` is used to show whether each value is positive or negative visualizing a Win/Loss scenario.

{% tabs %}

{% highlight xaml %}

<chart:SfSparkWinLossChart ItemsSource="{Binding Data}" 
                     YBindingPath="YValue">
. . .
</chart:SfSparkWinLossChart>

{% endhighlight %}

{% highlight c# %}

SfSparkWinLossChart chart = new SfSparkWinLossChart()
{
    ItemsSource = new SparkDataViewModel().Data,
    YBindingPath = "YValue",
};
this.Content = chart;

{% endhighlight %}

{% endtabs %}