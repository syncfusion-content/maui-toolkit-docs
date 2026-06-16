---
layout: post
title: Getting Started with .NET MAUI Accordion Control | Syncfusion®
description: Learn here about getting started with Syncfusion® Toolkit for .NET MAUI Accordion control, its elements and more.
platform: maui-toolkit
control: SfAccordion
documentation: ug
---

# Getting Started with MAUI Accordion

This section guides you through setting up and configuring a `Accordion` in your .NET MAUI application. Follow the steps below to add a basic Accordion to your project.

{% tabcontents %}
{% tabcontent Visual Studio %}

## Prerequisites
Before proceeding, ensure the following are in place:

 1. Install [.NET 9 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) or later.
 2. Set up a .NET MAUI environment with Visual Studio 2026 (v18.0.0 or later) or VS Code.

## Step 1: Create a new .NET MAUI Project

 1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
 2. Name the project and choose a location. Then, click **Next**.
 3. Select the .NET Framework version, and then click **Create**.
 
## Step 2: Install the Syncfusion® .NET MAUI Toolkit Package

 1. In **Solution Explorer**, right-click the project and choose **Manage NuGet Packages**.
 2. Search for [Syncfusion.Maui.Toolkit](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.html) and install the latest version.
 3. Ensure the necessary dependencies are installed correctly, and the project is restored.

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

{% endtabcontent %}
{% endtabcontents %}

## Step 3: Register Syncfusion handler

In the **MauiProgram.cs file**, register the handler for Syncfusion<sup>®</sup> Toolkit.

Make sure to add the namespace.
 
{% highlight MauiProgram.cs %}
using Syncfusion.Maui.Toolkit.Hosting;
{% endhighlight %}
 
Register the Syncfusion core handler in your CreateMauiApp method of `MauiProgram.cs` file to use Syncfusion controls.
 
{% highlight MauiProgram.cs %}
builder.ConfigureSyncfusionToolkit();
{% endhighlight %}
 
## Step 4: Add an Accordion control
 
 1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Accordion` namespace into your code.
 2. Initialize SfAccordion Control.
 
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

## Step 5: Define the accordion items

Create an `AccordionItem` instance containing a `header` and `content`, and then add it to the `Items` collection of SfAccordion.

In this example, a Grid is loaded in both the header and content of accordion items.

N> When loading Label as direct children of `Header` or `Content` of `AccordionItem`, then it will lead to an exception. So, load `Label` inside `Grid` to overcome the crash.

{% tabs %}
{% highlight xaml %}
<syncfusion:SfAccordion>
    <syncfusion:SfAccordion.Items>
        <syncfusion:AccordionItem>
            <syncfusion:AccordionItem.Header>
                <Grid  HeightRequest="48">
                    <Label Text="Can I download and utilize the Syncfusion .NET MAUI Accordion for free?"
                           Margin="16,14,0,14" />
                </Grid>
            </syncfusion:AccordionItem.Header>
            <syncfusion:AccordionItem.Content>
                <Grid  BackgroundColor="#f4f4f4"
                       RowDefinitions="Auto">
                    <Label Text="No, this is a commercial product and requires a paid license. However, a free community license is also available for companies and individuals whose organizations have less than $1 million USD in annual gross revenue, 5 or fewer developers, and 10 or fewer total employees."
                           Margin="16,3,0,3"
                           FontSize="12" />
                </Grid>
            </syncfusion:AccordionItem.Content>
        </syncfusion:AccordionItem>
        <syncfusion:AccordionItem>
            <syncfusion:AccordionItem.Header>
                <Grid  HeightRequest="48">
                    <Label Text="Why should you choose the Syncfusion .NET MAUI Accordion?"
                           Margin="16,14,0,14" />
                </Grid>
            </syncfusion:AccordionItem.Header>
            <syncfusion:AccordionItem.Content>
                <Grid BackgroundColor="#f4f4f4"
                      RowDefinitions="Auto,Auto,Auto">
                    <Label Grid.Row="0"
                           Text="Easily arrange accordion items vertically."
                           FontSize="12"
                           Margin="16,3,0,3" />
                    <Label Grid.Row="1"
                           Text="Simple configuration and APIs."
                           FontSize="12"
                           Margin="16,3,0,3" />
                    <Label Grid.Row="2"
                           Text="Mobile-touch friendly."
                           FontSize="12"
                           Margin="16,3,0,3" />
                </Grid>
            </syncfusion:AccordionItem.Content>
        </syncfusion:AccordionItem>
    </syncfusion:SfAccordion.Items>
</syncfusion:SfAccordion>
{% endhighlight %}
{% highlight c# %}

var accordion = new SfAccordion
{
    Margin = new Thickness(0, 50, 0, 0)
};

var item1 = new AccordionItem();

item1.Header = new Grid
{
    HeightRequest = 48,
    Children =
        {
            new Label
            {
                Text = "Can I download and utilize the Syncfusion .NET MAUI Accordion for free?",
                Margin = new Thickness(16,14,0,14)
            }
        }
};

var contentGrid1 = new Grid
{
    BackgroundColor = Color.FromArgb("#f4f4f4"),
    RowDefinitions =
        {
            new RowDefinition { Height = GridLength.Auto }
        }
};

var contentLabel1 = new Label
{
    Text = "No, this is a commercial product and requires a paid license. However, a free community license is also available for companies and individuals whose organizations have less than $1 million USD in annual gross revenue, 5 or fewer developers, and 10 or fewer total employees.",
    Margin = new Thickness(16, 3, 0, 3),
    FontSize = 12
};

Grid.SetRow(contentLabel1, 0);
contentGrid1.Children.Add(contentLabel1);

item1.Content = contentGrid1;

var item2 = new AccordionItem();

item2.Header = new Grid
{
    HeightRequest = 48,
    Children =
        {
            new Label
            {
                Text = "Why should you choose the Syncfusion .NET MAUI Accordion?",
                Margin = new Thickness(16,14,0,14)
            }
        }
};

var contentGrid2 = new Grid
{
    BackgroundColor = Color.FromArgb("#f4f4f4"),
    RowDefinitions =
        {
            new RowDefinition { Height = GridLength.Auto },
            new RowDefinition { Height = GridLength.Auto },
            new RowDefinition { Height = GridLength.Auto }
        }
};

var label1 = new Label
{
    Text = "Easily arrange accordion items vertically.",
    FontSize = 12,
    Margin = new Thickness(16, 3, 0, 3)
};
Grid.SetRow(label1, 0);

var label2 = new Label
{
    Text = "Simple configuration and APIs.",
    FontSize = 12,
    Margin = new Thickness(16, 3, 0, 3)
};
Grid.SetRow(label2, 1);

var label3 = new Label
{
    Text = "Mobile-touch friendly.",
    FontSize = 12,
    Margin = new Thickness(16, 3, 0, 3)
};
Grid.SetRow(label3, 2);

contentGrid2.Children.Add(label1);
contentGrid2.Children.Add(label2);
contentGrid2.Children.Add(label3);

item2.Content = contentGrid2;

accordion.Items.Add(item1);
accordion.Items.Add(item2);

Content = accordion;
{% endhighlight %}
{% endtabs %}

The following screenshot illustrates the result of the above code.

<img alt="Defining the Accordion items" src="Images\getting-started\maui-accordion-with-defining-accordion-items.png"/> 

N> When adding the template control inside the `Grid` with a height set to `Auto`, the child element will not receive the height changes at runtime. Since the `SfAccordion` is a template-based control, the default height value cannot be determined. Therefore, it is recommended to provide the `HorizontalOptions` and `VerticalOptions` as `FillAndExpand` options for the control.