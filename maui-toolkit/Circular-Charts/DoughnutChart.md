---
layout: post
title: Doughnut chart in .NET MAUI Chart control | Syncfusion
description: Learn here all about doughnut chart and its features in Syncfusion® .NET MAUI Chart (SfCircularChart) control.
platform: maui-toolkit
control: SfCircularChart
documentation: ug
---

# Doughnut Chart in .NET MAUI Chart

The [DoughnutSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DoughnutSeries.html) is similar to [PieSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.PieSeries.html). It is used to show the relationship between parts of data and the whole data. To render a [DoughnutSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DoughnutSeries.html) in circular chart, create an instance of the [DoughnutSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DoughnutSeries.html) and add it to the [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCircularChart.html#Syncfusion_Maui_Toolkit_Charts_SfCircularChart_Series) collection property of [SfCircularChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCircularChart.html).

N> The circular chart has [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCircularChart.html#Syncfusion_Maui_Toolkit_Charts_SfCircularChart_Series) as its default content.

{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>
    <chart:DoughnutSeries ItemsSource="{Binding Data}" 
                          XBindingPath="Product" 
                          YBindingPath="SalesRate"/>
</chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

// Create a new instance of SfCircularChart
SfCircularChart chart = new SfCircularChart();

// Create a new instance of DoughnutSeries
DoughnutSeries series = new DoughnutSeries();
series.ItemsSource = (new SalesViewModel()).Data;
series.XBindingPath = "Product";
series.YBindingPath = "SalesRate";

// Add the series to the chart's Series collection
chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Doughnut chart type in MAUI Chart](Chart-Types_images/maui_doughnut_chart.png)

## Inner Radius

The [InnerRadius](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DoughnutSeries.html#Syncfusion_Maui_Toolkit_Charts_DoughnutSeries_InnerRadius) property of doughnut series is used to define the inner circle size.
{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>
    <chart:DoughnutSeries ItemsSource="{Binding Data}"
                          InnerRadius="0.7"
                          XBindingPath="Product"
                          YBindingPath="SalesRate"/>
</chart:SfCircularChart>
    
{% endhighlight %}

{% highlight c# %}

SfCircularChart chart = new SfCircularChart();

DoughnutSeries series = new DoughnutSeries();
series.ItemsSource = (new SalesViewModel()).Data;
series.XBindingPath = "Product";
series.YBindingPath = "SalesRate";
// Set the inner radius of the doughnut chart (70% of the available space)
series.InnerRadius = 0.7;
chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Doughnut chart with coefficient in MAUI Chart](Chart-Types_images/maui_doughnut_chart_doughnutcoefficient.png)

## Semi Doughnut

By using the [StartAngle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.CircularSeries.html#Syncfusion_Maui_Toolkit_Charts_CircularSeries_StartAngle) and [EndAngle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.CircularSeries.html#Syncfusion_Maui_Toolkit_Charts_CircularSeries_EndAngle) properties, you can draw doughnut series in different shapes such as semi-doughnut or quarter doughnut series.
{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>    
    <chart:DoughnutSeries ItemsSource="{Binding Data}"
                          XBindingPath="Product"
                          YBindingPath="SalesRate"
                          StartAngle="180" EndAngle="360"/>
</chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

SfCircularChart chart = new SfCircularChart();       

DoughnutSeries series = new DoughnutSeries();
series.ItemsSource = (new SalesViewModel()).Data;
series.XBindingPath = "Product";
series.YBindingPath = "SalesRate";
// Set the starting angle of the doughnut chart (in degrees)
series.StartAngle = 180;
// Set the ending angle of the doughnut chart (in degrees)
series.EndAngle = 360;

chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Semi doughnut chart in MAUI Chart](Chart-Types_images/maui_semi_doughnut_chart.png)

## Center View

The view placed in the center of the doughnut chart is useful for sharing additional information about the chart data. Any view can be added to the center of the doughnut chart using the [CenterView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DoughnutSeries.html#Syncfusion_Maui_Toolkit_Charts_DoughnutSeries_CenterView) property of [DoughnutSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DoughnutSeries.html). The binding context of the [CenterView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DoughnutSeries.html#Syncfusion_Maui_Toolkit_Charts_DoughnutSeries_CenterView) will be the respective doughnut series.

### Center Hole Size

The [CenterHoleSize](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DoughnutSeries.html#Syncfusion_Maui_Toolkit_Charts_DoughnutSeries_CenterHoleSize) property of [DoughnutSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DoughnutSeries.html) is used to get the diameter value of the center hole. Using the [CenterHoleSize](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.DoughnutSeries.html#Syncfusion_Maui_Toolkit_Charts_DoughnutSeries_CenterHoleSize), you can ensure that the view in the doughnut center does not overlap with the series.

{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>
    <chart:DoughnutSeries ItemsSource="{Binding Data}" XBindingPath="Name" YBindingPath="Value">
        <chart:DoughnutSeries.CenterView>
            <Border HeightRequest="{Binding CenterHoleSize}" WidthRequest="{Binding CenterHoleSize}">
                <Border.StrokeShape>
                    <RoundRectangle CornerRadius="200"/>
                </Border.StrokeShape>
                <StackLayout>
                    <Label Text="Total :"/>
                    <Label Text="357,580 km²"/>
                </StackLayout>
            </Border>
        </chart:DoughnutSeries.CenterView>
    </chart:DoughnutSeries>
</chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

SfCircularChart chart = new SfCircularChart();

// Create a new DoughnutSeries
DoughnutSeries series = new DoughnutSeries();
series.ItemsSource = (new ViewModel()).Data;
series.XBindingPath = "Name";
series.YBindingPath = "Value";

// Create a border to contain the center view content
Border border = new Border();

Label name = new Label();
name.Text = "Total :";

Label value = new Label();
value.Text = "357,580 km²";

StackLayout layout = new StackLayout();
layout.Children.Add(name);
layout.Children.Add(value);
border.Content = layout;

// Set the border (containing the labels) as the center view of the doughnut series
series.CenterView = border;

chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Center View in MAUI doughnut Chart](Chart-Types_images/maui_center_View.png)

