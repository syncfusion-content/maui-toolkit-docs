---
ayout: post
title: Events in .NET MAUI NumericEntry control | Syncfusion<sup>®</sup>
description: Learn here all about the Events support in Syncfusion<sup>®</sup> .NET MAUI NumericEntry (SfNumericEntry) control and more details.
platform: maui
control: SfNumericEntry
documentation: ug
---

# Events in .NET MAUI NumericEntry (SfNumericEntry)

The NumericEntry control has the events `ValueChanged` and `Completed` to notify after user inputs in [.NET MAUI NumericEntry](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html).

## ValueChanged

The [ValueChanged](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html#Syncfusion_Maui_Toolkit_NumericEntry_SfNumericEntry_ValueChanged) event is triggered when the [Value](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html#Syncfusion_Maui_Toolkit_NumericEntry_SfNumericEntry_Value) property of the `NumericEntry` control is changed. The value will not be changed when the user enters the input. The value of the `NumericEntry` control will be changed after validation is performed on the `Enter` keypress or when the focus is lost in the control. The `ValueChanged` contains the following properties.

 * `NewValue`- Contains the new input value.
 * `OldValue`- Contains the previous input value.

{% tabs %}
{% highlight xaml %}

<editors:SfNumericEntry HorizontalOptions="Center"
                        VerticalOptions="Center"
                        ValueChanged="sfNumericEntry_ValueChanged" />

{% endhighlight %}
{% highlight C# %}

SfNumericEntry sfNumericEntry = new SfNumericEntry();
sfNumericEntry.HorizontalOptions = LayoutOptions.Center;
sfNumericEntry.VerticalOptions = LayoutOptions.Center;
sfNumericEntry.ValueChanged += sfNumericEntry_ValueChanged;

{% endhighlight %}
{% endtabs %}

You can handle the event as follows.

{% tabs %}
{% highlight C# %}

private void sfNumericEntry_ValueChanged(object sender, Syncfusion.Maui.Toolkit.NumericEntry.NumericEntryValueChangedEventArgs e)
{
    var oldValue = e.OldValue;
    var newValue = e.NewValue;
}

{% endhighlight %}
{% endtabs %}

## Completed

The `NumericEntry` control includes a [Completed](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html#Syncfusion_Maui_Toolkit_NumericEntry_SfNumericEntry_Completed) event, which is triggered when the user finishes editing and presses the return key on the keyboard.This event enables handling actions such as input validation, submitting data, or automatically focusing on the next field.

{% tabs %}
{% highlight xaml %}

<editors:SfNumericEntry HorizontalOptions="Center"
                        VerticalOptions="Center"
                        Completed="sfNumericEntry_Completed" />

{% endhighlight %}
{% highlight C# %}

SfNumericEntry sfNumericEntry = new SfNumericEntry();
sfNumericEntry.HorizontalOptions = LayoutOptions.Center;
sfNumericEntry.VerticalOptions = LayoutOptions.Center;
sfNumericEntry.Completed += sfNumericEntry_Completed;

{% endhighlight %}
{% endtabs %}

You can handle the event as follows.

{% tabs %}
{% highlight C# %}

private void sfNumericEntry_Completed(object sender, EventArgs e)
{
    // To do your requirement here.
}

{% endhighlight %}
{% endtabs %}
