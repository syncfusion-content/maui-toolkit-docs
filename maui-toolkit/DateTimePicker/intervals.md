---
layout: post
title: Intervals in .NET MAUI Date Time Picker control | Syncfusion®
description: Learn about intervals in Syncfusion® .NET MAUI Date Time Picker control for day, month, year, and time step configuration.
platform: maui
control: SfDateTimePicker
documentation: ug
---

# Intervals in .NET MAUI Date Time Picker control
The `SfDateTimePicker` provides six intervals in [.NET MAUI Date Time Picker](https://www.syncfusion.com/maui-controls/maui-datetimepicker).

 * [`DayInterval`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html#Syncfusion_Maui_Toolkit_Picker_SfDateTimePicker_DayInterval)
 * [`MonthInterval`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html#Syncfusion_Maui_Toolkit_Picker_SfDateTimePicker_MonthInterval)
 * [`YearInterval`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html#Syncfusion_Maui_Toolkit_Picker_SfDateTimePicker_YearInterval)
 * [`HourInterval`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html#Syncfusion_Maui_Toolkit_Picker_SfDateTimePicker_HourInterval)
 * [`MinuteInterval`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html#Syncfusion_Maui_Toolkit_Picker_SfDateTimePicker_MinuteInterval)
 * [`SecondInterval`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html#Syncfusion_Maui_Toolkit_Picker_SfDateTimePicker_SecondInterval)
 * [`MilliSecondInterval`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html#Syncfusion_Maui_Toolkit_Picker_SfDateTimePicker_MilliSecondInterval)

## Day interval
Date Time picker provides an option to give an interval between days using the [DayInterval](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html#Syncfusion_Maui_Toolkit_Picker_SfDateTimePicker_DayInterval) property of [SfDateTimePicker](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html).

{% tabs %}
{% highlight xaml tabtitle="XAML" hl_lines="2" %}

<picker:SfDateTimePicker x:Name="dateTimePicker"
                         DayInterval="2"/>

{% endhighlight %}
{% highlight c# tabtitle="C#" hl_lines="2" %}

SfDateTimePicker dateTimePicker = new SfDateTimePicker();
dateTimePicker.DayInterval = 2;
this.Content = dateTimePicker;

{% endhighlight %}
{% endtabs %}

   ![Day interval in .NET MAUI Date Time picker.](images/intervals/maui-date-time-picker-day-interval.png)

## Month interval
Date Time picker provides an option to give an interval between months using the [MonthInterval](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html#Syncfusion_Maui_Toolkit_Picker_SfDateTimePicker_MonthInterval) property of [SfDateTimePicker](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html).

{% tabs %}
{% highlight xaml tabtitle="XAML" hl_lines="2" %}

<picker:SfDateTimePicker x:Name="dateTimePicker"
                         MonthInterval="2"/>

{% endhighlight %}
{% highlight c# tabtitle="C#" hl_lines="2" %}

SfDateTimePicker dateTimePicker = new SfDateTimePicker();
dateTimePicker.MonthInterval = 2;
this.Content = dateTimePicker;

{% endhighlight %}
{% endtabs %}

   ![Day interval in .NET MAUI Date Time picker.](images/intervals/maui-date-time-picker-month-interval.png)

## Year interval
Date Time picker provides an option to give an interval between years using the [YearInterval](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html#Syncfusion_Maui_Toolkit_Picker_SfDateTimePicker_YearInterval) property of [SfDateTimePicker](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html).

{% tabs %}
{% highlight xaml tabtitle="XAML" hl_lines="2" %}

<picker:SfDateTimePicker x:Name="dateTimePicker"
                         YearInterval="2"/>

{% endhighlight %}
{% highlight c# tabtitle="C#" hl_lines="2" %}

SfDateTimePicker dateTimePicker = new SfDateTimePicker();
dateTimePicker.YearInterval = 2;
this.Content = dateTimePicker;

{% endhighlight %}
{% endtabs %}

   ![Year interval in .NET MAUI Date Time picker.](images/intervals/maui-date-time-picker-year-interval.png)

## Hour interval
Date Time picker provides an option to give an interval between hours using the [HourInterval](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html#Syncfusion_Maui_Toolkit_Picker_SfDateTimePicker_HourInterval) property of [SfDateTimePicker](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html).

{% tabs %}
{% highlight xaml tabtitle="XAML" hl_lines="2" %}

<picker:SfDateTimePicker x:Name="dateTimePicker"
                         HourInterval="2"/>

{% endhighlight %}
{% highlight c# tabtitle="C#" hl_lines="2" %}  

SfDateTimePicker dateTimePicker = new SfDateTimePicker();
dateTimePicker.HourInterval = 2;
this.Content = dateTimePicker;

{% endhighlight %}
{% endtabs %}

   ![Hour interval in .NET MAUI Date Time picker.](images/intervals/maui-date-time-picker-hour-interval.png)

## Minute interval
Date Time picker provides an option to give an interval between minutes using the [MinuteInterval](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html#Syncfusion_Maui_Toolkit_Picker_SfDateTimePicker_MinuteInterval) property of [SfDateTimePicker](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html).

{% tabs %}
{% highlight xaml tabtitle="XAML" hl_lines="2" %}

<picker:SfDateTimePicker x:Name="dateTimePicker"
                         MinuteInterval="2"/>

{% endhighlight %}
{% highlight c# tabtitle="C#" hl_lines="2" %}  

SfDateTimePicker dateTimePicker = new SfDateTimePicker();
dateTimePicker.MinuteInterval = 2;
this.Content = dateTimePicker;

{% endhighlight %}
{% endtabs %}

   ![Minute interval in .NET MAUI Date Time picker.](images/intervals/maui-date-time-picker-minute-interval.png)

## Second interval
Date Time picker provides an option to give an interval between seconds using the [SecondInterval](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html#Syncfusion_Maui_Toolkit_Picker_SfDateTimePicker_SecondInterval) property of [SfDateTimePicker](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html).

{% tabs %}
{% highlight xaml tabtitle="XAML" hl_lines="2" %}

<picker:SfDateTimePicker x:Name="dateTimePicker"
                         SecondInterval="2"/>

{% endhighlight %}
{% highlight c# tabtitle="C#" hl_lines="2" %}  

SfDateTimePicker dateTimePicker = new SfDateTimePicker()
dateTimePicker.SecondInterval = 2;
this.Content = dateTimePicker;

{% endhighlight %}
{% endtabs %}

   ![Second interval in .NET MAUI Date Time picker.](images/intervals/maui-date-time-picker-second-interval.png)

## MilliSecond interval
Date Time picker provides an option to give an interval between milliseconds using the [MilliSecondInterval](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html#Syncfusion_Maui_Toolkit_Picker_SfDateTimePicker_MilliSecondInterval) property of [SfDateTimePicker](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html).

{% tabs %}
{% highlight xaml tabtitle="XAML" hl_lines="2" %}

<picker:SfDateTimePicker x:Name="dateTimePicker"
                         MilliSecondInterval="2"/>

{% endhighlight %}
{% highlight c# tabtitle="C#" hl_lines="2" %}  

SfDateTimePicker dateTimePicker = new SfDateTimePicker()
dateTimePicker.MilliSecondInterval = 2;
this.Content = dateTimePicker;

{% endhighlight %}
{% endtabs %}

   ![MilliSecond interval in .NET MAUI Date Time picker.](images/intervals/maui-date-time-picker-millisecond-interval.png)