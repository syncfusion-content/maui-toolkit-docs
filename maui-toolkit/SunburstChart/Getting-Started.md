---
layout: post
title: Getting Started with .NET MAUI Sunburst Chart control | Syncfusion
description: Learn how to get started with the Syncfusion<sup>®</sup> .NET MAUI Sunburst Chart control, including setup, data binding, and key features.
platform: maui-toolkit
control: SfSunburstChart
documentation: ug
---

# Getting Started with .NET MAUI Sunburst Chart

This section explains how to populate the sunburst chart with data, a title, data labels, a legend, and a tooltip, as well as the essential aspects of getting started with the `SfSunburstChart`.

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

## Step 2: Install the Syncfusion<sup>®</sup> MAUI Toolkit Package

1. In **Solution Explorer**, right-click the project and choose **Manage NuGet Packages**.
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

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
        .UseMauiApp<App>()
        .ConfigureSyncfusionToolkit()
        .ConfigureFonts(fonts =>
        {
            fonts.AddFont("OpenSans-Regular.ttf", "OpenSansRegular");
        });

        return builder.Build();
    }
}

{% endhighlight %} 
{% endtabs %} 

## Step 4: Add .NET MAUI Sunburst Chart

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.SunburstChart` namespace into your code.
2. Initialize an instance of the `SfSunburstChart` control.

{% tabs %} 
{% highlight xaml %}

<ContentPage   
    . . .
    xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.SunburstChart;assembly=Syncfusion.Maui.Toolkit">

    <chart:SfSunburstChart/>

</ContentPage>
 
{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.SunburstChart;


public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        // Create a new instance of SfSunburstChart which is a type of chart control.           
        SfSunburstChart chart = new SfSunburstChart();
        // Set the newly created chart as the content of the current view.
        this.Content = chart;
    }
}   


{% endhighlight %}
{% endtabs %}

{% endtabcontent %}

{% tabcontent Visual Studio Code %}

## Prerequisites

Before proceeding, ensure that the following are set up:

1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later.
2. Set up a .NET MAUI environment with Visual Studio Code.
3. Ensure that the .NET MAUI extension is installed and configured as described [here](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-8.0&tabs=visual-studio-code).

## Step 1: Create a new .NET MAUI project

1. Open the command palette by pressing `Ctrl+Shift+P` and type **.NET:New Project** and enter.
2. Choose the **.NET MAUI App** template.
3. Select the project location, type the project name and press **Enter**.
4. Then choose **Create project**.

## Step 2: Install the Syncfusion<sup>®</sup> MAUI Toolkit Package

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
        .UseMauiApp<App>()
        .ConfigureSyncfusionToolkit()
        .ConfigureFonts(fonts =>
        {
            fonts.AddFont("OpenSans-Regular.ttf", "OpenSansRegular");
        });

        return builder.Build();
    }
}

{% endhighlight %} 
{% endtabs %} 

## Step 4: Add .NET MAUI Sunburst Chart

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.SunburstChart` namespace into your code.
2. Initialize an instance of the `SfSunburstChart` control.

{% tabs %} 
{% highlight xaml %}

<ContentPage   
    . . .
    xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.SunburstChart;assembly=Syncfusion.Maui.Toolkit">

    <chart:SfSunburstChart/>

</ContentPage>
 
{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.SunburstChart;

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
         // Create a new instance of SfSunburstChart which is a type of chart control.          
        SfSunburstChart chart = new SfSunburstChart();
        // Set the newly created chart as the content of the current view.
        this.Content = chart;
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

## Step 4: Add .NET MAUI sunburst Chart

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.SunburstChart` namespace into your code.
2. Initialize an instance of the `SfSunburstChart` control.

{% tabs %}
{% highlight XAML %}

<ContentPage 
    ...
    xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.SunburstChart;assembly=Syncfusion.Maui.Toolkit">

    <chart:SfSunburstChart/>

</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.SunburstChart;

. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        // Create a new instance of SfSunburstChart which is a type of chart control.
        SfSunburstChart chart = new SfSunburstChart();
        // Set the newly created chart as the content of the current view.
        this.Content = chart;
    }
}

{% endhighlight %}
{% endtabs %}

{% endtabcontent %}
{% endtabcontents %}

### Initialize View Model

Now, let us define a simple data model that represents a data point in the chart.

{% tabs %}  

{% highlight c# %}

public class SunburstModel
{
    public string JobDescription { get; set; }
    public string JobGroup { get; set; }
    public double EmployeesCount { get; set; }
    public string Country { get; set; }
}

{% endhighlight %} 

{% endtabs %} 

Next, create a `SunburstViewModel` class and initialize a list of `SunburstModel` objects as follows.

{% tabs %}  

{% highlight c# %}

public class SunburstViewModel
{
    public ObservableCollection<SunburstModel> DataSource { get; set; }

    public SunburstViewModel()
    {
        this.DataSource = new ObservableCollection<SunburstModel>
        {
            new SunburstModel ( "USA", "Sales", "Executive",  50 ),
            new SunburstModel ( "USA", "Sales", "Analyst",  40 ),
            new SunburstModel ( "USA", "Marketing",  40 ),
            new SunburstModel ( "USA", "Technical", "Testers",  35 ),
            new SunburstModel ( "USA", "Technical", "Developers",  175 ),
            new SunburstModel ( "USA", "Technical", "Developers",  70 ),
            new SunburstModel ( "USA", "Management",  40 ),
            new SunburstModel ( "USA", "Accounts",  60 ),
            new SunburstModel ( "India", "Technical", "Testers",  33 ),
            new SunburstModel ( "India", "Technical", "Developers",  125 ),
            new SunburstModel ( "India", "Technical", "Developers",  60 ),
            new SunburstModel ( "India", "HR Executives",  70 ),
            new SunburstModel ( "India", "Accounts",  45 ),
            new SunburstModel ( "Germany", "Sales", "Executive",  30 ),
            new SunburstModel ( "Germany", "Sales", "Analyst",  40 ),
            new SunburstModel ( "Germany", "Marketing",  50 ),
            new SunburstModel ( "Germany", "Technical", "Testers",  40 ),
            new SunburstModel ( "Germany", "Technical", "Developers",  60 ),
            new SunburstModel ( "Germany", "Technical", "Developers",  27 ),
            new SunburstModel ( "Germany", "Management",  40 ),
            new SunburstModel ( "Germany", "Accounts",  55 ),
            new SunburstModel ( "UK", "Technical", "Testers",  96 ),
            new SunburstModel ( "UK", "Technical", "Developers",  55 ),
            new SunburstModel ( "UK", "HR Executives",  60 ),
            new SunburstModel ( "UK", "Accounts",  45 )
        };
    }    
}

{% endhighlight %} 

{% endtabs %} 

Set the `SunburstViewModel` instance as the `BindingContext` of your page to bind the `SunburstViewModel` properties to the chart.

N> Add the namespace of the `SunburstViewModel` class to your XAML Page, if you prefer to set `BindingContext` in XAML.

{% tabs %} 

{% highlight xaml %} 

<ContentPage
    . . .
    xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.SunburstChart;assembly=Syncfusion.Maui.Toolkit"
    xmlns:model="clr-namespace:SunburstGettingStarted">

    <ContentPage.BindingContext>
        <model:SunburstViewModel></model:SunburstViewModel>
    </ContentPage.BindingContext>

</ContentPage>

{% endhighlight %}

{% highlight C# %} 

this.BindingContext = new SunburstViewModel();

{% endhighlight %}

{% endtabs %} 

### Populate Chart with Data

Bind `DataSource` to the Sunburst chart `ItemsSource` property from its BindingContext to create your Sunburst chart.
Then, add the `SunburstHierarchicalLevel` to `Levels` collection. Each hierarchy level is formed based on the property specified in the `GroupMemberPath` property, and each arc segment size is calculated using the `ValueMemberPath` property.

{% tabs %}   

{% highlight xaml %}
        
<ContentPage
    . . .
    xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.SunburstChart;assembly=Syncfusion.Maui.Toolkit"
    xmlns:model="clr-namespace:SunburstGettingStarted">

    <chart:SfSunburstChart x:Name="sunburst" 
                           ItemsSource="{Binding DataSource}" 
                           ValueMemberPath="EmployeesCount">

        <chart:SfSunburstChart.Levels>
            <chart:SunburstHierarchicalLevel GroupMemberPath="Country"/>
            <chart:SunburstHierarchicalLevel GroupMemberPath="JobDescription"/>
            <chart:SunburstHierarchicalLevel GroupMemberPath="JobGroup"/>
        </chart:SfSunburstChart.Levels>

    </chart:SfSunburstChart>
</ContentPage>

{% endhighlight %}

{% highlight C# %}

SfSunburstChart sunburst = new SfSunburstChart();

sunburst.ItemsSource = (new SunburstViewModel()).DataSource;
sunburst.ValueMemberPath = "EmployeesCount";

sunburst.Levels.Add(new SunburstHierarchicalLevel() { GroupMemberPath = "Country" });
sunburst.Levels.Add(new SunburstHierarchicalLevel() { GroupMemberPath = "JobDescription" });
sunburst.Levels.Add(new SunburstHierarchicalLevel() { GroupMemberPath = "JobGroup" });

this.Content = sunburst;

{% endhighlight %}

{% endtabs %} 

### Add a Title
The title of the sunburst chart provides quick information to the user about the data being plotted in the chart. The `Title` property is used to set title for the sunburst chart as follows.

{% tabs %} 

{% highlight xaml %}

<chart:SfSunburstChart>
    <chart:SfSunburstChart.Title>
        <Label Text="Employees Count"/>
    </chart:SfSunburstChart.Title>
    . . .
</chart:SfSunburstChart>

{% endhighlight %}

{% highlight C# %}

SfSunburstChart sunburst = new SfSunburstChart();
sunburst.Title = new Label()
{
    Text = "Employees Count"
};

this.Content = sunburst;

{% endhighlight %}

{% endtabs %}  

### Enable the Data Labels

The `ShowLabels` property of the chart can be used to enable data labels to improve the readability of the sunburst chart. The label visibility is set to `False` by default.

{% tabs %} 

{% highlight xaml %}

<chart:SfSunburstChart ShowLabels="True">
    . . .
</chart:SfSunburstChart>

{% endhighlight %}

{% highlight C# %}

SfSunburstChart sunburst = new SfSunburstChart();
. . .
sunburst.ShowLabels = true;
this.Content = sunburst;

{% endhighlight %}

{% endtabs %} 

### Enable a Legend

The legend provides information about the data points displayed in the sunburst chart. The `Legend` property of the chart enables the `SunburstLegend`.

{% tabs %} 

{% highlight xaml %}

<chart:SfSunburstChart>
    . . .
    <chart:SfSunburstChart.Legend>
        <chart:SunburstLegend/>
    </chart:SfSunburstChart.Legend>
</chart:SfSunburstChart>

{% endhighlight %}

{% highlight C# %}

SfSunburstChart sunburst = new SfSunburstChart();
. . .
sunburst.Legend = new SunburstLegend();
this.Content = sunburst;

{% endhighlight %}

{% endtabs %} 

### Enable Tooltip

Tooltips are used to display information about a segment when the mouse hovers over it. Enable the tooltips by setting the chart's `EnableTooltip` property to `True`.

{% tabs %} 

{% highlight xaml %}

<sunburst:SfSunburstChart EnableTooltip="True">
    . . .
</sunburst:SfSunburstChart>

{% endhighlight %}

{% highlight C# %}

SfSunburstChart sunburst = new SfSunburstChart();
. . .
sunburst.EnableTooltip = true;
this.Content = sunburst;

{% endhighlight %}

{% endtabs %}

The following code example gives you the complete code of above configurations.

{% tabs %} 

{% highlight xaml %}

<ContentPage
    . . .
    xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.SunburstChart;assembly=Syncfusion.Maui.Toolkit"
    xmlns:model="clr-namespace:SunburstGettingStarted">

    <chart:SfSunburstChart ItemsSource="{Binding DataSource}" 
                           ShowLabels="True"  
                           EnableTooltip="True"
                           ValueMemberPath="EmployeesCount">

        <chart:SfSunburstChart.BindingContext>
            <model:SunburstViewModel/>
        </chart:SfSunburstChart.BindingContext>

        <chart:SfSunburstChart.Title>
            <Label Text="Employees Count"/>
        </chart:SfSunburstChart.Title>

        <chart:SfSunburstChart.Legend>
            <sunburst:SunburstLegend/>
        </chart:SfSunburstChart.Legend> 

        <chart:SfSunburstChart.Levels>
            <chart:SunburstHierarchicalLevel GroupMemberPath="Country"/>
            <chart:SunburstHierarchicalLevel GroupMemberPath="JobDescription"/>
            <chart:SunburstHierarchicalLevel GroupMemberPath="JobGroup"/>
        </chart:SfSunburstChart.Levels>
    </chart:SfSunburstChart>

</ContentPage>
 
{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.SunburstChart;
. . .
public partial class MainPage : ContentPage
{   
    public MainPage()
    {
        SfSunburstChart sunburst = new SfSunburstChart();

        sunburst.ItemsSource = (new SunburstViewModel()).DataSource;
        sunburst.ValueMemberPath = "EmployeesCount";

        sunburst.Title = new Label
        {
            Text = "Employees Count"
        };

        sunburst.Legend = new SunburstLegend();

        sunburst.Levels.Add(new SunburstHierarchicalLevel() { GroupMemberPath = "Country" });
        sunburst.Levels.Add(new SunburstHierarchicalLevel() { GroupMemberPath = "JobDescription" });
        sunburst.Levels.Add(new SunburstHierarchicalLevel() { GroupMemberPath = "JobGroup" });

        sunburst.EnableTooltip = true;
        sunburst.ShowLabels = true;
        
        this.Content = sunburst;
    }
}

{% endhighlight %}

{% endtabs %}

![Getting started sample in MAUI Sunburst Chart.](Getting_started_image/maui_getting_started_image.png)

Find the complete getting started sample from this [link](https://github.com/SyncfusionExamples/GettingStarted_SunburstChart_MAUI).