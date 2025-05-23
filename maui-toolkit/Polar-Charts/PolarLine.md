---
layout: post
title: Polar Line Chart in .NET MAUI Chart Control | Syncfusion
description: Learn here all about the Polar line chart type and its features in the Syncfusion® .NET MAUI Chart (SfPolarChart) control.
platform: maui-toolkit
control: SfPolarChart
documentation: ug
---

# Polar Line Chart in .NET MAUI Chart

## Polar Line Chart

To display a line series in a polar chart, instantiate the [PolarLineSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.PolarLineSeries.html) and include it in the [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPolarChart.html#Syncfusion_Maui_Toolkit_Charts_SfPolarChart_Series) collection property of [SfPolarChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPolarChart.html).

{% tabs %}

{% highlight xaml %}

<chart:SfPolarChart>
    <chart:SfPolarChart.PrimaryAxis>
        <chart:CategoryAxis/>
    </chart:SfPolarChart.PrimaryAxis>

    <chart:SfPolarChart.SecondaryAxis>
        <chart:NumericalAxis/>
    </chart:SfPolarChart.SecondaryAxis>   

    <chart:PolarLineSeries ItemsSource="{Binding PlantDetails}" XBindingPath="Direction" YBindingPath="Tree"/>  
</chart:SfPolarChart>

{% endhighlight %}

{% highlight c# %}

// Create a new instance of SfPolarChart
SfPolarChart chart = new SfPolarChart();

// Create and set the primary axis (X-axis) as a CategoryAxis
CategoryAxis primaryAxis = new CategoryAxis();
chart.PrimaryAxis = primaryAxis;

// Create and set the secondary axis (Y-axis) as a NumericalAxis
NumericalAxis secondaryAxis = new NumericalAxis();
chart.SecondaryAxis = secondaryAxis;

// Create a new PolarLineSeries and configure its properties
PolarLineSeries series = new PolarLineSeries()
{
    ItemsSource = new ViewModel().PlantDetails,
    XBindingPath = "Direction",
    YBindingPath = "Tree"
};

// Add the configured series to the chart's Series collection
chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Polar line chart type in MAUI Chart](Chart-types_images/MAUI_polar_line_chart.png)

## Grid line Type

The [GridLineType](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPolarChart.html#Syncfusion_Maui_Toolkit_Charts_SfPolarChart_GridLineType) property used to customize the rendering style of axis grid lines. The default [GridLineType](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPolarChart.html#Syncfusion_Maui_Toolkit_Charts_SfPolarChart_GridLineType) is [Circle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.PolarChartGridLineType.html#Syncfusion_Maui_Toolkit_Charts_PolarChartGridLineType_Circle). Switching to the [Polygon](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.PolarChartGridLineType.html#Syncfusion_Maui_Toolkit_Charts_PolarChartGridLineType_Polygon) grid line type transforms the polar chart appearance, resembling a spider or web chart.

{% tabs %}

{% highlight xaml %}

<chart:SfPolarChart GridLineType="Polygon"> 
    . . .
    <chart:PolarLineSeries ItemsSource="{Binding PlantDetails}" XBindingPath="Direction" YBindingPath="Tree"/>  
</chart:SfPolarChart>

{% endhighlight %}

{% highlight c# %}

// Create a new instance of SfPolarChart
SfPolarChart chart = new SfPolarChart();

// Set the grid line type to Polygon
chart.GridLineType = PolarChartGridLineType.Polygon;

// ... (other chart configurations)

// Create a new PolarLineSeries
PolarLineSeries series = new PolarLineSeries()
{
    ItemsSource = new ViewModel().PlantDetails,
    XBindingPath = "Direction",
    YBindingPath = "Tree"
};

// Add the series to the chart's Series collection
chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Polar gridline type in MAUI Chart](Chart-types_images/MAUI_polar_line_gridline.png)

## Closed Series

The [IsClosed](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.PolarSeries.html#Syncfusion_Maui_Toolkit_Charts_PolarSeries_IsClosed) property is used to render the series with or without closed path. The default value of [IsClosed](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.PolarSeries.html#Syncfusion_Maui_Toolkit_Charts_PolarSeries_IsClosed) is `true`.

{% tabs %}

{% highlight xaml %}

<chart:SfPolarChart> 
    . . .
    <chart:PolarLineSeries ItemsSource="{Binding PlantDetails}" XBindingPath="Direction" YBindingPath="Tree"
                           IsClosed="False"/>  
</chart:SfPolarChart>

{% endhighlight %}

{% highlight c# %}

// Create a new instance of SfPolarChart
SfPolarChart chart = new SfPolarChart();
. . .

// Create a new PolarLineSeries
PolarLineSeries series = new PolarLineSeries()
{
    ItemsSource = new ViewModel().PlantDetails,
    XBindingPath = "Direction",
    YBindingPath = "Tree",
    // Set whether the line series should be closed or open
    // False means the start and end points won't be connected
    IsClosed = "False"
};

// Add the series to the chart's Series collection
chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Polar open series in MAUI Chart](Chart-types_images/MAUI_polar_line_IsClosed.png)

## Enable Marker

A marker, also known as a symbol, is used to determine or highlight the position of the data point. To enable markers in the series, set the [ShowMarkers](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.PolarSeries.html#Syncfusion_Maui_Toolkit_Charts_PolarSeries_ShowMarkers) property to true.

{% tabs %}

{% highlight xaml %}

<chart:SfPolarChart>
    ...
    <chart:PolarLineSeries ItemsSource="{Binding PlantDetails}" XBindingPath="Direction" YBindingPath="Tree" 
                           ShowMarkers="True"/>
</chart:SfPolarChart>

{% endhighlight %}

{% highlight c# %}

// Create a new instance of SfPolarChart
SfPolarChart chart = new SfPolarChart();
...

// Create a new PolarLineSeries
PolarLineSeries series = new PolarLineSeries()
{
    ItemsSource = new ViewModel().PlantDetails,
    XBindingPath = "Direction",
    YBindingPath = "Tree",
    ShowMarkers = true // Enable markers at data points
};

// Add the series to the chart's collection of series
chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

### Marker customization

In order to change the series markers appearance, create an instance of the [MarkerSettings](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.PolarSeries.html#Syncfusion_Maui_Toolkit_Charts_PolarSeries_MarkerSettings) property. The following properties are used to customize marker appearance.

* [Type](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Type), of type `ShapeType`, describes the shape of the series marker. The default value of this property is `ShapeType.Circle`.
* [Stroke](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Stroke), of type `Brush`, indicates the brush used to paint the marker border.
* [StrokeWidth](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_StrokeWidth), of type `double`, indicates the width of the marker border.
* [Fill](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Fill), of type `Brush`, indicates the color of the marker.
* [Width](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Width), of type `double`, indicates the width of the marker.
* [Height](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Height), of type `double`, indicates the height of the marker.

{% tabs %}

{% highlight xaml %}

<chart:SfPolarChart>
    ...
    <chart:PolarLineSeries ItemsSource="{Binding PlantDetails}" XBindingPath="Direction" YBindingPath="Tree"
                           ShowMarkers="True">
        <chart:PolarLineSeries.MarkerSettings>
            <chart:ChartMarkerSettings Type="Diamond" Fill="Brown" Stroke="Black"
                                       StrokeWidth="1" Height="8" Width="8"/>
        </chart:PolarLineSeries.MarkerSettings>
    </chart:PolarLineSeries>
</chart:SfPolarChart>

{% endhighlight %}

{% highlight c# %}

// Create a new SfPolarChart instance
SfPolarChart chart = new SfPolarChart();
...

// Create and configure ChartMarkerSettings
ChartMarkerSettings chartMarker = new ChartMarkerSettings();
chartMarker.Type = ShapeType.Diamond; // Set marker shape to diamond
chartMarker.Fill = Colors.Brown; // Set fill color for markers
chartMarker.Stroke = Colors.Black; // Set outline color for markers
chartMarker.StrokeWidth = 1; // Set outline width for markers
chartMarker.Height = 8; // Set marker height
chartMarker.Width = 8; // Set marker width

// Create a new PolarLineSeries
PolarLineSeries series = new PolarLineSeries()
{
    ItemsSource = new ViewModel().PlantDetails,
    XBindingPath = "Direction",
    YBindingPath = "Tree",
    ShowMarkers = true, // Enable markers for data points
    MarkerSettings = chartMarker // Apply marker settings to the series
};

// Add the series to the chart
chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}