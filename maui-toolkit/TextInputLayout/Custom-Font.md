---
layout: post
title: Font Customization  in .NET MAUI TextInputLayout control | Syncfusion
description: Learn here all about Font Customization  support in Syncfusion .NET MAUI Text Input Layout (SfTextInputLayout) control and more.
platform: maui-toolkit
control: SfTextInputLayout
documentation: ug
keywords: .net maui text input layout, syncfusion text input layout, text input layout maui, .net maui error label, .net maui hint label.
---

# Font Customization  in .NET MAUI Text Input Layout (SfTextInputLayout)

You can customize the appearance (size, attributes, and family) of the font by setting the [FontFamily](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.LabelStyle.html#Syncfusion_Maui_Toolkit_TextInputLayout_LabelStyle_FontFamily), [FontSize](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.LabelStyle.html#Syncfusion_Maui_Toolkit_TextInputLayout_LabelStyle_FontSize), and [FontAttributes](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.LabelStyle.html#Syncfusion_Maui_Toolkit_TextInputLayout_LabelStyle_FontAttributes) properties of the [LabelStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.LabelStyle.html) property.

Refer to this [documentation](https://learn.microsoft.com/en-us/dotnet/maui/user-interface/fonts) to configure the custom fonts in the .NET MAUI.

## Hint

You can customize the font of the `Hint` label by setting the FontFamily, FontSize, and FontAttributes, properties of [HintLabelStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.SfTextInputLayout.html#Syncfusion_Maui_Toolkit_TextInputLayout_SfTextInputLayout_HintLabelStyle) in the [SfTextInputLayout](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.SfTextInputLayout.html).

{% tabs %} 

{% highlight xaml %}

<inputLayout:SfTextInputLayout Hint="Name"
                               ContainerType="Outlined"
                               HelperText="Enter your name">
    <Entry />
    <inputLayout:SfTextInputLayout.HintLabelStyle>
        <inputLayout:LabelStyle FontSize="16" FontFamily="Lobster-Regular"/>
    </inputLayout:SfTextInputLayout.HintLabelStyle>
</inputLayout:SfTextInputLayout> 

{% endhighlight %}

{% highlight C# %} 

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Name";
inputLayout.ContainerType = ContainerType.Outlined;
inputLayout.HelperText = "Enter your name";
inputLayout.HintLabelStyle = new LabelStyle() { FontFamily = "Lobster-Regular", FontSize = 16};
inputLayout.Content = new Entry(); 

{% endhighlight %}

{% endtabs %}

![Hint label style in .NET MAUI TextInputLayout.](images/CustomFont/HintLabelStyle.png)

## Helper text

You can customize the font of the `HelperText` label by setting the FontFamily, FontSize, and FontAttributes properties of [HelperLabelStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.SfTextInputLayout.html#Syncfusion_Maui_Toolkit_TextInputLayout_SfTextInputLayout_HelperLabelStyle) in the [SfTextInputLayout](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.SfTextInputLayout.html).

{% tabs %} 

{% highlight xaml %}

<inputLayout:SfTextInputLayout Hint="Name"
                               ContainerType="Outlined"
                               CharMaxLength="3"
                               HelperText="Enter your name">
    <Entry />
    <inputLayout:SfTextInputLayout.HelperLabelStyle>
        <inputLayout:LabelStyle FontSize="12" FontFamily="Lobster-Regular"/>
    </inputLayout:SfTextInputLayout.HelperLabelStyle>
</inputLayout:SfTextInputLayout> 

{% endhighlight %}

{% highlight C# %} 

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Name";
inputLayout.ContainerType = ContainerType.Outlined;
inputLayout.HelperText = "Enter your name";
inputLayout.HelperLabelStyle = new LabelStyle() { FontFamily = "Lobster-Regular", FontSize = 12};
inputLayout.Content = new Entry(); 

{% endhighlight %}

{% endtabs %}

![Helper label style in .NET MAUI TextInputLayout.](images/CustomFont/HelperLabelStyle.png)

## Error text

You can customize the font of `ErrorText` label by setting the FontFamily, FontSize, and FontAttributes properties of [ErrorLabelStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.SfTextInputLayout.html#Syncfusion_Maui_Toolkit_TextInputLayout_SfTextInputLayout_ErrorLabelStyle) in [SfTextInputLayout](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.SfTextInputLayout.html).

{% tabs %} 

{% highlight xaml %}

<inputLayout:SfTextInputLayout
                   Hint="Name"
                   ContainerType="Outlined"
                   HasError="True"
                   ErrorText="Enter valid name">
    <Entry />
    <inputLayout:SfTextInputLayout.ErrorLabelStyle>
        <inputLayout:LabelStyle FontSize="12" FontFamily="Lobster-Regular"/>
    </inputLayout:SfTextInputLayout.ErrorLabelStyle>
</inputLayout:SfTextInputLayout> 

{% endhighlight %}

{% highlight C# %} 

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Name";
inputLayout.ContainerType = ContainerType.Outlined;
inputLayout.HasError = true;
inputLayout.ErrorText = "Enter valid name";
inputLayout.ErrorLabelStyle = new LabelStyle() { FontFamily = "Lobster-Regular", FontSize = 12};
inputLayout.Content = new Entry(); 

{% endhighlight %}

{% endtabs %}

![Error label style in .NET MAUI TextInputLayout.](images/CustomFont/ErrorLabelStyle.png)