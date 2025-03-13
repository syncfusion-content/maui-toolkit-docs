---
layout: post
title: Styling Modes in .NET MAUI OTP Input | Syncfusion®
description: Learn here about styling modes in Syncfusion® .NET MAUI OTP Input (SfOtpInput) control in your cross-platform applications.
platform: maui-toolkit
control: OTP Input
documentation: ug
---

# Styling Modes in OTP Input

Styling modes specify the visual style variants for input fields in the OTP Input component, allowing you to customize appearances according to your application's design needs.


## Outline mode

You can customize the appearance of input fields with a border around them by setting the `StylingMode` property to `Outlined.`  This is the default styling mode for the OTP Input component.

{% tabs %}	
{% highlight xaml %}

<otpInput:SfOtpInput StylingMode="Outlined" />
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    StylingMode = OtpInputStyle.Outlined
};

{% endhighlight %}
{% endtabs %}

![Outlined Image for OTP Input](images/outlined.png)

## Filled mode

You can customize the appearance of input fields by filling them with color by setting the `StylingMode` property to `Filled.` 

{% tabs %}	
{% highlight xaml %}

<otpInput:SfOtpInput StylingMode="Filled" />
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    StylingMode = OtpInputStyle.Filled
};

{% endhighlight %}
{% endtabs %}

![Filled Image for OTP Input](images/filled.png)

## Underline mode

You can customize the appearance of input fields with an underline by setting the `StylingMode` property to `Underlined.`

{% tabs %}	
{% highlight xaml %}

<otpInput:SfOtpInput StylingMode="Underlined" />
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    StylingMode = OtpInputStyle.Underlined
};

{% endhighlight %}
{% endtabs %}

![Underlined Image for OTP Input](images/underlined.png)