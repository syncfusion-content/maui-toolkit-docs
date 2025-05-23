---
layout: post
title: Picker Text Dispaly Mode in .NET MAUI Picker Control | Syncfusion<sup>&reg;</sup>
description: Learn about the picker text display mode in Syncfusion<sup>&reg;</sup> .NET MAUI Picker (SfPicker) control and its basic features.
platform: maui
control: SfPicker
documentation: ug
---

# Picker Text display mode in .NET MAUI Picker (SfPicker)

The picker text display mode is specified in the picker property enumeration, which is used to display the picker items based on the modes. It offers four modes: [Default](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.PickerTextDisplayMode.html#Syncfusion_Maui_Toolkit_Picker_PickerTextDisplayMode_Default), [Fade](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.PickerTextDisplayMode.html#Syncfusion_Maui_Toolkit_Picker_PickerTextDisplayMode_Fade), [Shrink](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.PickerTextDisplayMode.html#Syncfusion_Maui_Toolkit_Picker_PickerTextDisplayMode_Shrink) and [FadeAndShrink](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.PickerTextDisplayMode.html#Syncfusion_Maui_Toolkit_Picker_PickerTextDisplayMode_FadeAndShrink). The default picker text display mode is [Default](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.PickerTextDisplayMode.html#Syncfusion_Maui_Toolkit_Picker_PickerTextDisplayMode_Default) in the [SfPicker](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfPicker.html).

## Fade Mode

The fade mode in the picker gradually decreases the visibility of unselected items relative to the selected item. This effect is achieved by setting the [TextDisplayMode](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.PickerBase.html#Syncfusion_Maui_Toolkit_Picker_PickerBase_TextDisplayMode) property to [Fade](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.PickerTextDisplayMode.html#Syncfusion_Maui_Toolkit_Picker_PickerTextDisplayMode_Fade) in [SfPicker](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfPicker.html).

{% tabs %}

{% highlight xaml tabtitle="XAML" hl_lines="2" %}

<picker:SfPicker x:Name="picker"
                 TextDisplayMode="Fade"/>

{% endhighlight %}

{% highlight c# tabtitle="C#" hl_lines="3" %}

SfPicker picker = new SfPicker()
{
    TextDisplayMode = PickerTextDisplayMode.Fade
};

this.Content = picker;

{% endhighlight %}

{% endtabs %}

![Fade mode in .NET MAUI Picker.](images/text-display-mode/picker-fade.png)

## Shrink Mode

The shrink mode is used to display the font size of picker items decreased from the selected item by setting the [TextDisplayMode](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.PickerBase.html#Syncfusion_Maui_Toolkit_Picker_PickerBase_TextDisplayMode) property to [Shrink](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.PickerTextDisplayMode.html#Syncfusion_Maui_Toolkit_Picker_PickerTextDisplayMode_Shrink) in [SfPicker](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfPicker.html).

{% tabs %}

{% highlight xaml tabtitle="XAML" hl_lines="2" %}

<picker:SfPicker x:Name="picker"
                 TextDisplayMode="Shrink"/>

{% endhighlight %}

{% highlight c# tabtitle="C#" hl_lines="3" %}

SfPicker picker = new SfPicker()
{
    TextDisplayMode = PickerTextDisplayMode.Shrink
};

this.Content = picker;

{% endhighlight %}

{% endtabs %}

![Shrink mode in .NET MAUI Date picker.](images/text-display-mode/picker-shrink.png)

## FadeAndShrink Mode

The fade and shrink mode are used to decrease the opacity and font size of picker items from the selected item by setting the [TextDisplayMode](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.PickerBase.html#Syncfusion_Maui_Toolkit_Picker_PickerBase_TextDisplayMode) property to [FadeAndShrink](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.PickerTextDisplayMode.html#Syncfusion_Maui_Toolkit_Picker_PickerTextDisplayMode_FadeAndShrink) in [SfPicker](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfPicker.html).

{% tabs %}

{% highlight xaml tabtitle="XAML" hl_lines="2" %}

<picker:SfPicker x:Name="picker"
                 TextDisplayMode="FadeAndShrink"/>

{% endhighlight %}

{% highlight c# tabtitle="C#" hl_lines="3" %}

SfPicker picker = new SfPicker()
{
    TextDisplayMode = PickerTextDisplayMode.FadeAndShrink
};

this.Content = picker;

{% endhighlight %}

{% endtabs %}

![Fade and Shrink mode in .NET MAUI Date picker.](images/text-display-mode/picker-fade-shrink.png)