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

Before proceeding, ensure the following are set up:

1. Install [.NET 9 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) or later.
2. Set up a .NET MAUI environment with Visual Studio 2022 v17.12 or later.

## Step 1: Create a new .NET MAUI project

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Then click **Next**.
3. Select the .NET framework version and click **Create**.

## Step 2: Install the Syncfusion<sup>&reg;</sup> .NET MAUI Toolkit NuGet package

1. In **Solution Explorer,** right-click the project and choose **Manage NuGet Packages.**
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

{% endtabcontent %}
{% tabcontent Visual Studio Code %}

## Prerequisites

Before proceeding, ensure the following are set up:

1. Install [.NET 9 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) or later.
2. Set up a .NET MAUI environment with Visual Studio Code.
3. Ensure that the .NET MAUI workloads are installed and configured as described [here](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-9.0&tabs=visual-studio-code).

## Step 1: Create a new .NET MAUI project

1. Open the command palette by pressing `Ctrl+Shift+P` and type **.NET:New Project** and enter.
2. Choose the **.NET MAUI App** template.
3. Select the project location, type the project name and press **Enter**.
4. Then choose **Create project.**

## Step 2: Install the Syncfusion<sup>&reg;</sup> .NET MAUI Toolkit NuGet package

1. Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (backtick) to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your .csproj file is located.
3. Run the command `dotnet add package Syncfusion.Maui.Toolkit` to install the Syncfusion<sup>®</sup> .NET MAUI Toolkit NuGet package.
4. To ensure all dependencies are installed, run `dotnet restore`.

{% endtabcontent %}
{% tabcontent JetBrains Rider %}

## Prerequisites

Before proceeding, ensure the following are set up:

1. Install [.NET 9 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) or later.
2. Set up a .NET MAUI environment with JetBrains Rider 2024.3 or later.
3. Make sure the MAUI workloads are installed and configured as described [here.](https://www.jetbrains.com/help/rider/MAUI.html#before-you-start)

## Step 1: Create a new .NET MAUI project

1. Go to **File > New Solution,** Select .NET (C#) and choose the .NET MAUI App template.
2. Enter the Project Name, Solution Name, and Location.
3. Select the .NET framework version and click Create.

## Step 2: Install the Syncfusion<sup>®</sup> MAUI Toolkit NuGet package

1. In **Solution Explorer,** right-click the project and choose **Manage NuGet Packages.**
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored. If not, Open the Terminal in Rider and manually run: `dotnet restore`

{% endtabcontent %}
{% endtabcontents %}

## Step 3: Register Syncfusion handler
 
Make sure to add the namespace.
 
{% tabs %}
{% highlight c# %}
using Syncfusion.Maui.Toolkit.Hosting;
{% endhighlight %}
{% endtabs %}
 
Register the Syncfusion toolkit handler in your `CreateMauiApp` method of `MauiProgram.cs` file to use Syncfusion controls.
 
{% tabs %}
{% highlight c# %}
builder.ConfigureSyncfusionToolkit();
{% endhighlight %}
{% endtabs %}

## Step 4: Create the Model

Define a simple data Model to represent a data point in the chart:

{% tabs %}  

{% highlight c# %}

public class SparkDataModel
{
    public double Value { get; set; }
}

{% endhighlight %} 

{% endtabs %} 

## Step 5: Initialize the ViewModel

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

## Step 6: Import Spark Chart namespace

Add the following namespace in your XAML or C#.
{% tabs %}
{% highlight xaml %}

xmlns:sparkchart="clr-namespace:Syncfusion.Maui.Toolkit.SparkCharts;assembly=Syncfusion.Maui.Toolkit"

{% endhighlight %}
{% highlight c# %}

using Syncfusion.Maui.Toolkit.SparkCharts;

{% endhighlight %}
{% endtabs %}

{% endtabcontent %}
{% endtabcontents %}

## Step 7: Add the Spark Charts component

Binding `Data` to the spark chart [ItemsSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SparkCharts.SfSparkChart.html#Syncfusion_Maui_Toolkit_SparkCharts_SfSparkChart_ItemsSource) property from its BindingContext to create our own spark chart.

{% tabs %} 
{% highlight xaml %}

<sparkchart:SfSparkLineChart ItemsSource="{Binding Data}" 
                             YBindingPath="Value">
    <sparkchart:SfSparkLineChart.BindingContext>
        <model:SparkChartViewModel/>
    </sparkchart:SfSparkLineChart.BindingContext>
</sparkchart:SfSparkLineChart>

</ContentPage>

{% endhighlight %}

{% highlight C# %}

SparkChartViewModel viewModel = new SparkChartViewModel();
SfSparkLineChart sparkchart = new SfSparkLineChart()
{
    ItemsSource = viewModel.Data,
    YBindingPath = "Value",
    BindingContext = viewModel;
};
this.Content = sparkchart;

{% endhighlight %}

{% endtabs %}

![Spark Line Chart in MAUI Spark Chart](getting_started_images/MAUI_Spark_Chart.png)

You can download the Spark Chart Getting Started sample from [here](https://github.com/SyncfusionExamples/maui-toolkit-samples/tree/master/SparkChart/GettingStarted).
