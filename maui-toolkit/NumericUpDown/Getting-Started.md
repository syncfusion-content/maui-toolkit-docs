---
layout: post
title: Getting Started with .NET MAUI NumericUpDown | Syncfusion
description: Learn how to get started with Syncfusion .NET MAUI NumericUpDown (SfNumericUpDown) control, its elements, and more in here.
platform: MAUI
control: SfNumericUpDown
documentation: ug
---

# Getting Started with .NET MAUI Numeric UpDown

This section guides you through setting up and configuring a [Numeric UpDown](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html) in your .NET MAUI application. Follow the steps below to add a basic Numeric UpDown to your project.

## Prerequisites

Before proceeding, ensure the following are in place:

1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later.
2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.8 or later) or Visual Studio Code. For Visual Studio Code users, ensure that the .NET MAUI workload is installed and configured as described [here](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-8.0&tabs=visual-studio-code).

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

## Step 4: Add a Basic Numeric UpDown

Step 1. To initialize the control, import the `Syncfusion.Maui.Toolkit.NumericUpDown` namespace into your code. 

Step 2: Add the namespace as shown in the following code sample.

{% tabs %}
{% highlight xaml %}

	<xmlns:editors="clr-namespace:Syncfusion.Maui.Toolkit.NumericUpDown;assembly=Syncfusion.Maui.Toolkit"/>

{% endhighlight %}
{% highlight c# %}

	using Syncfusion.Maui.Toolkit.NumericUpDown;

{% endhighlight %}
{% endtabs %}

Step 3: Add the [SfNumericUpDown](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html) control with a required optimal name using the included namespace.

{% tabs %}
{% highlight xaml %}

	<editors:SfNumericUpDown x:Name="numericUpDown" />
	
{% endhighlight %}
{% highlight C# %}

    SfNumericUpDown sfNumericUpDown = new SfNumericUpDown();   

{% endhighlight %}
{% endtabs %}

![.NET MAUI NumericUpDown Application](GettingStarted_images/gettingStarted_img.png)

## Editing the value
By default, the [NumericUpDown](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html) control allows you to enter numeric input, restricts the alphabetic input. It provides increment and decrement buttons for convenient value adjustments. Once the `Enter` key is pressed or control focus is lost, the value of the `NumericUpDown` control is validated and updated based on the format applied.

{% tabs %}
{% highlight xaml %}

<editors:SfNumericUpDown HorizontalOptions="Center" 
                         VerticalOptions="Center" 
                         CustomFormat="0.000" />

{% endhighlight %}
{% highlight C# %}

SfNumericUpDown sfNumericUpDown = new SfNumericUpDown();
sfNumericUpDown.HorizontalOptions = LayoutOptions.Center;
sfNumericUpDown.VerticalOptions = LayoutOptions.Center;
sfNumericUpDown.CustomFormat = "0.000";

{% endhighlight %}
{% endtabs %}

![.NET MAUI NumericUpDown value editing](GettingStarted_images/editing_value.gif)

## Change number format

You can change the format in which the value should be displayed using the [CustomFormat](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html#Syncfusion_Maui_Toolkit_NumericEntry_SfNumericEntry_CustomFormat
) property. By default, the value of the `CustomFormat` property is **null**.

{% tabs %}
{% highlight xaml %}

<editors:SfNumericUpDown HorizontalOptions="Center"
                        VerticalOptions="Center"
                        Value="12.5" 
                        CustomFormat="C2" />

{% endhighlight %}
{% highlight C# %}

SfNumericUpDown sfNumericUpDown = new SfNumericUpDown();
sfNumericUpDown.HorizontalOptions = LayoutOptions.Center;
sfNumericUpDown.VerticalOptions = LayoutOptions.Center;
sfNumericUpDown.Value = 12.5;
sfNumericUpDown.CustomFormat = "C2";

{% endhighlight %}
{% endtabs %}

![.NET MAUI NumericUpDown value editing](GettingStarted_images/custom_format.png)

## Accept null value

By default, the [NumericUpDown](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html) control allows a **null** value. A null value is assigned when the user clicks the clear button or clears the input. You can disable this by setting the value of the [AllowNull](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html#Syncfusion_Maui_Toolkit_NumericEntry_SfNumericEntry_AllowNull) property as **false**. When the value of the `AllowNull` property is set to **false**, and the input is cleared, the `NumericUpDown` control returns it to **0**.

{% tabs %}
{% highlight xaml %}

<editors:SfNumericUpDown HorizontalOptions="Center"
                         VerticalOptions="Center"
                         Value="12315"
                         AllowNull="False" />

{% endhighlight %}
{% highlight C# %}

SfNumericUpDown sfNumericUpDown = new SfNumericUpDown();
sfNumericUpDown.Value=12315;
sfNumericUpDown.HorizontalOptions = LayoutOptions.Center;
sfNumericUpDown.VerticalOptions = LayoutOptions.Center;
sfNumericUpDown.AllowNull = false;

{% endhighlight %}
{% endtabs %}

![.NET MAUI NumericUpDown prevent empty textbox](GettingStarted_images/allowNull.gif)