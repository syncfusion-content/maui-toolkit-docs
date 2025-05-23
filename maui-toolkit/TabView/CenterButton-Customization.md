---
layout: post
title: Center Button Customization in .NET MAUI Tab View | Syncfusion®
description: Learn here all about the center button customization in the Syncfusion® .NET MAUI Tab View(SfTabView) control.
platform: maui-toolkit
control: SfTabView
documentation: UG
---

# Center Button Customization in .NET MAUI Tab View (SfTabView)

This section explains how to enable and customize the center button in .NET MAUI [SfTabView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html).

## Enable the center button 

You can enable the center button in Tab View by setting the [IsCenterButtonEnabled](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_IsCenterButtonEnabled) property to `True.`

{% tabs %}

{% highlight xaml %}

<tabView:SfTabView x:Name="tabView"
                   IsCenterButtonEnabled="True" />

{% endhighlight %}

{% highlight C# %}

public MainPage()
{
    InitializeComponent();
    SfTabView tabView = new SfTabView();
    tabView.IsCenterButtonEnabled = true;
    this.Content = tabView;
}
{% endhighlight %}

{% endtabs %}

## Customize the center button

You can customize the center button using the properties of [CenterButtonSettings](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.CenterButtonSettings.html). The following properties are used to customize the view of the center button: [Background](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.CenterButtonSettings.html#Syncfusion_Maui_Toolkit_TabView_CenterButtonSettings_Background), [Stroke](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.CenterButtonSettings.html#Syncfusion_Maui_Toolkit_TabView_CenterButtonSettings_Stroke), [StrokeThickness](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.CenterButtonSettings.html#Syncfusion_Maui_Toolkit_TabView_CenterButtonSettings_StrokeThickness), [CornerRadius](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.CenterButtonSettings.html#Syncfusion_Maui_Toolkit_TabView_CenterButtonSettings_CornerRadius), [TextColor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.CenterButtonSettings.html#Syncfusion_Maui_Toolkit_TabView_CenterButtonSettings_TextColor), [Height](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.CenterButtonSettings.html#Syncfusion_Maui_Toolkit_TabView_CenterButtonSettings_Height), [Title](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.CenterButtonSettings.html#Syncfusion_Maui_Toolkit_TabView_CenterButtonSettings_Title), [FontAttributes](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.CenterButtonSettings.html#Syncfusion_Maui_Toolkit_TabView_CenterButtonSettings_FontAttributes), [FontFamily](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.CenterButtonSettings.html#Syncfusion_Maui_Toolkit_TabView_CenterButtonSettings_FontFamily), [FontSize](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.CenterButtonSettings.html#Syncfusion_Maui_Toolkit_TabView_CenterButtonSettings_FontSize), [Width](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.CenterButtonSettings.html#Syncfusion_Maui_Toolkit_TabView_CenterButtonSettings_Width), [ImageSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.CenterButtonSettings.html#Syncfusion_Maui_Toolkit_TabView_CenterButtonSettings_ImageSource), [ImageSize](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.CenterButtonSettings.html#Syncfusion_Maui_Toolkit_TabView_CenterButtonSettings_ImageSize), and [DisplayMode.](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.CenterButtonSettings.html#Syncfusion_Maui_Toolkit_TabView_CenterButtonSettings_DisplayMode)

{% tabs %}

{% highlight xaml %}

<tabView:SfTabView.CenterButtonSettings>
  <tabView:CenterButtonSettings Height="45"
                                Width="45"
                                CornerRadius="50"
                                Background="#6750A4"
                                ImageSize="25"
                                DisplayMode="Image"
                                ImageSource="image.png">
  </tabView:CenterButtonSettings>
</tabView:SfTabView.CenterButtonSettings>

{% endhighlight %}

{% highlight C# %}

public MainPage()
{
    InitializeComponent();
    SfTabView tabView = new SfTabView();
    CenterButtonSettings centerButtonSettings = new CenterButtonSettings()
    {
        Height = 45,
        Width = 45,
        DisplayMode = CenterButtonDisplayMode.Image,
        ImageSize = 25,
        Background = Color.FromArgb("#6750A4");
        CornerRadius = new CornerRadius(50),
        ImageSource = "image.png"        
    };

    tabView.CenterButtonSettings = centerButtonSettings;
}
{% endhighlight %}

{% endtabs %}

![Customize the center button](images/CenterButton-Customizaton.jpg) 

## CenterButtonTapped event

When the center button is tapped, the [CenterButtonTapped](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_CenterButtonTapped) event occurs. Using this event, we can set alert messages.

{% tabs %}

{% highlight xaml %}

<tabView:SfTabView CenterButtonTapped="OnCenterButtonTapped">
</tabView:SfTabView>

{% endhighlight %}

{% highlight C# %}

public MainPage()
{
    InitializeComponent();
    tabView.CenterButtonTapped += OnCenterButtonTapped;
}

private void OnCenterButtonTapped(object sender, EventArgs e)
{
    DisplayAlert("Message", "CenterButton Clicked", "Ok");
}

{% endhighlight %}

{% endtabs %}
