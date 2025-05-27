---
layout: post
title: Waterfall Chart in .NET MAUI Chart control | Syncfusion
description: Learn here all about the Waterfall Series chart and its features in Syncfusion® .NET MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
Keywords: .net maui waterfall chart, .net maui bridge chart, waterfall chart customization .net maui, syncfusion maui waterfall chart, cartesian waterfall chart maui, .net maui chart waterfall visualization.
---

# Waterfall Chart in .NET MAUI Chart

## Waterfall Chart

[WaterfallSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.WaterfallSeries.html) clarifies the cumulative effect of a set of provided positive and negative values. The series is represented by rectangles with connectors between them. To render a waterfall chart, create an instance of [WaterfallSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.WaterfallSeries.html) and add it to the [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html#Syncfusion_Maui_Toolkit_Charts_SfCartesianChart_Series) collection property of the [SfCartesianChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html).

* [SummaryBindingPath](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.WaterfallSeries.html#Syncfusion_Maui_Toolkit_Charts_WaterfallSeries_SummaryBindingPath) - A string property used to set the path value on the source object to identify summary values for the series.
* [SummaryPointsBrush](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.WaterfallSeries.html#Syncfusion_Maui_Toolkit_Charts_WaterfallSeries_SummaryPointsBrush) - A brush property used to change the fill color of summary segments in the series.
* [NegativePointsBrush](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.WaterfallSeries.html#Syncfusion_Maui_Toolkit_Charts_WaterfallSeries_NegativePointsBrush) - A brush property used to change the fill color of negative segments in the series.
* [AllowAutoSum](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.WaterfallSeries.html#Syncfusion_Maui_Toolkit_Charts_WaterfallSeries_AllowAutoSum) - A boolean property that controls summary segment calculation. By default, this property is true. When set to false, it renders segments using the Y values from the provided ItemsSource collection.
* [ShowConnectorLine](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.WaterfallSeries.html#Syncfusion_Maui_Toolkit_Charts_WaterfallSeries_ShowConnectorLine) - A boolean property used to enable or disable connector lines. The default value is `true`.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    <chart:SfCartesianChart.XAxes>
        <chart:CategoryAxis/>
    </chart:SfCartesianChart.XAxes>

    <chart:SfCartesianChart.YAxes>
        <chart:NumericalAxis/>
    </chart:SfCartesianChart.YAxes>
    
    <chart:SfCartesianChart.Series>
        <chart:WaterfallSeries ItemsSource="{Binding Sales}"
                               XBindingPath="Department"
                               YBindingPath="Value"
                               AllowAutoSum="True"
                               NegativePointsBrush="Red"
                               SummaryBindingPath="IsSummary"
                               SummaryPointsBrush="RoyalBlue"
                               ShowConnectorLine="True"/>
    </chart:SfCartesianChart.Series>   
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
CategoryAxis xAxis = new CategoryAxis();
NumericalAxis yAxis = new NumericalAxis();
chart.XAxes.Add(xAxis);
chart.YAxes.Add(yAxis);
   
ViewModel viewModel = new ViewModel();

// Create a new WaterfallSeries to display the data
WaterfallSeries series = new WaterfallSeries()
{
    ItemsSource = new viewModel().Sales,
    XBindingPath = "Department",
    YBindingPath = "Value",
    AllowAutoSum = true,
    NegativePointsBrush = new SolidColorBrush(Colors.Red),
    SummaryBindingPath = "IsSummary",
    SummaryPointsBrush = new SolidColorBrush(Colors.RoyalBlue),
    ShowConnectorLine = true,
};

// Add the created series to the chart   
chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Waterfall Chart in MAUI Chart](Chart-types-images/maui_waterfall_Basic.png)

## Connector Line Customization

The connector lines can be customized using the [ConnectorLineStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.WaterfallSeries.html#Syncfusion_Maui_Toolkit_Charts_WaterfallSeries_ConnectorLineStyle) property of the series.
The following code example demonstrates how to apply a style to connector lines:

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart.Series>
    <chart:WaterfallSeries ItemsSource="{Binding Sales}"
                           XBindingPath="Department"
                           YBindingPath="Value">
        <chart:WaterfallSeries.ConnectorLineStyle>
                <chart:ChartLineStyle Stroke="DarkViolet" StrokeWidth="2"/>
        </chart:WaterfallSeries.ConnectorLineStyle>
    </chart:WaterfallSeries>
</chart:SfCartesianChart.Series>   
    
{% endhighlight %}

{% highlight c# %}

// Define the style for the connector lines in the waterfall chart
ChartLineStyle lineStyle = new ChartLineStyle()
{
    Stroke = new SolidColorBrush(Colors.DarkViolet),
    StrokeThickness = 2
};

WaterfallSeries series = new WaterfallSeries()
{
    ItemsSource = new viewModel().Sales,
    XBindingPath = "Department",
    YBindingPath = "Value",
    ConnectorLineStyle = lineStyle, // Apply the defined line style to the connector lines
};
    
{% endhighlight %}

{% endtabs %}

![Connector line customization in Waterfall Chart](Chart-types-images/maui_waterfall_LineStyle.png)