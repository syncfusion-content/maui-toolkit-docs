---
layout: post
title: Getting started with .NET MAUI Carousel View | Syncfusion<sup>®</sup>
description: Learn how to set up, configure, and use the Syncfusion<sup>®</sup> .NET MAUI Carousel View (SfCarousel) control in your cross-platform applications.
platform: maui
control: Carousel
documentation: ug
---

# Getting Started with .NET MAUI Carousel

This section guides you through setting up and configuring a [Carousel](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.CarouselView.SfCarousel.html) in your .NET MAUI application. Follow the steps below to add a basic Carousel to your project.

{% tabcontents %}
{% tabcontent Visual Studio %}

## Prerequisites

Before proceeding, ensure the following are setup:
1. Ensure [.NET 9 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) or later is installed.
2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.8 or later) or Visual Studio 2026 (v18.0.0 or later).

## Step 1: Create a New .NET MAUI Project

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Click **Next**.
3. Select the .NET framework version and click **Create**.

## Step 2: Install the Syncfusion<sup>®</sup> .NET MAUI Toolkit Package

1. In **Solution Explorer**, right-click the project and choose **Manage NuGet Packages**.
2. Search for [Syncfusion.Maui.Toolkit](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.html) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

{% endtabcontent %}
{% tabcontent Visual Studio Code %}

## Prerequisites

Before proceeding, ensure the following are set up:

1. Install [.NET 9 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) or later is installed.
2. Set up a .NET MAUI environment with Visual Studio Code.
3. Ensure that the .NET MAUI extension is installed and configured as described [here](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-9.0&tabs=visual-studio-code).

## Step 1: Create a New .NET MAUI Project

1. Open the command palette by pressing `Ctrl+Shift+P` and type **.NET: New Project** and press **Enter**.
2. Choose the **.NET MAUI App** template.
3. Select the project location, type the project name, and press **Enter**.
4. Choose **Create project**.

## Step 2: Install the Syncfusion<sup>®</sup> .NET MAUI Toolkit Package

1. Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (back tick) to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your .csproj file is located.
3. Run the command `dotnet add package Syncfusion.Maui.Toolkit` to install the Syncfusion<sup>®</sup> .NET MAUI Toolkit NuGet package.
4. To ensure all dependencies are installed, run `dotnet restore`.

{% endtabcontent %}

{% tabcontent JetBrains Rider %}

## Prerequisites

Before proceeding, ensure the following are set up:

1. Ensure you have the latest version of JetBrains Rider.
2. Install [.NET 9 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) or later is installed.
3. Make sure the MAUI workloads are installed and configured as described [here.](https://www.jetbrains.com/help/rider/MAUI.html#before-you-start)

## Step 1: Create a new .NET MAUI Project

1. Go to **File > New Solution,** Select .NET (C#) and choose the .NET MAUI App template.
2. Enter the Project Name, Solution Name, and Location.
3. Select the .NET framework version and click Create.

## Step 2: Install the Syncfusion<sup>®</sup> MAUI Toolkit NuGet Package

1. In **Solution Explorer,** right-click the project and choose **Manage NuGet Packages.**
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored. If not, Open the Terminal in Rider and manually run: `dotnet restore`

{% endtabcontent %}
{% endtabcontents %}

## Step 3: Register Syncfusion handler

Make sure to add the namespace.
 
{% highlight MauiProgram.cs %}
using Syncfusion.Maui.Toolkit.Hosting;
{% endhighlight %}
 
Register the Syncfusion core handler in your CreateMauiApp method of `MauiProgram.cs` file to use Syncfusion controls.
 
{% highlight MauiProgram.cs %}
builder.ConfigureSyncfusionToolkit();
{% endhighlight %}

## Step 4: Import Carousel View namespace

Add the following namespace in your XAML or C#.
{% tabs %}
{% highlight xaml %}

xmlns:carousel="clr-namespace:Syncfusion.Maui.Toolkit.Carousel;assembly=Syncfusion.Maui.Toolkit"

{% endhighlight %}
{% highlight c# %}

using Syncfusion.Maui.Toolkit.Carousel;

{% endhighlight %}
{% endtabs %}

## Step 5: Define the Model and ViewModel

Carousel items can be added to the control using the [ItemsSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html#Syncfusion_Maui_Toolkit_Carousel_SfCarousel_ItemsSource) property of [SfCarousel](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html). Objects of any class can be given as items for `SfCarousel` by using `ItemsSource`. The views corresponding to the objects can be set using the [ItemTemplate](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html#Syncfusion_Maui_Toolkit_Carousel_SfCarousel_ItemTemplate) for the content.

Create a model class using the image collection property that is initialized with the required number of data objects, as shown in the following code example.

{% highlight C# %}

// Model
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

//View Model
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

{% endhighlight %}

N> The images used in the above view model should be added in the Resources folder of the Application.

## Step 6: Add the Carousel View component
The following code example illustrates how to add the collection in Carousel,

{% tabs %}

{% highlight xaml %}
<ContentPage.Resources>
    <ResourceDictionary>
        <DataTemplate x:Key="itemTemplate">
            <Image Source="{Binding Image}" 
                    Aspect="AspectFit"/>
        </DataTemplate>
    </ResourceDictionary>
<ContentPage.Resources>

    <carousel:SfCarousel x:Name="carousel"
                         ItemTemplate="{StaticResource itemTemplate}" 
                         ItemsSource="{Binding ImageCollection}"
                         ItemHeight="170"
                         ItemWidth="270"
                         SelectedIndex="4">
        <carousel:SfCarousel.BindingContext>
            <local:CarouselViewModel/>
        </carousel:SfCarousel.BindingContext>
    </carousel:SfCarousel>
{% endhighlight %}

{% highlight C# %}
    CarouselViewModel carouselViewModel = new CarouselViewModel();

    SfCarousel carousel = new SfCarousel()
    {
        ItemHeight = 170,
        ItemWidth = 270,
        SelectedIndex = 4
    };

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

{% endhighlight %}

{% endtabs %}

![OverView image for Carousel](images/gettingstarted.png)

You can download the Carousel View Getting Started sample from [here](https://github.com/SyncfusionExamples/Getting-Started-with-.NET-MAUI-SfCarousel)