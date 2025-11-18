---
layout: post
title: Stacked Column Chart in .NET MAUI Chart control | Syncfusion
description: Learn here all about stacked column and bar chart support in Syncfusion® .NET MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
keywords: .net maui stacked column chart, maui stacked column chart, stacked column chart customization .net maui, syncfusion maui stacked column chart, cartesian stacked column chart maui, .net maui chart stacked column visualization, .net maui cumulative column chart.
---

# Stacked Column Chart in .NET MAUI Chart

## Stacked Column Chart

The stacked column chart represents data values in a stacked format, where columns are stacked on top of each other to indicate the cumulative value of data points.

To render a stacked column chart, create an instance of the [StackingColumnSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StackingColumnSeries.html) and add it to the [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html#Syncfusion_Maui_Toolkit_Charts_SfCartesianChart_Series) collection property of the [SfCartesianChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html).

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

    <chart:StackingColumnSeries ItemsSource="{Binding Data1}"
                                XBindingPath="Name"
                                YBindingPath="Value"/>        

    <chart:StackingColumnSeries ItemsSource="{Binding Data2}"
                                XBindingPath="Name"
                                YBindingPath="Value"/>         
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
CategoryAxis primaryAxis = new CategoryAxis();
chart.XAxes.Add(primaryAxis);
NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

// Create a StackingColumnSeries for the chart
StackingColumnSeries series1 = new StackingColumnSeries()
{
    ItemsSource = new ViewModel().Data1,
    XBindingPath = "Name",
    YBindingPath = "Value",
};
StackingColumnSeries series2 = new StackingColumnSeries()
{
    ItemsSource = new ViewModel().Data2,
    XBindingPath = "Name",
    YBindingPath = "Value",
};

// Add series to the chart
chart.Series.Add(series1);
chart.Series.Add(series2);     
this.Content = chart;

{% endhighlight %}

{% endtabs %}


## Grouping Series

Comparing multiple series in a stacked chart can be difficult. Grouping solves this problem by organizing related series together.
The [GroupingLabel](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StackingSeriesBase.html#Syncfusion_Maui_Toolkit_Charts_StackingSeriesBase_GroupingLabel) property is used to group series by assigning a label to each stacked column series. This label identifies the specific group to which the stacked column series belongs and can be used to group similar series.

N> If the [GroupingLabel](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StackingSeriesBase.html#Syncfusion_Maui_Toolkit_Charts_StackingSeriesBase_GroupingLabel) is not provided, the stacked column will consider all series as a single group.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    ....
    <chart:StackingColumnSeries ItemsSource="{Binding Data1}"
                                XBindingPath="Name"
                                YBindingPath="Value"
                                GroupingLabel="GroupOne"/>

    <chart:StackingColumnSeries ItemsSource="{Binding Data2}" 
                                XBindingPath="Name"
                                YBindingPath="Value"
                                GroupingLabel="GroupTwo"/>

    <chart:StackingColumnSeries ItemsSource="{Binding Data3}" 
                                XBindingPath="Name"
                                YBindingPath="Value"
                                GroupingLabel="GroupOne"/>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
CategoryAxis primaryAxis = new CategoryAxis();
chart.XAxes.Add(primaryAxis);
NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

StackingColumnSeries series1 = new StackingColumnSeries()
{
    ItemsSource = new ViewModel().Data1,
    XBindingPath = "Name",
    YBindingPath = "Value",
    GroupingLabel = "GroupOne" // Assign series to "GroupOne"
};
StackingColumnSeries series2 = new StackingColumnSeries()
{
    ItemsSource = new ViewModel().Data2,
    XBindingPath = "Name",
    YBindingPath = "Value",
    GroupingLabel = "GroupTwo" // Assign series to "GroupTwo"
};
StackingColumnSeries series3 = new StackingColumnSeries()
{
    ItemsSource = new ViewModel().Data3,
    XBindingPath = "Name",
    YBindingPath = "Value",
    GroupingLabel = "GroupOne" // Assign series to "GroupOne"
};

// Add all series to the chart
chart.Series.Add(series1);
chart.Series.Add(series2); 
chart.Series.Add(series3);      
this.Content = chart;

{% endhighlight %}

{% endtabs %}

## Appearance Customization

* [Spacing](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StackingColumnSeries.html#Syncfusion_Maui_Toolkit_Charts_StackingColumnSeries_Spacing) of the `Double` type that changes the spacing between two segments. The default value is 0, with a range from 0 to 1.
* [Width](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StackingColumnSeries.html#Syncfusion_Maui_Toolkit_Charts_StackingColumnSeries_Width) of the `Double` type that changes the width of the rectangle. The default value is 0.8, with a range from 0 to 1.
* [CornerRadius](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StackingColumnSeries.html#Syncfusion_Maui_Toolkit_Charts_StackingColumnSeries_CornerRadius) of the type `CornerRadius`, defines the rounded corners for the stacked column.
* [Stroke](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StackingSeriesBase.html#Syncfusion_Maui_Toolkit_Charts_StackingSeriesBase_Stroke) of the type `Brush` defines the color used for the border of the stacked column..
* [StrokeWidth](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.XYDataSeries.html#Syncfusion_Maui_Toolkit_Charts_XYDataSeries_StrokeWidth) of the type `Double` defines the width of the stacked segment border.