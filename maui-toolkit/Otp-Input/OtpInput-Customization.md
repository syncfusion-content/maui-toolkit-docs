---
layout: post
title: Customization in .NET MAUI OTP Input (SfOtpInput) | Syncfusion®
description: Learn how to customize OTP input in Syncfusion® .NET MAUI OTP Input (SfOtpInput) control. Explore various options to enhance the appearance of your OTP input.
platform: maui-toolkit
control: OTP Input
documentation: ug
---

# Customization in .NET MAUI OTP Input (SfOtpInput)

An `OTP Input` consists of multiple elements that can be customized to enhance both its appearance and functionality.

## Placeholder

The placeholder for the OTP Input specifies the text that appears as a hint until the user enters a value.

Set the placeholder text using the `Placeholder` property. When a single character is assigned, each input field will show the same character.

{% tabs %}	
{% highlight xaml %}

<otpInput:SfOtpInput Placeholder="_" />
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Placeholder = "_"
};

{% endhighlight %}
{% endtabs %}

![Placeholder Image for OTP Input](images/placeholder.png)

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

![Placeholder Image for OTP Input](images/placeholderLength.png)

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

![PlaceholderColor Image for OTP Input](images/placeholderColor.png)

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

![Separator Image for OTP Input](images/separator.png)

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

![InputLength Image for OTP Input](images/length.png)

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

![InputBackground Image for OTP Input](images/inputBackground.png)

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

![Stroke Image for OTP Input](images/stroke.png)

## Text color

You can set the `TextColor` property to any color to customize the text appearance of the input fields. 

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

![TextColor Image for OTP Input](images/textColor.png)

## Mask character

You can set the `MaskCharacter` property to any character to define how the masked input is displayed, enhancing security by obscuring sensitive information. The `MaskCharacter` property applies only when `Type` is set to `Password.`

{% tabs %}
{% highlight xaml %}

<otpInput:SfOtpInput Type="Password" MaskCharacter="#" />

{% endhighlight %}
{% highlight C# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Type = OtpInputType.Password,
    MaskCharacter = '#'
};

{% endhighlight %}
{% endtabs %}

![MaskCharacter Image for OTP Input](images/maskCharacter.png)

## Input state

The `InputState` property in the OTP Input allows you to visually represent the validation status of the input fields.

### Success

The `InputState` can be set to `Success` to indicate that the input is correct. When the `InputState` is set to `Success,` the stroke of the OTP Input turns green.

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

![Success state Image for OTP Input](images/success.png)

### Warning

The `InputState` can be set to `Warning` to indicate a potential issue with the input, prompting the user to correct it. The stroke of the OTP Input turns orange-brown when `InputState` is set to `Warning.`

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

![Warning state Image for OTP Input](images/warning.png)

### Error

The `InputState` can be set to `Error` to indicate that the input is invalid or requires correction. The stroke of OTP Input turns red when `InputState` is set to `Error.`

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

![Error state Image for OTP Input](images/error.png)