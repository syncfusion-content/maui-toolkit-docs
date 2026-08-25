---
layout: post
title: Date Restriction in .NET MAUI Date Time Picker control | Syncfusion®
description: Learn about date restriction in Syncfusion® .NET MAUI Date Time Picker control to manage selectable date and time ranges.
platform: maui
control: SfDateTimePicker
documentation: ug
---

# Date Restriction in .NET MAUI Date Time Picker control

## Minimum date
The Date time picker provides an option to restrict the selection of date and time using the [MinimumDate](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html#Syncfusion_Maui_Toolkit_Picker_SfDateTimePicker_MinimumDate) property in [SfDateTimePicker](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html), and you cannot select the date and time beyond the minimum date range. The MinimumDate value has to be lesser than the MaximumDate value.

{% tabs %}
{% highlight xaml tabtitle="XAML" hl_lines="2" %}

<picker:SfDateTimePicker x:Name="dateTimePicker"
                         MinimumDate="2000/5/6 3:34:12 AM">
</picker:SfDateTimePicker>

{% endhighlight %}
{% highlight c# tabtitle="C#" hl_lines="2" %}

SfDateTimePicker dateTimePicker = new SfDateTimePicker();
dateTimePicker.MinimumDate = new DateTime(2000, 5, 6, 3, 34, 12);
this.Content = dateTimePicker;

{% endhighlight %}  
{% endtabs %}

   ![Minimum date in .NET MAUI Date Time picker.](images/date-restriction/maui-date-time-picker-minimum-date.png)

## Maximum date
The Date time picker provides an option to restrict the selection of date and time using the [MaximumDate](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html#Syncfusion_Maui_Toolkit_Picker_SfDateTimePicker_MaximumDate) property in [SfDateTimePicker](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html), and you cannot select the date and time beyond the maximum date range.

{% tabs %}
{% highlight xaml tabtitle="XAML" hl_lines="2" %}

<picker:SfDateTimePicker x:Name="dateTimePicker"
                         MaximumDate="2042/10/10 12:15:03 PM">
</picker:SfDateTimePicker>

{% endhighlight %}
{% highlight c# tabtitle="C#" hl_lines="2" %}

SfDateTimePicker dateTimePicker = new SfDateTimePicker();
dateTimePicker.MaximumDate = new DateTime(2042, 10, 10, 12, 15, 03);
this.Content = dateTimePicker;

{% endhighlight %}  
{% endtabs %}

   ![Maximum date in .NET MAUI Date Time picker.](images/date-restriction/maui-date-time-picker-maximum-date.png)

## Blackout Date times

The [Blackout Date times](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html#Syncfusion_Maui_Toolkit_Picker_SfDateTimePicker_BlackoutDateTimes) property in the [SfDateTimePicker](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfDateTimePicker.html) component allows you to block the selection of specific dates and times. You can define a list of entire dates or particular time slots within those dates to disable, preventing their selection. This feature is useful for enforcing availability rules, such as restricting specific days or hours.

{% tabs %}
{% highlight xaml tabtitle="XAML" %}

<picker:SfDateTimePicker x:Name="dateTimePicker">
   <picker:SfDateTimePicker.BlackoutDateTimes>
      <date:DateTime>2001-08-10</date:DateTime>
      <date:DateTime>2001-08-12</date:DateTime>
      <date:DateTime>2001-08-14</date:DateTime>
      <date:DateTime>2001-08-17</date:DateTime>
      <date:DateTime>2001-08-18</date:DateTime>
      <date:DateTime>2001-08-20</date:DateTime>
      <date:DateTime>2001-08-23</date:DateTime>
      <date:DateTime>2001-08-27</date:DateTime>
      <date:DateTime>2001-08-03</date:DateTime>
      <date:DateTime>2001-08-15 12:11:00</date:DateTime>
      <date:DateTime>2001-08-15 12:12:00</date:DateTime>
      <date:DateTime>2001-08-15 12:08:00</date:DateTime>
      <date:DateTime>2001-08-15 12:06:00</date:DateTime>
      <date:DateTime>2001-08-15 12:14:00</date:DateTime>
   </picker:SfDateTimePicker.BlackoutDateTimes>
</picker:SfDateTimePicker>

{% endhighlight %}
{% highlight c# tabtitle="C#" %}

SfDateTimePicker dateTimePicker = new SfDateTimePicker();
dateTimePicker.BlackoutDateTimes.Add(new DateTime(2001, 8, 10));
dateTimePicker.BlackoutDateTimes.Add(new DateTime(2001, 8, 12));
dateTimePicker.BlackoutDateTimes.Add(new DateTime(2001, 8, 14));
dateTimePicker.BlackoutDateTimes.Add(new DateTime(2001, 8, 17));
dateTimePicker.BlackoutDateTimes.Add(new DateTime(2001, 8, 18));
dateTimePicker.BlackoutDateTimes.Add(new DateTime(2001, 8, 20));
dateTimePicker.BlackoutDateTimes.Add(new DateTime(2001, 8, 23));
dateTimePicker.BlackoutDateTimes.Add(new DateTime(2001, 8, 27));
dateTimePicker.BlackoutDateTimes.Add(new DateTime(2001, 8, 3));
dateTimePicker.BlackoutDateTimes.Add(new DateTime(2001, 8, 15, 12, 11, 0));
dateTimePicker.BlackoutDateTimes.Add(new DateTime(2001, 8, 15, 12, 12, 0));
dateTimePicker.BlackoutDateTimes.Add(new DateTime(2001, 8, 15, 12, 8, 0));
dateTimePicker.BlackoutDateTimes.Add(new DateTime(2001, 8, 15, 12, 6, 0));
dateTimePicker.BlackoutDateTimes.Add(new DateTime(2001, 8, 15, 12, 14, 0));
this.Content = dateTimePicker;

{% endhighlight %}  
{% endtabs %}

![Blackout date times day columns in .NET MAUI Date Time picker.](images/date-restriction/maui-date-time-picker-blackout-date-times-day.png)

![Blackout date times time columns in .NET MAUI Date Time picker.](images/date-restriction/maui-date-time-picker-blackout-date-times-time.png)

N> The `Selection View` will not be applicable when setting `Blackout date times`.