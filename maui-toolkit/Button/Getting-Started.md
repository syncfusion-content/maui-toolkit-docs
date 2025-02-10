---
layout: post
title: Getting Started with .NET MAUI Button | Syncfusion<sup>®</sup>
description: Learn here about getting started with the Syncfusion<sup>®</sup> .NET MAUI Button (SfButton) control, its elements and more.
platform: MAUI
control: SfButton
documentation: ug
---

# Getting Started with .NET MAUI Button

This section guides you through setting up and configuring a [Button](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html) in your .NET MAUI application. Follow the steps below to add a basic Button to your project.

{% tabcontents %}
{% tabcontent Visual Studio %}

## Prerequisites

Before proceeding, ensure the following are in place:

1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later.
2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.8 or later).

## Step 1: Create a New .NET MAUI Project

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Then, click **Next**.
3. Select the .NET framework version and click **Create**.

## Step 2: Install the Syncfusion<sup>®</sup> MAUI Toolkit Package

1. In **Solution Explorer,** right-click the project and choose **Manage NuGet Packages.**
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

## Step 3: Register the handler

In the MauiProgram.cs file, register the handler for Syncfusion<sup>®</sup> Toolkit.

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

Step 2: Initialize [SfButton](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html) control.

{% tabs %}

{% highlight xaml %}
<ContentPage 
    xmlns:buttons="clr-namespace:Syncfusion.Maui.Toolkit.Buttons;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	 	<buttons:SfButton x:Name="button" />
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.Buttons;

	public partial class MainPage : ContentPage
	{ 
		public MainPage()
		{   
			InitializeComponent();
			SfButton button = new SfButton();
			this.Content = button;
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
3. Ensure that the .NET MAUI extension is installed and configured as described [here.](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-8.0&tabs=visual-studio-code)

## Step 1: Create a New .NET MAUI Project

1. Open the Command Palette by pressing **Ctrl+Shift+P** and type **.NET:New Project** and press Enter.
2. Choose the **.NET MAUI App** template.
3. Select the project location, type the project name and press **Enter**.
4. Then choose **Create project**

## Step 2: Install the Syncfusion<sup>®</sup> MAUI Toolkit Package

1. Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (backtick) to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your .csproj file is located.
3. Run the command `dotnet add package Syncfusion.Maui.Toolkit` to install the Syncfusion<sup>®</sup> .NET MAUI Toolkit NuGet package.
4. To ensure all dependencies are installed, run `dotnet restore`.

## Step 3: Register the handler

In the MauiProgram.cs file, register the handler for Syncfusion<sup>®</sup> Toolkit.

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

Step 2: Initialize [SfButton](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html) control.

{% tabs %}

{% highlight xaml %}
<ContentPage 
    xmlns:buttons="clr-namespace:Syncfusion.Maui.Toolkit.Buttons;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	 	<buttons:SfButton x:Name="button" />
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.Buttons;

	public partial class MainPage : ContentPage
	{ 
		public MainPage()
		{   
			InitializeComponent();
			SfButton button = new SfButton();
			this.Content = button;
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

In the MauiProgram.cs file, register the handler for Syncfusion<sup>®</sup> Toolkit.

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

Step 2: Initialize [SfButton](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html) control.

{% tabs %}

{% highlight xaml %}
<ContentPage 
    xmlns:buttons="clr-namespace:Syncfusion.Maui.Toolkit.Buttons;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	 	<buttons:SfButton x:Name="button" />
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.Buttons;

	public partial class MainPage : ContentPage
	{ 
		public MainPage()
		{   
			InitializeComponent();
			SfButton button = new SfButton();
			this.Content = button;
		}  
	}  

{% endhighlight %}

{% endtabs %}
{% endtabcontent %}
{% endtabcontents %}

## Button icon

The button icon can be defined using the [ImageSource](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.ButtonBase.html#Syncfusion_Maui_Core_ButtonBase_ImageSource) and [ShowIcon](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.ButtonBase.html#Syncfusion_Maui_Core_ButtonBase_ShowIcon) properties of [SfButton](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html).

N> Ensure that the images mentioned in the code snippets are located in the **Resources** folder of your sample project.

{% tabs %}
{% highlight xaml %}

<buttons:SfButton x:Name="SfButton" 
                    Text="Button"
                    TextColor="White" 
                    ShowIcon="True"
                    CornerRadius="2" 
                    ImageSource="button_Heart.png"/>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.TextColor = Colors.White;
button.ImageSource = "button_Heart.png";
button.ShowIcon = true;
button.CornerRadius= 2;

{% endhighlight %}
{% endtabs %}

![.NET MAUI Button with button icon.](images/getting-started/net-maui-button-with-icon.png)


## Button background image

The button background image can be defined using the [BackgroundImageSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ButtonBase.html#Syncfusion_Maui_Toolkit_ButtonBase_BackgroundImageSource) property of [SfButton](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html).

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

