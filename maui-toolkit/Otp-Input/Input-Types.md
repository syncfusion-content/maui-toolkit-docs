---
layout: post
title: Input Types in .NET MAUI OTP Input | Syncfusion®
description: Learn here about input types in Syncfusion® .NET MAUI OTP Input (SfOtpInput) control in your cross-platform applications.
platform: maui-toolkit
control: OTP Input
documentation: ug
---

# Input Types in .NET MAUI OTP Input

## Types

This section explains the the various types of OTP (One-Time Password) input component, explaining their default behaviors and appropriate use cases.

### Number type

The `Type` property can be set to `Number`, prompting the input to handle numeric-only codes. This is ideal for scenarios demanding numeric OTPs. By default, the `Type` property is set to `Number`.

{% tabs %}	
{% highlight xaml %}

<otpInput:SfOtpInput Value="1234" Type="Number" />
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Value = "1234",
    Type = OtpInputType.Number
};

{% endhighlight %}
{% endtabs %}

![Number Image for OTP Input](images/number.png)

### Text type

You can set the `Type` property to `Text` for inputs that may include both letters and numbers, suitable for alphanumeric OTPs.

{% tabs %}	
{% highlight xaml %}

<otpInput:SfOtpInput Value="e3c7" Type="Text" />
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Value = "e3c7",
    Type = OtpInputType.Text
};

{% endhighlight %}
{% endtabs %}

![Text Image for OTP Input](images/text.png)

### Password type

You can set the `Type` property to `Password` to use this input type as password in the OTP Input.

{% tabs %}	
{% highlight xaml %}

<otpInput:SfOtpInput Value="e3c7" Type="Password" />
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Value = "e3c7",
    Type = OtpInputType.Password
};

{% endhighlight %}
{% endtabs %}

![Password Image for OTP Input](images/password.png)