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

1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later is installed.
2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.8 or later).

## Step 1: Create a new .NET MAUI project

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Then, click **Next.**
3. Select the .NET framework version and click **Create.**

## Step 2: Install the Syncfusion<sup>®</sup> MAUI Toolkit Package

1. In **Solution Explorer,** right-click the project and choose **Manage NuGet Packages.**
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

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

## Step 4: Add .NET MAUI Pyramid Chart

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Charts` namespace into your code.

2. Initialize an instance of the [SfPyramidChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPyramidChart.html) control.

{% tabs %}

{% highlight xaml %}

<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.Charts;assembly=Syncfusion.Maui.Toolkit"
             x:Class="GettingStarted.MainPage">

        <chart:SfPyramidChart/>

</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.Charts; // Import the namespace required for Syncfusion MAUI Toolkit Chart.

. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfPyramidChart chart = new SfPyramidChart(); // Create an instance of the SfPyramidChart.
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

## Step 2: Install the Syncfusion<sup>®</sup> MAUI Toolkit Package

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

## Step 4: Add .NET MAUI Pyramid Chart

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Charts` namespace into your code.
2. Initialize an instance of the [SfPyramidChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPyramidChart.html) control.

{% tabs %}

{% highlight xaml %}

<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.Charts;assembly=Syncfusion.Maui.Toolkit"
             x:Class="GettingStarted.MainPage">

        <chart:SfPyramidChart/>

</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.Charts; // Import the namespace required for Syncfusion MAUI Toolkit Chart.

. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfPyramidChart chart = new SfPyramidChart(); // Create an instance of the SfPyramidChart.
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

## Step 4: Add .NET MAUI Pyramid Chart

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Charts` namespace into your code.
2. Initialize an instance of the [SfPyramidChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPyramidChart.html) control.

{% tabs %}

{% highlight xaml %}

<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.Charts;assembly=Syncfusion.Maui.Toolkit"
             x:Class="GettingStarted.MainPage">

        <chart:SfPyramidChart/>

</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.Charts; // Import the namespace required for Syncfusion MAUI Toolkit Chart.

. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfPyramidChart chart = new SfPyramidChart(); // Create an instance of the SfPyramidChart.
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

{% highlight C# %}

public class StageModel
{
    public string Name { get; set; }
    public double Value { get; set; }
}

{% endhighlight %} 

{% endtabs %} 

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

Set the `StageViewModel` instance as the `BindingContext` of your view to bind the `StageViewModel` properties to the chart:
 
N> If you prefer to set the `BindingContext` in XAML, make sure to add the appropriate namespace for the `StageViewModel` class in your XAML page.

{% tabs %} 

{% highlight xaml %}

<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.Charts;assembly=Syncfusion.Maui.Toolkit"
             xmlns:model="clr-namespace:GettingStarted"
             x:Class="GettingStarted.MainPage">
    <chart:SfPyramidChart>
        <chart:SfPyramidChart.BindingContext>
            <model:StageViewModel/>
        </chart:SfPyramidChart.BindingContext>
    </chart:SfPyramidChart>
</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.Charts;

. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfPyramidChart chart = new SfPyramidChart();
        StageViewModel viewModel = new StageViewModel(); // Create an instance of the view model.
        chart.BindingContext = viewModel; // Set the view model as the BindingContext of the chart.
        this.Content = chart;
    }
}

{% endhighlight %}

{% endtabs %} 

### Populate chart with data

Binding `Data` to the pyramid chart [ItemsSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPyramidChart.html#Syncfusion_Maui_Toolkit_Charts_SfPyramidChart_ItemsSource) property from its BindingContext to create our own pyramid chart.

{% tabs %}   

{% highlight xaml %}

<chart:SfPyramidChart ItemsSource="{Binding Data}" 
                      XBindingPath="Name" 
                      YBindingPath="Value"/>
. . .            
</chart:SfPyramidChart>

{% endhighlight %}

{% highlight C# %}

SfPyramidChart chart = new SfPyramidChart();
StageViewModel viewModel = new StageViewModel();
chart.BindingContext = viewModel;

// Bind the chart's data source to the ViewModel's data collection.
chart.ItemsSource = viewModel.Data; 

// Set X-axis binding to the 'Name' property in the ViewModel.
chart.XBindingPath = "Name";

// Set Y-axis binding to the 'Value' property in the ViewModel.
chart.YBindingPath = "Value"; 
this.Content = chart;

{% endhighlight %}

{% endtabs %} 

### Add a title

The title of the chart acts as the title to provide quick information to the user about the data being plotted in the chart. You can set the title using the [Title](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartBase.html#Syncfusion_Maui_Toolkit_Charts_ChartBase_Title) property of the pyramid chart as follows.

{% tabs %} 

{% highlight xaml %}

<chart:SfPyramidChart>
    <chart:SfPyramidChart.Title>
        <Label Text="Pyramid Stages"/>
    </chart:SfPyramidChart.Title>
    . . .
</chart:SfPyramidChart>

{% endhighlight %}

{% highlight C# %}

SfPyramidChart chart = new SfPyramidChart();

// Set the title of the chart.
chart.Title = new Label()
{
    Text = "Pyramid Stages",
};
this.Content = chart;

{% endhighlight %}

{% endtabs %}  

### Enable the data labels

The [ShowDataLabels](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPyramidChart.html#Syncfusion_Maui_Toolkit_Charts_SfPyramidChart_ShowDataLabels) property of the chart can be used to enable data labels to improve the readability of the pyramid chart. The label visibility is set to `False` by default.

{% tabs %} 

{% highlight xaml %}

<chart:SfPyramidChart ShowDataLabels="True">
    . . .
</chart:SfPyramidChart>

{% endhighlight %}

{% highlight C# %}

SfPyramidChart chart = new SfPyramidChart();
. . .
chart.ShowDataLabels = true; // Enable data labels in the chart.
this.Content = chart;

{% endhighlight %}

{% endtabs %} 

### Enable a legend

The legend provides information about the data point displayed in the pyramid chart. The [Legend](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartBase.html#Syncfusion_Maui_Toolkit_Charts_ChartBase_Legend) property of the chart was used to enable it.

{% tabs %} 

{% highlight xaml %}

<chart:SfPyramidChart>
    . . .
    <chart:SfPyramidChart.Legend>
    <chart:ChartLegend/>
    </chart:SfPyramidChart.Legend>
</chart:SfPyramidChart>

{% endhighlight %}

{% highlight C# %}

SfPyramidChart chart = new SfPyramidChart();
. . .
chart.Legend = new ChartLegend(); // Enable legend in the chart.
this.Content = chart;

{% endhighlight %}

{% endtabs %} 

### Enable Tooltip

Tooltips are used to show information about the segment, when mouse over on it. Enable tooltip by setting the chart [EnableTooltip](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPyramidChart.html#Syncfusion_Maui_Toolkit_Charts_SfPyramidChart_EnableTooltip) property as true.

{% tabs %} 

{% highlight xaml %}

<chart:SfPyramidChart EnableTooltip="True">
    . . .
</chart:SfPyramidChart>

{% endhighlight %}

{% highlight C# %}

SfPyramidChart chart = new SfPyramidChart();
. . .
chart.EnableTooltip = true; // Enable tooltip in the chart.
this.Content = chart;

{% endhighlight %}

{% endtabs %}

The following code example gives you the complete code of above configurations.

{% tabs %} 

{% highlight xaml %}

<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.Charts;assembly=Syncfusion.Maui.Toolkit"
             xmlns:model="clr-namespace:GettingStarted"
             x:Class="GettingStarted.MainPage">

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
 
</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.Charts;

. . .

public partial class MainPage : ContentPage
{   
    public MainWindow()
    {
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
    }
}

{% endhighlight %}

{% endtabs %}

![Pyramid chart in .NET MAUI Chart](Getting-Started_Images/MAUI_pyramid_chart.png)

You can find the complete getting started sample from this [link](https://github.com/SyncfusionExamples/maui-toolkit-samples/tree/master/PyramidChart/GettingStarted).