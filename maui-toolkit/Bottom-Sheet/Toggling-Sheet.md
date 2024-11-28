---
layout: post
title: Toggle methods in .NET MAUI Bottom Sheet | Syncfusion
description: Learn here all about toggle methods support in Syncfusion .NET MAUI Bottom Sheet(SfBottomSheet) control.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---

# Toggle methods in .NET MAUI Bottom Sheet (SfBottomSheet)

Bottom sheet can be toggled using

* Show method
* Close method

## Opening and Closing Sheet Programmatically
The `Show` method enables programmatically opening the bottom sheet, and the `Close` method enables programmatically closing the bottom sheet.

{% tabs %}

{% highlight xaml %}

<Grid>
    <VerticalStackLayout Padding="20">
       <Button Text="Open Bottom Sheet" Clicked="OpenBottomSheet" WidthRequest="180" CornerRadius="30"/>
    </VerticalStackLayout>
    <bottomSheet:SfBottomSheet x:Name="bottomSheet">
        <bottomSheet:SfBottomSheet.BottomSheetContent>
            <Button Text="Close Bottom Sheet" Clicked="CloseBottomSheet" HeightRequest="50" WidthRequest="180" CornerRadius="30"/>
        </bottomSheet:SfBottomSheet.BottomSheetContent>
    </bottomSheet:SfBottomSheet>
</Grid>

{% endhighlight %}
{% highlight c# %}

Grid grid = new Grid();
VerticalStackLayout verticalStack = new VerticalStackLayout
{
    Padding = new Thickness(20)
};

Button openButton = new Button
{
    Text = "Open Bottom Sheet",
    WidthRequest = 180,
    CornerRadius = 30,
};

openButton.Clicked += OpenBottomSheet;
verticalStack.Children.Add(openButton);
grid.Children.Add(verticalStack);
SfBottomSheet bottomSheet = new SfBottomSheet();
Button closeButton = new Button
{
    Text = "Close Bottom Sheet",
    HeightRequest = 50,
    WidthRequest = 180,
    CornerRadius = 30,
};

closeButton.Clicked += CloseBottomSheet;
bottomSheet.BottomSheetContent = closeButton;
grid.Children.Add(bottomSheet);
Content = grid;

{% endhighlight %}
{% endtabs %}

Using `Show` and `Close` methods,

{% highlight c# %}

private void OpenBottomSheet(object sender, EventArgs e)
{
    bottomSheet.Show();
}

private void CloseBottomSheet(object sender, EventArgs e)
{
    bottomSheet.Close();
}

{% endhighlight %}

![Toggle Gif for BottomSheet](images/toggleMethod.gif)