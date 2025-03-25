---
layout : post
title: Populating Data in .NET MAUI Carousel View control | Syncfusion
description: Learn here all about Populating Data support in Syncfusion<sup>®</sup> .NET MAUI Carousel View (SfCarousel) control and more.
platform : maui
control : Carousel
documentation : ug
---

# Populating Data in .NET MAUI Carousel View (SfCarousel)

The [SfCarousel](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html) control supports binding to various item sources, such as IList and ObservableCollection.

## Through Binding

Items can be populated in the [SfCarousel](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html) control by binding an item source and applying a custom template, as explained below.

### Create a Model with Data

The [SfCarousel](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html) items can be populated with a collection of image data. For example, a user may want to create an **SfCarousel** control to display a list of images.

The **SfCarousel** model is structured as follows.

{% highlight C# %}

namespace CarouselSample
{
    public class GalleryModel
    {
        public GalleryModel(string imageString)
        {
            ImageName = imageString;
        }
        private string _imageName;

        public string ImageName
        {
            get { return _imageName; }
            set { _imageName = value; }
        }
    }
}

{% endhighlight %}

Populate the **SfCarousel** items collection in the ViewModel with the image data.

{% highlight C# %}

using System.Collections.Generic;

namespace CarouselSample
{
    public class GalleryViewModel
    {
        public GalleryViewModel()
        {
            ImageCollection.Add(new GalleryModel("carousel_person1.png"));
            ImageCollection.Add(new GalleryModel("carousel_person2.png"));
            ImageCollection.Add(new GalleryModel("carousel_person3.png"));
            ImageCollection.Add(new GalleryModel("carousel_person4.png"));
            ImageCollection.Add(new GalleryModel("carousel_person5.png"));
        }
        private List<GalleryModel> imageCollection = new List<GalleryModel>();
        public List<GalleryModel> ImageCollection
        {
            get { return imageCollection; }
            set { imageCollection = value; }
        }
    }
}

{% endhighlight %}

### Binding the Data with Custom Template

The [SfCarousel](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html) supports adding custom views as carousel items by designing a view inside its [ItemTemplate](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html#Syncfusion_Maui_Toolkit_Carousel_SfCarousel_ItemTemplate). This template will be applied to all items, with data bound accordingly.

{% tabs %}

{% highlight xaml %}

<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:carousel="clr-namespace:Syncfusion.Maui.Toolkit.Carousel;assembly=Syncfusion.Maui.Toolkit"
             xmlns:local="clr-namespace:CarouselSample"
             x:Class="CarouselSample.MainPage">
    <ContentPage.BindingContext>
        <local:GalleryViewModel/>
    </ContentPage.BindingContext>
    <ContentPage.Resources>
        <ResourceDictionary>
            <DataTemplate x:Key="itemTemplate">
                <Image Source="{Binding ImageName}" 
                       Aspect="AspectFit"/>
            </DataTemplate>
        </ResourceDictionary>
    </ContentPage.Resources>
    <ContentPage.Content>
        <carousel:SfCarousel x:Name="carousel"  
                             ItemTemplate="{StaticResource itemTemplate}" 
                             ItemsSource="{Binding ImageCollection}" 
                             HeightRequest="400" 
                             WidthRequest="800" />
    </ContentPage.Content>
</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.Carousel;

namespace CarouselSample
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();
            GalleryViewModel galleryViewModel = new GalleryViewModel();

            SfCarousel carousel = new SfCarousel()
            {
                HeightRequest = 400,
                WidthRequest = 800
            };

            var itemTemplate = new DataTemplate(() =>
            {
                var grid = new Grid();
                var nameLabel = new Image();
                nameLabel.SetBinding(Image.SourceProperty, "ImageName");
                grid.Children.Add(nameLabel);
                return grid;
            });

            carousel.BindingContext = galleryViewModel;
            carousel.ItemTemplate = itemTemplate;
            carousel.SetBinding(SfCarousel.ItemsSourceProperty, "ImageCollection");

            this.Content = carousel;
        }
    }
}

{% endhighlight %}
{% endtabs %}


