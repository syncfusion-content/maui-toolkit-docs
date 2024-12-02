---
layout: post
title: Getting Started with .NET MAUI Button | Syncfusion
description: Learn here about getting started with the Syncfusion .NET MAUI Button (SfButton) control, its elements and more.
platform: MAUI
control: SfButton
documentation: ug
---

# Getting Started with .NET MAUI Button

This section guides you through setting up and configuring a [Button](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Buttons.SfButton.html) in your .NET MAUI application. Follow the steps below to add a basic Button to your project.

To quickly get started with the .NET MAUI Button, watch this video.

{% youtube "https://www.youtube.com/watch?v=KTGkYShi1YE" %}

## Prerequisites

Before proceeding, ensure the following are in place:

1. Install [.NET 7 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/7.0) or later.
2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.3 or later) or Visual Studio Code. For Visual Studio Code users, ensure that the .NET MAUI workload is installed and configured as described [here](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-8.0&tabs=visual-studio-code).

## Step 1: Create a New MAUI Project

### Visual Studio

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Then, click **Next**.
3. Select the .NET framework version and click **Create**.

### Visual Studio Code

1. Open the Command Palette by pressing **Ctrl+Shift+P** and type **.NET:New Project** and press Enter.
2. Choose the **.NET MAUI App** template.
3. Select the project location, type the project name and press Enter.
4. Then choose **Create project**

## Step 2: Install the Syncfusion MAUI Toolkit Package

### Visual Studio
1. In **Solution Explorer,** right-click the project and choose **Manage NuGet Packages.**
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

### Visual Studio Code
1. Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (backtick) to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your .csproj file is located.
3. Run the command `dotnet add package Syncfusion.Maui.Toolkit` to install the Syncfusion .NET MAUI Toolkit NuGet package.
4. To ensure all dependencies are installed, run `dotnet restore`.

## Step 3: Register the handler

In the MauiProgram.cs file, register the handler for Syncfusion Toolkit.

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

## Step 4: Add a Basic Button control

Step 1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Buttons` namespace into your code. 

Step 2: Add the namespace as shown in the following code sample.

{% tabs %}
{% highlight xaml %}

	xmlns:buttons="clr-namespace:Syncfusion.Maui.Toolkit.Buttons;assembly=Syncfusion.Maui.Toolkit"

{% endhighlight %}
{% highlight c# %}

	using Syncfusion.Maui.Toolkit.Buttons;

{% endhighlight %}
{% endtabs %}

## Initialize Button

Now, add the [SfButton](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Buttons.SfButton.html) control with a required optimal name using the included namespace.

{% tabs %}

{% highlight xaml %}

<buttons:SfButton x:Name="button" />
	
{% endhighlight %}

{% highlight C# %}

SfButton button = new SfButton();

{% endhighlight %}

{% endtabs %}

## Button icon

The button icon can be defined using the [ImageSource](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.ButtonBase.html#Syncfusion_Maui_Core_ButtonBase_ImageSource) and [ShowIcon](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.ButtonBase.html#Syncfusion_Maui_Core_ButtonBase_ShowIcon) properties of [SfButton](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Buttons.SfButton.html).

N> Ensure that the images mentioned in the code snippets are located in the **Resources** folder of your sample project.

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="SfButton" 
                    Text="Button"
                    TextColor="White" 
                    ShowIcon="True" 
                    ImageSource="button_Heart.png"/>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.TextColor = Colors.White;
button.ImageSource = "button_Heart.png";
button.ShowIcon = true;

{% endhighlight %}
{% endtabs %}

![.NET MAUI Button with button icon.](images/getting-started/net-maui-button-with-icon.png)


## Button background image

The button background image can be defined using the [BackgroundImageSource](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.ButtonBase.html#Syncfusion_Maui_Core_ButtonBase_BackgroundImageSource) property of [SfButton](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Buttons.SfButton.html).

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="SfButton" 
                    Text="Nature"
                    FontAttributes="Bold" 
                    BackgroundImageSource="button_background.png" 
                    CornerRadius="10" 
                    WidthRequest="150"/>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Nature";
button.FontAttributes = FontAttributes.Bold;
button.BackgroundImageSource = "button_background.png";
button.CornerRadius = 10;
button.WidthRequest = 150;

{% endhighlight %}
{% endtabs %}

![.NET MAUI Button with background image.](images/getting-started/net-maui-button-with-background-image.png)

Find the complete getting started sample of the .NET MAUI Button from this [link.](https://github.com/SyncfusionExamples/maui-button-samples)

N> You can refer to our [.NET MAUI Button](https://www.syncfusion.com/maui-controls/maui-button) feature tour page for its groundbreaking feature representations. You can also explore our [.NET MAUI Button Example](https://github.com/syncfusion/maui-demos/tree/master/MAUI/Buttons) that shows you how to render the Button in .NET MAUI.
