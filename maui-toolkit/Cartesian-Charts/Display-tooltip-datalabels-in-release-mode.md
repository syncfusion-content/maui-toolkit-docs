---
layout: post
title: Display tooltip and datalabels in release mode in Syncfusion SfCartesianChart
description: Learn here all about displaying tooltip and datalabels in release mode in SfCartesianChart in Syncfusion® .NET MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
keywords: .NET MAUI chart tooltip, .NET MAUI chart data label, TooltipInfo Item binding, ChartDataLabel Item binding, Release mode trimming, Preserve attribute MAUI.
---

# Display tooltip and datalabels in release mode .NET MAUI SfCartesianChart

The `binding context` inside tooltip and datalabels templates is not your model directly. These templates run in the scope of [TooltipInfo](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Charts.TooltipInfo.html) and [ChartDataLabel](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Charts.ChartDataLabel.html), which expose an `Item` property that contains the actual data model from the charts [ItemsSource](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Charts.ChartSeries.html#Syncfusion_Maui_Charts_ChartSeries_ItemsSource). To read your model’s fields in a template, bind through Item or converter.


{% highlight xaml %}

    <chart:SfCartesianChart>
    .....
    <chart:SfCartesianChart.Resources>

        <DataTemplate x:Key="TooltipTemplate">
            <StackLayout x:DataType="chart:TooltipInfo" Orientation="Vertical">
                <Label Text="{Binding Item,
                            Converter={StaticResource TooltipConverter},
                            ConverterParameter=Planned,
                            StringFormat='Planned : {0}h'}"/>
            </StackLayout>
        </DataTemplate>

        <DataTemplate x:Key="DataLabelTemplate">
            <StackLayout x:DataType="chart:ChartDataLabel" Orientation="Vertical">
                <Label Text="{Binding Item,
                            Converter={StaticResource TooltipConverter},
                            ConverterParameter=Planned,
                            StringFormat='Planned : {0}h'}" />
            </StackLayout>
        </DataTemplate>
    </chart:SfCartesianChart.Resources>

    <chart:SplineAreaSeries
        ....
        TooltipTemplate="{StaticResource TooltipTemplate}"
        ShowDataLabels="True"
        LabelTemplate="{StaticResource DataLabelTemplate}" />
    </chart:SfCartesianChart>

{% endhighlight %}


{% highlight C# %}

    public class TooltipConverter : IValueConverter
    {
        public object? Convert(object? value, Type targetType, object? parameter, CultureInfo culture)
        {
            // value is TooltipInfo.Item or ChartDataLabel.Item -> your Model
            if (value is Model model && parameter?.ToString() == "Planned")
                return model.Planned;

            return value;
        }
        public object? ConvertBack(object? value, Type targetType, object? parameter, CultureInfo culture) => value;
    }

{% endhighlight %}

## See also 

[How to display tooltip and datalabels in release mode .NET MAUI SfCartesianChart](https://support.syncfusion.com/kb/article/21677/why-tooltip-and-datalabel-are-not-showing-in-release-mode-in-net-maui-sfcartesianchart)