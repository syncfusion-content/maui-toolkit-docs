---
layout: post
title: Getting Started with .NET MAUI Chart control | Syncfusion
description: Learn here all about getting started with Syncfusion® .NET MAUI Chart (SfPyramidChart) control, its elements, and more.
platform: maui-toolkit
control: SfPyramidChart
documentation: ug
---

# Getting Started with .NET MAUI Pyramid Chart

This section explains how to populate the Pyramid Chart with data, including adding a title, data labels, a legend, and tooltips. It also covers the essential aspects needed to get started with the [Pyramid Chart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPyramidChart.html).

{% tabcontents %}
{% tabcontent Visual Studio %}

## Prerequisites

Before proceeding, ensure that the following are set up:

1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) or later is installed.
2. Set up a .NET MAUI environment with Visual Studio 2026 (v18.0.0 or later).

## Step 1: Create a new .NET MAUI project

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Then, click **Next.**
3. Select the .NET framework version and click **Create.**

## Step 2: Install the Syncfusion<sup>®</sup> MAUI Toolkit Package

1. In **Solution Explorer,** right-click the project and choose **Manage NuGet Packages.**
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

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

## Step 2: Install the Syncfusion<sup>®</sup> MAUI Toolkit Package

1. Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (backtick) to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your .csproj file is located.
3. Run the command `dotnet add package Syncfusion.Maui.Toolkit` to install the Syncfusion<sup>®</sup> .NET MAUI Toolkit NuGet package.
4. To ensure all dependencies are installed, run `dotnet restore`.

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

{% endtabcontent %}
{% endtabcontents %}

## Step 3: Register the handler

Make sure to add the namespace.
 
{% highlight MauiProgram.cs %}
using Syncfusion.Maui.Toolkit.Hosting;
{% endhighlight %}
 
Register the Syncfusion core handler in your CreateMauiApp method of `MauiProgram.cs` file to use Syncfusion controls.
 
{% highlight MauiProgram.cs %}
builder.ConfigureSyncfusionToolkit();
{% endhighlight %}

## Step 4: Create the Model

Define a simple data model to represent a data point in the chart:

{% tabs %}  

{% highlight C# %}

public class StageModel
{
    public string Name { get; set; }
    public double Value { get; set; }
}

{% endhighlight %} 

{% endtabs %} 

## Step 5: Create the ViewModel

Next, create a `StageViewModel` class and initialize a list of `StageModel` objects:

{% tabs %}  

{% highlight C# %}

public class StageViewModel
{
    public List<StageModel> Data { get; set; }
    public StageViewModel()
    {
        Data = new List<StageModel>()
        {
            new StageModel(){Name = "Stage A", Value = 12},
            new StageModel(){Name = "Stage B", Value = 21},
            new StageModel(){Name = "Stage C", Value = 29},
            new StageModel(){Name = "Stage D", Value = 37},
        };
    }
}

{% endhighlight %} 

{% endtabs %} 

## Step 6: Import Pyramid Chart namespace

Add the following namespace in your XAML or C#.
{% tabs %}
{% highlight xaml %}

xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.Charts;assembly=Syncfusion.Maui.Toolkit"

{% endhighlight %}
{% highlight c# %}

using Syncfusion.Maui.Toolkit.Charts;

{% endhighlight %}
{% endtabs %}

## Step 7: Add the Pyramid Chart component

Binding `Data` to the pyramid chart [ItemsSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPyramidChart.html#Syncfusion_Maui_Toolkit_Charts_SfPyramidChart_ItemsSource) property from its BindingContext to create our own pyramid chart.

{% tabs %} 
{% highlight xaml %}

<chart:SfPyramidChart ItemsSource="{Binding Data}" 
                       ShowDataLabels="True" 
                       EnableTooltip="True" 
                       XBindingPath="Name" 
                       YBindingPath="Value">
        <chart:SfPyramidChart.Title>
            <Label Text="Pyramid Stages"/>
        </chart:SfPyramidChart.Title>
        <chart:SfPyramidChart.BindingContext>
            <model:StageViewModel/>
        </chart:SfPyramidChart.BindingContext>
        <chart:SfPyramidChart.Legend>
            <chart:ChartLegend/>
        </chart:SfPyramidChart.Legend>
    </chart:SfPyramidChart>

{% endhighlight %}
{% highlight C# %}

SfPyramidChart chart = new SfPyramidChart();
chart.Title = new Label()
{
    Text = "Pyramid Stages"
};
chart.Legend = new ChartLegend();
StageViewModel viewModel = new StageViewModel();
chart.BindingContext = viewModel;

chart.ItemsSource = viewModel.Data;
chart.XBindingPath = "Name";
chart.YBindingPath = "Value";
chart.EnableTooltip = true;
chart.ShowDataLabels = true;
this.Content = chart;

{% endhighlight %}
{% endtabs %}

![Pyramid chart in .NET MAUI Chart](Getting-Started_Images/MAUI_pyramid_chart.png)

You can download the Pyramid Chart Getting Started sample from [here](https://github.com/SyncfusionExamples/maui-toolkit-samples/tree/master/PyramidChart/GettingStarted).