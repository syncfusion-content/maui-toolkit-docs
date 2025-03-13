---
layout: post
title: Center button customization in .NET MAUI Tab View | Syncfusion®
description: Learn here all about the center button customization in the Syncfusion® .NET MAUI Tab View(SfTabView) control.
platform: maui-toolkit
control: Tab View
documentation: ug
---

# Center Button Customization in .NET MAUI Tab View (SfTabView)

This section explains how to enable and customize the center button in .NET MAUI [SfTabView.](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html)

## Enable the center button 

You can enable the center button in Tab View by setting the `IsCenterButtonEnabled` property to `True.`

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

You can customize the center button using the properties of `CenterButtonSettings`. The following properties are used to customize the view of center button `Background`, `Stroke`,`StrokeThickness`, `CornerRadius`, `TextColor`, `Height`, `Title`, `FontAttributes`, `FontFamily`, `FontSize`, `Width`, `ImageSource`, `ImageSize`, and `DisplayMode`.

{% tabs %}

{% highlight xaml %}

<tabView:SfTabView.CenterButtonSettings>
     <tabView:CenterButtonSettings Title="Home" 
                              Height="70" 
                              Width="80"
                              Background="White" 
                              Stroke="HotPink" 
                              StrokeThickness="3" 
                              CornerRadius="10" 
                              TextColor="Green" 
                              ImageSource="image.png" 
                              ImageSize="24" 
                              DisplayMode="ImageWithText" 
                              FontFamily="SevillanaRegular" 
                              FontAttributes="Bold" 
                              FontSize="16" />
</tabView:SfTabView.CenterButtonSettings>

{% endhighlight %}

{% highlight C# %}

public MainPage()
{
    InitializeComponent();
    SfTabView tabView = new SfTabView();
    CenterButtonSettings centerButtonSettings = new CenterButtonSettings()
    {
        Height = 80,
        Width = 100,
        Title = "Center Button",
        FontAttributes = FontAttributes.Bold,
        TextColor = Colors.Green,
        DisplayMode = CenterButtonDisplayMode.ImageWithText,
        ImageSource = "Home.png",
        ImageSize = 24,
        FontFamily = "SevillanaRegular",
        CornerRadius = new CornerRadius(10),
    };

    tabView.CenterButtonSettings = centerButtonSettings;
}
{% endhighlight %}

{% endtabs %}

## Center button tapped event

When the center button is tapped, the `CenterButtonTapped` event occurs. Using this event we can set alert messages.

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
