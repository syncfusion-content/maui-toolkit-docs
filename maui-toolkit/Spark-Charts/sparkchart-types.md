---
layout: post
title: Chart types in .NET MAUI Spark Chart Control | Syncfusion
description: Learn here all about chart types supported in Syncfusion® .NET MAUI Spark Charts (SfSparkChart) control and more.
platform: maui-toolkit
control: SfSparkChart
documentation: ug
---

# Chart types in .NET MAUI Spark Charts

N> **Prerequisite:** Ensure that the required NuGet package is installed, the necessary namespaces are imported, and the **Spark Charts** control is properly configured in your application. For detailed setup and configuration instructions, refer to the **[Getting Started](https://help.syncfusion.com/maui-toolkit/spark-charts/getting-started)** guide.

The [SfSparkChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkChart.html) control supports four chart types: line, area, column, and win-loss.

## Line chart

The [SfSparkLineChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkLineChart.html) is used for identifying patterns and trends in the data, such as seasonal effects, large changes, and turning points over a period of time.

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkLineChart ItemsSource="{Binding Data}" 
                    YBindingPath="YValue">
    <!-- code omitted for brevity -->
</sparkchart:SfSparkLineChart>

{% endhighlight %}

{% highlight c# %}

SfSparkLineChart sparkchart = new SfSparkLineChart()
{
    ItemsSource = new SparkChartViewModel().Data,
    YBindingPath = "YValue",
};
//code omitted for brevity
this.Content = sparkchart;

{% endhighlight %}

{% endtabs %}

![Spark Line chart in MAUI Spark Chart](sparkchart_types_images/MAUI_Line_Sparkline.png)

## Area chart

The [SfSparkAreaChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkAreaChart.html) is used to emphasize a change in values. Use this to communicate the magnitude of a trend rather than individual data values.

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkAreaChart ItemsSource="{Binding Data}" 
                    YBindingPath="YValue">
    <!-- code omitted for brevity -->
</sparkchart:SfSparkAreaChart>

{% endhighlight %}

{% highlight c# %}

SfSparkAreaChart sparkchart = new SfSparkAreaChart()
{
    ItemsSource = new SparkChartViewModel().Data,
    YBindingPath = "YValue",
};
//code omitted for brevity
this.Content = sparkchart;

{% endhighlight %}

{% endtabs %}

![Spark Area chart in MAUI Spark Chart](sparkchart_types_images/MAUI_Area_Sparkline.png)

## Column chart

The [SfSparkColumnChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkColumnChart.html) uses vertical bars to compare values across data points.

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkColumnChart ItemsSource="{Binding Data}" 
                    YBindingPath="YValue">
    <!-- code omitted for brevity -->
</sparkchart:SfSparkColumnChart>

{% endhighlight %}

{% highlight c# %}

SfSparkColumnChart sparkchart = new SfSparkColumnChart()
{
    ItemsSource = new SparkChartViewModel().Data,
    YBindingPath = "YValue",
};
//code omitted for brevity
this.Content = sparkchart;

{% endhighlight %}

{% endtabs %}

![Spark Column chart in MAUI Spark Chart](sparkchart_types_images/MAUI_Column_Sparkline.png)

## Win-loss chart

The [SfSparkWinLossChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkWinLossChart.html) is used to show whether each value is positive or negative, visualizing a win-loss scenario. Positive values are rendered as bars above the axis, negative values as bars below the axis, and zero values are not rendered.

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkWinLossChart ItemsSource="{Binding Data}" 
                     YBindingPath="YValue">
    <!-- code omitted for brevity -->
</sparkchart:SfSparkWinLossChart>

{% endhighlight %}

{% highlight c# %}

SfSparkWinLossChart sparkchart = new SfSparkWinLossChart()
{
    ItemsSource = new SparkChartViewModel().Data,
    YBindingPath = "YValue",
};
//code omitted for brevity
this.Content = sparkchart;

{% endhighlight %}

{% endtabs %}

![Spark WinLoss chart in MAUI Spark Chart](sparkchart_types_images/MAUI_WinLoss_Sparkline.png)