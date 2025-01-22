---
layout: post
title: Customization in .NET MAUI OtpInput (SfOtpInput) | Syncfusion®
description: Learn how to customize OTP input in Syncfusion® .NET MAUI OtpInput (SfOtpInput) control. Explore various options to enhance the appearance of your OTP input.
platform: maui-toolkit
control: OtpInput
documentation: ug
---

# Customization in .NET MAUI OtpInput (SfOtpInput)

An `OtpInput` consists of multiple elements that can be customized to enhance both its appearance and functionality.

## Placeholder

The placeholder for the OtpInput specifies the text that appears as a hint until the user enters a value.

Set the placeholder text using the `Placeholder` property. When a single character is assigned, each input field will show the same character.

{% tabs %}	
{% highlight xaml %}

<otpInput:SfOtpInput Placeholder="x" />
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Placeholder = "x"
};

{% endhighlight %}
{% endtabs %}

For placeholders with multiple characters, available input fields will sequentially display each character.

{% tabs %}	
{% highlight xaml %}

<otpInput:SfOtpInput Placeholder="wxyz" />
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Placeholder = "wxyz"
};

{% endhighlight %}
{% endtabs %}

### PlaceholderColor

The color of placeholder text can be changed using the `PlaceholderColor` property.

{% tabs %}
{% highlight xaml %}

<otpInput:SfOtpInput Placeholder="x" PlaceholderColor="Red" />

{% endhighlight %}
{% highlight C# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Placeholder = "x",
    PlaceholderColor = Colors.Red
};

{% endhighlight %}
{% endtabs %}

## Separator

The `Separator` property defines a character or symbol used to separate each input field, visually distinguishing inputs.

{% tabs %}
{% highlight xaml %}

<otpInput:SfOtpInput Separator="/" />

{% endhighlight %}
{% highlight C# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Separator = "/"
};

{% endhighlight %}
{% endtabs %}

## Setting input length

You can specify the length of OTP by using the `Length` property. The default value is `4`.

{% tabs %}
{% highlight xaml %}

<otpInput:SfOtpInput Length="6" />

{% endhighlight %}
{% highlight C# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Length = 6
};

{% endhighlight %}
{% endtabs %}

## Disable inputs

You can disable the OtpInput component by using the `IsEnabled` property. By default the value is `true`.

{% tabs %}
{% highlight xaml %}

<otpInput:SfOtpInput IsEnabled="False" />

{% endhighlight %}
{% highlight C# %}

SfOtpInput otpInput = new SfOtpInput()
{
    IsEnabled = false
};

{% endhighlight %}
{% endtabs %}