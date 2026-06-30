---
layout: post
title: Getting started with .NET MAUI Picker control | Syncfusion
description: Learn about getting started with Syncfusion<sup>&reg;</sup> .NET MAUI Picker (SfPicker) control and its basic features.
platform: maui
control: SfPicker
documentation: ug
---

# Getting started with .NET MAUI Picker
This section explains how to add the [.NET MAUI Picker](https://www.syncfusion.com/maui-controls/maui-picker) control. It covers only the basic features needed to get started with the Syncfusion Picker. Follow the steps below to add a .NET MAUI Picker control to your project.

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

## Step 4: Import Picker namespace

Add the following namespace in your XAML or C#.
{% tabs %}
{% highlight xaml %}

xmlns:picker="clr-namespace:Syncfusion.Maui.Toolkit.Picker;assembly=Syncfusion.Maui.Toolkit"

{% endhighlight %}
{% highlight c# %}

using Syncfusion.Maui.Toolkit.Picker;

{% endhighlight %}
{% endtabs %}

## Step 5: Add the Picker component

Initialize the [SfPicker](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.SfPicker.html) control and it allows you to bind data collection by setting the [ItemsSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.PickerColumn.html?tabs=tabid-9%2Ctabid-7%2Ctabid-3%2Ctabid-5%2Ctabid-11%2Ctabid-1#Syncfusion_Maui_Toolkit_Picker_PickerColumn_ItemsSourceProperty) property from the [PickerColumn](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Picker.PickerColumn.html?tabs=tabid-9%2Ctabid-7%2Ctabid-3%2Ctabid-5%2Ctabid-11%2Ctabid-1). Bind data collection in both XAML and C#.

{% tabs %}
{% highlight xaml tabtitle="XAML" hl_lines="6 10 11 12" %}

<picker:SfPicker x:Name="picker">
    <picker:SfPicker.HeaderView>
        <picker:PickerHeaderView Text="Select a color" Height="40" />
    </picker:SfPicker.HeaderView>
    <picker:SfPicker.Columns>
        <picker:PickerColumn ItemsSource="{Binding DataSource}" />
    </picker:SfPicker.Columns>
</picker:SfPicker>

{% endhighlight %}
{% highlight c# tabtitle="C#" hl_lines="1 8" %}

ItemInfo itemInfo = new ItemInfo();
SfPicker picker = new SfPicker()
{
    Columns = new ObservableCollection<PickerColumn>()
    {
        new PickerColumn()
        {
            ItemsSource = itemInfo.DataSource,
        }
    }
};

this.Content = picker;

{% endhighlight %}
{% endtabs %}

![Picker items in .NET MAUI picker.](images/getting-started/maui-picker-items.png)