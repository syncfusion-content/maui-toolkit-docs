---
layout: post
title: Events in .NET MAUI OtpInput control | Syncfusion®
description: Learn about event support in Syncfusion® Toolkit for .NET MAUI OtpInput (SfOtpInput) control and more.
platform: maui-toolkit
control: OtpInput
documentation: ug
---

# Event in .NET MAUI OtpInput (SfOtpInput)

## ValueChanged event

The OTP Input component triggers the `ValueChanged` event when the value of each OTP Input is changed. The `OtpInputValueChangedEventArgs` passed as an event argument provides the details of the each value is changed.

{% tabs %}
{% highlight xaml %}

<otp:SfOtpInput ValueChanged="OnValueChanged"></otp:SfOtpInput>

{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput();
otpInput.ValueChanged += OnValueChanged;

{% endhighlight %}
{% endtabs %}

{% highlight c# %}

private void OnValueChanged(object sender, OtpInputValueChangedEventArgs e)
{
    // Codes that need to be executed once the input value is Changed.
}

{% endhighlight %}