---
layout: post
title: StackedArea100 Chart in .NET MAUI Chart control | Syncfusion
description: Learn here all about StackedArea100 chart support in Syncfusion® .NET MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
keywords: .net maui stacked area 100 chart, maui stacked area 100 chart, stacked area 100 chart customization .net maui, syncfusion maui stacked area 100 chart, cartesian stacked area 100 chart maui, .net maui chart stacked area 100 visualization, .net maui 100% stacked area chart.
---

# StackedArea100 Chart in .NET MAUI Chart

The stacked area 100% chart enables users to visually represent data points vertically, one above the other, to indicate the cumulative value of the data points at 100%.

## StackedArea100 Chart

To render the StackedArea100 chart, create an instance of the [StackingArea100Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StackingArea100Series.html), and add it to the [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html#Syncfusion_Maui_Toolkit_Charts_SfCartesianChart_Series) collection property of the [SfCartesianChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html).

N> The Cartesian chart has a [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html#Syncfusion_Maui_Toolkit_Charts_SfCartesianChart_Series) as its default content.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>

    <chart:SfCartesianChart.XAxes>
        <chart:CategoryAxis/>
    </chart:SfCartesianChart.XAxes>

    <chart:SfCartesianChart.YAxes>
        <chart:NumericalAxis/>
    </chart:SfCartesianChart.YAxes>   

    <chart:StackingArea100Series ItemsSource="{Binding Data1}"
                                XBindingPath="Year"
                                YBindingPath="Value"/>        

    <chart:StackingArea100Series ItemsSource="{Binding Data2}"
                                XBindingPath="Year"
                                YBindingPath="Value"/>         

    <chart:StackingArea100Series ItemsSource="{Binding Data3}"
                                XBindingPath="Year"
                                YBindingPath="Value"/>         

    <chart:StackingArea100Series ItemsSource="{Binding Data4}"
                                XBindingPath="Year"
                                YBindingPath="Value"/>         

</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
CategoryAxis primaryAxis = new CategoryAxis();
chart.XAxes.Add(primaryAxis);
NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

ViewModel viewModel = new ViewModel();

// Create a StackingArea100Series for the chart
StackingArea100Series series1 = new StackingArea100Series()
{
    XBindingPath = "Year",
    YBindingPath = "Value",
    ItemsSource = viewModel.Data1
};

StackingArea100Series series2 = new StackingArea100Series()
{
    XBindingPath = "Year",
    YBindingPath = "Value",
    ItemsSource = viewModel.Data2
};

StackingArea100Series series3 = new StackingArea100Series()
{
    XBindingPath = "Year",
    YBindingPath = "Value",
    ItemsSource = viewModel.Data3
};

StackingArea100Series series4 = new StackingArea100Series()
{
    XBindingPath = "Year",
    YBindingPath = "Value",
    ItemsSource = viewModel.Data4
};

// Add all series to the chart
chart.Series.Add(series1);
chart.Series.Add(series2);     
chart.Series.Add(series3); 
chart.Series.Add(series4);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Stacking Area 100 Chart in .NET MAUI Cartesian Charts](chart-types-images/net-maui-cartesian-charts-stacked-area-100-chart.png)

## Enable Marker

A marker, also known as a symbol, is used to determine or highlight the position of the data point. To enable markers in the series, set the [ShowMarkers](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StackingAreaSeries.html#Syncfusion_Maui_Toolkit_Charts_StackingAreaSeries_ShowMarkers) property to `true`.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    ...
    <chart:StackingArea100Series ItemsSource="{Binding Data}"
                                 XBindingPath="Year"
                                 YBindingPath="Value"
                                 ShowMarkers="True"/>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
...
StackingArea100Series series = new StackingArea100Series()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "Year",
    YBindingPath = "Value",
    ShowMarkers = true // Display markers on the series
};

chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

### Marker Customization

To customize the appearance of series markers, create an instance of the [MarkerSettings](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StackingAreaSeries.html#Syncfusion_Maui_Toolkit_Charts_StackingAreaSeries_MarkerSettings) property. The following properties are used to customize marker appearance:

* [Type](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Type), of type `ShapeType`, defines the shape of the series marker. The default value is [ShapeType.Circle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeType.html#Syncfusion_Maui_Toolkit_Charts_ShapeType_Circle).
* [Stroke](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Stroke), of type `Brush`, specifies the brush used to paint the marker border.
* [StrokeWidth](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_StrokeWidth), of type `double`, specifies the width of the marker border.
* [Fill](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Fill), of type `Brush`, specifies the fill color of the marker.
* [Width](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Width), of type `double`, specifies the width of the marker.
* [Height](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Height), of type `double`, specifies the height of the marker.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    ...
    <chart:StackingArea100Series ItemsSource="{Binding Data}"
                                 XBindingPath="Year"
                                 YBindingPath="Value"
                                 ShowMarkers="True">
        <chart:StackingArea100Series.MarkerSettings>
            <chart:ChartMarkerSettings Type="Diamond"
                                       Fill="LightBlue"
                                       Stroke="Blue"
                                       StrokeWidth="1"
                                       Height="8"
                                       Width="8"/>
        </chart:StackingArea100Series.MarkerSettings>
    </chart:StackingArea100Series>
    ...
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
...
// Configure chart marker settings, defining appearance and style
ChartMarkerSettings chartMarker = new ChartMarkerSettings()
{
    Type = ShapeType.Diamond,
    Fill = Colors.LightBlue,
    Stroke = Colors.Blue,
    StrokeWidth = 1,
    Height = 8,
    Width = 8
};

StackingArea100Series series = new StackingArea100Series()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "Year",
    YBindingPath = "Value",
    ShowMarkers = true,
    MarkerSettings = chartMarker  // Apply the defined marker settings to the series
};
...
chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}