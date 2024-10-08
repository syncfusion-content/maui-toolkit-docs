---
layout: post
title: Getting started with .NET MAUI Carousel View (SfCarousel) control | Syncfusion
description: Learn how to set up, configure, and use the Syncfusion .NET MAUI Carousel View (SfCarousel) control in your cross-platform applications.
platform: maui
control: Carousel
documentation: ug
---

# Getting Started with .NET MAUI Carousel

This section guides you through setting up and configuring a [Carousel](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.CarouselView.SfCarousel.html) in your .NET MAUI application. Follow the steps below to add a basic Carousel to your project.

## Prerequisites

Before proceeding, ensure the following are setup:
1. Ensure [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later is installed.
2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.8 or later) or Visual Studio Code. For Visual Studio Code users, ensure that the .NET MAUI workload is installed and configured as described [here](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-8.0&tabs=visual-studio-code).

## Step 1: Create a New .NET MAUI Project

### Visual Studio

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Click **Next**.
3. Select the .NET framework version and click **Create**.

### Visual Studio Code

1. Open the command palette by pressing `Ctrl+Shift+P` and type **.NET: New Project** and press **Enter**.
2. Choose the **.NET MAUI App** template.
3. Select the project location, type the project name, and press **Enter**.
4. Choose **Create project**.

## Step 2: Install the Syncfusion .NET MAUI Toolkit Package

### Visual Studio

1. In **Solution Explorer**, right-click the project and choose **Manage NuGet Packages**.
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

### Visual Studio Code

1. Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (backtick) to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your .csproj file is located.
3. Run the following command to install the Syncfusion .NET MAUI Toolkit NuGet package:
  
{% tabs %}
{% highlight sh  %}

    dotnet add package Syncfusion.Maui.Toolkit

{% endhighlight %}
{% endtabs %}
4. To ensure all dependencies are installed, run:

{% tabs %}
{% highlight sh  %}

    dotnet restore
    
{% endhighlight %}
{% endtabs %}

## Step 3: Register the handler

In the **MauiProgram.cs** file, register the handler for Syncfusion Toolkit.

{% tabs %}
{% highlight C# tabtitle="MauiProgram.cs" hl_lines="1 9" %}    
    using Syncfusion.Maui.Toolkit.Hosting;

    public static class MauiProgram
    {
	    public static MauiApp CreateMauiApp()
	    {
	        var builder = MauiApp.CreateBuilder();
		    builder
			    .ConfigureSyncfusionToolkit()
			    .UseMauiApp<App>()
			    .ConfigureFonts(fonts =>
			    {
				    fonts.AddFont("OpenSans-Regular.ttf", "OpenSansRegular");
				    fonts.AddFont("OpenSans-Semibold.ttf", "OpenSansSemibold");
			    });

		    return builder.Build();
	    }
    }
{% endhighlight %}
{% endtabs %} 

## Step 4: Add a Basic Carousel

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Carousel` namespace into your code.

2. Initialize [SfCarousel](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html)

{% tabs %}

{% highlight xaml %}

<?xml version="1.0" encoding="utf-8" ?>
<ContentPage 
            ...
            xmlns:carousel="clr-namespace:Syncfusion.Maui.Toolkit.Carousel;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
        <carousel:SfCarousel />
    </ContentPage.Content>  
</ContentPage>
	
{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.Carousel;
namespace CarouselGettingStarted
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();           
            SfCarousel carousel = new SfCarousel();
            this.Content = carousel;
        }
    }   
}

{% endhighlight %}

{% endtabs %}

## Step 5: Populate Carousel Items in .NET MAUI Carousel

Carousel items can be added to the control using the [ItemsSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html#Syncfusion_Maui_Toolkit_Carousel_SfCarousel_ItemsSource) property of [SfCarousel](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html).

Objects of any class can be given as items for `SfCarousel` by using `ItemsSource`. The views corresponding to the objects can be set using the [ItemTemplate](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html#Syncfusion_Maui_Toolkit_Carousel_SfCarousel_ItemTemplate) for the content.

Create a model class using the image collection property that is initialized with the required number of data objects, as shown in the following code example.

{% highlight C# %}

// Model

public class CarouselModel
{
    public CarouselModel(string imageString)
    {
        Image = imageString;
    }
    private string _image;

    public string Image
    {
        get { return _image; }
        set { _image = value; }
    }
}

//View Model

public class CarouselViewModel
{
    public CarouselViewModel()
    {
        ImageCollection.Add(new CarouselModel("carousel_person1.png"));
        ImageCollection.Add(new CarouselModel("carousel_person2.png"));
        ImageCollection.Add(new CarouselModel("carousel_person3.png"));
        ImageCollection.Add(new CarouselModel("carousel_person4.png"));
        ImageCollection.Add(new CarouselModel("carousel_person5.png"));
    }
    private List<CarouselModel> imageCollection = new List<CarouselModel>();
    public List<CarouselModel> ImageCollection
    {
        get { return imageCollection; }
        set { imageCollection = value; }
    }
}

{% endhighlight %}

N> The images used in the above view model should be added in the Resources folder of the Application.

The following code example illustrates how to add the collection in Carousel,

{% tabs %}

{% highlight xaml %}

<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:carousel="clr-namespace:Syncfusion.Maui.Toolkit.Carousel;assembly=Syncfusion.Maui.Toolkit"
             xmlns:local="clr-namespace:CarouselSample"
             x:Class="CarouselSample.MainPage">
             
    <ContentPage.BindingContext>
        <local:CarouselViewModel/>
    </ContentPage.BindingContext>

    <ContentPage.Resources>
        <ResourceDictionary>
            <DataTemplate x:Key="itemTemplate">
                <Image Source="{Binding Image}" 
                        Aspect="AspectFit"/>
            </DataTemplate>
        </ResourceDictionary>
    </ContentPage.Resources>
    <ContentPage.Content>
        <carousel:SfCarousel x:Name="carousel"  
                            ItemTemplate="{StaticResource itemTemplate}" 
                            ItemsSource="{Binding ImageCollection}" />
    </ContentPage.Content>
    </ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.Carousel;
using System.Collections.ObjectModel;

namespace CarouselSample
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();
            CarouselViewModel carouselViewModel = new CarouselViewModel();

            SfCarousel carousel = new SfCarousel();

            var itemTemplate = new DataTemplate(() =>
            {
                var grid = new Grid();
                var nameLabel = new Image();
                nameLabel.SetBinding(Image.SourceProperty, "Image");
                grid.Children.Add(nameLabel);
                return grid;
            });

            carousel.BindingContext = carouselViewModel;
            carousel.ItemTemplate = itemTemplate;
            carousel.SetBinding(SfCarousel.ItemsSourceProperty, "ImageCollection");

            this.Content = carousel;
        }
    }
}

{% endhighlight %}

{% endtabs %}

## Step 6: Setting the height and width of the carousel item

[ItemHeight](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html#Syncfusion_Maui_Toolkit_Carousel_SfCarousel_ItemHeight) and [ItemWidth](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html#Syncfusion_Maui_Toolkit_Carousel_SfCarousel_ItemWidth) properties are used to change the height and width of carouselItem in carousel panel.

{% tabs %}

{% highlight xaml %}

<carousel:SfCarousel x:Name="carousel"
                     ItemTemplate="{StaticResource itemTemplate}" 
                     ItemsSource="{Binding ImageCollection}"
                     ItemHeight="170"
                     ItemWidth="270"/>

{% endhighlight %}

{% highlight C# %}

SfCarousel carousel = new SfCarousel()
{
    ItemWidth = 170,
    ItemHeight = 250
};

carousel.ItemTemplate = itemTemplate;
carousel.SetBinding(SfCarousel.ItemsSourceProperty, "ImageCollection");

{% endhighlight %}

{% endtabs %}

## Step 7: Set Desire Item to be Selected

We can bring particular item to the center of the screen using [SelectedIndex](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html#Syncfusion_Maui_Toolkit_Carousel_SfCarousel_SelectedIndex) property in [SfCarousel](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html) control.

{% tabs %}

{% highlight xaml %}

<carousel:SfCarousel x:Name="carousel"
                     ItemTemplate="{StaticResource itemTemplate}" 
                     ItemsSource="{Binding ImageCollection}"
                     ItemHeight="170"
                     ItemWidth="270"
                     SelectedIndex="4"/>
	
{% endhighlight %}

{% highlight C# %}

SfCarousel carousel = new SfCarousel()
{
    ItemWidth = 170,
    ItemHeight = 250,
    SelectedIndex = 4,
};

carousel.ItemTemplate = itemTemplate;
carousel.SetBinding(SfCarousel.ItemsSourceProperty, "ImageCollection");

{% endhighlight %}

{% endtabs %}

N> The [SelectedIndex](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html#Syncfusion_Maui_Toolkit_Carousel_SfCarousel_SelectedIndex)  property will be 0 by default.

![OverView image for Carousel](images/gettingstarted.png)

N> You can find the complete getting started sample from this [link].
