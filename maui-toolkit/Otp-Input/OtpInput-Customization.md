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

You can specify the number of input fields to match the desired OTP code length by using the `Length` property. The default value is `4`.

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

You can disable the OtpInput component by using the `IsEnabled` property. By default, this property's value is set to `True.`

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

## Input background

You can set the `InputBackground` property to any color to customize the appearance of the input fields. The `InputBackground` property applies only when `StylingMode` is set to `Filled.`

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

## Stroke

You can set the `Stroke` property to any color to customize the border appearance of the input fields. 

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

## Text color

You can set the `TextColor` property to any color to customize the text appearance of the input fields. 

{% tabs %}
{% highlight xaml %}

<otpInput:SfOtpInput TextColor="Orange" Value="1234" Type="Number" />

{% endhighlight %}
{% highlight C# %}

SfOtpInput otpInput = new SfOtpInput()
{
    TextColor = Colors.Orange,
    Value = "1234",
    Type = OtpInputType.Number
};

{% endhighlight %}
{% endtabs %}

## Mask character

You can set the `MaskCharacter` property to any character to define how the masked input is displayed, enhancing security by obscuring sensitive information. The `MaskCharacter` property applies only when `Type` is set to `Password.`

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

## Input state

The `InputState` property in the OtpInput allows you to visually represent the validation status of the input fields.

### Success

The `InputState` can be set to `Success` to indicate that the input is correct. When the `InputState` is set to `Success,` the stroke of the OtpInput turns green.

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

The `InputState` can be set to `Warning` to indicate a potential issue with the input, prompting the user to correct it. The stroke of the OtpInput turns orange-brown when `InputState` is set to `Warning.`

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

The `InputState` can be set to `Error` to indicate that the input is invalid or requires correction. The stroke of OtpInput turns red when `InputState` is set to `Error.`

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