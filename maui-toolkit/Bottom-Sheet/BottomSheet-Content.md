---
layout: post
title: Set Bottom Sheet Content in .NET MAUI Bottom Sheet | Syncfusion
description: Learn here all about setting bottom sheet content support in Syncfusion .NET MAUI Bottom Sheet (SfBottomSheet) control.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---

# Set Main Content and Bottom Sheet Content in .NET MAUI Bottom Sheet

* The main content of the `BottomSheet` is always visible and can be set using the `Content` property.

* The `BottomSheet` content is only viewable when the sheet is in the FullExpanded, HalfExpanded, or Collapsed state. Its content can be set as : `BottomSheetContent`.

{% tabs %}
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet">
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

bottomSheet.BottomSheetContent = bottomSheetContent;
bottomSheet.Content = verticalStackLayout;
this.Content = bottomSheet;
  
{% endhighlight %}
{% endtabs %}

{% tabs %}
{% highlight c# %}

private void OpenBottomSheet(object sender, EventArgs e)
{
    bottomSheet.Show();
}

{% endhighlight %}
{% endtabs %}

![BottomSheetContent Image for BottomSheet](images/bottomSheetContent.png)