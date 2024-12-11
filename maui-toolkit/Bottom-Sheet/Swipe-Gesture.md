---
layout: post
title: Swiping in .NET MAUI Bottom Sheet | Syncfusion
description: Learn here all about swiping support in Syncfusion .NET MAUI Bottom Sheet (SfBottomSheet) control and more.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---
# Swiping in .NET MAUI Bottom Sheet (SfBottomSheet)

The [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html) supports the swiping for expanding the sheet. 

## Enable Swiping

The [EnableSwiping](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_EnableSwiping) property allows you to enable or disable swipe functionality in the [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html). By default, the EnableSwiping property is set to `true`.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" EnableSwiping="True">
    <bottomSheet:SfBottomSheet.Content>
        <VerticalStackLayout Padding="20">
            <Button Text="Open Bottom Sheet" Clicked="OpenBottomSheet" WidthRequest="180" CornerRadius="30" VerticalOptions="Center"/>
        </VerticalStackLayout>
    </bottomSheet:SfBottomSheet.Content>
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <Label Text="Bottom Sheet Content" VerticalOptions="Center" HorizontalOptions="Center" FontSize="14" />
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

var verticalStackLayout = new VerticalStackLayout
{
    Padding = new Thickness(20)
};

var button = new Button
{
    Text = "Open Bottom Sheet",
    WidthRequest = 180,
    CornerRadius = 30,
    VerticalOptions = LayoutOptions.Center
};

button.Clicked += OpenBottomSheet;
verticalStackLayout.Children.Add(button);
SfBottomSheet bottomSheet = new SfBottomSheet();
var bottomSheetContent = new Label
{
    Text = "Bottom Sheet Content",
    VerticalOptions = LayoutOptions.Center,
    HorizontalOptions = LayoutOptions.Center,
    FontSize = 14
};

bottomSheet.EnableSwiping = true;
bottomSheet.BottomSheetContent = bottomSheetContent;
bottomSheet.Content = verticalStackLayout;
this.Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

{% highlight c# %}

private void OpenBottomSheet(object sender, EventArgs e)
{
    bottomSheet.Show();
}

{% endhighlight %}

![Swiping Image for BottomSheet](images/swiping.gif)