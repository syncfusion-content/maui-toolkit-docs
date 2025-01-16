---
layout: post
title: Use UpDown Button in .NET MAUI NumericUpDown | Syncfusion
description: Learn here all about how to use UpDown Button (SpinButton) in Syncfusion .NET MAUI NumericUpDown (SfNumericUpDown) control and more.
platform: MAUI
control:  SfNumericUpDown
documentation: ug
---

# UpDown Button in .NET MAUI NumericUpDown

This section describes how to change the value in the [NumericUpDown](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html) control using keys, mouse scrolling, and the up-down button

## Increase or decrease value

You can increment or decrement the value in the `NumericUpDown` control using the **UpArrow**, **DownArrow**, **PageUp**, and **PageDown** keys. You can change the increment or decrement value when the Arrow keys are pressed using the [SmallChange](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html#Syncfusion_Maui_Toolkit_NumericUpDown_SfNumericUpDown_SmallChange) property and Page keys using the [LargeChange](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html#Syncfusion_Maui_Toolkit_NumericUpDown_SfNumericUpDown_Large) property. By default, the value of the `SmallChange` property is **1**, and the `LargeChange` property is **10**. 

N> The value in the `NumericUpDown` can also be changed by mouse scrolling. The mouse scrolling increases or decreases the value based on the `SmallChange` property.

{% tabs %}
{% highlight xaml %}

<editors:SfNumericUpDown WidthRequest="200" 
                         HorizontalOptions="Center"
                         VerticalOptions="Center" 
                         SmallChange="5"
                         Value="10"
                         LargeChange="10" />

{% endhighlight %}
{% highlight C# %}

SfNumericUpDown sfNumericUpDown= new SfNumericUpDown();
sfNumericUpDown.WidthRequest = 200;
sfNumericUpDown.Value=10;
sfNumericUpDown.SmallChange=5;
sfNumericUpDown.LargeChange=10;
sfNumericUpDown.HorizontalOptions = LayoutOptions.Center;
sfNumericUpDown.VerticalOptions = LayoutOptions.Center;

{% endhighlight %}
{% endtabs %}

![.NET MAUI NumericUpDown Placeholder Text](UpDownButton_images/valuechange-bykeys.gif)

## UpDown button placement

You can increase or decrease the value of the `NumericUpDown` control using the up-down button. By default, the value of the [UpDownPlacementMode](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html#Syncfusion_Maui_Toolkit_NumericUpDown_SfNumericUpDown_UpDownPlacementMode) property is **Inline** which positions the up-down buttons in a horizontal orientation. You can adjust the position of the up-down buttons by setting the `UpDownPlacementMode` property to **InlineVertical** for vertical orientation.

N> When using the up-down button, the `NumericUpDown` control value changes based on the value of the `SmallChange` property.

{% tabs %}
{% highlight XAML %}

<editors:SfNumericUpDown WidthRequest="200"
                         HorizontalOptions="Center"
                         VerticalOptions="Center"
                         Value="24";
                         UpDownPlacementMode="InlineVertical" />
                     
{% endhighlight %}
{% highlight c# %}

SfNumericUpDown sfNumericUpDown = new SfNumericUpDown();
sfNumericUpDown.WidthRequest = 200;
sfNumericUpDown.HorizontalOptions = LayoutOptions.Center;
sfNumericUpDown.VerticalOptions = LayoutOptions.Center;
sfNumericUpDown.Value=360;
sfNumericUpDown.UpDownPlacementMode = NumericUpDownUpDownPlacementMode.Inline;

{% endhighlight %}
{% endtabs %}

![UpDown Placement in .NET MAUI NumericUpDown](UpDownButton_images/UpDownButtonPlacement.png)

## UpDown button alignment

The UpDown button alignment in the `NumericUpDown` control can be customized using the [UpDownButtonAlignment](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html#Syncfusion_Maui_Toolkit_NumericUpDown_SfNumericUpDown_UpDownButtonAlignment) property. The buttons can be aligned to the following positions:

**Left**: Positions the buttons to the left of the control. 
**Right**: Positions the buttons to the right of the control. 
**Both**: Positions the buttons on both sides of the control. 

The default updown button alignment is **Right**.

{% tabs %}
{% highlight XAML %}

<editors:SfNumericUpDown WidthRequest="200"
                         HorizontalOptions="Center"
                         VerticalOptions="Center"
                         Value="24";
                         UpDownButtonAlignment="Both" />
                     
{% endhighlight %}
{% highlight c# %}

SfNumericUpDown sfNumericUpDown = new SfNumericUpDown();
sfNumericUpDown.WidthRequest = 200;
sfNumericUpDown.HorizontalOptions = LayoutOptions.Center;
sfNumericUpDown.VerticalOptions = LayoutOptions.Center;
sfNumericUpDown.Value=360;
sfNumericUpDown.UpDownButtonAlignment = NumericUpDownUpDownPlacementMode.Inline;

{% endhighlight %}
{% endtabs %}

![UpDown Placement in .NET MAUI NumericUpDown](UpDownButton_images/upDownButtonAlignment.png)

## UpDown button customization

## UpDown button color

Customize the `NumericUpDown` control button color by using the [UpDownButtonColor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html#Syncfusion_Maui_Toolkit_NumericUpDown_SfNumericUpDown_UpDownButtonColor) property.

{% tabs %}
{% highlight XAML %}

<editors:SfNumericUpDown HeightRequest="50"
                         WidthRequest="200"
                         HorizontalOptions="Center"
                         VerticalOptions="Center"
                         Value="360"
                         UpDownButtonColor="Blue"/>
                     
{% endhighlight %}
{% highlight c# %}

SfNumericUpDown sfNumericUpDown = new SfNumericUpDown();
sfNumericUpDown.HeightRequest= 50;
sfNumericUpDown.WidthRequest = 200;
sfNumericUpDown.HorizontalOptions = LayoutOptions.Center
sfNumericUpDown.VerticalOptions = LayoutOptions.Center;
sfNumericUpDown.Value = 360;
sfNumericUpDown.UpDownPlacementMode = NumericUpDownUpDownPlacementMode.Inline;
sfNumericUpDown.UpDownButtonColor = Colors.Blue;

{% endhighlight %}
{% endtabs %}

![UpDownButtonColor support in .NET MAUI NumericUpDown](UpDownButton_images/UpDownButtonColor.png)

## UpDown button template

The `NumericUpDown` control supports customization of the UpDownButton's appearance through the use of the [UpButtonTemplate](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html#Syncfusion_Maui_Toolkit_NumericUpDown_SfNumericUpDown_UpButtonTemplate) and [DownButtonTemplate](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html#Syncfusion_Maui_Toolkit_NumericUpDown_SfNumericUpDown_DownButtonTemplate) properties.

N> The UpDownButton template only supports Inline Placement mode.

{% tabs %}
{% highlight XAML %}

<VerticalStackLayout Spacing="10" VerticalOptions="Center">
    <editors:SfNumericUpDown x:Name="NumericUpDown"
                             WidthRequest="200"
                             HeightRequest="40" 
                             VerticalOptions="Center"
                             Value="50">
        <editors:SfNumericUpDown.UpButtonTemplate>
            <DataTemplate>
                <Grid>
                    <Label  Text="&#8593;" 
                            FontFamily="FontIcon"  
                            FontAttributes="Bold" 
                            Padding="6,6,8,0" 
                            TextColor="Green" />
                </Grid>
            </DataTemplate>
        </editors:SfNumericUpDown.UpButtonTemplate>
        <editors:SfNumericUpDown.DownButtonTemplate>
            <DataTemplate>
                <Grid>
                    <Label  Text="&#8595;" 
                            FontFamily="FontIcon"  
                            FontAttributes="Bold" 
                            Padding="6,6,8,0" 
                            TextColor="Red" />
                </Grid>
            </DataTemplate>
        </editors:SfNumericUpDown.DownButtonTemplate>
    </editors:SfNumericUpDown>
</VerticalStackLayout>
                     
{% endhighlight %}
{% highlight c# %}

 public partial class MainPage : ContentPage
 {
     public MainPage()
     {
         InitializeComponent();
         var verticalStackLayout = new StackLayout
         {
             Spacing = 10,
             VerticalOptions = LayoutOptions.Center
         };
         var NumericUpDown = new SfNumericUpDown
         {
             WidthRequest = 200,
             HeightRequest = 40,
             VerticalOptions = LayoutOptions.Center,
             Value = 50
         };
         var upButtonTemplate = new DataTemplate(() =>
         {
             var grid = new Grid();
             var label = new Label
             {
                 Padding = new Thickness(6, 6, 8, 0),
                 FontFamily = "FontIcon",
                 FontAttributes="Bold" 
                 Text = "\ue791", // Use Unicode directly for the icon
                 TextColor = Colors.Green,
             };
             grid.Children.Add(label);
             return grid;
         });
         var downButtonTemplate = new DataTemplate(() =>
         {
             var grid = new Grid();
             var label = new Label
             {
                 Padding = new Thickness(6, 6, 8, 0),
                 FontFamily = "FontIcon",
                 FontAttributes="Bold" 
                 Text = "\ue792",
                 TextColor = Colors.Red,
             };
             grid.Children.Add(label);
             return grid;
         });
         NumericUpDown.UpButtonTemplate = upButtonTemplate;
         NumericUpDown.DownButtonTemplate = downButtonTemplate;
         verticalStackLayout.Children.Add(NumericUpDown);
         Content = verticalStackLayout;
     }
 }

{% endhighlight %}
{% endtabs %}

![UpDownButtonTemplate support in .NET MAUI NumericUpDown](UpDownButton_images/UpDownButtonTemplate.png)

## Auto reverse in SfNumericUpDown

[Auto-reverse](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html#Syncfusion_Maui_Toolkit_NumericUpDown_SfNumericUpDown_AutoReverse) in NumericUpDown allows the control to automatically switch direction when reaching its [Minimum](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html#Syncfusion_Maui_Toolkit_NumericEntry_SfNumericEntry_Minimum) or [Maximum](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html#Syncfusion_Maui_Toolkit_NumericEntry_SfNumericEntry_Maximum) value. When incrementing, it starts at the `Minimum` and progresses to the `Maximum`, and conversely.

N> The default value of this property is `false.`
{% tabs %}
{% highlight XAML %}

<editors:SfNumericUpDown WidthRequest="200"
                        UpDownPlacementMode="Inline"
                        AutoReverse="True"
                        Minimum="0"
                        Maximum="10"/>
                        
                     
{% endhighlight %}
{% highlight c# %}

SfNumericUpDown sfNumericUpDown = new SfNumericUpDown();
sfNumericUpDown.WidthRequest = 200;
sfNumericUpDown.UpDownPlacementMode = NumericUpDownUpDownPlacementMode.Inline;
sfNumericUpDown.AutoReverse = true;
sfNumericUpDown.Minimum=0;
sfNumericUpDown.Maximum=10;

{% endhighlight %}
{% endtabs %}

![AutoReverse support in .NET MAUI NumericUpDown](UpDownButton_images/AutoReverseSupport.gif)

