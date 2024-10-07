---
layout: post
title: Getting Started with .NET MAUI Segmented control | Syncfusion
description: Learn about getting started with Syncfusion .NET MAUI Segmented control (SfSegmentedControl) in mobile and desktop applications from a single shared codebase.
platform: maui-toolkit
control: Segmented (SfSegmented) control
documentation: ug
---

# Getting Started with the .NET MAUI Segmented Control

This section provides a quick overview of how to get started with the .NET MAUI Segmented control (SfSegmentedControl) for .NET MAUI and a walk-through to configure the .NET MAUI Segmented control in a real-time scenario. Follow the steps below to add .NET MAUI Segmented control to your project.

## Prerequisites

Before proceeding, ensure the following are setup:
1. Install [.NET 7 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/7.0) or later is installed.
2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.3 or later) or Visual Studio Code. For Visual Studio Code users, ensure that the .NET MAUI workload is installed and configured as described [here.](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-8.0&tabs=visual-studio-code)

## Step 1: Create a New .NET MAUI Project

### Visual Studio

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Then click **Next**.
3. Select the .NET framework version and click **Create**.

### Visual Studio Code

1. Open the command palette by pressing `Ctrl+Shift+P` and type **.NET:New Project** and enter.
2. Choose the **.NET MAUI App** template.
3. Select the project location, type the project name and press **Enter**.
4. Then choose **Create project.**

## Step 2: Install the Syncfusion .NET MAUI Toolkit Package

### Visual Studio

1. In **Solution Explorer,** right-click the project and choose **Manage NuGet Packages.**
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

### Visual Studio Code

1. Press ``Ctrl + '(backtick)`` to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your .csproj file is located.
3. Run the following command to install the Syncfusion .NET MAUI Toolkit NuGet package:
  
   `sh: dotnet add package Syncfusion.Maui.Toolkit`
4. To ensure all dependencies are installed, run:

     `sh:dotnet restore`

## Step 3: Register the handler

In the **MauiProgram.cs** file, register the handler for Syncfusion Toolkit.

{% tabs %}
{% highlight C# tabtitle="MauiProgram.cs" hl_lines="1 8" %}

    
    using Syncfusion.Maui.Core.Hosting;
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

## Step 4: Add .NET MAUI Segmented Control

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.SegmentedControl` namespace into your code.
2. Initialize `SfSegmentedControl` class.

{% tabs %}
{% highlight XAML %}

<ContentPage   
            
    xmlns:SegmentedControl="clr-namespace:Syncfusion.Maui.Toolkit.SegmentedControl;assembly=Syncfusion.Maui.Toolkit"

        <SegmentedControl:SfSegmentedControl />

</ContentPage>

{% endhighlight %}
{% highlight C# %}

using Syncfusion.Maui.Toolkit.SegmentedControl;

. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfSegmentedControl SegmentedControl = new SfSegmentedControl();
        this.Content = SegmentedControl;
    }
}

{% endhighlight %}
{% endtabs %}

## Step 5: Populating segmented items

You can use `ItemsSource` property of `SfSegmentedControl` to populate the segmented items.

{% tabs %}
{% highlight XAML %}

<ContentPage   
    xmlns:SegmentedControl="clr-namespace:Syncfusion.Maui.Toolkit.SegmentedControl;assembly=Syncfusion.Maui.Toolkit">
    <SegmentedControl:SfSegmentedControl x:Name="segmentedControl">
        <SegmentedControl:SfSegmentedControl.ItemsSource>
            <x:Array Type="{x:Type x:String}">
                <x:String>Day</x:String>
                <x:String>Week</x:String>
                <x:String>Month</x:String>
                <x:String>Year</x:String>
            </x:Array>
        </SegmentedControl:SfSegmentedControl.ItemsSource>
    </SegmentedControl:SfSegmentedControl>
</ContentPage>

{% endhighlight %}
{% highlight C# %}

using Syncfusion.Maui.Toolkit.SegmentedControl;
. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
          SfSegmentedControl SegmentedControl = new SfSegmentedControl();
          SegmentedControl.ItemsSource = new List<SfSegmentItem>
          {
            new SfSegmentItem { Text = "Day" },
            new SfSegmentItem { Text = "Week" },
            new SfSegmentItem { Text = "Month" },
            new SfSegmentItem { Text = "Year" }
         };
        this.Content = SegmentedControl;
    }
}

{% endhighlight %}
{% endtabs %}

![Getting started in .NET MAUI Segmented control.](images/getting-started/getting-started.png)
