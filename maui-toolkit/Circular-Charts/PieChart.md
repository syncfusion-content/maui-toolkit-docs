---
layout: post
title: Pie Chart in .NET MAUI Chart control | Syncfusion
description: Learn here all about the pie chart and its features in Syncfusion® .NET MAUI Chart (SfCircularChart) control.
platform: maui-toolkit
control: SfCircularChart
documentation: ug
---

# Pie Chart in .NET MAUI Chart

To render a [PieSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.PieSeries.html) in circular chart, create an instance of the [PieSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.PieSeries.html) and add it to the [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCircularChart.html#Syncfusion_Maui_Toolkit_Charts_SfCircularChart_Series) collection property of [SfCircularChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCircularChart.html).

N> The circular chart has [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCircularChart.html#Syncfusion_Maui_Toolkit_Charts_SfCircularChart_Series) as its default content.

{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>
    <chart:PieSeries ItemsSource="{Binding Data}" 
                     XBindingPath="Product" 
                     YBindingPath="SalesRate"/>
</chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

SfCircularChart chart = new SfCircularChart();

// Create an instance of PieSeries
PieSeries series = new PieSeries();
series.ItemsSource = (new SalesViewModel()).Data;
series.XBindingPath = "Product";
series.YBindingPath = "SalesRate";

// Add the configured series to the chart's series collection.
chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Pie chart type in MAUI Chart](Chart-Types_images/maui_pie_chart.png)

## Radius

The rendering size of the [PieSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.PieSeries.html) can be controlled using the [Radius](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.CircularSeries.html#Syncfusion_Maui_Toolkit_Charts_CircularSeries_Radius) property as shown in the following code sample.

{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>
    <chart:PieSeries ItemsSource="{Binding Data}" 
                     XBindingPath="Product" 
                     YBindingPath="SalesRate"
                     Radius="0.9"/>            
</chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

SfCircularChart chart = new SfCircularChart();

PieSeries series = new PieSeries();
series.ItemsSource = (new SalesViewModel()).Data;
series.XBindingPath = "Product";
series.YBindingPath = "SalesRate";
series.Radius = 0.9; // Set the radius of the pie chart 

chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Pie chart with circular coefficient in MAUI Chart](Chart-Types_images/maui_pie_chart_circularcoefficient.png)

## Semi Pie

By using the [StartAngle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.CircularSeries.html#Syncfusion_Maui_Toolkit_Charts_CircularSeries_StartAngle) and [EndAngle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.CircularSeries.html#Syncfusion_Maui_Toolkit_Charts_CircularSeries_EndAngle) properties, you can draw pie series in different shapes such as semi-pie or quarter pie series.

{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>
    <chart:PieSeries ItemsSource="{Binding Data}"
                     XBindingPath="Product"
                     YBindingPath="SalesRate"
                     StartAngle="180"
                     EndAngle="360"/>
</chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

SfCircularChart chart = new SfCircularChart();

PieSeries series = new PieSeries();
series.ItemsSource = (new SalesViewModel()).Data;
series.XBindingPath = "Product";
series.YBindingPath = "SalesRate";
series.StartAngle = 180; // Set the starting angle for the pie slices
series.EndAngle = 360; // Set the ending angle for the pie slices

chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Semi pie chart in MAUI Chart](Chart-Types_images/maui_semi_pie_chart.png)