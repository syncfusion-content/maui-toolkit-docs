---
layout: post
title: How to Add the Custom View for Syncfusion® SfButton
description: Learn about how to add a custom content view for the .NET MAUI Toolkit's SfButton control in detail.
platform: maui
control: Sfbutton
documentation: ug
---

# Add the custom view for button

You can customize the appearance of the button by adding your custom view in the [`Content`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html#Syncfusion_Maui_Toolkit_Buttons_SfButton_Content) property. The following code sample demonstrates how to apply the busy indicator control as a custom view for a button.

{% tabs %}
{% highlight xaml %}


<ContentPage.Content>
    <button:SfButton  CornerRadius="10"  WidthRequest="120" Text="SfButton" Background="#4125BC">
        <button:SfButton.Content>
            <DataTemplate>
                <HorizontalStackLayout Spacing = "8" Padding="5">
                    <ActivityIndicator Color = "White" IsRunning="True"/>
                    <Label Text = "Loading..." VerticalOptions="Center" TextColor="White"/>
                </HorizontalStackLayout>
            </DataTemplate>
        </button:SfButton.Content>
    </button:SfButton>
</ContentPage.Content>

{% endhighlight %}
{% highlight c# %}
 
var customTemplate = new DataTemplate(() =>
{
    var activityIndicator = new ActivityIndicator
    {
        Color = Colors.White,
        IsRunning = true,
    };
    var label = new Label
    {
        Text = "Loading...",
        TextColor = Colors.White,
        VerticalOptions = LayoutOptions.Center
    };
    var stackLayout = new HorizontalStackLayout
    {
        Spacing = 8,
        Padding = new Thickness(5)
    };
    stackLayout.Children.Add(activityIndicator);
    stackLayout.Children.Add(label);
    return stackLayout;
});
SfButton button = new SfButton
{
    Text = "SfButton",
    WidthRequest = 120,
    Background = Color.FromArgb("#4125BC"),
    CornerRadius= 10,
    Content = customTemplate
};
{% endhighlight %}
{% endtabs %}

![SfButton with custom view](images/button-content.png)