---
layout: post
title: Show tooltip and datalabels in release mode | Syncfusion
description: Learn here all about displaying tooltip and datalabels in release mode in SfCartesianChart in Syncfusion® .NET MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
keywords: .NET MAUI chart tooltip, .NET MAUI chart data label, TooltipInfo Item binding, ChartDataLabel Item binding, Release mode trimming, Preserve attribute MAUI.
---

# Display tooltip and data labels in release mode

In [SfCartesianChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html), the tooltip and data label templates do not use item from [ItemsSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartSeries.html#Syncfusion_Maui_Toolkit_Charts_ChartSeries_ItemsSourceProperty) as their binding context. These elements are created by the chart at runtime and can represent calculated points, so the chart supplies its own context with all needed metadata. For tooltips this context is [TooltipInfo](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.TooltipInfo.html), and for data labels it is [ChartDataLabel](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartDataLabel.html). Both provide an Item property that points back to your original data object when a direct mapping exists. If you need fields from your model inside the template, bind through Item (or use a converter).

Release builds can remove types that are referenced only from XAML. To prevent this, reference a value converter from XAML and preserve your ViewModel, business model, and converter classes. With .NET 9 compiled bindings, set **x:DataType="chart:TooltipInfo"** for tooltip templates and **x:DataType="chart:ChartDataLabel"** for data label templates, then bind via Item. Use the converter to extract the required property from Item.

{% tabs %}

{% highlight xaml %}

    <chart:SfCartesianChart>
        <chart:SfCartesianChart.Resources>
            <local:ValueConverter x:Key="valueConverter" />

            <DataTemplate x:Key="tooltiptemplate">
                <StackLayout x:DataType="chart:TooltipInfo" Orientation="Vertical">
                    <Label Text="{Binding Item, Converter={StaticResource valueConverter},
                                          ConverterParameter=Planned,
                                          StringFormat='Planned : {0}h'}"
                           TextColor="White" />
                </StackLayout>
            </DataTemplate>

            <DataTemplate x:Key="labelTemplate">
                <StackLayout x:DataType="chart:ChartDataLabel" Orientation="Vertical">
                    <Label Text="{Binding Item, Converter={StaticResource valueConverter},
                                          ConverterParameter=Planned,
                                          StringFormat='Label : {0}h'}"
                           TextColor="Black" />
                </StackLayout>
            </DataTemplate>
        </chart:SfCartesianChart.Resources>

        <chart:SplineAreaSeries x:Name="series"
                                ItemsSource="{Binding ChartData}"
                                XBindingPath="WeekNumber"
                                YBindingPath="Planned"
                                EnableTooltip="True"
                                ShowDataLabels="True"
                                LabelTemplate="{StaticResource labelTemplate}"
                                TooltipTemplate="{StaticResource tooltiptemplate}">
        </chart:SplineAreaSeries>

    </chart:SfCartesianChart>

{% endhighlight %}


{% highlight C# %}

    public class ValueConverter : IValueConverter
    {
        public object Convert(object value, Type targetType, object parameter, CultureInfo culture)
        {
            return value is WeekPlan weekPlan ? weekPlan.Planned : value;
        }

        public object ConvertBack(object value, Type targetType, object parameter, CultureInfo culture) => value;
    }

{% endhighlight %}

{% endtabs %}

## See also 

[Why Tooltip and DataLabel Are Missing in Release Mode .NET MAUI Chart?](https://support.syncfusion.com/kb/article/21677/why-tooltip-and-datalabel-are-not-showing-in-release-mode-in-net-maui-sfcartesianchart)