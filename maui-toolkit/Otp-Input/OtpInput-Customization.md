---
layout: post
title: Customization in .NET MAUI OTP Input (SfOtpInput) | Syncfusion®
description: Learn how to customize the Syncfusion® .NET MAUI OTP Input (SfOtpInput) control. Explore various options to enhance the appearance of your OTP Input.
platform: maui-toolkit
control: SfOtpInput
documentation: UG
---

# Customization in .NET MAUI OTP Input (SfOtpInput)

An [OTP Input](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html) consists of multiple customizable elements to enhance its appearance and functionality.

## Placeholder

The placeholder specifies the hint text that appears until the user enters a value

Use the [Placeholder](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_Placeholder) property to set this text. If a single character is assigned, each input field will display the same character.

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

![Placeholder](images/placeholder.png)

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

![Placeholder](images/placeholderLength.png)

### Placeholder color

The color of placeholder text can be changed using the [PlaceholderColor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_PlaceholderColor) property.

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

![PlaceholderColor](images/placeholderColor.png)

## Separator

The [Separator](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_Separator) property defines a character or symbol used to separate each input field, visually distinguishing inputs.

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

![Separator](images/separator.png)

## Setting input length

You can specify the number of input fields to match the desired OTP code length by using the [Length](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_Length) property. The default value is `4`.

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

![Input length](images/length.png)

## Input box size

You can specify the width and height of each input box by using the BoxWidth and BoxHeight properties. This customization allows you to tailor the OTP input appearance to match your application's design. The default values are 40 for both width and height.

{% tabs %} 
{% highlight xaml %} 

<otpInput:SfOtpInput BoxWidth="50" BoxHeight="50" /> 

{% endhighlight %} 
{% highlight C# %} 

SfOtpInput otpInput = new SfOtpInput() 
{ 
    BoxWidth = 50, 
    BoxHeight = 50 
}; 

{% endhighlight %} 
{% endtabs %}

## Input background

The [InputBackground](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_InputBackground) property customizes the appearance of input fields. This property works when [StylingMode](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_StylingMode) is set to [Filled](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.OtpInputStyle.html#Syncfusion_Maui_Toolkit_OtpInput_OtpInputStyle_Filled).

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

![InputBackground](images/inputBackground.png)

## Stroke

You can set the [Stroke](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_Stroke) property to any color to customize the border appearance of the input fields. 

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

![Stroke](images/stroke.png)

## Text color

You can set the [TextColor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_TextColor) property to any color to customize the text appearance of the input fields. 

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

![TextColor](images/textColor.png)

## Mask character

Set the [MaskCharacter](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_MaskCharacter) property to any character to define how the masked input is displayed, enhancing security by obscuring sensitive information. The `MaskCharacter` property applies only when [Type](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_Type) is set to [Password](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.OtpInputType.html#Syncfusion_Maui_Toolkit_OtpInput_OtpInputType_Password).

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

![MaskCharacter](images/maskCharacter.png)

## Input state

The [InputState](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_InputState) property visually represent the validation status of the input fields.

### Success

The [InputState](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_InputState) can be set to [Success](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.OtpInputState.html#Syncfusion_Maui_Toolkit_OtpInput_OtpInputState_Success) to indicate that the input is correct. When the `InputState` is set to `Success`, the stroke of the OTP Input turns green.

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

![Success state](images/success.png)

### Warning

The [InputState](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_InputState) can be set to [Warning](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.OtpInputState.html#Syncfusion_Maui_Toolkit_OtpInput_OtpInputState_Warning) to indicate a potential issue with the input, prompting the user to correct it. The stroke of the OTP Input turns orange-brown when `InputState` is set to `Warning`.

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

![Warning state](images/warning.png)

### Error

The [InputState](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_InputState) can be set to [Error](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.OtpInputState.html#Syncfusion_Maui_Toolkit_OtpInput_OtpInputState_Error) to indicate that the input is invalid or requires correction. The stroke of OTP Input turns red when `InputState` is set to `Error`.

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

![Error state](images/error.png)
