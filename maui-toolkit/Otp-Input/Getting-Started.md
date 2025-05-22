---
layout: post
title: Getting Started with .NET MAUI OTP Input Control | Syncfusion®
description: Learn how to get started with the Syncfusion® .NET MAUI OTP Input (SfOtpInput) control in your cross-platform applications.
platform: maui-toolkit
control: SfOtpInput
documentation: UG
---

# Getting Started with .NET MAUI OTP Input

This section provides a detailed guide on how to get started with the [OTP Input](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html) for .NET MAUI and includes a walkthrough to configure the .NET MAUI OTP Input in a real-time scenario. Follow the steps below to add the .NET MAUI OTP Input to your project.

To quickly get started with the .NET MAUI OTP Input, watch this video.
{% youtube "https://www.youtube.com/watch?v=VmeTz2XEvag" %}

{% tabcontents %}
{% tabcontent Visual Studio %}

## Prerequisites

Before proceeding, ensure the following are set up:

1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later.
2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.8 or later).

## Step 1: Create a new .NET MAUI project

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Then, click **Next**.
3. Select the .NET framework version and click **Create**.

## Step 2: Install the Syncfusion<sup>®</sup> MAUI Toolkit package

1. In **Solution Explorer**, right-click the project and choose **Manage NuGet Packages**.
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure all necessary dependencies are installed correctly and the project is restored.

## Step 3: Register the handler

In the `MauiProgram.cs` file, register the handler for the Syncfusion<sup>®</sup> Toolkit.

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

## Step 4: Add a basic OTP Input

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.OtpInput` namespace.

2. Initialize [SfOtpInput](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html).

{% tabs %}
{% highlight xaml %}

<otpInput:SfOtpInput />

{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput();

{% endhighlight %}
{% endtabs %}

{% endtabcontent %}
{% tabcontent Visual Studio Code %}

## Prerequisites

Before proceeding, ensure the following are set up:

1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later.
2. Set up a .NET MAUI environment with Visual Studio Code.
3. Ensure that the .NET MAUI extension is installed and configured as described [here](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-8.0&tabs=visual-studio-code).

## Step 1: Create a new .NET MAUI project

1. Open the command palette by pressing `Ctrl+Shift+P` and type **.NET:New Project** and enter.
2. Choose the **.NET MAUI App** template.
3. Select the project location, type the project name and press **Enter**.
4. Then choose **Create project**.

## Step 2: Install the Syncfusion<sup>®</sup> MAUI Toolkit package

1. Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (backtick) to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your .csproj file is located.
3. Run the command `dotnet add package Syncfusion.Maui.Toolkit` to install the Syncfusion<sup>®</sup> .NET MAUI Toolkit NuGet package.
4. To ensure all dependencies are installed, run `dotnet restore`.

## Step 3: Register the handler

In the `MauiProgram.cs` file, register the handler for Syncfusion<sup>®</sup> Toolkit.

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

## Step 4: Add a basic OTP Input

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.OtpInput` namespace.

2. Initialize [SfOtpInput](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html).

{% tabs %}
{% highlight xaml %}

<otpInput:SfOtpInput />

{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput();

{% endhighlight %}
{% endtabs %}

{% endtabcontent %}

{% tabcontent JetBrains Rider %}

## Prerequisites

Before proceeding, ensure the following are set up:

1. Ensure you have the latest version of JetBrains Rider.
2. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later.
3. Make sure the MAUI workloads are installed and configured as described [here](https://www.jetbrains.com/help/rider/MAUI.html#before-you-start).

## Step 1: Create a new .NET MAUI project

1. Go to **File > New Solution**, select .NET (C#) and choose the **.NET MAUI App** template.
2. Enter the Project Name, Solution Name, and Location.
3. Select the .NET framework version and click **Create**.

## Step 2: Install the Syncfusion<sup>®</sup> MAUI Toolkit NuGet package

1. In **Solution Explorer**, right-click the project and choose **Manage NuGet Packages**.
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored. If not, open the Terminal in Rider and manually run: `dotnet restore`.

## Step 3: Register the handler

In the `MauiProgram.cs` file, register the handler for Syncfusion<sup>®</sup> Toolkit.

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

## Step 4: Add a basic OTP Input

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.OtpInput` namespace.

2. Initialize [SfOtpInput](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html).

{% tabs %}
{% highlight xaml %}

<otpInput:SfOtpInput />

{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput();

{% endhighlight %}
{% endtabs %}

{% endtabcontent %}
{% endtabcontents %}

## Value

You can specify the value of OTP Input by using the [Value](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.OtpInput.SfOtpInput.html#Syncfusion_Maui_Toolkit_OtpInput_SfOtpInput_Value) property.

{% tabs %}	
{% highlight xaml %}

<otpInput:SfOtpInput Value="e3c7" Type="Text" />
	
{% endhighlight %}
{% highlight c# %}

SfOtpInput otpInput = new SfOtpInput()
{
    Value = "e3c7",
    Type = OtpInputType.Text
};

{% endhighlight %}
{% endtabs %}

![Value](images/value.png)