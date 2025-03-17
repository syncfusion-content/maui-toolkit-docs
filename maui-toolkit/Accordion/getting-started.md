---
layout: post
title: Getting Started with .NET MAUI Accordion Control | Syncfusion®
description: Learn here about getting started with Syncfusion® Toolkit for .NET MAUI Accordion control, its elements and more.
platform: maui-toolkit
control: SfAccordion
documentation: ug
---

# Getting Started with MAUI Accordion

This section guides you through setting up and configuring a [Accordion](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Accordion.SfAccordion.html?tabs=tabid-1) in your .NET MAUI application. Follow the steps below to add a basic Accordion to your project.

{% tabcontents %}
{% tabcontent Visual Studio %}

## Prerequisites
Before proceeding, ensure the following are in place:

 1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later.
 2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.3 or later) or VS Code.

## Step 1: Create a new .NET MAUI Project

 1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
 2. Name the project and choose a location. Then, click **Next**.
 3. Select the .NET Framework version, and then click **Create**.
 
## Step 2: Install the Syncfusion® .NET MAUI Toolkit Package

 1. In **Solution Explorer**, right-click the project and choose **Manage NuGet Packages**.
 2. Search for [Syncfusion.Maui.Toolkit](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.html) and install the latest version.
 3. Ensure the necessary dependencies are installed correctly, and the project is restored.

## Step 3: Register the handler

In the **MauiProgram.cs file**, register the handler for Syncfusion<sup>®</sup> Toolkit.

{% highlight c# hl_lines="1 9" %}

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
 
## Step 4: Add a Basic Accordion control
 
 1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Accordion` namespace into your code.
 2. Initialize [SfAccordion](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Accordion.SfAccordion.html?tabs=tabid-1) Control.
 
{% tabs %}
{% highlight xaml hl_lines="4" %}
<ContentPage>  
      xmlns:syncfusion="clr-namespace:Syncfusion.Maui.Toolkit.Accordion;assembly=Syncfusion.Maui.Toolkit">
    <syncfusion:SfAccordion />
</ContentPage>
{% endhighlight %}

{% highlight c# hl_lines="8" %}
using Syncfusion.Maui.Toolkit.Accordion;
. . .
public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfAccordion accordion = new SfAccordion();
        this.Content = accordion;
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

## Step 1: Create a new .NET MAUI Project

1. Open the command palette by pressing `Ctrl+Shift+P` and type **.NET:New Project** and enter.
2. Choose the **.NET MAUI App** template.
3. Select the project location, type the project name and press **Enter.**
4. Then choose **Create project.**

## Step 2: Install the Syncfusion<sup>®</sup> MAUI Core NuGet Package

1. Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (backtick) to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your .csproj file is located.
3. Run the command `dotnet add package Syncfusion.Maui.Toolkit` to install the Syncfusion<sup>®</sup> .NET MAUI Toolkit NuGet package.
4. To ensure all dependencies are installed, run `dotnet restore`.

## Step 3: Register the handler

In the **MauiProgram.cs file**, register the handler for Syncfusion<sup>®</sup> Toolkit.

{% highlight c# hl_lines="1 9" %}

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
 
## Step 4: Add a Basic Accordion control
 
 1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Accordion` namespace into your code.
 2. Initialize [SfAccordion](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Accordion.SfAccordion.html?tabs=tabid-1) Control.
 
{% tabs %}
{% highlight xaml hl_lines="4" %}
<ContentPage>  
      xmlns:syncfusion="clr-namespace:Syncfusion.Maui.Toolkit.Accordion;assembly=Syncfusion.Maui.Toolkit">
    <syncfusion:SfAccordion />
</ContentPage>
{% endhighlight %}

{% highlight c# hl_lines="8" %}
using Syncfusion.Maui.Toolkit.Accordion;
. . .
public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfAccordion accordion = new SfAccordion();
        this.Content = accordion;
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

In the **MauiProgram.cs file**, register the handler for Syncfusion<sup>®</sup> Toolkit.

{% highlight c# hl_lines="1 9" %}

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
 
## Step 4: Add a Basic Accordion control
 
 1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Accordion` namespace into your code.
 2. Initialize [SfAccordion](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Accordion.SfAccordion.html?tabs=tabid-1) Control.
 
{% tabs %}
{% highlight xaml hl_lines="4" %}
<ContentPage>  
      xmlns:syncfusion="clr-namespace:Syncfusion.Maui.Toolkit.Accordion;assembly=Syncfusion.Maui.Toolkit">
    <syncfusion:SfAccordion />
</ContentPage>
{% endhighlight %}

{% highlight c# hl_lines="8" %}
using Syncfusion.Maui.Toolkit.Accordion;
. . .
public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfAccordion accordion = new SfAccordion();
        this.Content = accordion;
    }
}
{% endhighlight %}
{% endtabs %}
{% endtabcontent %}
{% endtabcontents %}

## Step 5: Define the accordion items

Create an [AccordionItem](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Accordion.AccordionItem.html?tabs=tabid-1) instance containing a [Header](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Accordion.AccordionItem.html#Syncfusion_Maui_Toolkit_Accordion_AccordionItem_Header) and [Content](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Accordion.AccordionItem.html#Syncfusion_Maui_Toolkit_Accordion_AccordionItem_Content), and then add it to the [Items](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Accordion.SfAccordion.html?tabs=tabid-1#Syncfusion_Maui_Toolkit_Accordion_SfAccordion_Items) collection of SfAccordion.

In this example, a Grid is loaded in both the header and content of accordion items.

N> When loading Label as direct children of `Header` or `Content` of `AccordionItem`, then it will lead to an exception. So, load `Label` inside `Grid` to overcome the crash.

{% tabs %}
{% highlight xaml hl_lines="9 10" %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:local="clr-namespace:GettingStarted"
             x:Class="GettingStarted.MainPage"
             xmlns:syncfusion="clr-namespace:Syncfusion.Maui.Toolkit.Accordion;assembly=Syncfusion.Maui.Toolkit">
<ContentPage.Content>
        <syncfusion:SfAccordion >
            <syncfusion:SfAccordion.Items>
                <syncfusion:AccordionItem>
                    <syncfusion:AccordionItem.Header>
                        <Grid  HeightRequest="48">
                            <Label Text="Robin Rane" Margin="16,14,0,14" CharacterSpacing="0.25" FontFamily="Roboto-Regular"  FontSize="14" />
                        </Grid>
                    </syncfusion:AccordionItem.Header>
                    <syncfusion:AccordionItem.Content>
                        <Grid ColumnSpacing="10" RowSpacing="2" BackgroundColor="#f4f4f4"  >
                            <Grid Margin="16,6,0,0">
                                <Grid.Resources>
                                    <Style TargetType="Label">
                                        <Setter Property="FontFamily" Value="Roboto-Regular"/>
                                    </Style>
                                </Grid.Resources>
                                <Grid.RowDefinitions >
                                    <RowDefinition Height="25"/>
                                    <RowDefinition Height="25"/>
                                    <RowDefinition Height="25"/>
                                    <RowDefinition Height="25"/>
                                    <RowDefinition Height="{OnPlatform Default=90,Android=90,WinUI=70, iOS=100,MacCatalyst=70 }"/>
                                    <RowDefinition Height="Auto"/>
                                </Grid.RowDefinitions>
                                <Grid.ColumnDefinitions>
                                    <ColumnDefinition Width="100"/>
                                    <ColumnDefinition Width="100"/>
                                    <ColumnDefinition Width="*"/>
                                </Grid.ColumnDefinitions>
                                <Frame  Grid.RowSpan="4" BorderColor="Transparent" Grid.Row="0" Grid.Column="0"  Padding="0" Margin="0,0,0,7">
                                    <Image  Source="emp_01.png"/>
                                </Frame>
                                <Label Text="Position" Grid.Column="1" Grid.Row="0" Margin="6,0,0,0"/>
                                <Label Text="Chairman" Grid.Row="0" Grid.Column="2"/>
                                <Label Text="Organization " Grid.Row="1" Grid.Column="1" Margin="6,0,0,0"/>
                                <Label Text="ABC Inc." Grid.Row="1" Grid.Column="2"/>
                                <Label Text="Date Of Birth " Grid.Row="2" Grid.Column="1" Margin="6,0,0,0"/>
                                <Label Text="09/17/1973" Grid.Row="2" Grid.Column="2"/>
                                <Label Text="Location " Grid.Row="3" Grid.Column="1" Margin="6,0,0,0"/>
                                <Label Text="Boston" Grid.Row="3" Grid.Column="2"/>
                                <Label Padding="0,10,0,10" Grid.Row="4" Grid.ColumnSpan="3"  LineBreakMode="WordWrap"  
                                            FontSize="14" CharacterSpacing="0.25" VerticalTextAlignment="Center" 
                                                Text="Robin Rane, Chairman of ABC Inc., leads with dedication and vision.Under his guidance, the company thrives and continues to make a significant impact in the industry.">
                                </Label>
                                <StackLayout Grid.Row="5" Orientation="Horizontal" Margin="0,0,0,12">
                                    <Label Text="&#xe700;" FontSize="16" Margin="0,2,2,2"
                                                   FontFamily='{OnPlatform Android=AccordionFontIcons.ttf#,WinUI=AccordionFontIcons.ttf#AccordionFontIcons,MacCatalyst=AccordionFontIcons,iOS=AccordionFontIcons}'
                                                   VerticalOptions="Center" VerticalTextAlignment="Center"/>
                                    <Label Text="(617) 555-1234" Grid.Column="1" VerticalOptions="Center" CharacterSpacing="0.25" FontSize="14"/>
                                </StackLayout>
                            </Grid>
                        </Grid>
                    </syncfusion:AccordionItem.Content>
                </syncfusion:AccordionItem>
            </syncfusion:SfAccordion.Items>
        </syncfusion:SfAccordion>
    </ContentPage.Content>
</ContentPage>

{% endhighlight %}
{% endtabs %}

## Step 6: Running the Application

Press **F5** to build and run the application. Once compiled, the Accordion will be displayed with the data provided.

Here is the result of the previous codes,

![.NET MAUI Accordion with items](Images/getting-started/maui-accordion-with-defining-accordion-items.png)

N> When adding the template control inside the `StackLayout` or `Grid` with a height set to `Auto`, the child element will not receive the height changes at runtime. Since the `SfAccordion` is a template-based control, the default height value cannot be determined. Therefore, it is recommended to provide the `HorizontalOptions` and `VerticalOptions` as `FillAndExpand` options for the control.

## Animation duration

The `SfAccordion` allows you to customize the duration of the expanding and collapsing animations for accordion items by using the [AnimationDuration](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Accordion.SfAccordion.html?tabs=tabid-1#Syncfusion_Maui_Toolkit_Accordion_SfAccordion_AnimationDuration) property. By default, the animation duration is set to `200 milliseconds`.

{% tabs %}
{% highlight xaml hl_lines="2" %}
    <syncfusion:SfAccordion x:Name="accordion" 
                            AnimationDuration="150" /> 
{% endhighlight %}
{% highlight c# %}
    accordion.AnimationDuration = 150;
{% endhighlight %}
{% endtabs %}

## Animation easing

You can customize the rate of change of a parameter over time or the animation style of an accordion item by using the [AnimationEasing](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Accordion.SfAccordion.html?tabs=tabid-1#Syncfusion_Maui_Toolkit_Accordion_SfAccordion_AnimationEasing) property. By default, the animation easing is set to `Linear`.  

{% tabs %}
{% highlight xaml hl_lines="2" %}
         <syncfusion:SfAccordion x:Name="accordion"
                                AnimationEasing="SinOut" />
{% endhighlight %}
{% highlight c# %}
    accordion.AnimationEasing = ExpanderAnimationEasing.SinOut;
{% endhighlight %}
{% endtabs %}

## Auto scroll position

The `SfAccordion` allows you to customize the scroll position of the expanded accordion item using the [AutoScrollPosition](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Accordion.SfAccordion.html#Syncfusion_Maui_Toolkit_Accordion_SfAccordion_AutoScrollPosition) property. By default, the auto-scroll position is set to `MakeVisible`.  

{% tabs %}
{% highlight xaml hl_lines="2" %}
    <syncfusion:SfAccordion x:Name="accordion"
                             AutoScrollPosition="Top"/>
{% endhighlight %}
{% highlight c# %}
    accordion.AutoScrollPosition = AccordionAutoScrollPosition.Top;
{% endhighlight %}
{% endtabs %}

## Bring an accordion item into view

The [BringIntoView](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Accordion.SfAccordion.html#Syncfusion_Maui_Toolkit_Accordion_SfAccordion_BringIntoView_Syncfusion_Maui_Toolkit_Accordion_AccordionItem_) method is used to bring a specific item into view by scrolling to it programmatically.

{% tabs %}
{% highlight xaml %}
<ContentPage.Content>
    <StackLayout>
        <Button Clicked="Button_Clicked" Text="Button"/>
        <syncfusion:SfAccordion x:Name="accordion">
            <syncfusion:SfAccordion.Items>
                <syncfusion:AccordionItem>
                    <syncfusion:AccordionItem.Header>
                        <Grid  HeightRequest="48">
                            <Label Text="Robin Rane" Margin="16,14,0,14" CharacterSpacing="0.25" FontFamily="Roboto-Regular"  FontSize="14" />
                        </Grid>
                    </syncfusion:AccordionItem.Header>
                    <syncfusion:AccordionItem.Content>
                        <Grid ColumnSpacing="10" RowSpacing="2" BackgroundColor="#f4f4f4"  >
                            <Grid Margin="16,6,0,0">
                                <Grid.Resources>
                                    <Style TargetType="Label">
                                        <Setter Property="FontFamily" Value="Roboto-Regular"/>
                                    </Style>
                                </Grid.Resources>
                                <Grid.RowDefinitions >
                                    <RowDefinition Height="25"/>
                                    <RowDefinition Height="25"/>
                                    <RowDefinition Height="25"/>
                                    <RowDefinition Height="25"/>
                                    <RowDefinition Height="{OnPlatform Default=90,Android=90,WinUI=70, iOS=100,MacCatalyst=70 }"/>
                                    <RowDefinition Height="Auto"/>
                                </Grid.RowDefinitions>
                                <Grid.ColumnDefinitions>
                                    <ColumnDefinition Width="100"/>
                                    <ColumnDefinition Width="100"/>
                                    <ColumnDefinition Width="*"/>
                                </Grid.ColumnDefinitions>
                                <Frame  Grid.RowSpan="4" BorderColor="Transparent" Grid.Row="0" Grid.Column="0"  Padding="0" Margin="0,0,0,7">
                                    <Image  Source="emp_01.png"/>
                                </Frame>
                                <Label Text="Position" Grid.Column="1" Grid.Row="0" Margin="6,0,0,0"/>
                                <Label Text="Chairman" Grid.Row="0" Grid.Column="2"/>
                                <Label Text="Organization " Grid.Row="1" Grid.Column="1" Margin="6,0,0,0"/>
                                <Label Text="ABC Inc." Grid.Row="1" Grid.Column="2"/>
                                <Label Text="Date Of Birth " Grid.Row="2" Grid.Column="1" Margin="6,0,0,0"/>
                                <Label Text="09/17/1973" Grid.Row="2" Grid.Column="2"/>
                                <Label Text="Location " Grid.Row="3" Grid.Column="1" Margin="6,0,0,0"/>
                                <Label Text="Boston" Grid.Row="3" Grid.Column="2"/>
                                <Label Padding="0,10,0,10" Grid.Row="4" Grid.ColumnSpan="3"        LineBreakMode="WordWrap"  
                                        FontSize="14" CharacterSpacing="0.25" VerticalTextAlignment="Center" 
                                            Text="Robin Rane, Chairman of ABC Inc., leads with dedication and vision.Under his guidance, the company thrives and continues to make a significant impact in the industry.">
                                </Label>
                                <StackLayout Grid.Row="5" Orientation="Horizontal" Margin="0,0,0,12">
                                    <Label Text="&#xe700;" FontSize="16" Margin="0,2,2,2"
                                               FontFamily='{OnPlatform Android=AccordionFontIcons.ttf#,WinUI=AccordionFontIcons.ttf#AccordionFontIcons,MacCatalyst=AccordionFontIcons,iOS=AccordionFontIcons}'
                                               VerticalOptions="Center" VerticalTextAlignment="Center"/>
                                    <Label Text="(617) 555-1234" Grid.Column="1" VerticalOptions="Center" CharacterSpacing="0.25" FontSize="14"/>
                                </StackLayout>
                            </Grid>
                        </Grid>
                    </syncfusion:AccordionItem.Content>
                </syncfusion:AccordionItem>
            </syncfusion:SfAccordion.Items>
        </syncfusion:SfAccordion>
    </StackLayout>
</ContentPage.Content>
{% endhighlight %}
{% endtabs %}

{% tabs %}
{% highlight c# hl_lines="3" %}
private void Button_Clicked(object sender, EventArgs e)
{
    accordion.BringIntoView(accordion.Items[15]);
}
{% endhighlight %}
{% endtabs %}

## Expand mode

You can expand single or multiple items using the [ExpandMode](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Accordion.SfAccordion.html#Syncfusion_Maui_Toolkit_Accordion_SfAccordion_ExpandMode) property. By default, the expanded mode is set to `Single`.  

{% tabs %}
{% highlight xaml hl_lines="2" %}
    <syncfusion:SfAccordion x:Name="accordion" 
                            ExpandMode="Multiple" />
{% endhighlight %}
{% highlight c# %}
    accordion.ExpandMode = AccordionExpandMode.Multiple;
{% endhighlight %}
{% endtabs %}

## Item spacing

The `SfAccordion` allows you to customize the vertical spacing between the accordion items by using the [ItemSpacing](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Accordion.SfAccordion.html#Syncfusion_Maui_Toolkit_Accordion_SfAccordion_ItemSpacing) property. 

{% tabs %}
{% highlight xaml hl_lines="2" %}
    <syncfusion:SfAccordion x:Name="accordion" 
                            ItemSpacing="6.0d" />
{% endhighlight %}
{% highlight c# %}
    accordion.ItemSpacing = 6.0d;
{% endhighlight %}
{% endtabs %}