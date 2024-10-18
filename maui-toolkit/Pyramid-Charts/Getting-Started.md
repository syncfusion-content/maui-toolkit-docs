---
layout: post
title: Getting Started with .NET MAUI Chart control | Syncfusion
description: Learn here all about getting started with Syncfusion .NET MAUI Chart (SfPyramidChart) control, its elements, and more.
platform: maui-toolkit
control: SfPyramidChart
documentation: ug
---

# Getting Started with .NET MAUI Pyramid Chart

This section explains how to populate the Pyramid Chart with data, including adding a title, data labels, a legend, and tooltips. It also covers the essential aspects needed to get started with the Pyramid Chart.

## Prerequisites

Before proceeding, ensure that the following are set up:
1. [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later is installed.
2. A .NET MAUI development environment is configured using either:
    - Visual Studio 2022 (version 17.8 or later), or
    - Visual Studio Code, with the .NET MAUI workload installed and configured. For more information on setting up Visual Studio Code with .NET MAUI, see the official [documentation.](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-8.0&tabs=visual-studio-code)

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

1. In **Solution Explorer,** `right-click` the project and choose **Manage NuGet Packages.**
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

### Visual Studio Code

1. Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (backtick) to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your .csproj file is located.
3. Run the command `dotnet add package Syncfusion.Maui.Toolkit` to install the Syncfusion .NET MAUI Toolkit NuGet package.
4. To ensure all dependencies are installed, run `dotnet restore`.

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

## Step 4: Add .NET MAUI Pyramid Chart

1. Import the `Syncfusion.Maui.Toolkit.Charts` namespace into your code.
2. Initialize an instance of the `SfPyramidChart` control.

{% tabs %}

{% highlight XAML %}

<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.Charts;assembly=Syncfusion.Maui.Toolkit"
             x:Class="GettingStarted.MainPage">

        <chart:SfPyramidChart/>

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
        this.Content = chart;
    }
}

{% endhighlight %}

{% endtabs %}

### Initialize view model

Define a simple data model to represent a data point in the chart:

{% tabs %}  

{% highlight c# %}

public class StageModel
{
    public string Name { get; set; }
    public double Value { get; set; }
}

{% endhighlight %} 

{% endtabs %} 

Next, create a `StageViewModel` class and initialize a list of `StageModel` objects:

{% tabs %}  

{% highlight c# %}

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
        StageViewModel viewModel = new StageViewModel();
        chart.BindingContext = viewModel;
        this.Content = chart;
    }
}

{% endhighlight %}

{% endtabs %} 

### Populate chart with data

Binding `Data` to the pyramid chart [ItemsSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPyramidChart.html#Syncfusion_Maui_Toolkit_Charts_SfPyramidChart_ItemsSource) property from its BindingContext to create our own pyramid chart.

{% tabs %}   

{% highlight xaml %}

<chart:SfPyramidChart ItemsSource = "{Binding Data}" 
                      XBindingPath = "Name" 
                      YBindingPath = "Value"/>
. . .            
</chart:SfPyramidChart>

{% endhighlight %}

{% highlight C# %}

SfPyramidChart chart = new SfPyramidChart();
ViewModel viewModel = new ViewModel();
chart.BindingContext = viewModel;
chart.ItemsSource = viewModel.Data;
chart.XBindingPath = "Name";
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
        <Label Text = "Pyramid Stages"/>
    </chart:SfPyramidChart.Title>
    . . .
</chart:SfPyramidChart>

{% endhighlight %}

{% highlight C# %}

SfPyramidChart chart = new SfPyramidChart();
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

<chart:SfPyramidChart ShowDataLabels = "True">
    . . .
</chart:SfPyramidChart>

{% endhighlight %}

{% highlight C# %}

SfPyramidChart chart = new SfPyramidChart();
. . .
chart.ShowDataLabels = true;
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
chart.Legend = new ChartLegend();
this.Content = chart;
{% endhighlight %}

{% endtabs %} 

### Enable Tooltip

Tooltips are used to show information about the segment, when mouse over on it. Enable tooltip by setting the chart [EnableTooltip](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPyramidChart.html#Syncfusion_Maui_Toolkit_Charts_SfPyramidChart_EnableTooltip) property as true.

{% tabs %} 

{% highlight xaml %}

<chart:SfPyramidChart EnableTooltip = "True">
    . . .
</chart:SfPyramidChart>

{% endhighlight %}

{% highlight C# %}

SfPyramidChart chart = new SfPyramidChart();
. . .
chart.EnableTooltip = true;
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

    <chart:SfPyramidChart ItemsSource = "{Binding Data}" 
                       ShowDataLabels = "True" 
                       EnableTooltip = "True" 
                       XBindingPath = "Name" 
                       YBindingPath = "Value">

        <chart:SfPyramidChart.Title>
            <Label Text = "Pyramid Stages"/>
        </chart:SfPyramidChart.Title>

        <chart:SfPyramidChart.BindingContext>
            <model:ChartViewModel/>
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
        ViewModel viewModel = new ViewModel();
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