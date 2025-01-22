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

## Input Background

You can specify the color of OtpInput using `InputBackground` property.

{% tabs %}
{% highlight xaml %}

<otpInput:SfOtpInput InputBackground="LightPink" StylingMode="Filled" />

{% endhighlight %}
{% highlight C# %}

SfOtpInput otpInput = new SfOtpInput()
{
    InputBackground = Colors.LightPink,
    StylingMode = OtpInputStyle.Filled
};

{% endhighlight %}
{% endtabs %}

N> The `InputBackground` property applies only when `StylingMode` is set to `Filled.`

## Stroke

You can specify the color of border in OtpInput using `Stroke` property.

{% tabs %}
{% highlight xaml %}

<otpInput:SfOtpInput Stroke="Blue" />

{% endhighlight %}
{% highlight C# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Stroke = Colors.Blue
};

{% endhighlight %}
{% endtabs %}

## TextColor

You can specify the color of text in OtpInput using `TextColor` property.

{% tabs %}
{% highlight xaml %}

<otpInput:SfOtpInput TextColor="Orange" />

{% endhighlight %}
{% highlight C# %}

SfOtpInput otpInput = new SfOtpInput()
{
    TextColor = Colors.Orange
};

{% endhighlight %}
{% endtabs %}

## MaskCharacter

You can specify the character used to mask the text in OtpInput using `MaskCharacter` property.

{% tabs %}
{% highlight xaml %}

<otpInput:SfOtpInput Type="Password" MaskCharacter="*" />

{% endhighlight %}
{% highlight C# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Type = OtpInputType.Password,
    MaskCharacter = '*'
};

{% endhighlight %}
{% endtabs %}

N> The `MaskCharacter` property applies only when `Type` is set to `Password.`

## InputState

The `InputState` property in the OtpInput allows you to visually represent the validation status of the input fields.

### Success

The `Stroke` of OtpInput turns green when `InputState` is set to `Success.`

{% tabs %}
{% highlight xaml %}

<otpInput:SfOtpInput InputState="Success" />

{% endhighlight %}
{% highlight C# %}

SfOtpInput otpInput = new SfOtpInput()
{
    InputState = OtpInputState.Success
};

{% endhighlight %}
{% endtabs %}

### Warning

The `Stroke` of OtpInput turns yellow when `InputState` is set to `Warning.`

{% tabs %}
{% highlight xaml %}

<otpInput:SfOtpInput InputState="Warning" />

{% endhighlight %}
{% highlight C# %}

SfOtpInput otpInput = new SfOtpInput()
{
    InputState = OtpInputState.Warning
};

{% endhighlight %}
{% endtabs %}

### Error

The `Stroke` of OtpInput turns red when `InputState` is set to `Error.`

{% tabs %}
{% highlight xaml %}

<otpInput:SfOtpInput InputState="Error" />

{% endhighlight %}
{% highlight C# %}

SfOtpInput otpInput = new SfOtpInput()
{
    InputState = OtpInputState.Error
};

{% endhighlight %}
{% endtabs %}