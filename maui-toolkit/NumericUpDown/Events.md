---
ayout: post
title: Events in .NET MAUI Numeric UpDown control | Syncfusion®
description: Learn here all about the Events support in Syncfusion® .NET MAUI Numeric UpDown (SfNumericUpDown) control and more details.
platform: maui
control: SfNumericUpDown
documentation: ug
---

# Events in .NET MAUI Numeric UpDown

The NumericUpDown control has the events `ValueChanged` and `Completed` to notify after user interactions in [.NET MAUI Numeric UpDown](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html).

## ValueChanged

The [ValueChanged](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html#Syncfusion_Maui_Toolkit_NumericEntry_SfNumericEntry_ValuChanged) event is triggered when the [Value](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html#Syncfusion_Maui_Toolkit_NumericEntry_SfNumericEntry_Value) property of the `Numeric UpDown` control is changed. The value will not be changed when the user enters the input. The value of the `Numeric UpDown` control will be changed after validation is performed on the `Enter` keypress or when the focus is lost in the control. The `ValueChanged` contains the following properties.

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

private void sfNumericUpDown_ValueChanged(object sender, Syncfusion.Maui.Toolkit.NumericEntry.NumericEntryValueChangedEventArgs e)
{
    var oldValue = e.OldValue;
    var newValue = e.NewValue;
}

{% endhighlight %}
{% endtabs %}

## Completed

The `Numeric UpDown` control includes a [Completed](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html#Syncfusion_Maui_Toolkit_NumericEntry_SfNumericEntry_Completed) event, which is triggered when the user finishes editing and presses the return key on the keyboard.This event enables handling actions such as input validation, submitting data, or automatically focusing on the next field.

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

## Focused

The [Focused](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html#Syncfusion_Maui_Toolkit_NumericEntry_SfNumericEntry_Focused) event is triggered when the `Numeric UpDown` control receives focus. This event can be used to perform actions such as highlighting the control or displaying additional information when it becomes active.

{% tabs %}
{% highlight xaml %}

<editors:SfNumericUpDown Focused="OnNumericUpDownFocused" />

{% endhighlight %}
{% highlight C# %}

SfNumericUpDown sfNumericUpDown = new SfNumericUpDown();
sfNumericUpDown.Focused += OnNumericUpDownFocused;

// You can handle the event as follows.
private void OnNumericUpDownFocused(object sender, FocusEventArgs e)
{
    // To do your requirement here.
}

{% endhighlight %}
{% endtabs %}

## Unfocused

The [Unfocused](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html#Syncfusion_Maui_Toolkit_NumericEntry_SfNumericEntry_Unfocused) event is triggered when the `Numeric UpDown` control loses focus. This event can be used to perform actions such as validating the entered value or updating the UI when the control becomes inactive.

{% tabs %}
{% highlight xaml %}

<editors:SfNumericUpDown Unfocused="OnNumericUpDownUnFocused" />

{% endhighlight %}
{% highlight C# %}

SfNumericUpDown sfNumericUpDown = new SfNumericUpDown();
sfNumericUpDown.Unfocused += OnNumericUpDownUnFocused;

// You can handle the event as follows.
private void OnNumericUpDownUnFocused(object sender, FocusEventArgs e)
{
    // To do your requirement here.
}

{% endhighlight %}
{% endtabs %}

## Methods

### Focus

The `Numeric UpDown` allows for programmatically setting focus to the control using the [Focus()](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html) method. This is useful when you want to automatically focus the control on page load or after a specific user action.

{% tabs %}
{% highlight xaml %}
<VerticalStackLayout Spacing="10">
    <editors:SfNumericUpDown x:Name="sfNumericUpDown" />
    <Button Text="Set Focus" Clicked="OnFocusClicked" />
</VerticalStackLayout>
{% endhighlight %}
{% highlight C# %}

SfNumericUpDown sfNumericUpDown = new SfNumericUpDown();

// Call Focus() method to programmatically focus the control.
sfNumericUpDown.Focus();

// You can handle the button click as follows.
private void OnFocusClicked(object sender, EventArgs e)
{
    sfNumericUpDown.Focus();
}

{% endhighlight %}
{% endtabs %}

### Unfocus

The `Numeric UpDown` allows for programmatically setting unfocus to the control using the [Unfocus()](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html) method. This is useful when you want to automatically unfocus the control on page load or after a specific user action.

{% tabs %}
{% highlight xaml %}
<VerticalStackLayout Spacing="10">
    <editors:SfNumericUpDown x:Name="sfNumericUpDown" />
    <Button Text="Remove Focus" Clicked="OnUnFocusClicked" />
</VerticalStackLayout>
{% endhighlight %}
{% highlight C# %}

SfNumericUpDown sfNumericUpDown = new SfNumericUpDown();

// Call Unfocus() method to programmatically remove focus from the control.
sfNumericUpDown.Unfocus();

// You can handle the button click as follows.
private void OnUnFocusClicked(object sender, EventArgs e)
{
    sfNumericUpDown.Unfocus();
}

{% endhighlight %}
{% endtabs %}