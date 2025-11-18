---
layout: post
title: Tooltip in .NET MAUI Circular Chart control | Syncfusion
description: This section explains about how to enable tooltip and its customization in Syncfusion® .NET MAUI Chart (SfCircularChart) control
platform: maui-toolkit
control: SfCircularChart
documentation: ug
keywords: .net maui, maui chart, maui toolkit chart, circular chart, chart tooltip, chart tooltip behavior, enable tooltip, chart tooltip customization, tooltip template.
---

# Tooltip in .NET Circular MAUI Chart

Tooltip is used to display information or metadata of the tapped segment. The Circular Chart provides tooltip support for all series.

## Define Tooltip

To define the tooltip in the chart, set the [EnableTooltip](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartSeries.html#Syncfusion_Maui_Toolkit_Charts_ChartSeries_EnableTooltip) property of series to true. The default value of the [EnableTooltip](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartSeries.html#Syncfusion_Maui_Toolkit_Charts_ChartSeries_EnableTooltip) property is false.

{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>
    <!-- Other chart configurations -->
	<chart:PieSeries EnableTooltip="True"/>   
</chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

SfCircularChart chart = new SfCircularChart();
// Other chart configurations
PieSeries series = new PieSeries();
series.EnableTooltip = true; // Enable tooltips for this series
chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Tooltip support in MAUI chart](Tooltip_images/maui_chart_tooltip.png)

The [ChartTooltipBehavior](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartTooltipBehavior.html) is used to customize the tooltip. For customizing the tooltip, create an instance of [ChartTooltipBehavior](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartTooltipBehavior.html) and set it to the [TooltipBehavior](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartBase.html#Syncfusion_Maui_Toolkit_Charts_ChartBase_TooltipBehavior) property of [SfCircularChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCircularChart.html). The following properties are used to customize the tooltip:

* [Background](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartTooltipBehavior.html#Syncfusion_Maui_Toolkit_Charts_ChartTooltipBehavior_Background) - Gets or sets the background color of the tooltip.
* [FontAttributes](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartTooltipBehavior.html#Syncfusion_Maui_Toolkit_Charts_ChartTooltipBehavior_FontAttributes) - Gets or sets the font style for the tooltip text.
* [FontFamily](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartTooltipBehavior.html#Syncfusion_Maui_Toolkit_Charts_ChartTooltipBehavior_FontFamily) - Gets or sets the font family name for the tooltip text.
* [FontSize](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartTooltipBehavior.html#Syncfusion_Maui_Toolkit_Charts_ChartTooltipBehavior_FontSize) - Gets or sets the font size for the tooltip text.
* [Duration](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartTooltipBehavior.html#Syncfusion_Maui_Toolkit_Charts_ChartTooltipBehavior_Duration) - Gets or sets the duration in milliseconds for which the tooltip remains visible.
* [Margin](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartTooltipBehavior.html#Syncfusion_Maui_Toolkit_Charts_ChartTooltipBehavior_Margin) - Gets or sets the margin of the tooltip to customize its appearance.
* [TextColor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartTooltipBehavior.html#Syncfusion_Maui_Toolkit_Charts_ChartTooltipBehavior_TextColor) - Gets or sets the color for the tooltip text.

{% tabs %}

{% highlight xml %}

<chart:SfCircularChart>
    <!-- Other chart configurations -->
	<chart:SfCircularChart.TooltipBehavior>
		<chart:ChartTooltipBehavior Duration="2000"/>
	</chart:SfCircularChart.TooltipBehavior>
</chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

SfCircularChart chart = new SfCircularChart();
// Other chart configurations
chart.TooltipBehavior = new ChartTooltipBehavior()
{
    Duration = 2000, // Set the tooltip display duration in milliseconds
};
this.Content = chart;
{% endhighlight %}

{% endtabs %}

## Template

Circular chart provides support to customize the appearance of the tooltip by using the [TooltipTemplate](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartSeries.html#Syncfusion_Maui_Toolkit_Charts_ChartSeries_TooltipTemplate) property.

{% tabs %}

{% highlight xaml %}

<chart:SfCircularChart>
    <!-- Other chart configurations -->
    <chart:SfCircularChart.Resources>
        <DataTemplate x:Key="tooltipTemplate">
            <StackLayout Orientation="Horizontal">
				<Label Text="{Binding Item.Product}"
				       TextColor="Black"
				       FontAttributes="Bold"
				       FontSize="12"
				       HorizontalOptions="Center"
				       VerticalOptions="Center"/>
				<Label Text=" : " 
				       TextColor="Black"
				       FontAttributes="Bold"
				       FontSize="12"
				       HorizontalOptions="Center"
				       VerticalOptions="Center"/>
                		<Label Text="{Binding Item.SalesRate}"
			  	       TextColor="Black"
				       FontAttributes="Bold"
				       FontSize="12"
				       HorizontalOptions="Center"
				       VerticalOptions="Center"/>
            </StackLayout>
        </DataTemplate>
    </chart:SfCircularChart.Resources>

    <chart:PieSeries EnableTooltip="True"
		     ItemsSource="{Binding Data}" 
		     XBindingPath="Product" 
		     YBindingPath="SalesRate"
		     TooltipTemplate="{StaticResource tooltipTemplate}"/>
</chart:SfCircularChart>

{% endhighlight %}

{% highlight c# %}

SfCircularChart chart = new SfCircularChart();
// Other chart configurations
PieSeries series = new PieSeries();
series.EnableTooltip = true;
series.TooltipTemplate = chart.Resources["tooltipTemplate"] as DataTemplate; // Set a custom tooltip template from the chart's resources
// Other series configurations
chart.Series.Add(series);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Tooltip template in MAUI Chart](Tooltip_images/maui_chart_tooltip_customization.png)

