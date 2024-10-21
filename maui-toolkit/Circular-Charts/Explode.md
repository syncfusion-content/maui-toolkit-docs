---
layout: post
title: Explode segments in .NET MAUI Chart control | Syncfusion
description: This section explains about how to explode single segment or all segments in Syncfusion .NET MAUI Chart (SfCircularChart) control.
platform: maui-toolkit
control: SfCircularChart
documentation: ug
---

# Explode segments in .NET MAUI SfCircularChart

## Exploding a segment

Exploding a segment is used to pull attention to a specific area of the circular chart. The following properties are used to explode the segments in the circular chart.

* [ExplodeIndex](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.PieSeries.html#Syncfusion_Maui_Toolkit_Charts_PieSeries_ExplodeIndex) - Used to explode any specific segment.
* [ExplodeRadius](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.PieSeries.html#Syncfusion_Maui_Toolkit_Charts_PieSeries_ExplodeRadius) - Used to define the explode distance.
* [ExplodeOnTouch](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.PieSeries.html#Syncfusion_Maui_Toolkit_Charts_PieSeries_ExplodeOnTouch) - Enables the segment to be exploded on touch/tap interaction.

{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>
    . . .
    <chart:DoughnutSeries x:Name="DoughnutSeries"
                          ItemsSource="{Binding Data}"
                          XBindingPath="XValue"
                          YBindingPath="YValue"
                          ExplodeIndex="2"
                          ExplodeRadius="10"
                          ExplodeOnTouch="True"/>
</chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

// Create a new instance of SfCircularChart
SfCircularChart chart = new SfCircularChart();
. . .
// Create a new DoughnutSeries
DoughnutSeries series = new DoughnutSeries()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "XValue",
    YBindingPath = "YValue",
    ExplodeIndex = 2, // Set the index of the segment to be exploded (0-based)
    ExplodeRadius = 10, // Set the radius of explosion in pixels
    ExplodeOnTouch = true // Enable exploding segments on touch
};

chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Exploding a segment in a doughnut chart in MAUI.](Explode_images/explode_segment_in_circularchart.gif)

## Exploding all the segments

By setting the [ExplodeAll](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.PieSeries.html#Syncfusion_Maui_Toolkit_Charts_PieSeries_ExplodeAll) property of the [PieSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.PieSeries.html) to true, all segments in a circular chart can be visually exploded and highlighted on touch or tap interaction.

{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>
    . . .
    <chart:DoughnutSeries x:Name="DoughnutSeries"
                          ItemsSource="{Binding Data}"
                          XBindingPath="XValue"
                          YBindingPath="YValue"
                          ExplodeAll="True"/>
</chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

// Create a new instance of SfCircularChart
SfCircularChart chart = new SfCircularChart();
. . .
// Create a new DoughnutSeries
DoughnutSeries series = new DoughnutSeries()
{
    ItemsSource = new ViewModel().Data,
    XBindingPath = "XValue",
    YBindingPath = "YValue",
    ExplodeAll = true // Enable exploding for all segments in the doughnut chart
};

chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Exploding all support in MAUI.](Explode_images/MAUI_ExplodeAll.png)