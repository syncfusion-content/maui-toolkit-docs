---
layout: post
title: About .NET MAUI Shimmer control | Syncfusion
description: Learn here about the getting started with Syncfusion<sup>&reg;</sup> .NET MAUI Shimmer (SfShimmer) control, its elements and more.
platform: maui-toolkit
control: SfShimmer
documentation: ug
---

# Getting started of .NET MAUI Shimmer

This section explains how to add the [.NET MAUI Shimmer](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Shimmer.SfShimmer.html) control. Follow the steps below to add a .NET MAUI Shimmer control to your project.

{% tabcontents %}
{% tabcontent Visual Studio %}

## Prerequisites

Before proceeding, ensure the following are set up:
1. Install .NET SDK
  - [.NET 9 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) or later must be installed.
2. Set up a .NET MAUI Environment with Visual Studio. Supported Visual Studio Versions:
  - Visual Studio 2022: Version 17.13 or later (e.g., 17.14.7) for .NET 9 development.
  - Visual Studio 2026: Required for .NET 10 development.
 
## Step 1: Create a New .NET MAUI Project

 1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
 2. Name the project and choose a location. Then click **Next**.
 3. Select the .NET framework version and click **Create**.
 
## Step 2: Install the Syncfusion<sup>&reg;</sup> .NET MAUI Toolkit NuGet Package

 1. In **Solution Explorer**, right-click the project and choose **Manage NuGet Packages**.
 2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
 3. Ensure the necessary dependencies are installed correctly, and the project is restored.
 
{% endtabcontent %}
{% tabcontent Visual Studio Code %}

## Prerequisites

Before proceeding, ensure the following are set up:
 1. Install [.NET 9 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) or later is installed.
 2. Set up a .NET MAUI environment with Visual Studio Code. 
 3. Ensure that the .NET MAUI extension is installed and configured as described [here.](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-8.0&tabs=visual-studio-code)

## Step 1: Create a New .NET MAUI Project

 1. Open the command palette by pressing `Ctrl+Shift+P` and type **.NET:New Project** and enter.
 2. Choose the **.NET MAUI App** template.
 3. Select the project location, type the project name and press **Enter**.
 4. Then choose **Create project.**

## Step 2: Install the Syncfusion<sup>&reg;</sup> .NET MAUI Toolkit NuGet Package

1. Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (backtick) to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your .csproj file is located.
3. Run the command `dotnet add package Syncfusion.Maui.Toolkit` to install the Syncfusion<sup>&reg;</sup> .NET MAUI Toolkit NuGet package.
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

## Step 4: Import Shimmer namespace

Add the following namespace in your XAML or C#.
{% tabs %}
{% highlight xaml %}

xmlns:shimmer="clr-namespace:Syncfusion.Maui.Toolkit.Shimmer;assembly=Syncfusion.Maui.Toolkit"

{% endhighlight %}
{% highlight c# %}

using Syncfusion.Maui.Toolkit.Shimmer;

{% endhighlight %}
{% endtabs %}

{% endtabcontent %}
{% endtabcontents %}

## Step 5: Add the Shimmer component

The `.NET MAUI Shimmer` control provides seven different shimmer types of views. It can be assigned to the control using the [Type](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Shimmer.SfShimmer.html#Syncfusion_Maui_Toolkit_Shimmer_SfShimmer_Type) property. By default, the control is assigned to the [CirclePersona](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Shimmer.ShimmerType.html#Syncfusion_Maui_Toolkit_Shimmer_ShimmerType_CirclePersona) view.

{% tabs %}
{% highlight xaml tabtitle="XAML" hl_lines="2" %}

<shimmer:SfShimmer VerticalOptions="Fill"
                   Type="CirclePersona">
    <shimmer:SfShimmer.Content>
        <StackLayout>
            <Label
                Text="Content is loaded!"
                HorizontalOptions="CenterAndExpand"
                VerticalOptions="CenterAndExpand">
            </Label>
        </StackLayout>
    </shimmer:SfShimmer.Content>
</shimmer:SfShimmer>

{% endhighlight %}
{% highlight c# tabtitle="C#" hl_lines="3" %}

SfShimmer shimmer = new SfShimmer()
{
    Type = ShimmerType.CirclePersona,
    VerticalOptions = LayoutOptions.Fill,
    Content = new Label
    {
        Text = "Content is loaded!!"
    }
};

this.Content = shimmer;

{% endhighlight %}
{% endtabs %}

![Circle persona Shimmer view in .NET MAUI.](images/overview/maui-circle-persona.gif)