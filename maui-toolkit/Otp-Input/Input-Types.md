---
layout: post
title: Swiping in .NET MAUI OtpInput | Syncfusion®
description: Learn here about input types in Syncfusion® .NET MAUI OtpInput (SfOtpInput) control in your cross-platform applications.
platform: maui-toolkit
control: OtpInput
documentation: ug
---

# Input Types in Blazor OTP Input component

## Types

This section explains the the various types of OTP (One-Time Password) input component, explaining their default behaviors and appropriate use cases.

### Number type

You can set the `Type` property to `Number` to use this input type as number. This is ideal for OTP input scenarios with numeric-only codes. By default `Type` property is `Number`.

{% tabs %}	
{% highlight xaml %}

<otp:SfOtpInput Value="1234" Type="Number"></otp:SfOtpInput>
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Value = "1234",
    Type = OtpInputType.Number
};

{% endhighlight %}
{% endtabs %}

### Text type

You can set the `Type` property to `Text` to use this input type as text. This is suitable when the OTP input need to include both letters and numbers.

{% tabs %}	
{% highlight xaml %}

<otp:SfOtpInput Value="e3c7" Type="Text"></otp:SfOtpInput>
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Value = "1234",
    Type = OtpInputType.Text
};

{% endhighlight %}
{% endtabs %}

### Password type

You can set the `Type` property to `Password` to use this input type as password in the OTP Input.

{% tabs %}	
{% highlight xaml %}

<otp:SfOtpInput Value="e3c7" Type="Password"></otp:SfOtpInput>
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Value = "1234",
    Type = OtpInputType.Password
};

{% endhighlight %}
{% endtabs %}

## Value

You can specify the value of OTP Input by using the `Value` property.

{% tabs %}	
{% highlight xaml %}

<otp:SfOtpInput Value="e3c7"></otp:SfOtpInput>
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Value = "1234"
};

{% endhighlight %}
{% endtabs %}