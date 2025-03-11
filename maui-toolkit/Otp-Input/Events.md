---
layout: post
title: Events in .NET MAUI OtpInput control | Syncfusion®
description: Learn about event support in Syncfusion® Toolkit for .NET MAUI OtpInput (SfOtpInput) control and more.
platform: maui-toolkit
control: OtpInput
documentation: ug
---

# Events in .NET MAUI OtpInput (SfOtpInput)

Events in the OtpInput control allow developers to respond effectively to user interactions and input changes.

## ValueChanged event

The OtpInput component triggers the `ValueChanged` event whenever the value of an input field changes. This is particularly useful for validating input in real-time or triggering further actions as user input is completed. The `OtpInputValueChangedEventArgs` provides details about the specific changes in value.

{% tabs %}
{% highlight xaml %}

<otpInput:SfOtpInput ValueChanged="OnValueChanged" />

{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput();
otpInput.ValueChanged += OnValueChanged;

{% endhighlight %}
{% endtabs %}

{% highlight c# %}

private void OnValueChanged(object sender, OtpInputValueChangedEventArgs e)
{
    // Code executed when the input value changes.
    // Example: Update the interface to show the new input value.
    Console.WriteLine("New Value: " + e.NewValue);
}

{% endhighlight %}