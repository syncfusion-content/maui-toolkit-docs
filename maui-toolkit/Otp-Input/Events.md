---
layout: post
title: Events in .NET MAUI OTP Input Control | Syncfusion®
description: Learn about event support in the Syncfusion® Toolkit for .NET MAUI OTP Input (SfOtpInput) control and more.
platform: maui-toolkit
control: SfOtpInput
documentation: UG
---

# Events in .NET MAUI OTP Input (SfOtpInput)

Events in the OTP Input control allow developers to effectively respond to user interactions and input changes.

## ValueChanged event

The OTP Input component triggers the [ValueChanged](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_ValueChanged) event whenever the value of an input field changes. This is particularly useful for validating input in real-time or triggering further actions as the user completes their input. The [OtpInputValueChangedEventArgs](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.OtpInputValueChangedEventArgs.html) provides detailed information about the specific changes in value.

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