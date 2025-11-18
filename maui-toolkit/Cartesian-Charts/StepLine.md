---
layout: post
title: StepLine Chart in .NET MAUI Chart control | Syncfusion
description: Learn here all about stepline chart support in Syncfusion® .NET MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
keywords: .net maui step line chart, maui step line chart, step line chart customization .net maui, syncfusion maui step line chart, cartesian step line chart maui, .net maui chart step line visualization.
---

# Step Line Chart in .NET MAUI Chart

Step line chart is used to display data showing changes in values over time by connecting points on plots with a combination of horizontal and vertical lines. It's used when it is necessary to highlight irregular changes. The visualization appears as steps.

## Step Line Chart

To render the Step line chart, create an instance of the [StepLineSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StepLineSeries.html), and add it to the [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html#Syncfusion_Maui_Toolkit_Charts_SfCartesianChart_Series) collection property of the [SfCartesianChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html).

N> The Cartesian chart has [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html#Syncfusion_Maui_Toolkit_Charts_SfCartesianChart_Series) as its default content.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>

    <chart:SfCartesianChart.XAxes>
        <chart:DatetimeAxis/>
    </chart:SfCartesianChart.XAxes>

    <chart:SfCartesianChart.YAxes>
        <chart:NumericalAxis/>
    </chart:SfCartesianChart.YAxes>   

    <chart:StepLineSeries ItemsSource="{Binding Data1}"
                          XBindingPath="Date"
                          YBindingPath="Value"/>

    <chart:StepLineSeries ItemsSource="{Binding Data2}"
                          XBindingPath="Date"
                          YBindingPath="Value"/>

</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
DatetimeAxis primaryAxis = new DatetimeAxis();
chart.XAxes.Add(primaryAxis);
NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

// Create a StepLineSeries for the chart
StepLineSeries series1 = new StepLineSeries()
{
    ItemsSource = new ViewModel().Data1,
    XBindingPath = "Date",
    YBindingPath = "Value",
};

StepLineSeries series2 = new StepLineSeries()
{
    ItemsSource = new ViewModel().Data2,
    XBindingPath = "Date",
    YBindingPath = "Value",
};

// Add the series to the chart's Series collection.
chart.Series.Add(series1);
chart.Series.Add(series2);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![StepLine Chart in MAUI](Chart-types-images/StepLineChart.png)

## Dashed Step Line Chart

The [StrokeDashArray](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.LineSeries.html#Syncfusion_Maui_Toolkit_Charts_LineSeries_StrokeDashArray) property of the [StepLineSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.StepLineSeries.html) is used to render the Step line series with dashes. An odd value is considered as rendering size, and an even value is considered a gap.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>

    <chart:SfCartesianChart.Resources>
        <DoubleCollection x:Key="DashArray">
            <x:Double>5</x:Double>
            <x:Double>2</x:Double>
        </DoubleCollection>
    </chart:SfCartesianChart.Resources>

    <chart:SfCartesianChart.XAxes>
        <chart:DatetimeAxis/>
    </chart:SfCartesianChart.XAxes>

    <chart:SfCartesianChart.YAxes>
        <chart:NumericalAxis/>
    </chart:SfCartesianChart.YAxes>   

    <chart:StepLineSeries ItemsSource="{Binding Data}"
                          StrokeDashArray="{StaticResource DashArray}"
                          XBindingPath="Date"
                          YBindingPath="Value"/>

</chart:SfCartesianChart>

{% endhighlight %}

{% highlight C# %}

SfCartesianChart chart = new SfCartesianChart();

DatetimeAxis primaryAxis = new DatetimeAxis();
chart.XAxes.Add(primaryAxis);
NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

// Create a DoubleCollection for the StrokeDashArray
DoubleCollection doubleCollection = new DoubleCollection();
doubleCollection.Add(5);
doubleCollection.Add(2);

StepLineSeries steplineSeries = new StepLineSeries()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "Date",
    YBindingPath = "Value",
    StrokeDashArray = doubleCollection // Apply custom dash pattern to the series stroke.
};

chart.Series.Add(steplineSeries);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![StepLine Chart in MAUI](Chart-types-images/DashedStepLine.png)

## Vertical Step Line Chart 

The [IsTransposed](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html#Syncfusion_Maui_Toolkit_Charts_SfCartesianChart_IsTransposed) property of the [SfCartesianChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html) is used to render the Step line series vertically. To enable the Step line series vertically, set the IsTransposed property to true.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart IsTransposed="True">

    <chart:SfCartesianChart.XAxes>
        <chart:DatetimeAxis/>
    </chart:SfCartesianChart.XAxes>

    <chart:SfCartesianChart.YAxes>
        <chart:NumericalAxis/>
    </chart:SfCartesianChart.YAxes>   

    <chart:StepLineSeries ItemsSource="{Binding Data1}"
                          XBindingPath="Year"
                          YBindingPath="Value"/>

    <chart:StepLineSeries ItemsSource="{Binding Data2}"
                          XBindingPath="Year"
                          YBindingPath="Value"/>

</chart:SfCartesianChart>

{% endhighlight %}

{% highlight C# %}

SfCartesianChart chart = new SfCartesianChart();

chart.IsTransposed = true; // Set the chart to transpose the axes, swapping the X and Y axes

DatetimeAxis primaryAxis = new DatetimeAxis();
chart.XAxes.Add(primaryAxis);
NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

StepLineSeries steplineSeries1 = new StepLineSeries()
{
    ItemsSource = new ViewModel().Data1,
    XBindingPath = "Year",
    YBindingPath = "Value"
};

StepLineSeries steplineSeries2 = new StepLineSeries()
{
    ItemsSource = new ViewModel().Data2,
    XBindingPath = "Year",
    YBindingPath = "Value"
};

chart.Series.Add(steplineSeries1);
chart.Series.Add(steplineSeries2);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![StepLine Chart in MAUI](Chart-types-images/VerticalStepLine.png)