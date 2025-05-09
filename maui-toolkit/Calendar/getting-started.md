---
layout: post
title: Getting started with MAUI Calendar control | Syncfusion
description: Learn here all about getting started with Syncfusion<sup>&reg;</sup> .NET MAUI Calendar (SfCalendar) control and its basic features.
platform: maui
control: SfCalendar
documentation: ug
---

# Getting Started with the .NET MAUI Calendar

This section explains how to add the [.NET MAUI Calendar](https://www.syncfusion.com/maui-controls/maui-calendar) control. This section covers only the basic features needed to get started with Syncfusion Calendar. Follow the steps below to add .NET MAUI calendar control to your project.

{% tabcontents %}
{% tabcontent Visual Studio %}

## Prerequisites

Before proceeding, ensure the following are set up:
1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later is installed.
2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.8 or later).

## Step 1: Create a New .NET MAUI Project

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Then click **Next**.
3. Select the .NET framework version and click **Create**.

## Step 2: Install the Syncfusion<sup>&reg;</sup> .NET MAUI Tookit NuGet Package

1. In **Solution Explorer,** right-click the project and choose **Manage NuGet Packages.**
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

## Step 3: Register the handler

The [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) NuGet is a dependent package for all Syncfusion<sup>&reg;</sup> controls of .NET MAUI. In the **MauiProgram.cs** file, register the handler for Syncfusion<sup>&reg;</sup> toolkit.

{% tabs %}
{% highlight C# tabtitle="MauiProgram.cs" hl_lines="1 10" %}

using Syncfusion.Maui.Toolkit.Hosting;
namespace GettingStarted
{
    public static class MauiProgram
    {
        public static MauiApp CreateMauiApp()
        {
            var builder = MauiApp.CreateBuilder();

            builder.ConfigureSyncfusionToolkit();
            builder
            .UseMauiApp<App>()
            .ConfigureFonts(fonts =>
            {
                fonts.AddFont("OpenSans-Regular.ttf", "OpenSansRegular");
            });

            return builder.Build();
        }
    }
}

{% endhighlight %}
{% endtabs %}

## Step 4: Add .NET MAUI Calendar control

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Calendar` namespace into your code.
2. Initialize [SfCalendar](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Calendar.SfCalendar.html).

{% tabs %}
{% highlight XAML hl_lines="3 5" %}

<ContentPage   
    . . .
    xmlns:calendar="clr-namespace:Syncfusion.Maui.Toolkit.Calendar;assembly=Syncfusion.Maui.Toolkit">

    <calendar:SfCalendar />
</ContentPage>

{% endhighlight %}
{% highlight C# hl_lines="1 9 10" %}

using Syncfusion.Maui.Toolkit.Calendar;
. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfCalendar calendar = new SfCalendar();
        this.Content = calendar;
    }
}

{% endhighlight %}
{% endtabs %}


{% endtabcontent %}
{% tabcontent Visual Studio Code %}

## Prerequisites

Before proceeding, ensure the following are set up:
1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later is installed.
2. Set up a .NET MAUI environment with Visual Studio Code. 
3. Ensure that the .NET MAUI extension is installed and configured as described [here.](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-8.0&tabs=visual-studio-code).

## Step 1: Create a New .NET MAUI Project

1. Open the command palette by pressing `Ctrl+Shift+P` and type **.NET:New Project** and enter.
2. Choose the **.NET MAUI App** template.
3. Select the project location, type the project name and press **Enter**.
4. Then choose **Create project.**

## Step 2: Install the Syncfusion<sup>&reg;</sup> .NET MAUI Toolkit NuGet Package

1. Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (backtick) to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your .csproj file is located.
3. Run the command `dotnet add package Syncfusion.Maui.Toolkit` to install the Syncfusion<sup>®</sup> .NET MAUI Toolkit NuGet package.
4. To ensure all dependencies are installed, run `dotnet restore`.

## Step 3: Register the handler

The [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) NuGet is a dependent package for all Syncfusion<sup>&reg;</sup> controls of .NET MAUI. In the **MauiProgram.cs** file, register the handler for Syncfusion<sup>&reg;</sup> toolkit.

{% tabs %}
{% highlight C# tabtitle="MauiProgram.cs" hl_lines="1 10" %}

using Syncfusion.Maui.Toolkit.Hosting;
namespace GettingStarted
{
    public static class MauiProgram
    {
        public static MauiApp CreateMauiApp()
        {
            var builder = MauiApp.CreateBuilder();

            builder.ConfigureSyncfusionToolkit();
            builder
            .UseMauiApp<App>()
            .ConfigureFonts(fonts =>
            {
                fonts.AddFont("OpenSans-Regular.ttf", "OpenSansRegular");
            });

            return builder.Build();
        }
    }
}

{% endhighlight %}
{% endtabs %}

## Step 4: Add .NET MAUI Calendar control

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Calendar` namespace into your code.
2. Initialize [SfCalendar](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Calendar.SfCalendar.html).

{% tabs %}
{% highlight XAML hl_lines="3 5" %}

<ContentPage   
    . . .
    xmlns:calendar="clr-namespace:Syncfusion.Maui.Toolkit.Calendar;assembly=Syncfusion.Maui.Toolkit">

    <calendar:SfCalendar />
</ContentPage>

{% endhighlight %}
{% highlight C# hl_lines="1 9 10" %}

using Syncfusion.Maui.Toolkit.Calendar;
. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfCalendar calendar = new SfCalendar();
        this.Content = calendar;
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

The [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) NuGet is a dependent package for all Syncfusion<sup>&reg;</sup> controls of .NET MAUI. In the **MauiProgram.cs** file, register the handler for Syncfusion<sup>&reg;</sup> toolkit.

{% tabs %}
{% highlight C# tabtitle="MauiProgram.cs" hl_lines="1 10" %}

using Syncfusion.Maui.Toolkit.Hosting;
namespace GettingStarted
{
    public static class MauiProgram
    {
        public static MauiApp CreateMauiApp()
        {
            var builder = MauiApp.CreateBuilder();

            builder.ConfigureSyncfusionToolkit();
            builder
            .UseMauiApp<App>()
            .ConfigureFonts(fonts =>
            {
                fonts.AddFont("OpenSans-Regular.ttf", "OpenSansRegular");
            });

            return builder.Build();
        }
    }
}

{% endhighlight %}
{% endtabs %}

## Step 4: Add .NET MAUI Calendar control

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Calendar` namespace into your code.
2. Initialize [SfCalendar](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Calendar.SfCalendar.html).

{% tabs %}
{% highlight XAML hl_lines="3 5" %}

<ContentPage   
    . . .
    xmlns:calendar="clr-namespace:Syncfusion.Maui.Toolkit.Calendar;assembly=Syncfusion.Maui.Toolkit">

    <calendar:SfCalendar />
</ContentPage>

{% endhighlight %}
{% highlight C# hl_lines="1 9 10" %}

using Syncfusion.Maui.Toolkit.Calendar;
. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfCalendar calendar = new SfCalendar();
        this.Content = calendar;
    }
}

{% endhighlight %}
{% endtabs %}

{% endtabcontent %}
{% endtabcontents %}

## Change different calendar views

The [.NET MAUI Calendar](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Calendar.SfCalendar.html) control provides four different types of views to display dates, and it can be assigned to the control using the [View](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Calendar.SfCalendar.html#Syncfusion_Maui_Toolkit_Calendar_SfCalendar_View) property. By default, the control is assigned to the [Month](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Calendar.CalendarView.html#Syncfusion_Maui_Toolkit_Calendar_CalendarView_Month) view. Initially, all Calendar views will show the current date.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" %}

<calendar:SfCalendar  x:Name="calendar" 
                        View="Month">
</calendar:SfCalendar>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

this.calendar.View = CalendarView.Month;

{% endhighlight %}
{% endtabs %}

![Change different calendar views in .NET MAUI Calendar.](images/getting-started/net-maui-calendar-month-view.png)

## Change first day of week

The Calendar control is rendered with `Sunday` as the first day of the week and it allows customization to change the first day of the week using the [FirstDayOfWeek](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Calendar.CalendarMonthView.html#Syncfusion_Maui_Toolkit_Calendar_CalendarMonthView_FirstDayOfWeek) property in month view.

The following code explains how to show the Calendar with `Monday` as the first day of the week.

{% tabs %}  
{% highlight xaml tabtitle="MainPage.xaml" %}

<calendar:SfCalendar x:Name="calendar">
    <calendar:SfCalendar.MonthView>
        <calendar:CalendarMonthView FirstDayOfWeek="Monday"/>
    </calendar:SfCalendar.MonthView>
 </calendar:SfCalendar>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

this.calendar.MonthView.FirstDayOfWeek = DayOfWeek.Monday;

{% endhighlight %}  
{% endtabs %}

![Change first day of week in .NET MAUI Calendar.](images/getting-started/net-maui-calendar-first-day-of-week.png)

## Date selection

The [Calendar](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Calendar.SfCalendar.html) allows the user to select a single date, multiple dates, or a range of dates by interaction or programmatic selection. The default selection mode is `Single`.

The selection details can be obtained by using the [SelectionChanged](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Calendar.SfCalendar.html#Syncfusion_Maui_Toolkit_Calendar_SfCalendar_SelectionChanged) event of the calendar. It returns `CalendarSelectionChangedEventArgs`, which holds the details about the selected date or range.

The following code explains how to show the Calendar with `Multiple` as the Selection mode.

{% tabs %}  
{% highlight xaml tabtitle="MainPage.xaml" %}

<calendar:SfCalendar  x:Name="calendar" 
                      SelectionMode="Multiple">
</calendar:SfCalendar>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

this.calendar.SelectionMode = CalendarSelectionMode.Multiple;

{% endhighlight %}  
{% endtabs %}

![Change selection mode in .NET MAUI Calendar.](images/getting-started/net-maui-calendar-multiple-selection.png)

## Corner radius

You can customize the corner radius of the calendar using the [CornerRadius](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Calendar.SfCalendar.html#Syncfusion_Maui_Toolkit_Calendar_SfCalendar_CornerRadius) property of the SfCalendar, allowing you to set the desired roundness for the corners of the calendar. The default value of the `CornerRadius` property is `20`.

{% tabs %}  
{% highlight xaml tabtitle="XAML" hl_lines="3" %}

<calendar:SfCalendar x:Name="calendar" 
                     View="Month"
                     CornerRadius="15">
 </calendar:SfCalendar>

{% endhighlight %}
{% highlight c# tabtitle="C#" %}

this.calendar.CornerRadius = 15;

{% endhighlight %}
{% endtabs %}

![Change corner radius in .NET MAUI Calendar.](images/getting-started/net-maui-calendar-corner-radius.png)