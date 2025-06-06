---
layout: post
title: Stacked Line 100 Chart in .NET MAUI Chart control | Syncfusion
description: Learn here all about stacked line 100 chart support in Syncfusion® .NET MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
---

# Stacked Line 100 Chart in .NET MAUI Chart

## Stacked Line 100

The stacked line 100 chart is a type of chart that displays multiple line series stacked on top of each other, to indicate the cumulative value of the data points at 100%.

To render a stacked line 100 chart, create an instance of the [StackingLine100Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StackingLine100Series.html) and add it to the [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html#Syncfusion_Maui_Toolkit_Charts_SfCartesianChart_Series) collection property of the [SfCartesianChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html).

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

        <chart:StackingLine100Series ItemsSource="{Binding Data1}"
                                     XBindingPath="Month"
                                     YBindingPath="Value">        
        </chart:StackingLine100Series>

        <chart:StackingLine100Series ItemsSource="{Binding Data2}"
                                     XBindingPath="Month"
                                     YBindingPath="Value">         
        </chart:StackingLine100Series>

        <chart:StackingLine100Series ItemsSource="{Binding Data3}"
                                     XBindingPath="Month"
                                     YBindingPath="Value">         
        </chart:StackingLine100Series>

        <chart:StackingLine100Series ItemsSource="{Binding Data4}"
                                     XBindingPath="Month"
                                     YBindingPath="Value">      
        </chart:StackingLine100Series>

    </chart:SfCartesianChart>


{% endhighlight %}

{% highlight c# %}

    SfCartesianChart chart = new SfCartesianChart();
    CategoryAxis primaryAxis = new CategoryAxis();
    chart.XAxes.Add(primaryAxis);
    NumericalAxis secondaryAxis = new NumericalAxis();
    chart.YAxes.Add(secondaryAxis);

    ViewModel viewModel = new ViewModel();

    // Create a StackingLine100Series for the chart
    StackingLine100Series series1 = new  StackingLine100Series()
    {
        ItemsSource = viewModel.Data1,
        XBindingPath = "Month",
        YBindingPath = "Value",
    };

    StackingLine100Series series2 = new StackingLine100Series()
    {
        ItemsSource = viewModel.Data2,
        XBindingPath = "Month",
        YBindingPath = "Value",
    };
    StackingLine100Series series3 = new StackingLine100Series()
    {
        ItemsSource = viewModel.Data3,
        XBindingPath = "Month",
        YBindingPath = "Value",
    };

    StackingLine100Series series4 = new StackingLine100Series()
    {
        ItemsSource = viewModel.Data4
        XBindingPath = "Month",
        YBindingPath = "Value",
    };

    // Add all series to the chart
    chart.Series.Add(series1);
    chart.Series.Add(series2);     
    chart.Series.Add(series3); 
    chart.Series.Add(series4); 
    this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Stacking Line 100 Chart in .NET MAUI Cartesian Charts.](chart-types-images\net-maui-cartesian-charts-stacked-line-100-chart.png)

## Dashed Stacked Line 100

The [StrokeDashArray](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StackingSeriesBase.html#Syncfusion_Maui_Toolkit_Charts_StackingSeriesBase_StrokeDashArray) property of [StackingLine100Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StackingLine100Series.html) is used to render the stacking line 100 series with dashes. Odd value is considered as rendering size and even value is considered as gap.

{% tabs %}

{% highlight xaml %}

    <chart:SfCartesianChart>

        <chart:SfCartesianChart.Resources>
            <DoubleCollection x:Key="dashArray">
                <x:Double>5</x:Double>
                <x:Double>2</x:Double>
            </DoubleCollection>
        </chart:SfCartesianChart.Resources>

        <chart:SfCartesianChart.XAxes>
            <chart:CategoryAxis/>
        </chart:SfCartesianChart.XAxes>

        <chart:SfCartesianChart.YAxes>
            <chart:NumericalAxis/>
        </chart:SfCartesianChart.YAxes>  

        <chart:StackingLine100Series ItemsSource="{Binding Data1}"
                                     XBindingPath="Month"
                                     YBindingPath="Value"  
                                     StrokeDashArray="{StaticResource dashArray}"/>

        <chart:StackingLine100Series ItemsSource="{Binding Data2}"
                                     XBindingPath="Month"
                                     YBindingPath="Value"  
                                     StrokeDashArray="{StaticResource dashArray}"/>

        <chart:StackingLine100Series ItemsSource="{Binding Data3}"
                                     XBindingPath="Month"
                                     YBindingPath="Value"   
                                     StrokeDashArray="{StaticResource dashArray}"/>

        <chart:StackingLine100Series ItemsSource="{Binding Data4}"
                                     XBindingPath="Month"
                                     YBindingPath="Value"       
                                     StrokeDashArray="{StaticResource dashArray}"/>
    </chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

    SfCartesianChart chart = new SfCartesianChart();
    CategoryAxis primaryAxis = new CategoryAxis();
    chart.XAxes.Add(primaryAxis);
    NumericalAxis secondaryAxis = new NumericalAxis();
    chart.YAxes.Add(secondaryAxis);

    ViewModel viewModel = new ViewModel();
    
    // Create a collection of doubles to set the stroke dash pattern for the series
    DoubleCollection doubleCollection = new DoubleCollection();
    doubleCollection.Add(5);
    doubleCollection.Add(2);
    . . .
    StackingLine100Series series1 = new  StackingLine100Series()
    {
        ItemsSource = viewModel.Data1,
        XBindingPath = "Month",
        YBindingPath = "Value",
        StrokeDashArray = doubleCollection // Use defined dash pattern
    };

    StackingLine100Series series2 = new StackingLine100Series()
    {
        ItemsSource = viewModel.Data2,
        XBindingPath = "Month",
        YBindingPath = "Value",
        StrokeDashArray = doubleCollection // Use defined dash pattern
    };

    StackingLine100Series series3 = new StackingLine100Series()       
    {
        ItemsSource = viewModel.Data3,
        XBindingPath = "Month",
        YBindingPath = "Value",
        StrokeDashArray = doubleCollection // Use defined dash pattern
    };

    StackingLine100Series series4 = new StackingLine100Series()
    {
        ItemsSource = viewModel.Data4,
        XBindingPath = "Month",
        YBindingPath = "Value",
        StrokeDashArray = doubleCollection // Use defined dash pattern
    };

    chart.Series.Add(series1);
    chart.Series.Add(series2);     
    chart.Series.Add(series3); 
    chart.Series.Add(series4); 

    this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Dashed Stacked 100 Line chart in MAUI](Chart-types-images/maui_dashed_stacked_line_100_chart.png)

## Enable Marker

A marker, also known as a symbol, is used to determine or highlight the position of the data point. To enable markers in the series, set the [ShowMarkers](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StackingLineSeries.html#Syncfusion_Maui_Toolkit_Charts_StackingLineSeries_ShowMarkers) property to `true`.

{% tabs %}

{% highlight xaml %}

    <chart:SfCartesianChart>
        ...
        <chart:StackingLine100Series ItemsSource="{Binding Data1}"
                                     XBindingPath="Month"
                                     YBindingPath="Value"
                                     ShowMarkers="True"/>

        <chart:StackingLine100Series ItemsSource="{Binding Data2}"
                                     XBindingPath="Month"
                                     YBindingPath="Value"
                                     ShowMarkers="True"/>

        <chart:StackingLine100Series ItemsSource="{Binding Data3}"
                                     XBindingPath="Month"
                                     YBindingPath="Value"
                                     ShowMarkers="True"/>

        <chart:StackingLine100Series ItemsSource="{Binding Data4}"
                                     XBindingPath="Month"
                                     YBindingPath="Value"
                                     ShowMarkers="True"/>

    </chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

    SfCartesianChart chart = new SfCartesianChart();

    ViewModel viewModel = new ViewModel();
    ...
    StackingLine100Series series1 = new  StackingLine100Series()
    {
        ItemsSource = viewModel.Data1,
        XBindingPath = "Month",
        YBindingPath = "Value",
        ShowMarkers = true, // Enable markers on the series for data points
    };

    StackingLine100Series series2 = new StackingLine100Series()
    {
        ItemsSource = viewModel.Data2,
        XBindingPath = "Month",
        YBindingPath = "Value",
        ShowMarkers = true, // Enable markers on the series for data points
    };

    StackingLine100Series series3 = new StackingLine100Series()       
    {
        ItemsSource = viewModel.Data3,
        XBindingPath = "Month",
        YBindingPath = "Value",
        ShowMarkers = true, // Enable markers on the series for data points
    };

    StackingLine100Series series4 = new StackingLine100Series()
    {
        ItemsSource = viewModel.Data4,
        XBindingPath = "Month",
        YBindingPath = "Value",
        ShowMarkers = true, // Enable markers on the series for data points
    };

    chart.Series.Add(series1);
    chart.Series.Add(series2);     
    chart.Series.Add(series3); 
    chart.Series.Add(series4); 

    this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Stacked Line 100 Marker support in MAUI Chart](Chart-types-images/stacked_line_100_marker_support.png)

### Marker customization

In order to change the series markers appearance, create an instance of the [MarkerSettings](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StackingLineSeries.html#Syncfusion_Maui_Toolkit_Charts_StackingLineSeries_MarkerSettings) property. The following properties are used to customize marker appearance.

* [Type](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Type), of type `ShapeType`, describes the shape of the series marker. The default value of this property is [ShapeType.Circle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeType.html#Syncfusion_Maui_Toolkit_Charts_ShapeType_Circle).
* [Stroke](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Stroke), of type `Brush`, indicates the brush used to paint the marker border.
* [StrokeWidth](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_StrokeWidth), of type `double`, indicates the width of the marker border.
* [Fill](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Fill), of type `Brush`, indicates the color of the marker.
* [Width](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Width), of type `double`, indicates the width of the marker.
* [Height](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartMarkerSettings.html#Syncfusion_Maui_Toolkit_Charts_ChartMarkerSettings_Height), of type `double`, indicates the height of the marker.

{% tabs %}

{% highlight xaml %}

    <chart:SfCartesianChart>
        ...
        <chart:StackingLine100Series ItemsSource="{Binding Data}"
                                  XBindingPath="Month"
                                  YBindingPath="Value"
                                  ShowMarkers="True">
            <chart:StackingLine100Series.MarkerSettings>
                <chart:ChartMarkerSettings Type="Diamond" 
                                           StrokeWidth="2"
                                           Fill="White"
                                           Height="8"
                                           Width="8"/>
            </chart:StackingLine100Series.MarkerSettings>    
        </chart:StackingLine100Series>
    </chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

    SfCartesianChart chart = new SfCartesianChart();

    ViewModel viewModel = new ViewModel();
    ...
    // Configure marker settings for the data points in the chart series.
    ChartMarkerSettings chartMarker= new ChartMarkerSettings()
    {
        Type = ShapeType.Diamond,
        Fill = Colors.White,
        StrokeWidth = 2,
        Height = 8,
        Width = 8,
    };

    StackingLine100Series series = new  StackingLine100Series()
    {
        ItemsSource = viewModel.Data,
        XBindingPath = "Month",
        YBindingPath = "Value",
        ShowMarkers= true,
        MarkerSettings = chartMarker, // Apply the marker settings configured above.
    };

    chart.Series.Add(series);
    this.Content = chart;

{% endhighlight %}

{% endtabs %}