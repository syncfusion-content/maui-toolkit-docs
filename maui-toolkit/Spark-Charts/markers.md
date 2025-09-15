---
layout: post
title: Markers in .NET MAUI Spark Chart Control | Syncfusion
description: Learn here all about the markers supported in Syncfusion .NET MAUI Spark Charts (SfSparkChart) control and more.
platform: maui-toolkit
control: SfSparkChart
documentation: ug
---

# Markers in .NET MAUI Spark Charts

Markers, also known as symbols, are used to indicate or highlight the position of data points in the `SfSparkLineChart` and `SfSparkAreaChart`.

## Enable Marker

To enable markers in the `SfSparkLineChart` and `SfSparkAreaChart`, set the `ShowMarkers` property to `true`. Its default value is `false`.

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkLineChart ItemsSource="{Binding Data}" 
                    YBindingPath="Value"
                    ShowMarkers="True">
. . . 
</sparkchart:SfSparkLineChart>

{% endhighlight %}

{% highlight c# %}

SfSparkLineChart sparkchart = new SfSparkLineChart()
{
    ItemsSource = new SparkChartViewModel().Data,
    YBindingPath = "Value",
    ShowMarkers = true,
};

this.Content = sparkchart;

{% endhighlight %}

{% endtabs %}

## Marker Customization

To change the appearance of markers in the `SfSparkLineChart` and `SfSparkAreaChart`, create an instance of the `MarkerSettings` property. The following properties can be used to customize the marker's appearance.

* `ShapeType`, of type `SparkChartMarkerShape`, describes the shape of the marker. The default value of this property is `SparkChartMarkerShape.Circle`.
* `Stroke`, of type `Brush`, indicates the brush used to paint the marker border.
* `StrokeWidth`, of type `double`, indicates the width of the marker border.
* `Fill`, of type `Brush`, indicates the color of the marker.
* `Width`, of type `double`, indicates the width of the marker.
* `Height`, of type `double`, indicates the height of the marker.

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkLineChart ItemsSource="{Binding Data}" 
                    YBindingPath="Value"
                    ShowMarkers="True">

    <sparkchart:SfSparkLineChart.MarkerSettings>
        <sparkchart:SparkChartMarkerSettings 
            Stroke="Green"
            Height="5"
            Width="5"
            ShapeType="Diamond"
            StrokeWidth="4"/>
    </sparkchart:SfSparkLineChart.MarkerSettings>
    . . .
</sparkchart:SfSparkLineChart>

{% endhighlight %}

{% highlight c# %}

SfSparkLineChart sparkchart = new SfSparkLineChart()
{
    ItemsSource = new SparkChartViewModel().Data,
    YBindingPath = "Value",
    ShowMarkers = true,
    MarkerSettings = new SparkChartMarkerSettings
    {
        Stroke = new SolidColorBrush(Colors.Green),
        Height = 5,
        Width = 5,
        ShapeType = SparkChartMarkerShape.Diamond,
        StrokeWidth = 4,
    }
};

this.Content = sparkchart;

{% endhighlight %}

{% endtabs %}
