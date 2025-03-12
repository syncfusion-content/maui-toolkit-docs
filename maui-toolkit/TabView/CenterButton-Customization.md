---
layout: post
title: Center Button Customization in .NET MAUI Tab View (SfTabView) | Syncfusion®
description: Learn here all about center button Customization in .NET MAUI Tab View control and more.
platform: maui-toolkit
control: Tab View
documentation: ug
---

# Center Button Customization in .NET MAUI Tab View (SfTabView)

## Enable the center button 
This section explains how to create and customize The .NET MAUI [SfTabView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html) Center Button. Its appearance can be configured using `CenterButtonSettings,` and visibility can be controlled with `IsCenterButtonEnabled.`

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
We can customize the center button using the properties of CenterButtonSetting. The following properties are used to customize the view of center button `Background`, `Stroke`,`StrokeThickness`, `CornerRadius`, `TextColor`, `Height`, `Title`, `FontAttributes`, `FontFamily`, `FontSize`, `Width`, `ImageSource`, `ImageSize`, `DisplayMode`.


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
    var centerButton = tabView.CenterButtonSettings;        centerButton.Height = 80;
    centerButton.Width = 100;
    centerButton.Title = "Center Button";    
    centerButton.FontAttributes = FontAttributes.Bold;
    centerButton.TextColor = Colors.Green;        centerButton.DisplayMode = CenterButtonDisplayMode.ImageWithText;
    centerButton.ImageSource = "Home.png";        centerButton.ImageSize = 24;
    centerButton.FontFamily = "SevillanaRegular";        centerButton.CornerRadius = 10;
}
{% endhighlight %}

{% endtabs %}

## Center button tapped event

When center button is tapped, the `CenterButtonTapped` event occurs. Using this event we can set alert message.

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

![CenterButton .NET MAUI TabView](images/CenterButton.png)
