---
layout: post
title: Getting Started with .NET MAUI Spark Chart control | Syncfusion
description: Learn here all about getting started with Syncfusion® .NET MAUI Chart (SfSparkChart) control, its elements, and more.
platform: maui-toolkit
control: SfSparkChart
documentation: ug
---

# Getting Started with .NET MAUI Spark Charts (SparkChart)

This section explains how to populate the spark chart with data, configure the chart type, enable markers and data labels, and customize its appearance. It also covers the essential aspects for getting started with the spark chart.

{% tabcontents %}
{% tabcontent Visual Studio %}

## Prerequisites

Before proceeding, ensure that the following are set up:

1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later.
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

## Step 4: Add .NET MAUI Spark Charts

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.SparkCharts` namespace into your code.
2. Initialize an instance of the [SfSparkLineChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkLineChart.html) control.

{% tabs %} 
{% highlight xaml %}

<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:sparkchart="clr-namespace:Syncfusion.Maui.Toolkit.SparkCharts;assembly=Syncfusion.Maui.Toolkit"
             x:Class="GettingStarted.MainPage">

        <sparkchart:SfSparkLineChart/>

</ContentPage>
 
{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.SparkCharts; 

. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfSparkLineChart sparkchart = new SfSparkLineChart(); 
        this.Content = sparkchart; 
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
3. Ensure that the .NET MAUI extension is installed and configured as described [here](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-8.0&tabs=visual-studio-code)

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

## Step 4: Add .NET MAUI Spark Charts

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.SparkCharts` namespace.
2. Initialize [SfSparkLineChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkLineChart.html).

{% tabs %} 
{% highlight xaml %}

<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:sparkchart="clr-namespace:Syncfusion.Maui.Toolkit.SparkCharts;assembly=Syncfusion.Maui.Toolkit"
             x:Class="GettingStarted.MainPage">

        <sparkchart:SfSparkLineChart/>

</ContentPage>
 
{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.SparkCharts; 

. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfSparkLineChart sparkchart = new SfSparkLineChart(); 
        this.Content = sparkchart; 
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

## Step 4: Add .NET MAUI Spark Charts

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.SparkCharts` namespace.
2. Initialize [SfSparkLineChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkLineChart.html).

{% tabs %} 
{% highlight xaml %}

<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:sparkchart="clr-namespace:Syncfusion.Maui.Toolkit.SparkCharts;assembly=Syncfusion.Maui.Toolkit"
             x:Class="GettingStarted.MainPage">

        <sparkchart:SfSparkLineChart/>

</ContentPage>
 
{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.SparkCharts;

. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfSparkLineChart sparkchart = new SfSparkLineChart();
        this.Content = sparkchart;
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

Next, create a `SparkChartViewModel` class that holds a list of `SparkDataModel` objects as follows.

{% tabs %}  

{% highlight c# %}

public class SparkChartViewModel
{
    public List<SparkDataModel> Data { get; set; }

    public SparkChartViewModel()
    {
        Data = new List<SparkDataModel>()
        {
            new SparkDataModel(){ Value = 5000},
            new SparkDataModel(){ Value = 9000},
            new SparkDataModel(){ Value = 5000},
            new SparkDataModel(){ Value = 0},
            new SparkDataModel(){ Value = 3000},
            new SparkDataModel(){ Value = -4000},
            new SparkDataModel(){ Value = 5000},
            new SparkDataModel(){ Value = 0},
            new SparkDataModel(){ Value = 9000},
            new SparkDataModel(){ Value = -9000},
        };
    }
}

{% endhighlight %} 

{% endtabs %} 

Create a `SparkChartViewModel` instance and set it as the spark chart's `BindingContext`. This enables property binding from the `SparkChartViewModel` class.

N> Add the namespace of the `SparkChartViewModel` class to your XAML Page, if you prefer to set `BindingContext` in XAML.

{% tabs %} 

{% highlight xaml %}

<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:sparkchart="clr-namespace:Syncfusion.Maui.Toolkit.SparkCharts;assembly=Syncfusion.Maui.Toolkit"
             xmlns:model="clr-namespace:GettingStarted"
             x:Class="GettingStarted.MainPage">
    <sparkchart:SfSparkLineChart>
        <sparkchart:SfSparkLineChart.BindingContext>
            <model:SparkChartViewModel/>
        </sparkchart:SfSparkLineChart.BindingContext>
    </sparkchart:SfSparkLineChart>
</ContentPage>

{% endhighlight %}

{% highlight C# %}

SfSparkLineChart sparkchart = new SfSparkLineChart();
SparkChartViewModel viewModel = new SparkChartViewModel();
sparkchart.BindingContext = viewModel;

{% endhighlight %}

{% endtabs %} 

### Populate chart with data

Binding `Data` to the spark chart [ItemsSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkChart.html#Syncfusion_Maui_Toolkit_SparkCharts_SfSparkChart_ItemsSource) property from its BindingContext to create our own spark chart.

{% tabs %}

{% highlight xaml %}

<sparkchart:SfSparkLineChart ItemsSource="{Binding Data}" 
                    YBindingPath="Value">
. . .
</sparkchart:SfSparkLineChart>

{% endhighlight %}

{% highlight c# %}

SfSparkLineChart sparkchart = new SfSparkLineChart()
{
    ItemsSource = new SparkChartViewModel().Data,
    YBindingPath = "Value",
};

this.Content = sparkchart;

{% endhighlight %}

{% endtabs %}

The following code example gives you the complete code of above configurations.

{% tabs %} 

{% highlight xaml %}

ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:sparkchart="clr-namespace:Syncfusion.Maui.Toolkit.SparkCharts;assembly=Syncfusion.Maui.Toolkit"
             xmlns:model="clr-namespace:GettingStarted"
             x:Class="GettingStarted.MainPage">

    <sparkchart:SfSparkLineChart ItemsSource="{Binding Data}" 
            YBindingPath="Value">
        <sparkchart:SfSparkLineChart.BindingContext>
            <model:SparkChartViewModel/>
        </sparkchart:SfSparkLineChart.BindingContext>

    </sparkchart:SfSparkLineChart>

</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.SparkCharts;

. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SparkChartViewModel viewModel = new SparkChartViewModel();
        SfSparkLineChart sparkchart = new SfSparkLineChart()
        {
            ItemsSource = viewModel.Data,
            YBindingPath = "Value",
            BindingContext = viewModel;
        };
        this.Content = sparkchart;
    }
} 

{% endhighlight %}

{% endtabs %}

The following spark chart is created as a result of the previous codes.

![Spark Line Chart in MAUI Spark Chart](getting_started_images/MAUI_Spark_Chart.png)

You can find the complete getting started sample from this [link](https://github.com/SyncfusionExamples/maui-toolkit-samples/tree/master/SparkChart/GettingStarted).
