---
layout: post
title: Markers in .NET MAUI Spark Charts | Syncfusion
description: Learn here all about markers supported in Syncfusion .NET MAUI Spark Charts (SfSparkChart) control and more.
platform: maui
control: SfSparkChart
documentation: ug
---

# Markers in .NET MAUI Spark Charts

## Markers

Markers are used to provide information about the exact point location. You can enable markers using the `ShowMarkers` property in both `SfSparkLineChart`, and `SfSparkAreaChart` widgets.

* [ShowMarkers] - Enables or disables the display of markers for all data points.

{% tabs %}

{% highlight xaml %}

<chart:SfSparkLineChart ItemsSource="{Binding Data}" 
                    YBindingPath="Value"
                    ShowMarkers="True">
. . . 
</chart:SfSparkLineChart>

{% endhighlight %}

{% highlight c# %}

SfSparkChart chart = new SfSparkLineChart()
{
    ItemsSource = new SparkDataViewModel().Data,
    YBindingPath = "Value",
    ShowMarkers = true,
};

this.Content = chart;

{% endhighlight %}

{% endtabs %}

## Marker Customization

You can customize the appearance of markers using the `MarkerSettings` property. This allows you to control visual aspects such as color, shape, and size.

* [Fill] - Used to set the interior color of the marker.
* [Stroke] - Used to define the border color of the marker.
* [StrokeWidth] - Used to specify the thickness of the marker border.
* [Height] - Used to define the vertical size of the marker.
* [Width] - Used to define the horizontal size of the marker.
* [Shape] - Used to set the shape of the marker. Supported values include Circle, Square, Diamond, and Triangle.

{% tabs %}

{% highlight xaml %}

<chart:SfSparkLineChart ItemsSource="{Binding Data}" 
                    YBindingPath="Value"
                    ShowMarkers="True">

    <chart:SfSparkLineChart.MarkerSettings>
        <chart:SparkChartMarkerSettings 
            Stroke="Green"
            Height="5"
            Width="5"
            ShapeType="Diamond"
            StrokeWidth="4"/>
    </chart:SfSparkLineChart.MarkerSettings>
    . . .
</chart:SfSparkLineChart>

{% endhighlight %}

{% highlight c# %}

SfSparkLineChart chart = new SfSparkLineChart()
{
    ItemsSource = new SparkDataViewModel().Data,
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

this.Content = chart;

{% endhighlight %}

{% endtabs %}
