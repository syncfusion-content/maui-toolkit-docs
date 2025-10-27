---
layout: post
title: Axis in .NET MAUI Spark Chart Control | Syncfusion
description: Learn how to display and customize the axis in Syncfusion® .NET MAUI Spark Charts (SfSparkChart) using ShowAxis, AxisOrigin, and AxisLineStyle.
platform: maui-toolkit
control: SfSparkChart
documentation: ug
---

# Axis in .NET MAUI Spark Charts

Axis can be configured and customized using following properties. This feature is applicable for all the [SfSparkChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkChart.html) types except [SfSparkWinLossChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkWinLossChart.html).

- [ShowAxis](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkChart.html#Syncfusion_Maui_Toolkit_SparkCharts_SfSparkChart_ShowAxisProperty) : Enables or disables the axis. Default value is `false`.
- [AxisOrigin](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkChart.html#Syncfusion_Maui_Toolkit_SparkCharts_SfSparkChart_AxisOriginProperty) : Sets the Y-value where the axis is drawn. Default it renders at `0`.
- [AxisLineStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkChart.html#Syncfusion_Maui_Toolkit_SparkCharts_SfSparkChart_AxisLineStyleProperty) : Customizes the axis appearance
  - [Stroke](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SparkChartLineStyle.html#Syncfusion_Maui_Toolkit_SparkCharts_SparkChartLineStyle_StrokeProperty) : Specifies the line color of the axis.
  - [StrokeWidth](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SparkChartLineStyle.html#Syncfusion_Maui_Toolkit_SparkCharts_SparkChartLineStyle_StrokeWidthProperty) : Specifies the line thickness of the axis. Default it is set to 1.
  - [StrokeDashArray](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SparkChartLineStyle.html#Syncfusion_Maui_Toolkit_SparkCharts_SparkChartLineStyle_StrokeDashArrayProperty) : Specifies the dash pattern for the axis. Default it is set to null.

## Enable the axis

Set the [ShowAxis](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkChart.html#Syncfusion_Maui_Toolkit_SparkCharts_SfSparkChart_ShowAxisProperty) property to display the axis at the chart’s origin in [SfSparkChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkChart.html); by default, the  axis is set to `False`.

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkLineChart
    ItemsSource="{Binding Data}"
    YBindingPath="Value"
    ShowAxis="True">
</sparkchart:SfSparkLineChart>

{% endhighlight %}

{% highlight c# %}

var chart = new SfSparkLineChart
{
    ItemsSource = new SparkChartViewModel().Data,
    YBindingPath = "Value",
    ShowAxis = true
};

{% endhighlight %}

{% endtabs %}

![Axis in .NET MAUI Spark Line](sparkchart_axis_line_images\Default_axis_line.png)

## Axis origin

Set [AxisOrigin](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkChart.html#Syncfusion_Maui_Toolkit_SparkCharts_SfSparkChart_AxisOriginProperty) to draw the line at a specific Y value (for example, `0` to emphasize zero, or any custom value) of [SfSparkChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkChart.html).

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkLineChart
    ItemsSource="{Binding Data}"
    YBindingPath="Value"
    ShowAxis="True"
    AxisOrigin="8">
</sparkchart:SfSparkLineChart>

{% endhighlight %}

{% highlight c# %}

chart.AxisOrigin = 8;

{% endhighlight %}

{% endtabs %}

![Axis origin in .NET MAUI Spark Line](sparkchart_axis_line_images\axis_origin.png)

## Style the axis

### Stroke width

Controls the thickness of the axis of [SfSparkChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkChart.html).

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkLineChart.AxisLineStyle>
    <sparkchart:SparkChartLineStyle StrokeWidth="2" />
</sparkchart:SfSparkLineChart.AxisLineStyle>

{% endhighlight %}

{% highlight c# %}

chart.AxisLineStyle = new SparkChartLineStyle
{
    StrokeWidth = 2
};

{% endhighlight %}

{% endtabs %}

![Axis stroke width in .NET MAUI Spark Line](sparkchart_axis_line_images\axis_stroke_width.png)

### Stroke color

Sets the color of the axis of [SfSparkChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkChart.html).

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkLineChart.AxisLineStyle>
    <sparkchart:SparkChartLineStyle>
        <sparkchart:SparkChartLineStyle.Stroke>
            <SolidColorBrush Color="#333333" />
        </sparkchart:SparkChartLineStyle.Stroke>
    </sparkchart:SparkChartLineStyle>
</sparkchart:SfSparkLineChart.AxisLineStyle>

{% endhighlight %}

{% highlight c# %}

chart.AxisLineStyle = new SparkChartLineStyle
{
    Stroke = new SolidColorBrush(Color.FromArgb("#F9113D"))
};

{% endhighlight %}

{% endtabs %}

![Axis stroke color in .NET MAUI Spark Line](sparkchart_axis_line_images\axis_stroke_color.png)

### Dashed line (StrokeDashArray)

Applies a dash pattern to the axis of [SfSparkChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkChart.html).

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkLineChart.AxisLineStyle>
    <sparkchart:SparkChartLineStyle StrokeWidth="1.5">
        <sparkchart:SparkChartLineStyle.StrokeDashArray>
            4,2
        </sparkchart:SparkChartLineStyle.StrokeDashArray>
    </sparkchart:SparkChartLineStyle>
</sparkchart:SfSparkLineChart.AxisLineStyle>

{% endhighlight %}

{% highlight c# %}

chart.AxisLineStyle = new SparkChartLineStyle
{
    StrokeWidth = 1.5,
    StrokeDashArray = new DoubleCollection { 4, 2 }
};

{% endhighlight %}

{% endtabs %}

![Axis StrokeDashArray in .NET MAUI Spark Line](sparkchart_axis_line_images\axis_line_stye.png)
