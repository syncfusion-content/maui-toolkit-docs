---
layout: post
title: Customization in .NET MAUI Button control | Syncfusion<sup>®</sup>
description: Learn here all about Customization support in Syncfusion<sup>®</sup> .NET MAUI Button (SfButton) control and more.
platform: maui
control: SfButton
documentation: ug
---

# Customization in .NET MAUI Button (SfButton)

The [.NET MAUI Button](https://www.syncfusion.com/maui-controls/maui-button) control supports to customize the border color, image width, corner radius, background color, and more. The button control can be customized using the following properties:

## Text Customization

The text inside the button can be customized by its text color, font size, font attributes, font family and text alignment.

### TextColor

The [`TextColor`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ButtonBase.html#Syncfusion_Maui_Toolkit_ButtonBase_TextColor) property is used to customize the color of text in [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html).

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" WidthRequest="200" Text="Button" TextColor = "White" CornerRadius="10">
</buttons:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.TextColor = Colors.White;
button.CornerRadius= 10;

{% endhighlight %}
{% endtabs %}

![SfButton with text color](images/customization-images/Button_textcolor.png)

### FontSize

The [`FontSize`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ButtonBase.html#Syncfusion_Maui_Toolkit_ButtonBase_FontSize) property is used to customize the size of text in [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html).

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" WidthRequest="150" HeightRequest="40" Text="Button" FontSize = "18" CornerRadius="10">
</buttons:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.FontSize = 18;
button.CornerRadius= 10;

{% endhighlight %}
{% endtabs %}

![SfButton with font size](images/customization-images/Button_fontsize.png)

### FontAttributes

The [`FontAttributes`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ButtonBase.html#Syncfusion_Maui_Toolkit_ButtonBase_FontAttributes) property is used to customize the font style of text in [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html).

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" Text="Button" WidthRequest="150" HeightRequest="40"
                  FontAttributes = "Italic" CornerRadius="10">
</buttons:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.FontAttributes = FontAttributes.Italic;
button.CornerRadius= 10;

{% endhighlight %}
{% endtabs %}

![SfButton with fontattributes](images/customization-images/Button_fontattributes.png)

### FontFamily

The [`FontFamily`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ButtonBase.html#Syncfusion_Maui_Toolkit_ButtonBase_FontFamily) property is used to customize the font family of text in [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html).

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" Text="Button" WidthRequest="150" HeightRequest="40"
                  FontFamily = "Samantha-Demo" CornerRadius="10">
</buttons:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.FontFamily = "Samantha-Demo";
button.CornerRadius= 10;

{% endhighlight %}
{% endtabs %}

![SfButton with fontfamily](images/customization-images/Button_fontfamily.jpg)

### TextAlignment

The [`HorizontalTextAlignment`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ButtonBase.html#Syncfusion_Maui_Toolkit_ButtonBase_HorizontalTextAlignment) and [`VerticalTextAlignment`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ButtonBase.html#Syncfusion_Maui_Toolkit_ButtonBase_VerticalTextAlignment) properties are used to customize the alignment of text in [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html).

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" WidthRequest="150" HeightRequest="40"
                  Text="Button" HorizontalTextAlignment="Center" VerticalTextAlignment="Center">
</buttons:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.HorizontalTextAlignment = TextAlignment.Center;
button.VerticalTextAlignment = TextAlignment.Center;

{% endhighlight %}
{% endtabs %}

### Text Transform

Users can now customize the [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html) text casing using the [`TextTransform`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html#Syncfusion_Maui_Toolkit_Buttons_SfButton_TextTransform) property. They can easily switch between uppercase, lowercase, none, or default casing.

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" 
                 Text="Submit" 
                 TextTransform="Uppercase" 
                 WidthRequest="150" 
                 HeightRequest="40"
                 HorizontalTextAlignment="Center" 
                 VerticalTextAlignment="Center">
</buttons:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Submit";
button.TextTransform = "Uppercase";
button.HorizontalTextAlignment = TextAlignment.Center;
button.VerticalTextAlignment = TextAlignment.Center;

{% endhighlight %}
{% endtabs %}

![.NET MAUI Button Text Transform](images/customization-images/Button_texttransform.png)

## LineBreakMode
The [`LineBreakMode`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html#Syncfusion_Maui_Toolkit_Buttons_SfButton_LineBreakMode) allows you to wrap or truncate the text. The default value of this property is `NoWrap`. The following other options are available in LineBreakMode:

 * `NoWrap` - Avoids the text wrap. 
 * `WordWrap` - Wraps the text by words.
 * `CharacterWrap` - Wraps the text by character.
 * `HeadTruncation` - Truncates the text at the start.
 * `MiddleTruncation` - Truncates the text at the center.
 * `TailTruncation` - Truncates the text at the end.

 {% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" Text="Add Items To Cart" WidthRequest="150" HeightRequest="40"
                  LineBreakMode="MiddleTruncation" ImageSource="Cart.png">
</buttons:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Add Items To Cart";
button.LineBreakMode = LineBreakMode.MiddleTruncation;
button.ImageSource="Cart.png";

{% endhighlight %}
{% endtabs %}

![SfButton with LineBreakMode](images/customization-images/Button_linebreakmode.png)

## Background Customization

The background of the button can be customized by its background color, border color, border width and corner radius.

### Background Color

The [`Background`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html#Syncfusion_Maui_Toolkit_Buttons_SfButton_Background) property is used to customize the background color of [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html).

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" Text="Button" WidthRequest="150" HeightRequest="40" 
                  Background = "DeepSkyBlue" CornerRadius="10">
</buttons:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.Background = Colors.DeepSkyBlue;
button.CornerRadius= 10;

{% endhighlight %}
{% endtabs %}

N> When defining the background colors of the SfButton control, always use the `Background` property instead of the `BackgroundColor` property.

![SfButton with background color](images/customization-images/Button_backgroundcolor.png)

### Stroke

The [`Stroke`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ButtonBase.html#Syncfusion_Maui_Toolkit_ButtonBase_Stroke) property is used to customize the color of border in [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html).

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" Text="Button" Stroke="Red" CornerRadius="10">
</buttons:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.Stroke = Colors.Red;
button.CornerRadius= 10;

{% endhighlight %}
{% endtabs %}

![SfButton with stroke](images/customization-images/Button_border.png)

### StrokeThickness

The [`StrokeThickness`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html#Syncfusion_Maui_Toolkit_Buttons_SfButton_StrokeThickness) property is used to customize the thickness of border in [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html). 

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" Text="Button" Stroke="Red" StrokeThickness="6" CornerRadius="10">
</buttons:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.StrokeThickness = 6;
button.Stroke = Colors.Red;
button.CornerRadius= 10;

{% endhighlight %}
{% endtabs %}

![SfButton with strokethickness](images/customization-images/Button_borderthickness.png)

### CornerRadius

The [`CornerRadius`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html#Syncfusion_Maui_Toolkit_Buttons_SfButton_CornerRadius) property is used to customize the rounded edges in [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html) as demonstrated in the following code sample.

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" Text="Button" CornerRadius="20" WidthRequest="150" HeightRequest="40">
</buttons:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.CornerRadius = 20;

{% endhighlight %}
{% endtabs %}

![SfButton with cornerradius](images/customization-images/Button_cornerradius.png)

## Image Customization

The Image can be customized by its ShowIcon, ImageSource, ImageSize and ImageAlignment.

### ShowIcon

You can enable the Icon image using the [`ShowIcon`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ButtonBase.html#Syncfusion_Maui_Toolkit_ButtonBase_ShowIcon) property to know whether any image appears to the [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html).

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" Text="Button" ImageSource="Heart.png" ShowIcon="True" WidthRequest="150" HeightRequest="40">
</buttons:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.ImageSource = "Heart.png";
button.ShowIcon = True;

{% endhighlight %}
{% endtabs %}

### ImageSource

The [`ImageSource`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ButtonBase.html#Syncfusion_Maui_Toolkit_ButtonBase_ImageSource) property is used to customize the icon image of [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html) by adding a custom image.

N> Enable the [`ShowIcon`]() property to enable the [`ImageSource`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ButtonBase.html#Syncfusion_Maui_Toolkit_ButtonBase_ImageSource) property. 

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" Text="Button" ImageSource="Heart.png" ShowIcon="True" CornerRadius="2" WidthRequest="150" HeightRequest="40">
</buttons:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.ImageSource = "Heart.png";
button.ShowIcon = True;
button.CornerRadius= 2;

{% endhighlight %}
{% endtabs %}

![SfButton with image with content](images/customization-images/Button_icon.png)

### ImageSize

The [`ImageSize`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ButtonBase.html#Syncfusion_Maui_Toolkit_ButtonBase_ImageSize) property is used to customize the width of icon image in [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html).

N> Enable the `ShowIcon` property to enable the `ImageSize` property.

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" Text="Button" ImageSource="Heart.png" ShowIcon="True" ImageSize="50" WidthRequest="150" HeightRequest="40">
</buttons:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.ImageSource = "Heart.png";
button.ShowIcon = true;
button.ImageSize= 50;

{% endhighlight %}
{% endtabs %}

### ImageAlignment 

The [`ImageAlignment`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ButtonBase.html#Syncfusion_Maui_Toolkit_ButtonBase_ImageAlignment) property is used to customize the alignment of icon image in [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html). The following options are available in [`ImageAlignment`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ButtonBase.html#Syncfusion_Maui_Toolkit_ButtonBase_ImageAlignment):

* [`Start`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.Alignment.html#Syncfusion_Maui_Toolkit_Chips_Alignment_Start) - Places the image at the left most of [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html).
* [`End`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.Alignment.html#Syncfusion_Maui_Toolkit_Chips_Alignment_End) - Places the image at the right most of [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html).
* [`Top`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.Alignment.html#Syncfusion_Maui_Toolkit_Chips_Alignment_Top) - Places the image at the top of the text.
* [`Bottom`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.Alignment.html#Syncfusion_Maui_Toolkit_Chips_Alignment_Bottom) - Places the image at the bottom of the text.
* '[`Default`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.Alignment.html#Syncfusion_Maui_Toolkit_Chips_Alignment_Default) - By default the image places at the center of the text.
* [`Left`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.Alignment.html#Syncfusion_Maui_Toolkit_Chips_Alignment_Left) - Although the flow direction has been applied, it always places the image in the left part of [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html). For example, in the direction of the RTL flow, the image setting will move to the right. Use [`Left`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.Alignment.html#Syncfusion_Maui_Toolkit_Chips_Alignment_Left) alignment to show this in the same left position.
* [`Right`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.Alignment.html#Syncfusion_Maui_Toolkit_Chips_Alignment_Right) - Although flow direction has been applied, the image is always located in the right part of [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html). For example, in the direction of the RTL flow, the image setting will move to the left. But use [`Right`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.Alignment.html#Syncfusion_Maui_Toolkit_Chips_Alignment_Right) alignment to show this in the same right position.

N> Enable the `ShowIcon` property to enable the `ImageAlignment` property.

**End image alignment in `SfButton`**

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" 
                Text="Shopping"
                WidthRequest="150"
                HeightRequest="40"
                TextColor="Black"
                HorizontalOptions="Center"
                ImageSource="add_to_card.png"
                ShowIcon="True"
                ImageSize="25"
                Stroke="Black"
                CornerRadius="10"
                Background="White"
                ImageAlignment="End"/>

{% endhighlight %}

{% highlight c# %}
SfButton button = new SfButton()
{
    Text = "Shopping",
    TextColor = Colors.Black,
    HorizontalOptions = LayoutOptions.Center,
    ImageSource = "add_to_card.png",
    ShowIcon = true,
    ImageSize = 25,
    Stroke = Colors.Black,
    CornerRadius= 10,
    Background = Colors.White,
    ImageAlignment = Alignment.End
};

{% endhighlight %}
{% endtabs %}

![SfButton with image with icon image with end alignment](images/customization-images/Button_imagealignment_end.png)

**Start image alignment in `SfButton`**

{% tabs %}
{% highlight xaml %}

<buttons:SfButton  x:Name="button"
                    Text="Shopping"
                    WidthRequest="150"
                    HeightRequest="40"
                    TextColor="Black"
                    HorizontalOptions="Center"
                    ImageSource="add_to_card.png"
                    ShowIcon="True" 
                    ImageSize="25"
                    Stroke="Black"
                    CornerRadius="10"
                    Background="White"
                    ImageAlignment="Start"/>

{% endhighlight %}

{% highlight c# %}
SfButton button = new SfButton()
{
    Text = "Shopping",
    TextColor = Colors.Black,
    HorizontalOptions = LayoutOptions.Center,
    ImageSource = "add_to_card.png",
    ShowIcon = true,
    ImageSize = 25,
    Stroke = Colors.Black,
    CornerRadius= 10,
    Background = Colors.White,
    ImageAlignment = Alignment.Start
};


{% endhighlight %}
{% endtabs %}

![SfButton with image with icon image with start alignment](images/customization-images/Button_imagealignment_start.png)

**Top image alignment in `SfButton`**

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" 
                Text="Shopping"
                WidthRequest="150"
                HeightRequest="40"
                TextColor="Black"
                HorizontalOptions="Center"
                ImageSource="add_to_card.png"
                ShowIcon="True" 
                ImageSize="25"
                Stroke="Black"
                CornerRadius="10"
                Background="White"
                ImageAlignment="Top"/>

{% endhighlight %}

{% highlight c# %}
SfButton button = new SfButton()
{
    Text = "Shopping",
    TextColor = Colors.Black,
    HorizontalOptions = LayoutOptions.Center,
    ImageSource = "add_to_card.png",
    ShowIcon = true,
    ImageSize= 25,
    Stroke = Colors.Black,
    CornerRadius= 10,
    Background = Colors.White,
    ImageAlignment = Alignment.Top
};


{% endhighlight %}
{% endtabs %}

![SfButton with image with icon image with top alignment](images/customization-images/Button_imagealignment_top.png)

**Bottom image alignment in `SfButton`**

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" 
                Text="Shopping"
                WidthRequest="150"
                HeightRequest="40"
                TextColor="Black"
                HorizontalOptions="Center"
                ImageSource="add_to_card.png"
                ShowIcon="True" 
                ImageSize="25"
                Stroke="Black"
                CornerRadius="10"
                Background="White"
                ImageAlignment="Bottom"/>

{% endhighlight %}

{% highlight c# %}
SfButton button = new SfButton()
{
    Text = "Shopping",
    TextColor = Colors.Black,
    HorizontalOptions = LayoutOptions.Center,
    ImageSource = "add_to_card.png",
    ShowIcon = true,
    ImageSize = 25,
    Stroke = Colors.Black,
    CornerRadius= 10,
    Background = Colors.White,
    ImageAlignment = Alignment.Bottom
};


{% endhighlight %}
{% endtabs %}

![SfButton with image with icon image with top alignment](images/customization-images/Button_imagealignment_bottom.png)

**Default image alignment in `SfButton`**

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" 
                Text="Shopping"
                WidthRequest="150"
                HeightRequest="40"
                TextColor="Black"
                HorizontalOptions="Center"
                ImageSource="add_to_card.png"
                ShowIcon="True" 
                ImageSize="25"
                Stroke="Black"
                CornerRadius="10"
                Background="White"
                ImageAlignment="Default"/>

{% endhighlight %}

{% highlight c# %}
SfButton button = new SfButton()
{
    Text = "Shopping",
    TextColor = Colors.Black,
    HorizontalOptions = LayoutOptions.Center,
    ImageSource = "add_to_card.png",
    ShowIcon = true,
    ImageSize = 25,
    Stroke = Colors.Black,
    CornerRadius= 10,
    Background = Colors.White,
    ImageAlignment = Alignment.Center
};


{% endhighlight %}
{% endtabs %}

![SfButton with image with icon image with default alignment](images/customization-images/Button_imagealignment_default.png)

**Left image alignment in `SfButton`**

In RTL flow direction, image alignment with [`Start`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.Alignment.html#Syncfusion_Maui_Core_Alignment_Start) will change its direction of placing image to the right. To keep that in same left position, set [`Left`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.Alignment.html#Syncfusion_Maui_Core_Alignment_Left) alignment as shown in the following code sample.

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" 
                Text="Shopping"
                TextColor="Black"
                HorizontalOptions="Center"
                ImageSource="add_to_card.png"
                ShowIcon="True" 
                ImageSize="25"
                Stroke="Black"
                CornerRadius="10"
                Background="White"
                ImageAlignment="Left"/>

{% endhighlight %}

{% highlight c# %}

SfButton button = new SfButton()
{
    Text = "Shopping",
    TextColor = Colors.Black,
    HorizontalOptions = LayoutOptions.Center,
    ImageSource = "add_to_card.png",
    ShowIcon = true,
    ImageSize = 25,
    Stroke= Colors.Black,
    CornerRadius= 10,
    Background = Colors.White,
    ImageAlignment = Alignment.Left
};

{% endhighlight %}
{% endtabs %}

![SfButton with image with icon image with left alignment](images/customization-images/Button_imagealignment_left.png)

**Right image alignment in `SfButton`**

In RTL flow direction, image alignment with [`End`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.Alignment.html#Syncfusion_Maui_Core_Alignment_End) will change its direction of placing image to the left. To keep that in same right position, set [`Right`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.Alignment.html#Syncfusion_Maui_Core_Alignment_Right) alignment as shown in the following code sample.

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button"
                Text="Shopping"
                TextColor="Black"
                HorizontalOptions="Center"
                ImageSource="add_to_card.png"
                ShowIcon="True" 
                ImageSize="25"
                Stroke="Black"
                CornerRadius="10"
                Background="White"
                ImageAlignment="Right"/>

{% endhighlight %}

{% highlight c# %}
SfButton button = new SfButton()
{
    Text = "Shopping",
    TextColor = Colors.Black,
    HorizontalOptions = LayoutOptions.Center,
    ImageSource = "add_to_card.png",
    ShowIcon = true,
    ImageSize = 25,
    Stroke= Colors.Black,
    CornerRadius= 10,
    Background = Colors.White,
    ImageAlignment = Alignment.Right
};


{% endhighlight %}
{% endtabs %}

![SfButton with image with icon image with right alignment](images/customization-images/Button_imagealignment_right.png)

## BackgroundImageSource

The [BackgroundImageSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ButtonBase.html#Syncfusion_Maui_Toolkit_ButtonBase_BackgroundImageSource) property is used to set background image for the Button.

{% tabs %}

{% highlight xaml %}

<ContentPage.Content>
    <StackLayout Margin="8,8,8,8" >
        <buttons:SfButton WidthRequest="100"
                            HorizontalOptions="Center"
                            VerticalOptions="Center"
                            BackgroundImageSource="lion.png">
        </buttons:SfButton>
    </StackLayout>
</ContentPage.Content>

{% endhighlight %}

{% highlight c# %}

using Syncfusion.Maui.Toolkit.Buttons;
StackLayout stackLayout = new StackLayout();
SfButton button = new SfButton();
button.WidthRequest = 100;
button.HorizontalOptions = LayoutOptions.Center;
button.VerticalOptions = LayoutOptions.Center;
button.BackgroundImageSource="lion.png";
stackLayout.Children.Add(button);
this.Content = stackLayout;
        
{% endhighlight %}

{% endtabs %}

![SfButton with image property](images/getting-started/net-maui-button-with-background-image.png)

## BackgroundImageAspect

The [BackgroundImageAspect](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html#Syncfusion_Maui_Toolkit_Buttons_SfButton_BackgroundImageAspect) property is used to customize the aspect ratio of background image for the Button.

{% tabs %}

{% highlight xaml %}

<ContentPage.Content>
    <StackLayout Margin="8,8,8,8" >
        <buttons:SfButton WidthRequest="100"
                            HorizontalOptions="Center"
                            VerticalOptions="Center"
                            BackgroundImageSource="lion.png"
                            BackgroundImageAspect="Fill">
        </buttons:SfButton>
    </StackLayout>
</ContentPage.Content>

{% endhighlight %}

{% highlight c# %}

using Syncfusion.Maui.Toolkit.Buttons;
StackLayout stackLayout = new StackLayout();
SfButton button = new SfButton();
button.WidthRequest = 100;
button.HorizontalOptions = LayoutOptions.Center;
button.VerticalOptions = LayoutOptions.Center;
button.BackgroundImageSource = "lion.png";
button.BackgroundImageAspect = Aspect.Fill;
stackLayout.Children.Add(button);
this.Content = stackLayout;
        
{% endhighlight %}

{% endtabs %}

![SfButton with image property](images/getting-started/net-maui-button-with-background-image.png)

## EnableRippleEffect

The [EnableRippleEffect](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ButtonBase.html#Syncfusion_Maui_Toolkit_ButtonBase_EnableRippleEffect) property is used to control the presence of the ripple effects.

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="button" Text="Button" EnableRippleEffect="True" />

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.EnableRippleEffect = True;

{% endhighlight %}
{% endtabs %}

![.NET MAUI RippleEffect support](images/customization-images/Button_EnableRippleEffect.gif)

## Command

The [`Command`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ButtonBase.html#Syncfusion_Maui_Toolkit_ButtonBase_Command)  property is used to associate a command with an instance of [`SfButton`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html). This property is most often set with MVVM pattern to bind callbacks back into the ViewModel.

N> Default value is [`null`].

{% tabs %}
{% highlight xaml %}

 <ContentPage.BindingContext>
    <local:CommandDemoViewModel />
 </ContentPage.BindingContext>

<buttons:SfButton x:Name="button" 
                Text="Button" 
                Background="{Binding Background}" 
                Command="{Binding ButtonCommand}">
</buttons:SfButton>

{% endhighlight %}
{% highlight c# %}

// ViewModel

public class CommandDemoViewModel : INotifyPropertyChanged
{

    private Color _background = Color.Accent;

    public Color Background
    {
        get { return _background; }
        set
        {
            _background = value;
            NotifyPropertyChanged();
        }
    }

    private void NotifyPropertyChanged([CallerMemberName] String propertyName = "")
    {
        PropertyChanged?.Invoke(this, new PropertyChangedEventArgs(propertyName));
    }

    public event PropertyChangedEventHandler PropertyChanged;

    public CommandDemoViewModel()
    {
        SetBackgroundColor();
        this.Background=Color.Accent;
    }

    private void SetBackgroundColor()
    {
	    //do whatever you want to do here
        this.Background = this.Background == Color.DeepSkyBlue ? Color.Accent : Color.DeepSkyBlue;
    }

    public ICommand ButtonCommand => new Command(SetBackgroundColor);

}

{% endhighlight %}
{% endtabs %}
