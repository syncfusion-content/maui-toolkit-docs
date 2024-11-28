---
layout: post
title: Getting started with .NET MAUI Bottom Sheet control | Syncfusion
description: Learn here about getting started with Syncfusion .NET MAUI Bottom Sheet (SfBottomSheet) control in your cross-platform applications.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---

# Getting Started with .NET MAUI Bottom Sheet

This section provides a quick overview of how to get started with the `BottomSheet` for .NET MAUI and a walk-through to configure the .NET MAUI Bottom Sheet in a real-time scenario. Follow the steps below to add .NET MAUI Bottom Sheet to your project.

## Prerequisites

Before proceeding, ensure the following are set up:

1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later is installed.
2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.8 or later) or Visual Studio Code. For Visual Studio Code users, ensure that the .NET MAUI workload is installed and configured as described [here.](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-8.0&tabs=visual-studio-code).

## Step 1: Create a New MAUI Project

### Visual Studio

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Then, click **Next.**
3. Select the .NET framework version and click **Create.**

### Visual Studio Code

1. Open the command palette by pressing `Ctrl+Shift+P` and type **.NET:New Project** and enter.
2. Choose the **.NET MAUI App** template.
3. Select the project location, type the project name and press **Enter.**
4. Then choose **Create project.**

## Step 2: Install the Syncfusion MAUI Toolkit Package

### Visual Studio
1. In **Solution Explorer,** right-click the project and choose **Manage NuGet Packages.**
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

### Visual Studio Code
1. Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (backtick) to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your .csproj file is located.
3. Run the command `dotnet add package Syncfusion.Maui.Toolkit` to install the Syncfusion .NET MAUI Toolkit NuGet package.
4. To ensure all dependencies are installed, run `dotnet restore`.

## Step 3: Register the handler

In the MauiProgram.cs file, register the handler for Syncfusion Toolkit.

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

## Step 4: Add a Basic BottomSheet

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.BottomSheet` namespace into your code.

2. Initialize `SfBottomSheet`
{% tabs %}
{% highlight xaml %}

<ContentPage
    xmlns:bottomSheet="clr-namespace:Syncfusion.Maui.Toolkit.BottomSheet;assembly=Syncfusion.Maui.Toolkit">
    <Grid>
        <VerticalStackLayout Padding="20">
            <Button Text="Open Bottom Sheet" Clicked="OpenBottomSheet" WidthRequest="180" CornerRadius="30" VerticalOptions="Center"/>
        </VerticalStackLayout>
        <bottomSheet:SfBottomSheet x:Name="bottomSheet">
            <bottomSheet:SfBottomSheet.BottomSheetContent>
                <Label Text="Bottom Sheet Content" VerticalOptions="Center" HorizontalOptions="Center" FontSize="14" />
            </bottomSheet:SfBottomSheet.BottomSheetContent>
        </bottomSheet:SfBottomSheet>
    </Grid>
</ContentPage>
    
{% endhighlight %}
{% highlight c# %}

using Syncfusion.Maui.Toolkit.BottomSheet;

namespace BottomSheetGettingStarted
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();
            Grid grid=new Grid();
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
            grid.Children.Add(verticalStackLayout);
            grid.Children.Add(bottomSheet);
            this.Content = grid;
        }
    } 
}
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

N> It is mandatory to set `BottomSheetContent` for `SfBottomSheet` on initializing.

![Getting Started Image for BottomSheet](images/gettingStarted.png)