---
layout: post
title: Input Types in .NET MAUI OTP Input | Syncfusion®
description: Learn about the different input types available in the Syncfusion® .NET MAUI OTP Input (SfOtpInput) control for your cross-platform applications.
platform: maui-toolkit
control: SfOtpInput
documentation: UG
---

# Input Types in .NET MAUI OTP Input

## Types

This section explains the various types of the OTP (One-Time Password) Input component, their default behaviors, and suitable use cases.

### Number type

The [Type](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_Type) property can be set to [Number](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.OtpInputType.html#Syncfusion_Maui_Toolkit_OtpInput_OtpInputType_Number), prompting the input to handle numeric-only codes. This is ideal for scenarios demanding numeric OTPs. By default, the `Type` property is set to `Number`.

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

![Number](images/number.png)

### Text type

Set the [Type](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_Type) property to [Text](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.OtpInputType.html#Syncfusion_Maui_Toolkit_OtpInput_OtpInputType_Text) for inputs that may include both letters and numbers, making it suitable for alphanumeric OTPs.

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

![Text](images/text.png)

### Password type

Set the [Type](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_Type) property to [Password](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.OtpInputType.html#Syncfusion_Maui_Toolkit_OtpInput_OtpInputType_Password) to use this input type as a password in the OTP Input, hiding user input for privacy.

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

![Password](images/password.png)