---
ayout: post
title: Events in .NET MAUI NumericUpDown control | Syncfusion
description: Learn here all about the Events support in Syncfusion .NET MAUI NumericUpDown (SfNumericUpDown) control and more details.
platform: maui
control: SfNumericUpDown
documentation: ug
---

# Events in .NET MAUI NumericUpDown (SfNumericUpDown)

The NumericUpDown control has the events `ValueChanged` and `Completed` to notify after user interactions in [.NET MAUI NumericUpDown]().

## ValueChanged

The [ValueChanged]() event is triggered when the [Value]() property of the `NumericUpDown` control is changed. The value will not be changed when the user enters the input. The value of the `NumericUpDown` control will be changed after validation is performed on the `Enter` keypress or when the focus is lost in the control. The `ValueChanged` contains the following properties.

 * `NewValue`- Contains the new input value.
 * `OldValue`- Contains the previous input value.

{% tabs %}
{% highlight xaml %}

<editors:SfNumericUpDown HorizontalOptions="Center"
                        VerticalOptions="Center"
                        ValueChanged="sfNumericUpDown_ValueChanged" />

{% endhighlight %}
{% highlight C# %}

SfNumericUpDown sfNumericUpDown = new SfNumericUpDown();
sfNumericUpDown.HorizontalOptions = LayoutOptions.Center;
sfNumericUpDown.VerticalOptions = LayoutOptions.Center;
sfNumericUpDown.ValueChanged += sfNumericUpDown_ValueChanged;

{% endhighlight %}
{% endtabs %}

You can handle the event as follows.

{% tabs %}
{% highlight C# %}

private void sfNumericUpDown_ValueChanged(object sender, NumericEntryValueChangedEventArgs e)
{
    var oldValue = e.OldValue;
    var newValue = e.NewValue;
}

{% endhighlight %}
{% endtabs %}

## Completed

The `NumericUpDown` control includes a [Completed]() event, which is triggered when the user finishes editing and presses the return key on the keyboard.This event enables handling actions such as input validation, submitting data, or automatically focusing on the next field.

{% tabs %}
{% highlight xaml %}

<editors:SfNumericUpDown HorizontalOptions="Center"
                         VerticalOptions="Center"
                         Completed="sfNumericUpDown_Completed" />

{% endhighlight %}
{% highlight C# %}

SfNumericUpDown sfNumericUpDown = new SfNumericUpDown();
sfNumericUpDown.HorizontalOptions = LayoutOptions.Center;
sfNumericUpDown.VerticalOptions = LayoutOptions.Center;
sfNumericUpDown.Completed += sfNumericUpDown_Completed;

{% endhighlight %}
{% endtabs %}

You can handle the event as follows.

{% tabs %}
{% highlight C# %}

private void sfNumericUpDown_Completed(object sender, EventArgs e)
{
    // To do your requirement here.
}

{% endhighlight %}
{% endtabs %}
