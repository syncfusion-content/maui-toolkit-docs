---
layout: post
title: Error Bar Chart in .NET MAUI Chart Control | Syncfusion
description: Learn here all about error bar chart support in Syncfusion® .NET MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
keywords: .net maui error bar chart, error bar chart customization .net maui, syncfusion maui error bar chart, cartesian error bar chart maui, .net maui chart error bar visualization, .net maui uncertainty chart.
---

# Error Bar in .NET MAUI Chart

## Error Bar Chart

[ErrorBarSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarSeries.html) indicates the errors or uncertainty in reported values. This helps visualize the possible variations in measurements, and in the Chart control these values are displayed as data points.
The [HorizontalErrorValue](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarSeries.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarSeries_HorizontalErrorValue) and the [VerticalErrorValue](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarSeries.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarSeries_VerticalErrorValue) properties are used to set the error value (variation) to the series.

N> The Error Bar is not an individual chart; it associates with a main chart. Here, we use `Scatter Series Chart` as the main chart with the Error Bar Series Chart support.

The following code examples illustrate how to create an error bar series:

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>

    <chart:SfCartesianChart.XAxes>
        <chart:NumericalAxis/>
    </chart:SfCartesianChart.XAxes>

    <chart:SfCartesianChart.YAxes>
        <chart:NumericalAxis/>
    </chart:SfCartesianChart.YAxes>   

    <chart:ScatterSeries ItemsSource="{Binding EnergyProductions}" 
                         XBindingPath="ID" 
                         YBindingPath="Coal"
                         PointHeight="20"
                         PointWidth="20"/>
    <chart:ErrorBarSeries ItemsSource="{Binding EnergyProductions}"
                          XBindingPath="ID"
                          YBindingPath="Coal"
                          VerticalErrorValue="50"
                          HorizontalErrorValue="0.5"/>

</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
NumericalAxis primaryAxis = new NumericalAxis();
chart.XAxes.Add(primaryAxis);
NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

// Create a scatter series to plot data points
ScatterSeries scatterSeries = new ScatterSeries()
{
    ItemsSource = new ViewModel().EnergyProductions,
    XBindingPath = "ID",
    YBindingPath = "Coal",
    PointWidth = 20,
    PointHeight = 20
};

// Create an error bar series to display error ranges
ErrorBarSeries errorBar = new ErrorBarSeries()
{
    ItemsSource = new ViewModel().EnergyProductions,
    XBindingPath = "ID",
    YBindingPath = "Coal",
    HorizontalErrorValue = 0.5,
    VerticalErrorValue = 50
};

// Add both series to the chart's series collection
chart.Series.Add(scatterSeries);
chart.Series.Add(errorBar);

this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Error Bar Series in MAUI Chart](Chart-types-images/maui_errorbar_BasicRendering.png)

## Mode 
The error bar mode specifies whether the error bar should be drawn horizontally, vertically, or both. The [Mode](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarSeries.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarSeries_Mode) property is used to switch the error bar mode. By default, the Mode value is [Both](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarMode.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarMode_Both), which will display both horizontal and vertical error values.

### Both
To view both the horizontal and vertical error values, you can set the Mode as `Both` as shown in the following code example:

{% tabs %}

{% highlight xaml %}

<chart:ErrorBarSeries ItemsSource="{Binding EnergyProductions}"
                      XBindingPath="ID"
                      YBindingPath="Coal"
                      VerticalErrorValue="50"
                      HorizontalErrorValue="0.5"
                      Mode="Both">
</chart:ErrorBarSeries>

{% endhighlight %}

{% highlight c# %}

ErrorBarSeries errorBar = new ErrorBarSeries()
{
    ItemsSource = new ViewModel().EnergyProductions,
    XBindingPath = "ID",
    YBindingPath = "Coal",
    HorizontalErrorValue = 0.5,
    VerticalErrorValue = 50,
    Mode = ErrorBarMode.Both  // Specifies the mode of the error bars
};

{% endhighlight %}

{% endtabs %}

![Both Mode Support in Error Bar Series](Chart-types-images/maui_errorbar_BasicRendering.png)

### Horizontal

To view only horizontal error values, you can set the Mode as `Horizontal` as shown in the following code example:

{% tabs %}

{% highlight xaml %}

<chart:ErrorBarSeries ItemsSource="{Binding EnergyProductions}"
                      XBindingPath="ID"
                      YBindingPath="Coal"
                      VerticalErrorValue="50"
                      HorizontalErrorValue="0.5"
                      Mode="Horizontal">
</chart:ErrorBarSeries>

{% endhighlight %}

{% highlight c# %}

ErrorBarSeries errorBar = new ErrorBarSeries()
{
    ItemsSource = new ViewModel().EnergyProductions,
    XBindingPath = "ID",
    YBindingPath = "Coal",
    HorizontalErrorValue = 0.5,
    VerticalErrorValue = 50,
    Mode = ErrorBarMode.Horizontal
};

chart.Series.Add(errorBar);

{% endhighlight %}

{% endtabs %}

![Horizontal Mode Support in Error Bar Series](Chart-types-images/maui_errorbar_ModeHorizontal.png)

### Vertical

To view only vertical error values, you can set the Mode as `Vertical`, as shown in the following code example:

{% tabs %}

{% highlight xaml %}

<chart:ErrorBarSeries ItemsSource="{Binding EnergyProductions}"
                      XBindingPath="ID"
                      YBindingPath="Coal"
                      VerticalErrorValue="50"
                      HorizontalErrorValue="0.5"
                      Mode="Vertical">              
</chart:ErrorBarSeries>

{% endhighlight %}

{% highlight c# %}

ErrorBarSeries errorBar = new ErrorBarSeries()
{
    ItemsSource = new ViewModel().EnergyProductions,
    XBindingPath = "ID",
    YBindingPath = "Coal",
    HorizontalErrorValue = 0.5,
    VerticalErrorValue = 50,
    Mode = ErrorBarMode.Vertical
};

chart.Series.Add(errorBar);

{% endhighlight %}

{% endtabs %}

![Vertical Mode Support in Error Bar Series](Chart-types-images/maui_errorbar_ModeVertical.png)


## Direction 

The [HorizontalDirection](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarSeries.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarSeries_HorizontalDirection) and [VerticalDirection](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarSeries.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarSeries_VerticalDirection) properties specify whether to show positive, negative, or both directions of error values.

[ErrorBarDirection](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarDirection.html) contains the following values:

* `Both` - It indicates the actual data point value along with specific amounts of positive and negative error values.
* `Plus` - It indicates the actual data point value along with a specific amount of positive error value.
* `Minus` - It indicates the actual data point value along with a specific amount of negative error value.

The following code illustrates how to set the [HorizontalDirection](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarSeries.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarSeries_HorizontalDirection) and the [VerticalDirection](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarSeries.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarSeries_VerticalDirection) values to an error bar chart:

{% tabs %}

{% highlight xaml %}

<chart:ErrorBarSeries ItemsSource="{Binding EnergyProductions}"
                      XBindingPath="ID"
                      YBindingPath="Coal"
                      VerticalErrorValue="50"
                      HorizontalErrorValue="0.5"
                      HorizontalDirection="Plus"
                      VerticalDirection="Minus">
</chart:ErrorBarSeries>

{% endhighlight %}

{% highlight c# %}

ErrorBarSeries errorBar = new ErrorBarSeries()
{
    ItemsSource = new ViewModel().EnergyProductions,
    XBindingPath = "ID",
    YBindingPath = "Coal",
    HorizontalErrorValue = 0.5,
    VerticalErrorValue = 50,
    HorizontalDirection = ErrorBarDirection.Plus, // Sets the direction of the horizontal error bars
    VerticalDirection = ErrorBarDirection.Minus // Sets the direction of the vertical error bars
};

{% endhighlight %}

{% endtabs %}

![Direction Configuration in Error Bar Series](Chart-types-images/maui_errorbar_Direction.png)

## Type

The [Type](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarSeries.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarSeries_Type) property is used to define the error bar type value as [Fixed](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarType.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarType_Fixed), [Custom](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarType.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarType_Custom), [Percentage](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarType.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarType_Percentage), [StandardDeviation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarType.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarType_StandardDeviation), or [StandardError](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarType.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarType_StandardError). The default value of this property is [Fixed](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarType.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarType_Fixed). For all types, you need to set the values for [HorizontalErrorValue](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarSeries.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarSeries_HorizontalErrorValue) and [VerticalErrorValue](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarSeries.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarSeries_VerticalErrorValue) except for [Custom](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarType.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarType_Custom).

### Fixed

{% tabs %}

{% highlight xaml %}

<chart:ErrorBarSeries ItemsSource="{Binding EnergyProductions}"
                      XBindingPath="ID"
                      YBindingPath="Coal"
                      VerticalErrorValue="50"
                      HorizontalErrorValue="0.5"
                      Type="Fixed">                             
</chart:ErrorBarSeries>

{% endhighlight %}

{% highlight c# %}

ErrorBarSeries errorBar = new ErrorBarSeries()
{
    ItemsSource = new ViewModel().EnergyProductions,
    XBindingPath = "ID",
    YBindingPath = "Coal",
    HorizontalErrorValue = 0.5,
    VerticalErrorValue = 50,
    Type = ErrorBarType.Fixed,  // Specify the type of error bars
};

{% endhighlight %}

{% endtabs %}

![Fixed Type in Error Bar Series](Chart-types-images/maui_errorbar_BasicRendering.png)

### Percentage

{% tabs %}

{% highlight xaml %}

<chart:ErrorBarSeries ItemsSource="{Binding EnergyProductions}"
                      XBindingPath="ID"
                      YBindingPath="Coal"
                      VerticalErrorValue="50"
                      HorizontalErrorValue="0.5"
                      Type="Percentage">
</chart:ErrorBarSeries>

{% endhighlight %}

{% highlight c# %}

ErrorBarSeries errorBar = new ErrorBarSeries()
{
    ItemsSource = new ViewModel().EnergyProductions,
    XBindingPath = "ID",
    YBindingPath = "Coal",
    HorizontalErrorValue = 0.5,
    VerticalErrorValue = 50,
    Type = ErrorBarType.Percentage, // Specify the type of error bars
};

{% endhighlight %}

{% endtabs %}

![Percentage Type in Error Bar Series](Chart-types-images/maui_errorbar_TypePercentage.png)

### Standard Error

{% tabs %}

{% highlight xaml %}

<chart:ErrorBarSeries ItemsSource="{Binding EnergyProductions}"
                      XBindingPath="ID"
                      YBindingPath="Coal"
                      VerticalErrorValue="50"
                      HorizontalErrorValue="0.5"
                      Type="StandardError">
</chart:ErrorBarSeries>

{% endhighlight %}

{% highlight c# %}

ErrorBarSeries errorBar = new ErrorBarSeries()
{
    ItemsSource = new ViewModel().EnergyProductions,
    XBindingPath = "ID",
    YBindingPath = "Coal",
    HorizontalErrorValue = 0.5,
    VerticalErrorValue = 50,
    Type = ErrorBarType.StandardError, // Specify the type of error bars
};

{% endhighlight %}

{% endtabs %}

![Standard Error Type in Error Bar Series](Chart-types-images/maui_errorbar_TypeStandardError.png)

### Standard Deviation

{% tabs %}

{% highlight xaml %}

<chart:ErrorBarSeries ItemsSource="{Binding EnergyProductions}"
                      XBindingPath="ID"
                      YBindingPath="Coal"
                      VerticalErrorValue="50"
                      HorizontalErrorValue="0.5"
                      Type="StandardDeviation">
</chart:ErrorBarSeries>

{% endhighlight %}

{% highlight c# %}

ErrorBarSeries errorBar = new ErrorBarSeries()
{
    ItemsSource = new ViewModel().EnergyProductions,
    XBindingPath = "ID",
    YBindingPath = "Coal",
    HorizontalErrorValue = 0.5,
    VerticalErrorValue = 50,
    Type = ErrorBarType.StandardDeviation, // Specify the type of error bars
};

{% endhighlight %}

{% endtabs %}

![Standard Deviation Type in Error Bar Series](Chart-types-images/maui_errorbar_TypeStandardDeviation.png)

### Custom

If the Type is Custom, you have to bind the [HorizontalErrorPath](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarSeries.html#Syncfusion_Maui_Charts_ErrorBarSeries_HorizontalErrorPath) and the [VerticalErrorPath](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarSeries.html#Syncfusion_Maui_Charts_ErrorBarSeries_VerticalErrorPath) as shown in the following code sample:

{% tabs %}

{% highlight xaml %}

<chart:ErrorBarSeries ItemsSource="{Binding EnergyProductions}"
                      XBindingPath="ID"
                      YBindingPath="Coal"
                      VerticalErrorValue="50"
                      HorizontalErrorValue="0.5"
                      Type="Custom"
                      HorizontalErrorPath="HorizontalErrorValue"
                      VerticalErrorPath="VerticalErrorValue">    
</chart:ErrorBarSeries>

{% endhighlight %}

{% highlight c# %}

ErrorBarSeries errorBar = new ErrorBarSeries()
{
    ItemsSource = new ViewModel().EnergyProductions,
    XBindingPath = "ID",
    YBindingPath = "Coal",
    HorizontalErrorValue = 0.5,
    VerticalErrorValue = 50,
    Type = ErrorBarType.Custom, // Specify the type of error bars
    HorizontalErrorPath = "HorizontalErrorValue",
    VerticalErrorPath = "VerticalErrorValue"
};

{% endhighlight %}

{% endtabs %}

![Custom Type in Error Bar Series](Chart-types-images/maui_errorbar_TypeCustom.png)

## Customization

### Line Style

You can define the line style for the error bar lines using the [HorizontalLineStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarSeries.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarSeries_HorizontalLineStyle) and the [VerticalLineStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarSeries.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarSeries_VerticalLineStyle) properties as shown in the following code examples:

{% tabs %}

{% highlight xaml %}

<chart:ErrorBarSeries ItemsSource="{Binding EnergyProductions}"
                      XBindingPath="ID"
                      YBindingPath="Coal"
                      VerticalErrorValue="50"
                      HorizontalErrorValue="0.5">    

    <chart:ErrorBarSeries.HorizontalLineStyle>
        <chart:ErrorBarLineStyle Stroke="Red" StrokeWidth="2"/>
    </chart:ErrorBarSeries.HorizontalLineStyle>  

    <chart:ErrorBarSeries.VerticalLineStyle>
        <chart:ErrorBarLineStyle Stroke="Red" StrokeWidth="2"/>
    </chart:ErrorBarSeries.VerticalLineStyle> 

</chart:ErrorBarSeries>

{% endhighlight %}

{% highlight c# %}

ErrorBarSeries errorBar = new ErrorBarSeries()
{
    ItemsSource = new ViewModel().EnergyProductions,
    XBindingPath = "ID",
    YBindingPath = "Coal",
    HorizontalErrorValue = 0.5,
    VerticalErrorValue = 50,
};

// Customize the style for the horizontal error lines
errorBar.HorizontalLineStyle = new ErrorBarLineStyle()
{
    Stroke = new SolidColorBrush(Colors.Red),
    StrokeWidth = 2
};

// Customize the style for the vertical error lines
errorBar.VerticalLineStyle = new ErrorBarLineStyle()
{
    Stroke = new SolidColorBrush(Colors.Red),
    StrokeWidth = 2
};

{% endhighlight %}

{% endtabs %}

![Line Style in Error Bar Series](Chart-types-images/maui_errorbar_LineStyle.png)

### Cap Line Style

You can define the cap line style for the error bar lines using the [HorizontalCapLineStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarSeries.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarSeries_HorizontalCapLineStyle) and the [VerticalCapLineStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ErrorBarSeries.html#Syncfusion_Maui_Toolkit_Charts_ErrorBarSeries_VerticalCapLineStyle) properties as shown in the following code examples:

{% tabs %}

{% highlight xaml %}

<chart:ErrorBarSeries ItemsSource="{Binding EnergyProductions}"
                      XBindingPath="ID"
                      YBindingPath="Coal"
                      VerticalErrorValue="50"
                      HorizontalErrorValue="0.5">
    <chart:ErrorBarSeries.HorizontalCapLineStyle>
        <chart:ErrorBarCapLineStyle Stroke="Red"  
                                    StrokeWidth="2"/>
    </chart:ErrorBarSeries.HorizontalCapLineStyle>  
    <chart:ErrorBarSeries.VerticalCapLineStyle>
        <chart:ErrorBarCapLineStyle Stroke="Red"  
                                    StrokeWidth="2"/>
    </chart:ErrorBarSeries.VerticalCapLineStyle>  
</chart:ErrorBarSeries>

{% endhighlight %}

{% highlight c# %}

ErrorBarSeries errorBar = new ErrorBarSeries()
{
    ItemsSource = new ViewModel().EnergyProductions,
    XBindingPath = "ID",
    YBindingPath = "Coal",
    HorizontalErrorValue = 0.5,
    VerticalErrorValue = 50,
};

// Define the style for the horizontal cap lines of the error bars
errorBar.HorizontalCapLineStyle = new ErrorBarCapLineStyle()
{
    Stroke = new SolidColorBrush(Colors.Red),
    StrokeWidth = 2
};

// Define the style for the vertical cap lines of the error bars
errorBar.VerticalCapLineStyle = new ErrorBarCapLineStyle()
{
    Stroke = new SolidColorBrush(Colors.Red),
    StrokeWidth = 2
};

{% endhighlight %}

{% endtabs %}

![Cap Line Style in Error Bar Series](Chart-types-images/maui_errorbar_CapLineStyle.png)