---
layout: post
title: Getting started with .NET MAUI Cartesian Chart control | Syncfusion
description: This section explains about the getting started with Syncfusion® MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
keywords: .net maui cartesian chart, .net maui charting, cartesian chart maui, syncfusion cartesian chart maui, maui chart control, .net maui data visualization, cartesian chart example maui.
---

# Getting Started with .NET MAUI Cartesian Chart

This section explains how to populate the Cartesian chart with data, a title, data labels, a legend, and tooltips, as well as the essential aspects for getting started with the [SfCartesianChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html).

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

1. Install [.NET 9 SDK](Download .NET 9.0 (Linux, macOS, and Windows) | .NET) or later.
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

1. Install [.NET 9 SDK](Download .NET 9.0 (Linux, macOS, and Windows) | .NET) or later.
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

## Step 3: Register the handler

Make sure to add the namespace.
 
{% tabs %}
{% highlight MauiProgram.cs %}
using Syncfusion.Maui.Toolkit.Hosting;
{% endhighlight %}
 
Register the Syncfusion core handler in your CreateMauiApp method of `MauiProgram.cs` file to use Syncfusion controls.
 
{% highlight MauiProgram.cs %}
builder.ConfigureSyncfusionToolkit();
{% endhighlight %}
{% endtabs %}

## Step 4: Create the Model

Define a simple data model to represent a data point in the chart:

{% tabs %}  
{% highlight c# %}

public class PersonModel   
{   
    public string Name { get; set; }
    public double Height { get; set; }
}

{% endhighlight %} 
{% endtabs %} 

## Step 5: Initialize the ViewModel

Next, create a `PersonViewModel` class and initialize a list of `PersonModel` objects:

{% tabs %}  

{% highlight c# %}

public class PersonViewModel  
{
    public List<PersonModel> Data { get; set; }      

    public PersonViewModel()       
    {
        Data = new List<PersonModel>()
        {
            new PersonModel { Name = "David", Height = 170 },
            new PersonModel { Name = "Michael", Height = 96 },
            new PersonModel { Name = "Steve", Height = 65 },
            new PersonModel { Name = "Joel", Height = 182 },
            new PersonModel { Name = "Bob", Height = 134 }
        }; 
    }
 }

{% endhighlight %} 
{% endtabs %} 

## Step 6: Import Cartesian Charts namespace

Add the following namespace in your XAML or C#.
{% tabs %}
{% highlight xaml %}

xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.Charts;assembly=Syncfusion.Maui.Toolkit"

{% endhighlight %}
{% highlight c# %}

using Syncfusion.Maui.Toolkit.Charts;

{% endhighlight %}
{% endtabs %}

## Step 7: Add the Cartesian Chart Component

As we are going to visualize the comparison of heights in the data model, add [ColumnSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ColumnSeries.html) property of chart, and then bind the `Data` property of the above `PersonViewModel` to the `ColumnSeries.ItemsSource` as follows.

N> The Cartesian chart has [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html#Syncfusion_Maui_Toolkit_Charts_SfCartesianChart_Series) as its default content.

N> You need to set [XBindingPath](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartSeries.html#Syncfusion_Maui_Toolkit_Charts_ChartSeries_XBindingPath) and [YBindingPath](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.XYDataSeries.html#Syncfusion_Maui_Toolkit_Charts_XYDataSeries_YBindingPath) properties so that chart will fetch values from the respective properties in the data model to plot the series. 

{% tabs %} 
{% highlight xaml %}
    <chart:SfCartesianChart>

        <chart:SfCartesianChart.Title>
            <Label Text="Height Comparison"/>
        </chart:SfCartesianChart.Title>

        <chart:SfCartesianChart.Legend>
            <chart:ChartLegend/>
        </chart:SfCartesianChart.Legend>

        <chart:SfCartesianChart.XAxes>
            <chart:CategoryAxis>
                <chart:CategoryAxis.Title>
                    <chart:ChartAxisTitle Text="Name"/>
                </chart:CategoryAxis.Title>
            </chart:CategoryAxis>
        </chart:SfCartesianChart.XAxes>

        <chart:SfCartesianChart.YAxes>
            <chart:NumericalAxis>
                <chart:NumericalAxis.Title>
                    <chart:ChartAxisTitle Text="Height(in cm)"/>
                </chart:NumericalAxis.Title>
            </chart:NumericalAxis>
        </chart:SfCartesianChart.YAxes>

        <!--Initialize the series for chart-->
        <chart:ColumnSeries ItemsSource="{Binding Data}"
                            XBindingPath="Name" 
                            YBindingPath="Height"
                            EnableTooltip="True"
                            ShowDataLabels="True"
                            Label="Height">
            <chart:ColumnSeries.DataLabelSettings>
                <chart:CartesianDataLabelSettings LabelPlacement="Inner"/>
            </chart:ColumnSeries.DataLabelSettings>
        </chart:ColumnSeries>

        <chart:SfCartesianChart.BindingContext>
			<model:PersonViewModel/>
		</chart:SfCartesianChart.BindingContext>

    </chart:SfCartesianChart>
{% endhighlight %}

{% highlight C# %}

    this.BindingContext = new PersonViewModel();   
    SfCartesianChart chart = new SfCartesianChart();

    chart.Title = new Label()
    {
        Text = "Height Comparison"
    };

    chart.Legend = new ChartLegend ();

    // Initializing primary axis
    CategoryAxis primaryAxis = new CategoryAxis();
    primaryAxis.Title = new ChartAxisTitle()
    {
        Text = "Name",
    };
    chart.XAxes.Add(primaryAxis);

    //Initializing secondary Axis
    NumericalAxis secondaryAxis = new NumericalAxis();
    secondaryAxis.Title = new ChartAxisTitle()
    {
        Text= "Height(in cm)",
    };
    chart.YAxes.Add(secondaryAxis);

    //Initialize the two series for SfChart
    ColumnSeries series = new ColumnSeries()
    {
        ItemsSource = (new PersonViewModel()).Data,
        XBindingPath = "Name",
        YBindingPath = "Height",
        ShowDataLabels = true,
        EnableTooltip = true,
        Label = "Height",
        DataLabelSettings = new CartesianDataLabelSettings()
        {
            LabelPlacement = DataLabelPlacement.Inner
        }              
    };  

    //Adding Series to the Chart Series Collection
    chart.Series.Add(series);
    this.Content = chart;

{% endhighlight %}
{% endtabs %}

The following chart is created as a result of the previous codes.

![Getting started for .NET MAUI Chart](Getting-Started_Images/MAUI_chart.jpg)

You can find the complete Cartesian Chart getting started sample from this [link](https://github.com/SyncfusionExamples/maui-toolkit-samples/tree/master/CartesianChart/GettingStarted).