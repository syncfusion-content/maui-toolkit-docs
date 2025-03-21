---
layout: post
title: Styles in .NET MAUI Popup control | Syncfusion
description: Learn here all about Styles support in the Syncfusion .NET MAUI Popup (SfPopup) control, its elements, and more.
platform: maui-toolkit
control: SfPopup
documentation: ug
--- 

# Styles in .NET MAUI Popup (SfPopup)

The [SfPopup](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.SfPopup.html) applies style to all of its elements by using the [PopupStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html) property.

## Styling popup header

The [SfPopup](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.SfPopup.html) allows customizing the header appearance using the following properties.

<table>
<tr>
<th> Property </th>
<th> Description </th>
</tr>
<tr>
<td> {{'[HeaderBackground](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_HeaderBackground)'| markdownify }} </td>
<td> Gets or sets the background color for the header.</td>
</tr>
<tr>
<td> {{'[HeaderFontAttribute](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_HeaderFontAttribute)'| markdownify }} </td>
<td> Gets or sets the font attribute for the header title.</td>
</tr>
<tr>
<td> {{'[HeaderFontFamily](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_HeaderFontFamily)'| markdownify }} </td>
<td> Gets or sets the font style for the header title.</td>
</tr>
<tr>
<td> {{'[HeaderFontSize](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_HeaderFontSize)'| markdownify }} </td>
<td> Gets or sets the font size for the header title.</td>
</tr>
<tr>
<td> {{'[HeaderTextAlignment](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_HeaderTextAlignment)'| markdownify }} </td>
<td> Gets or sets the text alignment for the header.</td>
</tr>
<tr>
<td> {{'[HeaderTextColor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_HeaderTextColor)'| markdownify }} </td>
<td> Gets or sets the text color to be applied for the header title.</td>
</tr>
</table>

Refer to the following code example for customizing the header elements.

{% tabs %}
{% highlight xaml hl_lines="3 4 5 6 7 8" %}
<sfPopup:SfPopup x:Name="popup" >
    <sfPopup:SfPopup.PopupStyle>
        <sfPopup:PopupStyle HeaderBackground="DimGray"
                            HeaderFontAttribute="Bold"
                            HeaderFontFamily="Roboto-Medium"
                            HeaderFontSize="25"
                            HeaderTextAlignment="Center"
                            HeaderTextColor="White"/>
    </sfPopup:SfPopup.PopupStyle>
</sfPopup:SfPopup>
{% endhighlight %}
{% highlight c# hl_lines="8 9 10 11 12 13" %}
public partial class MainPage : ContentPage
{
    SfPopup popup;
    public MainPage()
    {
        InitializeComponent();
        popup = new SfPopup();
        popup.PopupStyle.HeaderBackground = Color.FromRgb(105,105,105);
        popup.PopupStyle.HeaderFontAttribute = FontAttributes.Bold;
        popup.PopupStyle.HeaderFontFamily = "Roboto-Medium";
        popup.PopupStyle.HeaderFontSize = 25;
        popup.PopupStyle.HeaderTextAlignment = TextAlignment.Center;
        popup.PopupStyle.HeaderTextColor = Color.White;
    }
}
{% endhighlight %}
{% endtabs %}

![Displaying a .NET MAUI Popup with header customization](Images/styles/maui-popup-with-header-customization.png)

## Styling popup footer

The SfPopup allows customizing the footer appearance using the following properties.

<table>
<tr>
<th> Property </th>
<th> Description </th>
</tr>
<tr>
<td> {{'[FooterBackground](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_FooterBackground)'| markdownify }} </td>
<td> Gets or sets the background color for the footer.</td>
</tr>
<tr>
<td> {{'[AcceptButtonBackground](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_AcceptButtonBackground)'| markdownify }} </td>
<td> Gets or sets the background color for the Accept button in the footer.</td>
</tr>
<tr>
<td> {{'[AcceptButtonTextColor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_AcceptButtonTextColor)'| markdownify }} </td>
<td> Gets or sets the foreground color for the Accept button in the footer.</td>
</tr>
<tr>
<td> {{'[DeclineButtonBackground](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_DeclineButtonBackground)'| markdownify }} </td>
<td> Gets or sets the background color for the Decline button in the footer.</td>
</tr>
<tr>
<td> {{'[DeclineButtonTextColor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_DeclineButtonTextColor)'| markdownify }} </td>
<td> Gets or sets the foreground color for the Decline button in the footer.</td>
</tr>
<tr>
<td> {{'[FooterButtonCornerRadius](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_FooterButtonCornerRadius)'| markdownify }} </td>
<td> Gets or sets the corner radius of the accept and decline buttons in the footer. The default value is 20.</td>
</tr>
</table>

Refer to the following code example for customizing the footer elements.

{% tabs %}
{% highlight xaml hl_lines="3 4 5 6 7 8" %}
<sfPopup:SfPopup x:Name="popup" AppearanceMode="TwoButton" ShowFooter="True" >
    <sfPopup:SfPopup.PopupStyle>
        <sfPopup:PopupStyle FooterBackground="LightGray"
                            AcceptButtonBackground ="DimGray"
                            AcceptButtonTextColor="White"
                            DeclineButtonBackground="DimGray"
                            DeclineButtonTextColor="White"
                            FooterButtonCornerRadius ="0,20,20,0"/>
    </sfPopup:SfPopup.PopupStyle>
</sfPopup:SfPopup>
{% endhighlight %}
{% highlight c# hl_lines="14 15 16 17 18 19" %}
public partial class MainPage : ContentPage
{
    SfPopup popup;
    public MainPage()
    {
        InitializeComponent();
        popup = new SfPopup();

        // Setting the AppearanceMode as TwoButton
        popup.ShowFooter = true;
        popup.AppearanceMode = Syncfusion.Maui.Popup.PopupButtonAppearanceMode.TwoButton;

        // Footer customization
        popup.PopupStyle.FooterBackground = Color.LightGray;
        popup.PopupStyle.AcceptButtonBackground = Color.FromRgb(105, 105, 105);
        popup.PopupStyle.AcceptButtonTextColor = Color.White;
        popup.PopupStyle.DeclineButtonBackground = Color.FromRgb(105, 105, 105);
        popup.PopupStyle.DeclineButtonTextColor = Color.White;
        popup.PopupStyle.FooterButtonCornerRadius = new CornerRadius(0,20,20,0);
    }
}
{% endhighlight %}
{% endtabs %}

![Displaying a .NET MAUI Popup with footer customization](Images/styles/maui-popup-with-footer-customization.png)

## Styling popup message

The `SfPopup` allows customizing the message appearance using the following properties.

<table>
<tr>
<th> Property </th>
<th> Description </th>
</tr>
<tr>
<td> {{'`MessageBackground`'| markdownify }} </td>
<td> Gets or sets the background color of content.</td>
</tr>
<tr>
<td> {{'`MessageFontAttribute`'| markdownify }} </td>
<td> Gets or sets the font attribute to be applied for the content.</td>
</tr>
<tr>
<td> {{'`MessageFontFamily`'| markdownify }} </td>
<td> Gets or sets the font style to be applied for the content.</td>
</tr>
<tr>
<td> {{'`MessageFontSize`'| markdownify }} </td>
<td> Gets or sets the font size of the content.</td>
</tr>
<tr>
<td> {{'`MessageTextAlignment`'| markdownify }} </td>
<td> Gets or sets the text alignment of the content.</td>
</tr>
<tr>
<td> {{'`MessageTextColor`'| markdownify }} </td>
<td> Gets or sets the foreground color of content.</td>
</tr>
</table>

Refer to the following code example for customizing the message elements.

{% tabs %}
{% highlight xaml hl_lines="3 4 5 6 7" %}
<sfPopup:SfPopup x:Name="popup">
    <sfPopup:SfPopup.PopupStyle>
        <sfPopup:PopupStyle MessageBackground="#4F6750A4"
                            MessageFontAttribute="Bold"
                            MessageFontFamily="Roboto-Medium"
                            MessageFontSize="18"
                            MessageTextAlignment="Center"
                            MessageTextColor="Gray"/>
    </sfPopup:SfPopup.PopupStyle>
</sfPopup:SfPopup>
{% endhighlight %}
{% highlight c# hl_lines="8 9 10 11 12 13" %}
public partial class MainPage : ContentPage
{
    SfPopup popup;
    public MainPage()
    {
        InitializeComponent();
        popup = new SfPopup();
        popup.PopupStyle.MessageBackground = Color.FromArgb("#4F6750A4");
        popup.PopupStyle.MessageFontAttribute = FontAttributes.Bold;
        popup.PopupStyle.MessageFontFamily = "Roboto-Medium";
        popup.PopupStyle.MessageFontSize = 18;
        popup.PopupStyle.MessageTextAlignment = TextAlignment.Center;
        popup.PopupStyle.MessageTextColor = Colors.Gray;
    }
}
{% endhighlight %}
{% endtabs %}

![Displaying a .NET MAUI Popup with message customization](Images/styles/maui-popup-with-message-customization.png)

## Stroke customization

The `SfPopup` allows customizing the stroke appearance using the following properties.

<table>
<tr>
<th> Property </th>
<th> Description </th>
</tr>
<tr>
<td> {{'[Stroke](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_Stroke)'| markdownify }} </td>
<td> Gets or sets the stroke color for the PopupView.</td>
</tr>
<tr>
<td> {{'[StrokeThickness](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_StrokeThickness)'| markdownify }} </td>
<td> Gets or sets the stroke thickness for the PopupView.</td>
</tr>
<tr>
<td> {{'[CornerRadius](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_CornerRadius)'| markdownify }} </td>
<td> Gets or sets the corner radius for the PopupView.</td>
</tr>
</table>

N> On Android 33 and above, it is possible to set different corner radii for each corner using the `CornerRadius` class. However, on versions below Android 33, a corner radius will be applied if the same value is provided for all corners. The corner radius may not be applied if different values are provided for each corner.

Refer to the following code example for customizing the stroke elements.

{% tabs %}
{% highlight xaml hl_lines="3 4 5" %}
<sfPopup:SfPopup x:Name="popup">
    <sfPopup:SfPopup.PopupStyle>
        <sfPopup:PopupStyle Stroke="LightBlue"
                            StrokeThickness="10"
                            CornerRadius="5" />
    </sfPopup:SfPopup.PopupStyle>
<sfPopup:SfPopup>
{% endhighlight %}
{% highlight c# hl_lines="8 9 10" %}
public partial class MainPage : ContentPage
{
    SfPopup popup;
    public MainPage()
    {
        InitializeComponent();
        popup = new SfPopup();
        popup.PopupStyle.Stroke = Colors.LightBlue;
        popup.PopupStyle.StrokeThickness = 10;
        popup.PopupStyle.CornerRadius = 5;
    }
}
{% endhighlight %}
{% endtabs %}

![Displaying a .NET MAUI Popup with stroke customization](Images/styles/maui-popup-with-stroke-customization.png)

## popup background

The `SfPopup` allows to customize the background color of the popup view using the [PopupBackground](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_PopupBackground) property.

{% tabs %}
{% highlight xaml hl_lines="3" %}
    <sfPopup:SfPopup x:Name="popup">
        <sfPopup:SfPopup.PopupStyle>
            <sfPopup:PopupStyle PopupBackground="#C3B0D6" />
        </sfPopup:SfPopup.PopupStyle>
    </sfPopup:SfPopup>
{% endhighlight %}
{% highlight c# hl_lines="8" %}
public partial class MainPage : ContentPage
{
    SfPopup popup;
    public MainPage()
    {
        InitializeComponent();
        popup = new SfPopup();
        popup.PopupStyle.PopupBackground = Color.FromArgb("C3B0D6");
    }
}
{% endhighlight %}
{% endtabs %}

![Displaying a .NET MAUI Popup with the PopupView Background](Images/styles/maui-popup-with-popupview-background.png)

## Styling overlay background

The SfPopup allows to customize the background color of overlay using the [OverlayColor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_OverlayColor) property.

{% tabs %}
{% highlight xaml hl_lines="3" %}
        <sfPopup:SfPopup x:Name="popup">
            <sfPopup:SfPopup.PopupStyle>
                    <sfPopup:PopupStyle OverlayColor="LightPink" />
            </sfPopup:Sfpopup.PopupStyle>
        </sfPopup:SfPopup>
{% endhighlight %}
{% highlight c# hl_lines="8" %}
public partial class MainPage : ContentPage
{
    SfPopup popup;
    public MainPage()
    {
        InitializeComponent();
        popup = new SfPopup();
        popup.PopupStyle.OverlayColor = Colors.LightPink;
    }
}
{% endhighlight %}
{% endtabs %}

![Displaying a .NET MAUI Popup with overlay customization](Images/styles/maui-popup-with-overlay-customization.png)

### Set overlay opacity

The `SfPopup` allows you adjust the opacity of the overlay color by setting the color value as rgba in hexadecimal value.

{% tabs %}
{% highlight xaml hl_lines="3" %}
        <sfPopup:SfPopup x:Name="popup">
            <sfPopup:SfPopup.PopupStyle>
                    <sfPopup:PopupStyle OverlayColor="#30FF0000" />
            </sfPopup:Sfpopup.PopupStyle>
        </sfPopup:SfPopup>
{% endhighlight %}
{% highlight c# hl_lines="8" %}
public partial class MainPage : ContentPage
{
    SfPopup popup;
    public MainPage()
    {
        InitializeComponent();
        popup = new SfPopup();
        popup.PopupStyle.OverlayColor = Color.FromArgb("#30FF0000");
    }
}
{% endhighlight %}
{% endtabs %}

### Blurred background

The `SfPopup` allows blurring of the background using the [OverlayMode](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.SfPopup.html#Syncfusion_Maui_Toolkit_Popup_SfPopup_OverlayMode) and [BlurIntensity](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_BlurIntensity) properties respectively.

{% tabs %}
{% highlight xaml hl_lines="13 16" %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="GettingStarted.MainPage"
             xmlns:sfPopup="clr-namespace:Syncfusion.Maui.Toolkit.Popup;assembly=Syncfusion.Maui.Toolkit">
    <StackLayout x:Name="layout">
        <Image Source="Blurred_Background.png" Aspect="Fill" >
             <Image.GestureRecognizers>
                 <TapGestureRecognizer Tapped="TapGestureRecognizer_Tapped"/>
             </Image.GestureRecognizers>
        </Image>
        <sfPopup:SfPopup x:Name="popup" 
                        OverlayMode="Blur" 
                        ShowCloseButton="True">
            <sfPopup:SfPopup.PopupStyle>
                <sfPopup:PopupStyle BlurIntensity="ExtraDark" />
            </sfPopup:SfPopup.PopupStyle>
        </sfPopup:SfPopup>
   </StackLayout>
</ContentPage>
{% endhighlight %}
{% highlight c# hl_lines="12 13" %}
using Syncfusion.Maui.Toolkit.Popup;
namespace GettingStarted
{
    public partial class MainPage : ContentPage
    {
        SfPopup popup;
        public MainPage()
        {
            InitializeComponent();
            popup = new SfPopup();
            popup.ShowCloseButton = true;
            popup.OverlayMode = Syncfusion.Maui.Popup.PopupOverlayMode.Blur;
            popup.PopupStyle.BlurIntensity = Syncfusion.Maui.Popup.PopupBlurIntensity.ExtraDark;
            var layout = new StackLayout();
            var image = new Image() { Source = "Blurred_Background.png", Aspect = Aspect.Fill };
            TapGestureRecognizer tapGestureRecognizer = new TapGestureRecognizer();
            tapGestureRecognizer.Tapped += TapGestureRecognizer_Tapped;
            image.GestureRecognizers.Add(tapGestureRecognizer);
            layout.Children.Add(image);
            Content = layout;
        }

        private void TapGestureRecognizer_Tapped(object sender, System.EventArgs e)
        {
            popup.Show();
        }
    }
}
{% endhighlight %}
{% endtabs %}

![Displaying a .NET MAUI Popup with blur overlay](Images/styles/maui-popup-with-blurred-background.png)

### Set custom blur intensity

The `SfPopup` allows customization of the blur effect by setting the [BlurIntensity](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_BlurIntensity) property to [Custom](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupBlurIntensity.html#Syncfusion_Maui_Toolkit_Popup_PopupBlurIntensity_Custom) and the [BlurRadius](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Popup.PopupStyle.html#Syncfusion_Maui_Toolkit_Popup_PopupStyle_BlurRadius), which adjusts the blur effect according to the specified value.

{% tabs %}
{% highlight xaml hl_lines="13 16" %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="GettingStarted.MainPage"
             xmlns:sfPopup="clr-namespace:Syncfusion.Maui.Toolkit.Popup;assembly=Syncfusion.Maui.Toolkit">
    <StackLayout x:Name="layout">
        <Image Source="Blurred_Background.png" Aspect="Fill" >
             <Image.GestureRecognizers>
                 <TapGestureRecognizer Tapped="TapGestureRecognizer_Tapped"/>
             </Image.GestureRecognizers>
        </Image>
        <sfPopup:SfPopup x:Name="popup" 
                        OverlayMode="Blur" 
                        ShowCloseButton="True">
            <sfPopup:SfPopup.PopupStyle>
                <sfPopup:PopupStyle BlurIntensity="Custom"
                                    BlurRadius="3" />
            </sfPopup:SfPopup.PopupStyle>
        </sfPopup:SfPopup>
   </StackLayout>
</ContentPage>
{% endhighlight %}
{% highlight c# hl_lines="12 13" %}
using Syncfusion.Maui.Toolkit.Popup;
namespace GettingStarted
{
    public partial class MainPage : ContentPage
    {
        SfPopup popup;
        public MainPage()
        {
            InitializeComponent();
            popup = new SfPopup();
            popup.OverlayMode = OverlayMode.Blur;
            popup.PopupStyle.BlurIntensity = Syncfusion.Maui.Popup.PopupBlurIntensity.Custom;
            popup.PopupStyle.BlurRadius = 3;
            var layout = new StackLayout();
            var image = new Image() { Source = "Blurred_Background.png", Aspect = Aspect.Fill };
            TapGestureRecognizer tapGestureRecognizer = new TapGestureRecognizer();
            tapGestureRecognizer.Tapped += TapGestureRecognizer_Tapped;
            image.GestureRecognizers.Add(tapGestureRecognizer);
            layout.Children.Add(image);
            Content = layout;
        }

        private void TapGestureRecognizer_Tapped(object sender, System.EventArgs e)
        {
            popup.Show();
        }
    }
}
{% endhighlight %}
{% endtabs %}

![Displaying a .NET MAUI Popup with blur radius](Images/styles/maui-popup-with-blur-radius.png)

### Change the close button icon

You can change the close button icon of the `SfPopup`, please find the code example of the same below.

{% tabs %}
{% highlight xaml hl_lines="16" %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:local="clr-namespace:PopupDemo"
             xmlns:sfPopup="clr-namespace:Syncfusion.Maui.Toolkit.Popup;assembly=Syncfusion.Maui.Toolkit"
             x:Class="PopupDemo.MainPage">
    <StackLayout>
        <Button x:Name="clickToShowPopup"
                Text="ClickToShowPopup"
                VerticalOptions="Start"
                HorizontalOptions="Center"
                Clicked="ClickToShowPopup_Clicked" />
        <sfPopup:SfPopup x:Name="popup"
                         ShowCloseButton="True">
            <sfPopup:SfPopup.PopupStyle>
                <sfPopup:PopupStyle CloseButtonIcon="closeicon.png" />
            </sfPopup:SfPopup.PopupStyle>
        </sfPopup:SfPopup>
    </StackLayout>
</ContentPage>
{% endhighlight %}
{% highlight c# hl_lines="8" %}
public partial class MainPage : ContentPage
{
    SfPopup popup;
    public MainPage()
    {
        InitializeComponent();
        popup = new SfPopup();
        popup.PopupStyle.ShowCloseButtonIcon = "closeicon.png";
    }
}
{% endhighlight %}
{% endtabs %}

![Displaying a .NET MAUI Popup with close button icon](Images/styles/maui-popup-with-close-button-icon.png)

### Set Shadow

The `SfPopup` allows you to add a shadow effect to the popup view. Refer to the code example below for reference.

{% tabs %}
{% highlight xaml hl_lines="15" %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:local="clr-namespace:PopupDemo"
             xmlns:sfPopup="clr-namespace:Syncfusion.Maui.Toolkit.Popup;assembly=Syncfusion.Maui.Toolkit"
             x:Class="PopupDemo.MainPage">
    <StackLayout>
        <Button x:Name="clickToShowPopup"
                Text="ClickToShowPopup"
                VerticalOptions="Start"
                HorizontalOptions="Center"
                Clicked="ClickToShowPopup_Clicked" />
        <sfPopup:SfPopup x:Name="popup">
            <sfPopup:SfPopup.PopupStyle>
                <sfPopup:PopupStyle HasShadow="True" />
            </sfPopup:SfPopup.PopupStyle>
        </sfPopup:SfPopup>
    </StackLayout>
</ContentPage>
{% endhighlight %}
{% highlight c# hl_lines="8" %}
public partial class MainPage : ContentPage
{
    SfPopup popup;
    public MainPage()
    {
        InitializeComponent();
        popup = new SfPopup();
        popup.PopupStyle.HasShadow = true;
    }
}
{% endhighlight %}
{% endtabs %}

![Displaying a .NET MAUI Popup with shadow](Images/styles/maui-popup-with-shadow.png)

## Limitations

The `SfPopup` control does not support dynamic style changes while it is open. Any modifications to style properties must be applied before the popup is displayed. If you need to change style properties at runtime, you will need to close the popup, apply the changes, and then reopen it for the updates to take effect.