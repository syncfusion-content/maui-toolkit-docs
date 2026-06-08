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

## Focused

The [Focused](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html#Syncfusion_Maui_Toolkit_NumericEntry_SfNumericEntry_Focused) event is triggered when the `NumericEntry` control receives focus. This event can be used to perform actions such as highlighting the control, displaying helper text, or resetting validation messages when the user starts interacting with the field.

{% tabs %}
{% highlight xaml %}

<editors:SfNumericEntry Focused="OnNumericEntryFocused" />

{% endhighlight %}
{% highlight C# %}

SfNumericEntry sfNumericEntry = new SfNumericEntry();
sfNumericEntry.Focused += OnNumericEntryFocused;

// You can handle the event as follows.
private void OnNumericEntryFocused(object sender, FocusEventArgs e)
{
    // To do your requirement here.
}

{% endhighlight %}
{% endtabs %}

## Unfocused

The [Unfocused](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html#Syncfusion_Maui_Toolkit_NumericEntry_SfNumericEntry_Unfocused) event is triggered when the `NumericEntry` control loses focus. This event can be used to perform actions such as validating input, saving data, or updating the UI when the user moves away from the field.

{% tabs %}
{% highlight xaml %}

<editors:SfNumericEntry Unfocused="OnNumericEntryUnFocused" />

{% endhighlight %}
{% highlight C# %}

SfNumericEntry sfNumericEntry = new SfNumericEntry();
sfNumericEntry.Unfocused += OnNumericEntryUnFocused;

// You can handle the event as follows.
private void OnNumericEntryUnFocused(object sender, FocusEventArgs e)
{
    // To do your requirement here.
}

{% endhighlight %}
{% endtabs %}

## Methods

### Focus

The `NumericEntry` allows for programmatically setting focus to the control using the [Focus()](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html) method. This is useful when you want to automatically focus the control on page load or after a specific user action.

{% tabs %}
{% highlight xaml %}
<VerticalStackLayout Spacing="10">
    <editors:SfNumericEntry x:Name="sfNumericEntry" />
    <Button Text="Set Focus" Clicked="OnFocusClicked" />
</VerticalStackLayout>
{% endhighlight %}
{% highlight C# %}

SfNumericEntry sfNumericEntry = new SfNumericEntry();

// Programmatically set focus.
sfNumericEntry.Focus();

// You can handle the button click to set focus as follows.
private void OnFocusClicked(object sender, EventArgs e)
{
    sfNumericEntry.Focus();
}

{% endhighlight %}
{% endtabs %}

### Unfocus

The `NumericEntry` allows for programmatically setting unfocus to the control using the [Unfocus()](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html) method. This is useful when you want to automatically unfocus the control on page load or after a specific user action.


{% tabs %}
{% highlight xaml %}
<VerticalStackLayout Spacing="10">
    <editors:SfNumericEntry x:Name="sfNumericEntry" />
    <Button Text="Remove Focus" Clicked="OnUnFocusClicked" />
</VerticalStackLayout>

{% endhighlight %}
{% highlight C# %}

SfNumericEntry sfNumericEntry = new SfNumericEntry();

// Programmatically remove focus.
sfNumericEntry.Unfocus();

// You can handle the button click to remove focus as follows.
private void OnUnFocusClicked(object sender, EventArgs e)
{
    sfNumericEntry.Unfocus();
}

{% endhighlight %}
{% endtabs %}