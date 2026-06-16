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
1. Install [.NET 9 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) or later is installed.
2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.3 or later) or Visual Studio 2026 (18.0.0).

## Step 1: Create a New .NET MAUI Project

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Then click **Next**.
3. Select the .NET framework version and click **Create**.

## Step 2: Install the Syncfusion<sup>&reg;</sup> .NET MAUI Toolkit NuGet Package

1. In **Solution Explorer,** right-click the project and choose **Manage NuGet Packages.**
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

{% endtabcontent %}
{% tabcontent Visual Studio Code %}

## Prerequisites

Before proceeding, ensure the following are set up:
1. Install [.NET 9 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) or later is installed.
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

{% endtabcontent %}
{% tabcontent JetBrains Rider %}

## Prerequisites

Before proceeding, ensure the following are set up:

1. Ensure you have the latest version of JetBrains Rider.
2. Install [.NET 9 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) or later is installed.
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

## Step 3: Register Syncfusion handler

Make sure to add the namespace.
 
{% highlight MauiProgram.cs %}
using Syncfusion.Maui.Toolkit.Hosting;
{% endhighlight %}
 
Register the Syncfusion core handler in your CreateMauiApp method of `MauiProgram.cs` file to use Syncfusion controls.
 
{% highlight MauiProgram.cs %}
builder.ConfigureSyncfusionToolkit();
{% endhighlight %}

## Step 4: Import Calendar namespace

Add the following namespace in your XAML or C#.
{% tabs %}
{% highlight xaml %}

xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.Calendar;assembly=Syncfusion.Maui.Toolkit"

{% endhighlight %}
{% highlight c# %}

using Syncfusion.Maui.Toolkit.Calendar;

{% endhighlight %}
{% endtabs %}

## Step 5: Add the Calendar component

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

The following screenshot illustrates the result of the above code.

![Change different calendar views in .NET MAUI Calendar.](images/getting-started/net-maui-calendar-month-view.png)