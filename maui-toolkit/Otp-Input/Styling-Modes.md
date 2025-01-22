---
layout: post
title: Swiping in .NET MAUI OtpInput | Syncfusion®
description: Learn here about styling modes in Syncfusion® .NET MAUI OtpInput (SfOtpInput) control in your cross-platform applications.
platform: maui-toolkit
control: OtpInput
documentation: ug
---

# Styling Modes in OTP Input component

Styling modes specify the style variants for the input fields in the OTP Input component. These modes allows you to customize the appearance of the OTP Input fields.

## Outline mode

You can use the outline style by setting the `StylingMode` property to `Outlined`. The default styling mode is `Outlined`.

{% tabs %}	
{% highlight xaml %}

<otp:SfOtpInput StylingMode="Outlined"></otp:SfOtpInput>
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    StylingMode = OtpInputStyle.Outlined
};

{% endhighlight %}
{% endtabs %}

## Filled mode

You can use the filled style by setting the `StylingMode` property to `Filled`.

{% tabs %}	
{% highlight xaml %}

<otp:SfOtpInput StylingMode="Filled"></otp:SfOtpInput>
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    StylingMode = OtpInputStyle.Filled
};

{% endhighlight %}
{% endtabs %}

## Underline mode

You can use the underline style by setting the `StylingMode` property to `Underlined`.

{% tabs %}	
{% highlight xaml %}

<otp:SfOtpInput StylingMode="Underlined"></otp:SfOtpInput>
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    StylingMode = OtpInputStyle.Underlined
};

{% endhighlight %}
{% endtabs %}