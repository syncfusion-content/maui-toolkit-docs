---
layout: post
title: Radial Bar chart in .NET MAUI Chart control | Syncfusion
description: Learn here all about radial bar chart and its features in Syncfusion® .NET MAUI Chart (SfCircularChart) control.
platform: maui-toolkit
control: SfCircularChart
documentation: ug
---

# Radial Bar Chart in .NET MAUI Chart

[RadialBarSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RadialBarSeries.html) is a type of doughnut chart that represents each segment as a separate circle. It is used to compare values between various categories. To render a [RadialBarSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RadialBarSeries.html) in circular chart, create an instance of the [RadialBarSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RadialBarSeries.html) and add it to the [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCircularChart.html#Syncfusion_Maui_Toolkit_Charts_SfCircularChart_Series) collection property of [SfCircularChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCircularChart.html).

N> The circular chart has [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCircularChart.html#Syncfusion_Maui_Toolkit_Charts_SfCircularChart_Series) as its default content.

The following properties can be used to customize the appearance of the radial bar segment:

 * [Opacity](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartSeries.html#Syncfusion_Maui_Toolkit_Charts_ChartSeries_Opacity) - Controls the transparency of the chart segments.

 * [Stroke](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.CircularSeries.html#Syncfusion_Maui_Toolkit_Charts_CircularSeries_Stroke) - Customizes the outer layer of the chart segments.

 * [StrokeWidth](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.CircularSeries.html#Syncfusion_Maui_Toolkit_Charts_CircularSeries_StrokeWidth) - Customizes the width of the stroke in chart segments.

 * [GapRatio](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RadialBarSeries.html#Syncfusion_Maui_Toolkit_Charts_RadialBarSeries_GapRatio) - Customizes the spacing between each chart segment.

 * [MaximumValue](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RadialBarSeries.html#Syncfusion_Maui_Toolkit_Charts_RadialBarSeries_MaximumValue) - Represents the span of the segment-filled area in the radial bar track. The default value is `double.NaN`.

 * [PaletteBrushes](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartSeries.html#Syncfusion_Maui_Toolkit_Charts_ChartSeries_PaletteBrushes) - Customizes the appearance of the series.

{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>
    <chart:RadialBarSeries ItemsSource="{Binding Data}" 
                           XBindingPath="Product" 
                           YBindingPath="SalesRate"/>
</chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

SfCircularChart chart = new SfCircularChart();

// Initialize a new RadialBarSeries
RadialBarSeries series = new RadialBarSeries();
series.ItemsSource = (new SalesViewModel()).Data;
series.XBindingPath = "Product";
series.YBindingPath = "SalesRate";

// Add the configured series to the SfCircularChart's series collection
chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![.NET MAUI Radial bar chart](Chart-Types_images/maui_radialbar_chart.png)

## Changing the Radial Bar Size

You can use the [Radius](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.CircularSeries.html#Syncfusion_Maui_Toolkit_Charts_CircularSeries_Radius) property to change the radial bar chart size. The default value of the radius is `0.8`.

{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>
    <chart:RadialBarSeries ItemsSource="{Binding Data}" 
                           XBindingPath="Product" 
                           YBindingPath="SalesRate" 
                           Radius="0.5"/>
</chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

SfCircularChart chart = new SfCircularChart();

RadialBarSeries series = new RadialBarSeries();
series.ItemsSource = (new SalesViewModel()).Data;
series.XBindingPath = "Product";
series.YBindingPath = "SalesRate";
series.Radius = 0.5; // Set the radius of the radial bars (50% of available space)

chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![.NET MAUI Radial bar chart radius customization](Chart-Types_images/maui_radius.png)

## Changing the Radial Bar Inner Radius

The [InnerRadius](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RadialBarSeries.html#Syncfusion_Maui_Toolkit_Charts_RadialBarSeries_InnerRadius) property of radial bar series is used to define the inner circle. The default value of this property is `0.4`.

{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>
    <chart:RadialBarSeries ItemsSource="{Binding Data}" 
                           XBindingPath="Product" 
                           YBindingPath="SalesRate" 
                           InnerRadius="0.1"/>
</chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

SfCircularChart chart = new SfCircularChart();

RadialBarSeries series = new RadialBarSeries();
series.ItemsSource = (new SalesViewModel()).Data;
series.XBindingPath = "Product";
series.YBindingPath = "SalesRate";
series.InnerRadius = 0.1; // Set the inner radius of the radial bar chart, which determines the center emptiness of the chart

chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![.NET MAUI Radial bar chart inner radius customization](Chart-Types_images/maui_inner_radius.png)

## CapStyle Customization

The [CapStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RadialBarSeries.html#Syncfusion_Maui_Toolkit_Charts_RadialBarSeries_CapStyle) property of the radial bar series is used to specify the shape of the start and end points of the circular segment. The default value of this property is `BothFlat`.

The following types are available for [CapStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RadialBarSeries.html#Syncfusion_Maui_Toolkit_Charts_RadialBarSeries_CapStyle) property:

 * [BothFlat](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.CapStyle.html#Syncfusion_Maui_Toolkit_Charts_CapStyle_BothFlat) - Start and end positions of the segment should be updated with a flat shape.

 * [BothCurve](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.CapStyle.html#Syncfusion_Maui_Toolkit_Charts_CapStyle_BothCurve) - Start and end positions of the segment should be updated with a curve shape.

 * [StartCurve](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.CapStyle.html#Syncfusion_Maui_Toolkit_Charts_CapStyle_StartCurve) - Start position of the segment should be updated with a curve shape.

 * [EndCurve](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.CapStyle.html#Syncfusion_Maui_Toolkit_Charts_CapStyle_EndCurve) - End position of the segment should be updated with a curve shape.

**BothCurve**

You can customize the CapStyle property of the radial bar based on its types.

{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>
    <chart:RadialBarSeries ItemsSource="{Binding Data}" 
                           XBindingPath="Product" 
                           YBindingPath="SalesRate"
                           CapStyle="BothCurve"/>
    </chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

SfCircularChart chart = new SfCircularChart();

RadialBarSeries series = new RadialBarSeries();
series.ItemsSource = (new SalesViewModel()).Data;
series.XBindingPath = "Product";
series.YBindingPath = "SalesRate";
series.CapStyle = CapStyle.BothCurve; // Set the cap style for the series

chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![.NET MAUI Radial bar chart cap style customization](Chart-Types_images/maui_bothcurve.png)

## Segment Spacing

The [GapRatio](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RadialBarSeries.html#Syncfusion_Maui_Toolkit_Charts_RadialBarSeries_GapRatio) property of the radial bar series is used to define the spacing between each segment. The default value of this property is `0.2`.

{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>
    <chart:RadialBarSeries ItemsSource="{Binding Data}" 
                           XBindingPath="Product" 
                           YBindingPath="SalesRate" 
                           InnerRadius="0.2"
                           GapRatio="0.4"/>
</chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

SfCircularChart chart = new SfCircularChart();

RadialBarSeries series = new RadialBarSeries();
series.ItemsSource = (new SalesViewModel()).Data;
series.XBindingPath = "Product";
series.YBindingPath = "SalesRate";
series.InnerRadius = 0.2;
series.GapRatio = 0.4; // Set the gap ratio between each radial bar (40% of available space)

chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![.NET MAUI Radial bar chart segment spacing customization](Chart-Types_images/maui_gapratio.png)

## Track Customization

You can use the following properties to customize the appearance of the circular bar track:

  * [TrackStroke](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RadialBarSeries.html#Syncfusion_Maui_Toolkit_Charts_RadialBarSeries_TrackStroke) - Customizes the circular bar border color.

  * [TrackStrokeWidth](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RadialBarSeries.html#Syncfusion_Maui_Toolkit_Charts_RadialBarSeries_TrackStrokeWidth) - Customizes the border width of the circular bar.

  * [TrackFill](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RadialBarSeries.html#Syncfusion_Maui_Toolkit_Charts_RadialBarSeries_TrackFill) - Customizes the circular bar area which is behind the radial bar segments.

{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>
    <chart:RadialBarSeries ItemsSource="{Binding Data}" 
                           XBindingPath="Product" 
                           YBindingPath="SalesRate" 
                           TrackFill="#FFF7ED" 
                           TrackStrokeWidth="1"
                           TrackStroke="#FED7AA"/>
</chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

SfCircularChart chart = new SfCircularChart();

RadialBarSeries series = new RadialBarSeries();
series.ItemsSource = (new SalesViewModel()).Data;
series.XBindingPath = "Product";
series.YBindingPath = "SalesRate";
series.TrackFill = new SolidColorBrush(Color.FromArgb("#FFF7ED")); // Set the fill color for the track
series.TrackStrokeWidth = 1; // Set the width of the stroke line for the track
series.TrackStroke = new SolidColorBrush(Color.FromArgb("#FED7AA")); // Set the stroke color for the track

chart.Series.Add(series);
this.Content = chart;
{% endhighlight %}

{% endtabs %}

![.NET MAUI Radial bar chart track customization](Chart-Types_images/maui_trackfill.png)

## CenterView

Any view can be added to the center of the radial bar chart using the [CenterView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RadialBarSeries.html#Syncfusion_Maui_Toolkit_Charts_RadialBarSeries_CenterView) property of [RadialBarSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RadialBarSeries.html). The view placed in the center of the radial bar chart is useful for sharing additional information about the chart. The binding context of the [CenterView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RadialBarSeries.html#Syncfusion_Maui_Toolkit_Charts_RadialBarSeries_CenterView) will be the respective radial bar series.

### CenterHoleSize

The [CenterHoleSize](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RadialBarSeries.html#Syncfusion_Maui_Toolkit_Charts_RadialBarSeries_CenterHoleSize) property of RadialBarSeries is used to get the diameter value of the center hole. Using the CenterHoleSize, you can ensure that the view in the radial bar center doesn't overlap with the series.

{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>
    <chart:RadialBarSeries ItemsSource="{Binding Data}" 
                           XBindingPath="XValue" 
                           YBindingPath="YValue" 
                           MaximumValue="100"
                           CapStyle="BothCurve">
        <chart:RadialBarSeries.CenterView>
            <StackLayout HeightRequest="{Binding CenterHoleSize}"
                         WidthRequest="{Binding CenterHoleSize}">
                <Image Source="person.png"/>
            </StackLayout>
        </chart:RadialBarSeries.CenterView>
    </chart:RadialBarSeries>
</chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

SfCircularChart chart = new SfCircularChart();

RadialBarSeries series = new RadialBarSeries();
series.ItemsSource = (new ViewModel()).Data;
series.XBindingPath = "XValue";
series.YBindingPath = "YValue";
series.CapStyle = CapStyle.BothCurve;

// Create a StackLayout to hold additional content in the center of the radial bar chart
StackLayout layout = new StackLayout();
Image image = new Image { Source = "person.png" };
layout.SetBinding(HeightRequestProperty, nameof(RadialBarSeries.CenterHoleSize));
layout.SetBinding(WidthRequestProperty, nameof(RadialBarSeries.CenterHoleSize));
layout.Children.Add(image);       

// Assign the layout as the center view of the series, allowing content to be shown inside the radial bar
series.CenterView = layout;
chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![.NET MAUI Radial bar chart center view customization](Chart-Types_images/maui_radialbarchart_centerview.png)

