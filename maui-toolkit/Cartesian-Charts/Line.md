---
layout: post
title: Line Chart in .NET MAUI Chart control | Syncfusion
description: Learn here all about the line chart and its types in Syncfusion® .NET MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
keywords: .net maui line chart, maui line chart, .net maui chart line type, line chart customization .net maui, syncfusion maui line chart, cartesian line chart maui, .net maui chart line visualization.
---

# Line Chart in .NET MAUI Chart

## Line Chart

Line chart is used to represent data trends at equal intervals by connecting points on a plot with straight lines. To render a line chart, create an instance of [LineSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.LineSeries.html), and add it to the [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html#Syncfusion_Maui_Toolkit_Charts_SfCartesianChart_Series) collection property of [SfCartesianChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html).

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

    <chart:LineSeries ItemsSource="{Binding Data}"
                      XBindingPath="Demand"
                      YBindingPath="Year2010"/>
    <chart:LineSeries ItemsSource="{Binding Data}"
                      XBindingPath="Demand"
                      YBindingPath="Year2011"/>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
CategoryAxis primaryAxis = new CategoryAxis();
chart.XAxes.Add(primaryAxis);
NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

// Create a LineSeries for the chart
LineSeries series1 = new LineSeries()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "Demand",
    YBindingPath = "Year2010",
};

LineSeries series2 = new LineSeries()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "Demand",
    YBindingPath = "Year2011",
};

// Add the line series to the chart
chart.Series.Add(series1);
chart.Series.Add(series2);

this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Line Chart in MAUI](Chart-types-images/maui_line_chart.png)

### Dashed line

The [StrokeDashArray](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.LineSeries.html#Syncfusion_Maui_Toolkit_Charts_LineSeries_StrokeDashArray) property of [LineSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.LineSeries.html) is used to render the line series with dashes. Odd value is considered as rendering size and even value is considered as gap.

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

    <chart:LineSeries ItemsSource="{Binding Data}" 
                      XBindingPath="Demand"
                      YBindingPath="Year2010"
                      StrokeDashArray="{StaticResource dashArray}"/>
    <chart:LineSeries ItemsSource="{Binding Data}" 
                      XBindingPath="Demand"
                      YBindingPath="Year2011"
                      StrokeDashArray="{StaticResource dashArray}"/>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();

// Create a DoubleCollection for the StrokeDashArray, which defines the pattern of dashes and gaps.
DoubleCollection doubleCollection = new DoubleCollection();
doubleCollection.Add(5);
doubleCollection.Add(2);

CategoryAxis primaryAxis = new CategoryAxis();
chart.XAxes.Add(primaryAxis);
NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

LineSeries series1 = new LineSeries()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "Demand",
    YBindingPath = "Year2010",
    StrokeDashArray = doubleCollection // Apply the stroke dash pattern.
};

LineSeries series2 = new LineSeries()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "Demand",
    YBindingPath = "Year2011",
    StrokeDashArray = doubleCollection // Apply the stroke dash pattern.
};

chart.Series.Add(series1);
chart.Series.Add(series2);

this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Dashed line chart in MAUI](Chart-types-images/maui_dashed_line_chart.png)

## Spline Chart 

The [SplineSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SplineSeries.html) resembles line series, but instead of connecting the data points with line segments, the data points are connected by smooth bezier curves.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    <chart:SfCartesianChart.XAxes>
        <chart:CategoryAxis/>
    </chart:SfCartesianChart.XAxes>

    <chart:SfCartesianChart.YAxes>
        <chart:NumericalAxis/>
    </chart:SfCartesianChart.YAxes>  

    <chart:SplineSeries ItemsSource="{Binding Data}" 
                        XBindingPath="Demand"
                        YBindingPath="Year2010"/>
    <chart:SplineSeries ItemsSource="{Binding Data}" 
                        XBindingPath="Demand"
                        YBindingPath="Year2011"/>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
CategoryAxis primaryAxis = new CategoryAxis();
chart.XAxes.Add(primaryAxis);
NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

// Create a SplineSeries for the chart
SplineSeries series1 = new SplineSeries()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "Demand",
    YBindingPath = "Year2010",
};

SplineSeries series2 = new SplineSeries()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "Demand",
    YBindingPath = "Year2011",
};

chart.Series.Add(series1);
chart.Series.Add(series2);

this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Spline chart type in MAUI Chart](Chart-types-images/maui_spline_chart.png)

### Spline rendering types

The [Type](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SplineSeries.html#Syncfusion_Maui_Toolkit_Charts_SplineSeries_Type) property allows you to change the rendering type of spline curve in series. The default value of [Type](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SplineSeries.html#Syncfusion_Maui_Toolkit_Charts_SplineSeries_Type) is [Natural](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SplineType.html#Syncfusion_Maui_Toolkit_Charts_SplineType_Natural).

The following types are used in SplineSeries:

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

    <chart:SplineSeries ItemsSource="{Binding Data}" 
                        XBindingPath="Demand"
                        YBindingPath="Year2010"
                        Type="Cardinal"/>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
CategoryAxis primaryAxis = new CategoryAxis();
chart.XAxes.Add(primaryAxis);
NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

SplineSeries series = new SplineSeries()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "Demand",
    YBindingPath = "Year2010",
    Type = SplineType.Cardinal // Define the spline type as Cardinal, which affects the shape of the curve.
};

chart.Series.Add(series);

this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Spline types chart in MAUI Chart](Chart-types-images/maui_spline_types_chart.png)

## Enable Marker

A marker, also known as a symbol, is used to determine or highlight the position of the data point. To enable markers in the series, set the [ShowMarkers](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.LineSeries.html#Syncfusion_Maui_Toolkit_Charts_LineSeries_ShowMarkers) property to `true`.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    ...
    <chart:LineSeries ItemsSource="{Binding Data}" 
                      XBindingPath="Demand"
                      YBindingPath="Year2010"
                      ShowMarkers="True"/>

    <chart:LineSeries ItemsSource="{Binding Data}"
                      XBindingPath="Demand"
                      YBindingPath="Year2011"
                      ShowMarkers="True"/>                  
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();

...
LineSeries series1 = new LineSeries()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "Demand",
    YBindingPath = "Year2010",
    ShowMarkers = true, // Enable markers to visually highlight data points on the line
};

LineSeries series2 = new LineSeries()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "Demand",
    YBindingPath = "Year2011",
    ShowMarkers = true, // Enable markers to visually highlight data points on the line
};

chart.Series.Add(series1);
chart.Series.Add(series2);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Marker support in MAUI Chart](Chart-types-images/marker_support.png)

### Marker customization

In order to change the series markers appearance, create an instance of the [MarkerSettings](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.LineSeries.html#Syncfusion_Maui_Toolkit_Charts_LineSeries_MarkerSettings) property. The following properties are used to customize marker appearance:

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
    <chart:LineSeries ItemsSource="{Binding Data}" 
                      XBindingPath="Year"
                      YBindingPath="Percentage"
                      ShowMarkers="True">
        <chart:LineSeries.MarkerSettings>
            <chart:ChartMarkerSettings Type="Diamond"
                                       Fill="Brown"
                                       Stroke="Black"
                                       StrokeWidth="1"
                                       Height="8"
                                       Width="8"/>
        </chart:LineSeries.MarkerSettings>
    </chart:LineSeries>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
...
// Set up marker settings for the chart series with a diamond shape
ChartMarkerSettings chartMarker = new ChartMarkerSettings()
{
    Type = ShapeType.Diamond,
    Fill = Colors.Brown,
    Stroke = Colors.Black,
    StrokeWidth = 1,
    Height = 8,
    Width = 8
};

LineSeries series = new LineSeries()
{
   ItemsSource = new ViewModel().Data,
   XBindingPath = "Year",
   YBindingPath = "Percentage",
   ShowMarkers = true,
   MarkerSettings = chartMarker, // Apply the specified marker settings
};

chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}