---
layout: post
title: StackedColumn100 Chart in .NET MAUI Chart control | Syncfusion
description: Learn here all about StackedColumn100 chart support in Syncfusion .NET MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
keywords: .net maui stacked column 100 chart, stacked column 100 chart customization .net maui, syncfusion maui stacked column 100 chart, cartesian stacked column 100 chart maui, .net maui chart stacked column 100 visualization, .net maui 100% stacked column chart, cartesian 100% stacked column chart maui.
---

# StackedColumn100 Chart in .NET MAUI Chart

The Stacked column 100 % series chart is a type of Stacked chart that is used to display the proportion of different categories within a single column. The columns are stacked on top of each other, and a cumulative portion of each stacked element always comes to a total of 100%.

## StackedColumn100 Chart

To render the StackedColumn100 chart, create an instance of the [StackingColumn100Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StackingColumn100Series.html), and add it to the [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html#Syncfusion_Maui_Toolkit_Charts_SfCartesianChart_Series) collection property of the [SfCartesianChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html).

N> The cartesian chart has [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html#Syncfusion_Maui_Toolkit_Charts_SfCartesianChart_Series) as its default content.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>

    <chart:SfCartesianChart.XAxes>
        <chart:CategoryAxis/>
    </chart:SfCartesianChart.XAxes>

    <chart:SfCartesianChart.YAxes>
        <chart:NumericalAxis/>
    </chart:SfCartesianChart.YAxes>   

    <chart:StackingColumn100Series ItemsSource="{Binding Data1}"
                                   XBindingPath="Name"
                                   YBindingPath="Value"/>

    <chart:StackingColumn100Series ItemsSource="{Binding Data2}"
                                   XBindingPath="Name"
                                   YBindingPath="Value"/>

    <chart:StackingColumn100Series ItemsSource="{Binding Data3}"
                                   XBindingPath="Name"
                                   YBindingPath="Value"/>

</chart:SfCartesianChart>

{% endhighlight xaml %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
CategoryAxis primaryAxis = new CategoryAxis();
chart.XAxes.Add(primaryAxis);
NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

// Create a StackingColumn100Series for the chart
StackingColumn100Series series1 = new StackingColumn100Series()
{
    ItemsSource = new ViewModel().Data1,
    XBindingPath = "Name",
    YBindingPath = "Value",
};
StackingColumn100Series series2 = new StackingColumn100Series()
{
    ItemsSource = new ViewModel().Data2,
    XBindingPath = "Name",
    YBindingPath = "Value",
};
StackingColumn100Series series3 = new StackingColumn100Series()
{
    ItemsSource = new ViewModel().Data3,
    XBindingPath = "Name",
    YBindingPath = "Value",
};
 
// Add all series to the chart
chart.Series.Add(series1);
chart.Series.Add(series2);
chart.Series.Add(series3);
this.Content = chart;

{% endhighlight C# %}

{% endtabs %}

![Stacking Column 100 Chart in MAUI](Chart-types-images/StackedColumn100Chart.png)

## Grouping Series 

We can group and stack the similar stacked column 100 series type using the [GroupingLabel](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StackingSeriesBase.html#Syncfusion_Maui_Toolkit_Charts_StackingSeriesBase_GroupingLabel) property. 

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>

    <chart:SfCartesianChart.XAxes>
        <chart:CategoryAxis/>
    </chart:SfCartesianChart.XAxes>

    <chart:SfCartesianChart.YAxes>
        <chart:NumericalAxis/>
    </chart:SfCartesianChart.YAxes>   

    <chart:StackingColumn100Series ItemsSource="{Binding Data1}"
                                   XBindingPath="XValue"
                                   YBindingPath="YValue"
                                   GroupingLabel="GroupOne"/>

    <chart:StackingColumn100Series ItemsSource="{Binding Data2}"
                                   XBindingPath="XValue"
                                   YBindingPath="YValue"
                                   GroupingLabel="GroupOne"/>

    <chart:StackingColumn100Series ItemsSource="{Binding Data3}"
                                   XBindingPath="XValue"
                                   YBindingPath="YValue"
                                   GroupingLabel="GroupTwo"/>

    <chart:StackingColumn100Series ItemsSource="{Binding Data4}"
                                   XBindingPath="XValue"
                                   YBindingPath="YValue"
                                   GroupingLabel="GroupTwo"/>

</chart:SfCartesianChart>

{% endhighlight xaml %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
CategoryAxis primaryAxis = new CategoryAxis();
chart.XAxes.Add(primaryAxis);
NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

StackingColumn100Series series1 = new StackingColumn100Series()
{
    ItemsSource = new ViewModel().Data1,
    XBindingPath = "XValue",
    YBindingPath = "YValue",
    GroupingLabel = "GroupOne" // Assign the series to "GroupOne"
};
StackingColumn100Series series2 = new StackingColumn100Series()
{
    ItemsSource = new ViewModel().Data2,
    XBindingPath = "XValue",
    YBindingPath = "YValue",
    GroupingLabel = "GroupOne" // Assign the series to "GroupOne"
};
StackingColumn100Series series3 = new StackingColumn100Series()
{
    ItemsSource = new ViewModel().Data3,
    XBindingPath = "XValue",
    YBindingPath = "YValue",
    GroupingLabel = "GroupTwo" // Assign the series to "GroupTwo"
};
StackingColumn100Series series4 = new StackingColumn100Series()
{
    ItemsSource = new ViewModel().Data4,
    XBindingPath = "XValue",
    YBindingPath = "YValue",
    GroupingLabel = "GroupTwo" // Assign the series to "GroupTwo"
};

// Add all series to the chart
chart.Series.Add(series1);
chart.Series.Add(series2);
chart.Series.Add(series3);
chart.Series.Add(series4);
this.Content = chart;

{% endhighlight C# %}

{% endtabs %}