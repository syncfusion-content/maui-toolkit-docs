---
layout: post
title: Customization in .NET MAUI OtpInput (SfOtpInput) | Syncfusion®
description: Learn how to customize otp input in Syncfusion® .NET MAUI OtpInput (SfOtpInput). Explore the options to enhance your otp input appearance.
platform: maui-toolkit
control: OtpInput
documentation: ug
---

# Customization in .NET MAUI OtpInput (SfOtpInput)

A `OtpInput` consists of several elements that can be customized to enhance its appearance and functionality.

## Placeholder in OtpInput component

The placeholder in OtpInput specifies the text that is shown as a hint or placeholder until the user enters a value in the input field. It acts as a guidance for the users regarding the expected input format or purpose of the input field.

You can set the placeholder text by using the `Placeholder` property. Additionally, when providing a single character as the placeholder value all input fields within the OTP Input component will display the same character.

{% tabs %}	
{% highlight xaml %}

<otp:SfOtpInput Placeholder="x"></otp:SfOtpInput>
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Placeholder = "x"
};

{% endhighlight %}
{% endtabs %}

When a placeholder with multiple placeholder characters is provided each input field will display characters from the placeholder string in sequence based on the available OtpInput length.

{% tabs %}	
{% highlight xaml %}

<otp:SfOtpInput Placeholder="wxyz"></otp:SfOtpInput>
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Placeholder = "wxyz"
};

{% endhighlight %}
{% endtabs %}

## PlaceholderColor in OtpInput component

The placeholder text color can be changed by using the `PlaceholderColor` property. The default value of PlaceholderColor property is `Colors.Gray`.

{% tabs %}
{% highlight xaml %}

<otp:SfOtpInput Placeholder="x" PlaceholderColor="Red"></otp:SfOtpInput>

{% endhighlight %}
{% highlight C# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Placeholder = "x",
    PlaceholderColor = Colors.Red
};

{% endhighlight %}
{% endtabs %}

## Separator in OtpInput component

The separator in OtpInput specifies the character or symbol used to separate each input field in the OtpInput component. This separator is displayed between each input field to visually distinguish between each inputs. You can set the separator character by using the `Separator` property.

{% tabs %}
{% highlight xaml %}

<otp:SfOtpInput Separator="/"></otp:SfOtpInput>

{% endhighlight %}
{% highlight C# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Separator = "/"
};

{% endhighlight %}
{% endtabs %}

## Appearance in OtpInput component

You can also customize the appearance of OtpInput component.

### Setting input length

You can specify the length of OTP by using the `Length` property. The default value is `4`.

{% tabs %}
{% highlight xaml %}

<otp:SfOtpInput Length="6"></otp:SfOtpInput>

{% endhighlight %}
{% highlight C# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Length = 6
};

{% endhighlight %}
{% endtabs %}

### Disable inputs

You can disable the OtpInput component by using the `IsEnabled` property. By default the value is `true`.

{% tabs %}
{% highlight xaml %}

<otp:SfOtpInput IsEnabled="False"></otp:SfOtpInput>

{% endhighlight %}
{% highlight C# %}

SfOtpInput otpInput = new SfOtpInput()
{
    IsEnabled = false
};

{% endhighlight %}
{% endtabs %}