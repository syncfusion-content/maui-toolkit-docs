---
layout: post
title: Chart types in .NET MAUI Spark Chart Control | Syncfusion
description: Learn here all about chart types supported in Syncfusion .NET MAUI Spark Charts (SfSparkChart) control and more.
platform: maui-toolkit
control: SfSparkChart
documentation: ug
---

# Chart types in .NET MAUI Spark Charts

The `SfSparkChart` control supports four different chart types such as Line, Column, Area, and Win-loss.

## Line Sparkline

The `SfSparkLineChart` chart is used for identifying patterns and trends in the data, such as seasonal effects, large changes, and turning points over a period of time.

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkLineChart ItemsSource="{Binding Data}" 
                    YBindingPath="Value">
. . .
</sparkchart:SfSparkLineChart>

{% endhighlight %}

{% highlight c# %}

SfSparkLineChart sparkchart = new SfSparkLineChart()
{
    ItemsSource = new SparkChartViewModel().Data,
    YBindingPath = "Value",
};

this.Content = sparkchart;

{% endhighlight %}

{% endtabs %}

![Spark chart in .NET MAUI Chart](sparkchart_types_images/MAUI_Line_Sparkline.png)

## Column Sparkline

The `SfSparkColumnChart` uses vertical bars to show the comparison between the different data.

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkColumnChart ItemsSource="{Binding Data}" 
                    YBindingPath="Value">
. . .
</sparkchart:SfSparkColumnChart>

{% endhighlight %}

{% highlight c# %}

SfSparkColumnChart sparkchart = new SfSparkColumnChart()
{
    ItemsSource = new SparkChartViewModel().Data,
    YBindingPath = "YValue",
};
this.Content = sparkchart;

{% endhighlight %}

{% endtabs %}

![Spark chart in .NET MAUI Chart](sparkchart_types_images/MAUI_Column_Sparkline.png)

## Area Sparkline

The `SfSparkAreaChart` is used to emphasize a change in values. This is primarily used when the magnitude of the trend is to be communicated rather than individual data values.

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkAreaChart ItemsSource="{Binding Data}" 
                    YBindingPath="Value">
. . .
</sparkchart:SfSparkAreaChart>

{% endhighlight %}

{% highlight c# %}

SfSparkAreaChart sparkchart = new SfSparkAreaChart()
{
    ItemsSource = new SparkChartViewModel().Data,
    YBindingPath = "Value",
};

this.Content = sparkchart;

{% endhighlight %}

{% endtabs %}

![Spark chart in .NET MAUI Chart](sparkchart_types_images/MAUI_Area_Sparkline.png)

## WinLoss Sparkline

The `SfSparkWinLossChart` is used to show whether each value is positive or negative visualizing a Win/Loss scenario.

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkWinLossChart ItemsSource="{Binding Data}" 
                     YBindingPath="YValue">
. . .
</sparkchart:SfSparkWinLossChart>

{% endhighlight %}

{% highlight c# %}

SfSparkWinLossChart sparkchart = new SfSparkWinLossChart()
{
    ItemsSource = new SparkChartViewModel().Data,
    YBindingPath = "YValue",
};
this.Content = sparkchart;

{% endhighlight %}

{% endtabs %}

![Spark chart in .NET MAUI Chart](sparkchart_types_images/MAUI_WinLoss_Sparkline.png)