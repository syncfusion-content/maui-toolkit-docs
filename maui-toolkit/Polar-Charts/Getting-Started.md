---
layout: post
title: Getting Started with .NET MAUI Chart Control | Syncfusion
description: This section explains about the getting started with Syncfusion .NET MAUI Chart (SfPolarChart) control.
platform: maui-toolkit
control: SfPolarChart
documentation: ug
---

# Getting Started with .NET MAUI Polar Chart

This section explains how to populate the Polar Chart with data, including adding a title, data labels, a legend, tooltips, and markers. It also covers the essential aspects needed to get started with the Polar Chart.

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
3. Run the following command to install the Syncfusion .NET MAUI Toolkit NuGet package:
  
{% tabs %}

{% highlight sh  %}

    dotnet add package Syncfusion.Maui.Toolkit

{% endhighlight %}

{% endtabs %}

4. To ensure all dependencies are installed, run:

{% tabs %}

{% highlight sh  %}

    dotnet restore
    
{% endhighlight %}

{% endtabs %}

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

## Step 4: Add .NET MAUI Cartesian Chart

1. Import the `Syncfusion.Maui.Toolkit.Charts` namespace into your code.
2. Initialize an instance of the `SfPolarChart` control.

{% tabs %}

{% highlight XAML %}

<ContentPage   
            
    xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.Charts;assembly=Syncfusion.Maui.Toolkit">

        <chart:SfPolarChart/>

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
        SfPolarChart chart = new SfPolarChart();
        this.Content = chart;
    }
}

{% endhighlight %}

{% endtabs %}

### Initialize Chart axis

[ChartAxis](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAxis.html) is used to locate the data points inside the chart area. The [PrimaryAxis](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPolarChart.html#Syncfusion_Maui_Charts_SfPolarChart_PrimaryAxis) and [SecondaryAxis](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPolarChart.html#Syncfusion_Maui_Charts_SfPolarChart_SecondaryAxis) properties of the chart are used to initialize the axis for the chart.

{% tabs %} 

{% highlight xaml %} 

<chart:SfPolarChart>                            
    <chart:SfPolarChart.PrimaryAxis>
        <chart:CategoryAxis/>
    </chart:SfPolarChart.PrimaryAxis>

    <chart:SfPolarChart.SecondaryAxis>
        <chart:NumericalAxis/>
    </chart:SfPolarChart.SecondaryAxis>                       
</chart:SfPolarChart>

{% endhighlight %}

{% highlight C# %} 

SfPolarChart chart = new SfPolarChart();
CategoryAxis primaryAxis = new CategoryAxis();
chart.PrimaryAxis = primaryAxis;
NumericalAxis secondaryAxis = new NumericalAxis();
chart.SecondaryAxis = secondaryAxis;

{% endhighlight %}

{% endtabs %} 

### Populate Chart with data

To create a polar chart, you can add a [PolarLineSeries](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.PolarLineSeries.html) to the polar chart [Series](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPolarChart.html#Syncfusion_Maui_Charts_SfPolarChart_Series) property of the chart, and  then bind the `PlantData` property of the above `ViewModel` to the `PolarLineSeries.ItemsSource` as follows.

N> In order to plot the series, the [XBindingPath](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartSeries.html#Syncfusion_Maui_Charts_ChartSeries_XBindingPath) and [YBindingPath](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.XYDataSeries.html#Syncfusion_Maui_Charts_XYDataSeries_YBindingPath) properties need to be configured correctly. These properties allow the chart to retrieve values from the corresponding properties in the data model.

{% tabs %}   

{% highlight xaml %}

<chart:SfPolarChart>
    <chart:SfPolarChart.PrimaryAxis>
        <chart:CategoryAxis>
        </chart:CategoryAxis>
    </chart:SfPolarChart.PrimaryAxis>

    <chart:SfPolarChart.SecondaryAxis>
        <chart:NumericalAxis Maximum="100">
        </chart:NumericalAxis>
    </chart:SfPolarChart.SecondaryAxis>

    <chart:PolarLineSeries  ItemsSource="{Binding PlantDetails}" XBindingPath="Direction" YBindingPath="Tree"/>
        
    <chart:PolarLineSeries  ItemsSource="{Binding PlantDetails}" XBindingPath="Direction" YBindingPath="Weed"/>

    <chart:PolarLineSeries  ItemsSource="{Binding PlantDetails}" XBindingPath="Direction" YBindingPath="Flower"/>
</chart:SfPolarChart>

{% endhighlight %}

{% highlight C# %}

SfPolarChart chart = new SfPolarChart();

// Initializing primary axis
CategoryAxis primaryAxis = new CategoryAxis();
chart.PrimaryAxis = primaryAxis;

//Initializing secondary Axis
NumericalAxis secondaryAxis = new NumericalAxis()
{
    Maximum="100"
};
chart.SecondaryAxis = secondaryAxis;

//Initialize the series
PolarLineSeries series1 = new PolarLineSeries();
series1.ItemsSource = (new ViewModel()).PlantDetails;
series1.XBindingPath = "Direction";
series1.YBindingPath = "Tree";

PolarLineSeries series2 = new PolarLineSeries();
series2.ItemsSource = (new ViewModel()).PlantDetails;
series2.XBindingPath = "Direction";
series2.YBindingPath = "Weed";

PolarLineSeries series3 = new PolarLineSeries();
series3.ItemsSource = (new ViewModel()).PlantDetails;
series3.XBindingPath = "Direction";
series3.YBindingPath = "Flower";

//Adding Series to the Chart Series Collection
chart.Series.Add(series1);
chart.Series.Add(series2);
chart.Series.Add(series3);

{% endhighlight %}

{% endtabs %} 

### Add a title

The title of the chart provides quick information to the user about the data being plotted in the chart. The [Title](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartBase.html#Syncfusion_Maui_Charts_ChartBase_Title) property is used to set the title for the chart as follows.

{% tabs %} 

{% highlight xaml %}

<Grid>
    <chart:SfPolarChart>
        <chart:SfPolarChart.Title>
            <Label Text="Plant Analysis" HorizontalTextAlignment="Center"/>
        </chart:SfPolarChart.Title> 
    </chart:SfPolarChart>
</Grid>

{% endhighlight %}

{% highlight C# %}

SfPolarChart chart = new SfPolarChart();
chart.Title = new Label
{
    Text = "Plant Analysis",
    HorizontalTextAlignment="Center"
};

{% endhighlight %}

{% endtabs %}  

### Enable the data labels

The [ShowDataLabels](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartSeries.html#Syncfusion_Maui_Charts_ChartSeries_ShowDataLabels) property of series can be used to enable the data labels to enhance the readability of the chart. The label visibility is set to `False` by default.

{% tabs %} 

{% highlight xaml %}

<chart:SfPolarChart>
    . . . 
    <chart:PolarLineSeries  ShowDataLabels="True">
    </chart:PolarLineSeries>
</chart:SfPolarChart>

{% endhighlight %}

{% highlight C# %}

SfPolarChart chart = new SfPolarChart()
. . .
PolarLineSeries series1 = new PolarLineSeries();
series1.ShowDataLabels = true;
chart.Series.Add(series1);

{% endhighlight %}

{% endtabs %}  

### Enable a legend

The legend provides information about the data point displayed in the chart. The [Legend](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartBase.html#Syncfusion_Maui_Charts_ChartBase_Legend) property of the chart was used to enable it.

{% tabs %} 

{% highlight xaml %}

<chart:SfPolarChart>
    . . .
    <chart:SfPolarChart.Legend>
        <chart:ChartLegend/>
    </chart:SfPolarChart.Legend>
    . . .
</chart:SfPolarChart>

{% endhighlight %}

{% highlight C# %}

SfPolarChart chart = new SfPolarChart();
chart.Legend = new ChartLegend(); 

{% endhighlight %}

{% endtabs %}  

N> Additionally, set a label for each series using the `Label` property of the chart series, which will be displayed in the corresponding legend.

{% tabs %} 

{% highlight xaml %}

<chart:SfPolarChart>
    . . .
    <chart:PolarLineSeries  ItemsSource="{Binding PlantDetails}" XBindingPath="Direction" YBindingPath="Tree"
                            Label="Tree"/>

    <chart:PolarLineSeries  ItemsSource="{Binding PlantDetails}" XBindingPath="Direction" YBindingPath="Weed" 
                            Label="Weed"/>

    <chart:PolarLineSeries  ItemsSource="{Binding PlantDetails}" XBindingPath="Direction" YBindingPath="Flower" 
                            Label="Flower"/>
</chart:SfPolarChart>

{% endhighlight %}

{% highlight C# %}

PolarLineSeries series1 = new PolarLineSeries(); 
series1.ItemsSource = (new ViewModel()).PlantDetails;
series1.XBindingPath = "Direction"; 
series1.YBindingPath = "Tree"; 
series1.Label = "Tree";

PolarLineSeries series2 = new PolarLineSeries();
series2.ItemsSource = (new ViewModel()).PlantDetails;
series2.XBindingPath = "Direction";
series2.YBindingPath = "Weed";
series2.Label = "Weed";

PolarLineSeries series3 = new PolarLineSeries();
series3.ItemsSource = (new ViewModel()).PlantDetails;
series3.XBindingPath = "Direction";
series3.YBindingPath = "Flower";
series3.Label = "Flower";

{% endhighlight %}

{% endtabs %}  

### Enable tooltip

Tooltips are used to display information about a segment when a user hovers over it. Enable the tooltip by setting the series [EnableTooltip](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartSeries.html#Syncfusion_Maui_Charts_ChartSeries_EnableTooltip) property to true.

{% tabs %} 

{% highlight xaml %}

<chart:SfPolarChart>
    ...
    <chart:PolarLineSeries EnableTooltip="True"/>
    ...
</chart:SfPolarChart> 

{% endhighlight %}

{% highlight C# %}

PolarLineSeries  series1 = new PolarLineSeries();
series1.EnableTooltip = true;

{% endhighlight %}

{% endtabs %}

The following code example gives you the complete code of above configurations.

{% tabs %} 

{% highlight xaml %}

<ContentPage
    xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
    xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
    x:Class="ChartGettingStarted.MainPage"
    xmlns:chart="clr-namespace:Syncfusion.Maui.Charts;assembly=Syncfusion.Maui.Charts"
    xmlns:model="clr-namespace:ChartGettingStarted">

    <ContentPage.BindingContext>
        <model:ViewModel></model:ViewModel>
    </ContentPage.BindingContext>

    <ContentPage.Content>
        <Grid>
            <chart:SfPolarChart>
                <chart:SfPolarChart.Title>
                    <Label Text="Plant Analysis" HorizontalTextAlignment="Center"/>
                </chart:SfPolarChart.Title>

                <chart:SfPolarChart.Legend>
                    <chart:ChartLegend/>
                </chart:SfPolarChart.Legend>
    
                <chart:SfPolarChart.PrimaryAxis>
                    <chart:CategoryAxis/>                    
                </chart:SfPolarChart.PrimaryAxis>

                <chart:SfPolarChart.SecondaryAxis>
                    <chart:NumericalAxis Maximum="100"/>                   
                </chart:SfPolarChart.SecondaryAxis>

                <chart:PolarLineSeries ItemsSource="{Binding PlantDetails}" XBindingPath="Direction" YBindingPath="Tree" 
                                       Label="Tree" EnableTooltip="True" ShowDataLabels="True"/>

                <chart:PolarLineSeries ItemsSource="{Binding PlantDetails}" XBindingPath="Direction" YBindingPath="Weed" 
                                       Label="Weed" EnableTooltip="True" ShowDataLabels="True"/>

                <chart:PolarLineSeries ItemsSource="{Binding PlantDetails}" XBindingPath="Direction" YBindingPath="Flower" 
                                       Label="Flower" EnableTooltip="True" ShowDataLabels="True"/>
            </chart:SfPolarChart>
        </Grid>
    </ContentPage.Content>
</ContentPage>
 
{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Charts;
namespace ChartGettingStarted
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();            
            SfPolarChart chart = new SfPolarChart();

            chart.Title = new Label
            {
                Text = "Plant Analysis",
                HorizontalTextAlignment="Center"
            };

            CategoryAxis primaryAxis = new CategoryAxis();
            chart.PrimaryAxis = primaryAxis;

            NumericalAxis secondaryAxis = new NumericalAxis()
            {
                Maximum="100"
            };
            chart.SecondaryAxis = secondaryAxis;

            PolarLineSeries  series1 = new PolarLineSeries()
            {
                ItemsSource = (new ViewModel()).PlantDetails,
                XBindingPath = "Direction",
                YBindingPath = "Tree",
                Label="Tree", 
                EnableTooltip="True", 
                ShowDataLabels="True"
            }; 

            PolarLineSeries  series2 = new PolarLineSeries()
            {
                ItemsSource = (new ViewModel()).PlantDetails,
                XBindingPath = "Direction",
                YBindingPath = "Weed",
                Label="Weed", 
                EnableTooltip="True", 
                ShowDataLabels="True"
            }; 

            PolarLineSeries series3 = new PolarLineSeries()
            {
                ItemsSource = (new ViewModel()).PlantDetails,
                XBindingPath = "Direction",
                YBindingPath = "Flower",
                Label="Flower", 
                EnableTooltip="True", 
                ShowDataLabels="True"
            };   

            chart.Series.Add(series1);
            chart.Series.Add(series2);
            chart.Series.Add(series3);
            this.Content = chart;
        }
    }   
}

{% endhighlight %}

{% endtabs %}

The following chart is created as a result of the previous codes.

![Getting started for .NET MAUI Chart](Getting-Started_Images/MAUI_polar_chart.png)

You can find the complete getting started sample from this [link]().