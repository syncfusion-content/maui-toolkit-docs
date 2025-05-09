---
layout: post
title: Customize each axis chart label using the callback event | Syncfusion
description: Learn here all about to customize each chart axis label using the callback event in Syncfusion® .NET MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
keywords: .net maui chart customize axis label callback, .net maui chart axis label callback event, sfcartesianchart axis label callback customization in .net maui, sfcartesianchart custom axis label event handling in .net maui.
---

# Customize each chart axis label using the callback event

The [LabelCreated](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html#Syncfusion_Maui_Toolkit_Charts_ChartAxis_LabelCreated) event is triggered upon label creation in a chart axis, providing the option to customize chart axis labels.

The following code sample demonstrates this:

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    . . .
    <chart:SfCartesianChart.XAxes>
        <chart:NumericalAxis LabelCreated="XAxes_LabelCreated"/>
    </chart:SfCartesianChart.XAxes>
    . . .
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight C# %}

SfCartesianChart chart = new SfCartesianChart();
. . .
NumericalAxis primaryAxis = new NumericalAxis();
// Subscribe to the LabelCreated event of the primary axis
// This event is triggered whenever a label is created on the axis
primaryAxis.LabelCreated += XAxes_LabelCreated;
chart.XAxes.Add(primaryAxis);
. . .
this.Content = chart;    
{% endhighlight %}

{% endtabs %}

{% tabs %}

{% highlight c# %}

int month = 0;

//Customize each axis label achieved by displaying the first label of each month with a month format, while other labels within the same month are formatted with a day format in the DateTimeAxis of the chart.

private void XAxes_LabelCreated(object sender, ChartAxisLabelEventArgs e)
{
    DateTime date = DateTime.Parse(e.Label);

    if (month != date.Month)
    {
        e.Label = date.ToString("MMM");
        month = date.Month;
    }
    else
        e.Label = date.Day.ToString();
}
    
{% endhighlight  %}

{% endtabs %}

![Customize each chart axis label](How-to_images/MAUI_Customize_each_chart_axis_label.png)