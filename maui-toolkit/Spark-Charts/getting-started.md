---
layout: post
title: Getting Started with .NET MAUI Chart control | Syncfusion
description: Learn here all about getting started with Syncfusion® .NET MAUI Chart (SfSparkChart) control, its elements, and more.
platform: maui
control: SfSparkChart
documentation: ug
---

> **Notice**: After **Volume 1 2025 (Mid of March 2025)**, feature enhancements for this control will no longer be available in the Syncfusion® package. Please switch to the **Syncfusion® Toolkit for .NET MAUI** for continued support. For a smooth transition refer this [migration document](https://help.syncfusion.com/maui-toolkit/migration).

# Getting Started with .NET MAUI Spark Charts (SparkChart)

This section explains how to populate the spark chart with data, configure chart type, enable markers and data labels, and customize its appearance as well as the essential aspects for getting started with the spark chart.

## Prerequisites

Before proceeding, ensure that the following are set up:

1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later is installed.
2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.8 or later).

## Step 1: Create a new .NET MAUI project

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Click **Next**.
3. Select the .NET framework version and click **Create**.

## Step 2: Install the Syncfusion<sup>®</sup> .NET MAUI Toolkit Package

1. In **Solution Explorer**, right-click the project and choose **Manage NuGet Packages**.
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

## Step 3: Register the handler

In the **MauiProgram.cs** file, register the handler for Syncfusion® Toolkit.

{% tabs %}
{% highlight C# tabtitle="MauiProgram.cs" hl_lines="6 17" %}

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

## Step 4: Add .NET MAUI Spark Chart

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Charts` namespace into your code.
2. Initialize an instance of the [SfSparkChart](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Toolkit.Charts.SfSparkChart.html) control.

{% tabs %} 
{% highlight xaml %}

<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.Charts;assembly=Syncfusion.Maui.Toolkit"
             x:Class="GettingStarted.MainPage">

        <chart:SfSparkChart/>

</ContentPage>
 
{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.Charts; // Import the namespace required for Syncfusion MAUI Toolkit Charts.

. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfSparkChart chart = new SfSparkChart(); // Create an instance of the SfSparkChart.
        this.Content = chart; // Set the chart as the content of the page.
    }
} 

{% endhighlight %}
{% endtabs %}

{% endtabcontent %}

{% tabcontent Visual Studio Code %}

## Prerequisites

Before proceeding, ensure that the following are set up:

1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later is installed.
2. Set up a .NET MAUI environment with Visual Studio Code.
3. Ensure that the .NET MAUI extension is installed and configured as described [here.](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-8.0&tabs=visual-studio-code)

## Step 1: Create a new .NET MAUI project

1. Open the command palette by pressing `Ctrl+Shift+P` and type **.NET:New Project** and enter.
2. Choose the **.NET MAUI App** template.
3. Select the project location, type the project name and press **Enter.**
4. Then choose **Create project.**

## Step 2: Install the Syncfusion<sup>®</sup> .NET MAUI Toolkit Package

1. Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (backtick) to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your .csproj file is located.
3. Run the command `dotnet add package Syncfusion.Maui.Toolkit` to install the Syncfusion<sup>®</sup> .NET MAUI Toolkit NuGet package.
4. To ensure all dependencies are installed, run `dotnet restore`.

## Step 3: Register the handler

In the **MauiProgram.cs** file, register the handler for Syncfusion<sup>®</sup> Toolkit.

{% tabs %}
{% highlight C# tabtitle="MauiProgram.cs" hl_lines="6 17" %}

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

## Step 4: Add .NET MAUI Spark Chart

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Charts` namespace.
2. Initialize [SfSparkChart](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Toolkit.Charts.SfSparkChart.html).

{% tabs %} 
{% highlight xaml %}

<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.Charts;assembly=Syncfusion.Maui.Toolkit"
             x:Class="GettingStarted.MainPage">

        <chart:SfSparkChart/>

</ContentPage>
 
{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.Charts; // Import the namespace required for Syncfusion MAUI Toolkit Charts.

. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfSparkChart chart = new SfSparkChart(); // Create an instance of the SfSparkChart.
        this.Content = chart; // Set the chart as the content of the page.
    }
} 
{% endhighlight %}
{% endtabs %}

{% endtabcontent %}

{% tabcontent JetBrains Rider %}

## Prerequisites

Before proceeding, ensure the following are set up:

1. Ensure you have the latest version of JetBrains Rider.
2. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later is installed.
3. Make sure the MAUI workloads are installed and configured as described [here.](https://www.jetbrains.com/help/rider/MAUI.html#before-you-start)

## Step 1: Create a new .NET MAUI Project

1. Go to **File > New Solution,** Select .NET (C#) and choose the .NET MAUI App template.
2. Enter the Project Name, Solution Name, and Location.
3. Select the .NET framework version and click Create.

## Step 2: Install the Syncfusion<sup>®</sup> MAUI Toolkit NuGet Package

1. In **Solution Explorer,** right-click the project and choose **Manage NuGet Packages.**
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored. If not, Open the Terminal in Rider and manually run: `dotnet restore`

## Step 3: Register the handler

In the **MauiProgram.cs** file, register the handler for Syncfusion<sup>®</sup> core.

{% tabs %}
{% highlight C# tabtitle="MauiProgram.cs" hl_lines="6 17" %}

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

## Step 4: Add .NET MAUI Spark Chart

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Charts` namespace.
2. Initialize [SfSparkChart](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Toolkit.Charts.SfSparkChart.html).

{% tabs %} 
{% highlight xaml %}

<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.Charts;assembly=Syncfusion.Maui.Toolkit"
             x:Class="GettingStarted.MainPage">

        <chart:SfSparkChart/>

</ContentPage>
 
{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.Charts; // Import the namespace required for Syncfusion MAUI Toolkit Charts.

. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfSparkChart chart = new SfSparkChart(); // Create an instance of the SfSparkChart.
        this.Content = chart; // Set the chart as the content of the page.
    }
} 
{% endhighlight %}
{% endtabs %}

{% endtabcontent %}

{% endtabcontents %}

### Initialize view model

Define a simple data model to represent a data point in the chart:

{% tabs %}  

{% highlight c# %}

public class SparkDataModel
{
    public double Value { get; set; }
}

{% endhighlight %} 

{% endtabs %} 

Next, create a view SparkDataViewModel class that holds a list of `SparkDataModel` objects as follows.

{% tabs %}  

{% highlight c# %}

public class SparkChartViewModel
{
    public List<SparkDataModel> Data { get; set; }

    public SparkChartViewModel()
    {
        Data = new List<SparkDataModel>()
        {
            new SparkDataModel() { Value = 10 },
            new SparkDataModel() { Value = 20 },
            new SparkDataModel() { Value = 15 },
            new SparkDataModel() { Value = 25 },
            new SparkDataModel() { Value = 30 },
            new SparkDataModel() { Value = 18 },
            new SparkDataModel() { Value = 22 },
            new SparkDataModel() { Value = 28 },
            new SparkDataModel() { Value = 35 },
            new SparkDataModel() { Value = 40 },
        };
    }
}

{% endhighlight %} 

{% endtabs %} 

Create a `SparkDataViewModel` instance and set it as the chart's `BindingContext`. This enables property binding from `SparkDataViewModel` class.

N> Add the namespace of `SparkDataViewModel` class to your XAML Page, if you prefer to set `BindingContext` in XAML.

{% tabs %} 

{% highlight xaml %}

<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.Charts;assembly=Syncfusion.Maui.Toolkit"
             xmlns:model="clr-namespace:GettingStarted"
             x:Class="GettingStarted.MainPage">
    <chart:SfSparkChart>
        <chart:SfSparkChart.BindingContext>
            <model:SparkDataViewModel/>
        </chart:SfSparkChart.BindingContext>
    </chart:SfSparkChart>
</ContentPage>

{% endhighlight %}

{% highlight C# %}

SfSparkChart chart = new SfSparkChart();
SparkDataViewModel viewModel = new SparkDataViewModel();
chart.BindingContext = viewModel;

{% endhighlight %}

{% endtabs %} 

### Populate chart with data

Binding `Data` to the spark chart [ItemsSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfSparkChart.html#Syncfusion_Maui_Toolkit_Charts_SfSparkChart_ItemsSource) property from its BindingContext to create our own spark chart.

{% tabs %}   

{% highlight xaml %}

<chart:SfSparkChart ItemsSource="{Binding Data}" 
                    Stroke="DodgerBlue" 
                    StrokeWidth="2" 
                    ShowMarkers="True" 
                    MarkerSize="6">
. . .
</chart:SfSparkChart>

{% endhighlight %}

{% highlight C# %}

SfSparkChart chart = new SfSparkChart { 
    Stroke = Colors.DodgerBlue, 
    StrokeWidth = 2, 
    ShowMarkers = true, 
    MarkerSize = 6 
};
SparkDataViewModel viewModel = new SparkDataViewModel(); 
chart.ItemsSource = viewModel.Data; 
this.Content = chart;

{% endhighlight %}

{% endtabs %} 

### Enable Tooltip

Trackball behavior provides tooltip-like interaction by displaying the value of the nearest data point on tap or hover.

{% tabs %} 

{% highlight xaml %}

<chart:SfSparkChart ItemsSource="{Binding Data}" ...>
    <chart:SfSparkChart.TrackballBehavior>
        <chart:SparkChartTrackballBehavior 
            ShowTrackballInfo="True"
            ActivationMode="Tap" />
    </chart:SfSparkChart.TrackballBehavior>
</chart:SfSparkChart>

{% endhighlight %}

{% highlight C# %}

chart.TrackballBehavior = new SparkChartTrackballBehavior
{
    ShowTrackballInfo = true,
    ActivationMode = SparkChartActivationMode.Tap
};

{% endhighlight %}

{% endtabs %} 

![Spark chart in .NET MAUI Chart]()

You can find the complete getting started sample from this [link](https://github.com/SyncfusionExamples/GettingStarted_FunnelChart_MAUI).