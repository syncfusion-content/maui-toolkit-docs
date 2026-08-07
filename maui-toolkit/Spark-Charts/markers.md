---
layout: post
title: Markers in .NET MAUI Spark Charts | Syncfusion®
description: Markers in .NET MAUI Spark Charts highlight data points with customizable marker styles, improving data visibility and trend identification.
platform: maui-toolkit
control: SfSparkChart
documentation: ug
---

# Markers in .NET MAUI Spark Charts

N> **Prerequisite:** Ensure that the required NuGet package is installed, the necessary namespaces are imported, and the **Spark Charts** control is properly configured in your application. For detailed setup and configuration instructions, refer to the **[Getting Started](https://help.syncfusion.com/maui-toolkit/spark-charts/getting-started)** guide.

Markers highlight the position of data points in the [SfSparkLineChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkLineChart.html) and [SfSparkAreaChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkAreaChart.html). Markers are supported only on the spark line and spark area charts.

## Enable Marker

To enable markers in the [SfSparkLineChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkLineChart.html) and [SfSparkAreaChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkAreaChart.html) controls, set the [ShowMarkers](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkLineChart.html#Syncfusion_Maui_Toolkit_SparkCharts_SfSparkLineChart_ShowMarkers) property to `true`. Its default value is `false`.

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkLineChart ItemsSource="{Binding Data}" 
                    YBindingPath="Value"
                    ShowMarkers="True">
    <!-- code omitted for brevity -->
</sparkchart:SfSparkLineChart>

{% endhighlight %}

{% highlight c# %}

SfSparkLineChart sparkchart = new SfSparkLineChart()
{
    ItemsSource = new SparkChartViewModel().Data,
    YBindingPath = "Value",
    ShowMarkers = true,
};
//code omitted for brevity
this.Content = sparkchart;

{% endhighlight %}

{% endtabs %}

![Spark Line Chart with marker in .NET MAUI](markers_images/MAUI_marker.png)

## Marker Customization

To customize the appearance of markers in the [SfSparkLineChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkLineChart.html) and [SfSparkAreaChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkAreaChart.html), set the [MarkerSettings](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkLineChart.html#Syncfusion_Maui_Toolkit_SparkCharts_SfSparkLineChart_MarkerSettings) property to a new [SparkChartMarkerSettings](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SparkChartMarkerSettings.html) instance. The configuration is identical for both spark line and spark area charts. The following properties can be used to customize the marker's appearance.

* [ShapeType](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SparkChartMarkerSettings.html#Syncfusion_Maui_Toolkit_SparkCharts_SparkChartMarkerSettings_ShapeType), of type [SparkChartMarkerShape](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SparkChartMarkerShape.html), describes the shape of the marker. The default value of this property is [SparkChartMarkerShape.Circle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SparkChartMarkerShape.html#Syncfusion_Maui_Toolkit_SparkCharts_SparkChartMarkerShape_Circle). Supported shapes include `Circle`, `Diamond`, `Rectangle`, `Triangle`, `Cross`, `Pentagon`, `Star`, and `InvertedTriangle`.
* [Stroke](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SparkChartMarkerSettings.html#Syncfusion_Maui_Toolkit_SparkCharts_SparkChartMarkerSettings_Stroke), of type `Brush`, indicates the brush used to paint the marker border. The default value is `null`.
* [StrokeWidth](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SparkChartMarkerSettings.html#Syncfusion_Maui_Toolkit_SparkCharts_SparkChartMarkerSettings_StrokeWidth), of type `double`, indicates the width of the marker border. The default value is `0`.
* [Fill](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SparkChartMarkerSettings.html#Syncfusion_Maui_Toolkit_SparkCharts_SparkChartMarkerSettings_Fill), of type `Brush`, indicates the brush used to fill the marker. The default value is `null`.
* [Width](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SparkChartMarkerSettings.html#Syncfusion_Maui_Toolkit_SparkCharts_SparkChartMarkerSettings_Width), of type `double`, indicates the width of the marker. The default value is `8`.
* [Height](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SparkChartMarkerSettings.html#Syncfusion_Maui_Toolkit_SparkCharts_SparkChartMarkerSettings_Height), of type `double`, indicates the height of the marker. The default value is `8`.

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkLineChart ItemsSource="{Binding Data}" 
                    YBindingPath="Value"
                    ShowMarkers="True">

    <sparkchart:SfSparkLineChart.MarkerSettings>
        <sparkchart:SparkChartMarkerSettings 
            Fill="Yellow"
            Stroke="Green"
            Height="5"
            Width="5"
            ShapeType="Diamond"
            StrokeWidth="4"/>
    </sparkchart:SfSparkLineChart.MarkerSettings>
    <!-- code omitted for brevity -->
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
        Fill = new SolidColorBrush(Colors.Yellow),
        Stroke = new SolidColorBrush(Colors.Green),
        Height = 5,
        Width = 5,
        ShapeType = SparkChartMarkerShape.Diamond,
        StrokeWidth = 4,
    }
};
//code omitted for brevity
this.Content = sparkchart;

{% endhighlight %}

{% endtabs %}

![Spark Line Chart with marker settings in .NET MAUI](markers_images/MAUI_marker_customized.png)