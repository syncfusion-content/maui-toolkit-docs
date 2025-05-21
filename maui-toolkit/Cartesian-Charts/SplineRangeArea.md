---
layout: post
title: Spline Range Area Chart in .NET MAUI Chart control | Syncfusion
description: Learn here all about Spline Range Area chart support in Syncfusion® .NET MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
keywords: .net maui spline range area chart, maui spline range area chart, spline range area chart customization .net maui, syncfusion maui spline range area chart, cartesian spline range area chart maui, .net maui chart spline range area visualization.
---

# Spline Range Area Chart in .NET MAUI Chart

## Spline Range Area Chart

Spline Range Area Chart is used to visualize data points with smooth curves. In this series, the area between the curves is filled to indicate a range of values, such as a high and low price range or an upper and lower limit.

To render a spline range area chart, create an instance of [SplineRangeAreaSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SplineRangeAreaSeries.html) and add it to the [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html#Syncfusion_Maui_Toolkit_Charts_SfCartesianChart_Series) collection property of [SfCartesianChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html).

Since the [SplineRangeAreaSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SplineRangeAreaSeries.html) requires two Y values for each point, your data should contain both high and low values. These high and low values specify the maximum and minimum ranges of the point.

N> The Cartesian chart has [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html#Syncfusion_Maui_Toolkit_Charts_SfCartesianChart_Series) as its default content.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>

    <chart:SfCartesianChart.XAxes>
        <chart:CategoryAxis/>
    </chart:SfCartesianChart.XAxes>

    <chart:SfCartesianChart.YAxes>
        <chart:NumericalAxis/>
    </chart:SfCartesianChart.YAxes>   

    <chart:SplineRangeAreaSeries ItemsSource="{Binding Data}"
                                 XBindingPath="XValue"
                                 High="HighValue"
                                 Low="LowValue"/>

</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();

CategoryAxis primaryAxis = new CategoryAxis();
chart.XAxes.Add(primaryAxis);

NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

// Create a SplineRangeAreaSeries for the chart
SplineRangeAreaSeries series = new SplineRangeAreaSeries()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "XValue",
    High = "HighValue",
    Low = "LowValue",
};

// Add the SplineRangeAreaSeries to the chart's series collection
chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Spline range area chart type in MAUI Chart](Chart-types-images/maui_spline_range_area_chart.png)

## Spline Rendering Types

The [Type](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SplineRangeAreaSeries.html#Syncfusion_Maui_Toolkit_Charts_SplineRangeAreaSeries_Type) property allows you to change the rendering type of the spline curve in the series. The default value of [Type](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SplineRangeAreaSeries.html#Syncfusion_Maui_Toolkit_Charts_SplineRangeAreaSeries_Type) is [Natural](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SplineType.html#Syncfusion_Maui_Toolkit_Charts_SplineType_Natural).

The following types are available in [SplineRangeAreaSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SplineRangeAreaSeries.html):

* `Natural`
* `Monotonic`
* `Cardinal`
* `Clamped`

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>

    <chart:SfCartesianChart.XAxes>
        <chart:CategoryAxis/>
    </chart:SfCartesianChart.XAxes>

    <chart:SfCartesianChart.YAxes>
        <chart:NumericalAxis/>
    </chart:SfCartesianChart.YAxes>  

    <chart:SplineRangeAreaSeries ItemsSource="{Binding Data}"
                                 XBindingPath="XValue"
                                 High="HighValue"
                                 Low="LowValue"
                                 Type="Cardinal"/>

</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();

CategoryAxis primaryAxis = new CategoryAxis();
chart.XAxes.Add(primaryAxis);

NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

SplineRangeAreaSeries series = new SplineRangeAreaSeries()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "XValue",
    High = "HighValue",
    Low = "LowValue",
    Type = SplineType.Cardinal // Set the type of the spline to 'Cardinal'
};

chart.Series.Add(series);

this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Spline types in MAUI Spline range area chart](Chart-types-images/maui_spline_range_area_types_chart.png)

## Enable Markers

A marker, also known as a symbol, is used to indicate or highlight the position of a data point. To enable markers in the series, set the [ShowMarkers](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SplineRangeAreaSeries.html#Syncfusion_Maui_Toolkit_Charts_SplineRangeAreaSeries_ShowMarkers) property to true.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    ...
    <chart:SplineRangeAreaSeries ItemsSource="{Binding Data}"
                                 XBindingPath="XValue"
                                 High="HighValue"
                                 Low="LowValue"
                                 ShowMarkers="True"/>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
...
SplineRangeAreaSeries series = new SplineRangeAreaSeries()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "XValue",
    High = "HighValue",
    Low = "LowValue",
    ShowMarkers = true,  // Display markers on the data points
};

chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

### Marker Customization

To customize the appearance of series markers, create an instance of the [MarkerSettings](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SplineRangeAreaSeries.html#Syncfusion_Maui_Toolkit_Charts_SplineRangeAreaSeries_MarkerSettings) property. The following properties are used to customize marker appearance:

* [Type](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Type) - Defines the shape of the series marker. The default value is [ShapeType.Circle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeType.html#Syncfusion_Maui_Toolkit_Charts_ShapeType_Circle).
* [Stroke](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Stroke) - Specifies the brush used to paint the marker border.
* [StrokeWidth](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_StrokeWidth) - Specifies the width of the marker border.
* [Fill](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Fill) - Specifies the color of the marker.
* [Width](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Width) - Specifies the width of the marker.
* [Height](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Height) - Specifies the height of the marker.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    ...
    <chart:SplineRangeAreaSeries ItemsSource="{Binding Data}" 
                                 XBindingPath="XValue"
                                 High="HighValue"
                                 Low="LowValue"
                                 ShowMarkers="True">
        <chart:SplineRangeAreaSeries.MarkerSettings>
            <chart:ChartMarkerSettings Type="Diamond"
                                       Fill="Brown"
                                       Stroke="Black"
                                       StrokeWidth="1"
                                       Height="8"
                                       Width="8"/>
        </chart:SplineRangeAreaSeries.MarkerSettings>
    </chart:SplineRangeAreaSeries>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
...
// Configure marker settings for the chart series
ChartMarkerSettings chartMarker = new ChartMarkerSettings()
{
    Type = ShapeType.Diamond,
    Fill = Colors.Brown,
    Stroke = Colors.Black,
    StrokeWidth = 1,
    Height = 8,
    Width = 8,
};

SplineRangeAreaSeries series = new SplineRangeAreaSeries()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "XValue",
    High = "HighValue",
    Low = "LowValue",
    ShowMarkers = true,
    MarkerSettings = chartMarker, // Apply the configured marker settings
};

chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}