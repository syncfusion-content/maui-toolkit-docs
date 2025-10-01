---
layout: post
title: Axis line in .NET MAUI Spark Chart Control | Syncfusion
description: Learn how to display and customize the axis line in Syncfusion® .NET MAUI Spark Charts (SfSparkChart) using ShowAxis, AxisOrigin, and AxisLineStyle.
platform: maui-toolkit
control: SfSparkChart
documentation: ug
---

# Axis line in .NET MAUI Spark Charts (SfSparkChart)

The Spark Chart axis line is a horizontal reference line that helps highlight a axis line (for example, zero) or any custom Y value. It is supported by all Spark Chart types of `SfSparkChart`.

Axis of the `SfSparkChart` can be configured and customized using following properties:

- `ShowAxis`: Enables or disables the axis line. Default `false`.
- `AxisOrigin`: Sets the Y-value where the axis line is drawn. Default it renders at `0`.
- `AxisLineStyle`: Customizes the appearance of the axis line. AxisLineStyle includes:
  - `Stroke`: Specifies the line color of the axis line.
  - `StrokeWidth`: Specifies the line thickness of the axis line. Default: 1.
  - `StrokeDashArray`: Specifies the dash pattern for the axis line. Default: null.

---

## Enable the axis line

Use `ShowAxis="True"` to display the axis line at the default origin of SfSparkChart. Default axis line is set to `False`.

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

![Axis line in .NET MAUI Spark Line](sparkchart_axis_line_images\Default_axis_line.png)

---

## Axis origin

Set `AxisOrigin` to draw the line at a specific Y value (for example, `0` to emphasize zero, or any custom value) of SfSparkChart.

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

![Axis line origin in .NET MAUI Spark Line](sparkchart_axis_line_images\axis_origin.png)

---

## Style the axis line

### Stroke width

Controls the thickness of the axis line of SfSparkChart.

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

![Axis line stroke width in .NET MAUI Spark Line](sparkchart_axis_line_images\axis_stroke_width.png)

### Stroke color

Sets the color of the axis line of SfSparkChart.

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

![Axis line stroke color in .NET MAUI Spark Line](sparkchart_axis_line_images\axis_stroke_color.png)

### Dashed line (StrokeDashArray)

Applies a dash pattern to the axis line of SfSparkChart.

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

---