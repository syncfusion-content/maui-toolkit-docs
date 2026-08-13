---
layout : post
title: How to Perform Actions in .NET MAUI Carousel | Syncfusion®
description: Learn how to perform an operation while changing the CarouselItem or collection in .NET MAUI Carousel.
platform : maui
control : Carousel
documentation : ug
---

# How to Perform an Action When an Item Changes in .NET MAUI Carousel

We can perform the operation while changing the CarouselItem using the [SelectionChanged](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html#Syncfusion_Maui_Toolkit_Carousel_SfCarousel_SelectionChanged) event. The SelectionChanged event returns the OldItem and selected NewItem.

{% tabs %}

{% highlight xaml %}

<carousel:SfCarousel x:Name="carousel"
                     ItemsSource="{Binding ImageCollection}"
                     ItemTemplate="{StaticResource itemTemplate}"
                     ItemHeight="200"
                     ItemWidth="200"
                     SelectionChanged="Carousel_SelectionChanged"/>

{% endhighlight %}

{% highlight C# %}

private void Carousel_SelectionChanged(object sender, Syncfusion.Maui.Toolkit.Carousel.SelectionChangedEventArgs e)
{
    int count = (sender as SfCarousel).SelectedIndex + 1;
    DisplayAlert("SelectionChanged", "Carousel item:" + count + " has Selected", "Ok");
}

{% endhighlight %}

{% endtabs %}


