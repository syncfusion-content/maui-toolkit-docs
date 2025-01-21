---
layout: post
title: Getting Started with .NET MAUI Popup control | Syncfusion
description: Learn here about getting started with Syncfusion .NET MAUI Popup (SfPopup) control, its elements and more.
platform: maui-toolkit
control: SfPopup
documentation: ug
---

# Getting Started with .NET MAUI Popup

This section guides you through setting up and configuring a `Popup` in your .NET MAUI application. Follow the steps below to add a basic Popup to your project.

## Prerequisites
Before proceeding, ensure the following are in place:

 1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later.
 2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.3 or later) or VS Code. For VS Code users, ensure that the .NET MAUI workload is installed and configured as described [here](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-8.0&tabs=visual-studio-code).

## Step 1: Create a .NET MAUI project
{% tabcontents %}
{% tabcontent Visual Studio %}

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Then, click **Next.**
3. Select the .NET framework version and click **Create.**

{% endtabcontent %}
{% tabcontent Visual Studio Code %}

1. Open the command palette by pressing `Ctrl+Shift+P` and type **.NET:New Project** and enter.
2. Choose the **.NET MAUI App** template.
3. Select the project location, type the project name and press **Enter.**
4. Then choose **Create project.**

{% endtabcontent %}
{% endtabcontents %}
 
## Step 2: Install the Syncfusion MAUI Popup NuGet Package
 
 1. In **Solution Explorer**, right-click the project and choose **Manage NuGet Packages**.
 2. Search for [Syncfusion.Maui.Toolkit](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.html) and install the latest version.
 3. Ensure the necessary dependencies are installed correctly, and the project is restored.

## Step 3: Register the handler

In the **MauiProgram.cs file**, register the handler for Syncfusion Toolkit.

{% tabs %}
{% highlight c# tabtitle="MauiProgram.cs" hl_lines="4 20" %}
using Microsoft.Maui.Controls.Hosting;
using Microsoft.Maui.Controls.Xaml;
using Microsoft.Maui.Hosting;
using Syncfusion.Maui.Toolkit.Hosting;

namespace GettingStarted
{
    public class MauiProgram 
    {
        public static MauiApp CreateMauiApp()
        {
            var builder = MauiApp.CreateBuilder();
            builder
                .UseMauiApp<App>()
                .ConfigureFonts(fonts =>
                {
                    fonts.AddFont("OpenSans-Regular.ttf", "OpenSansRegular");
                });

            builder.ConfigureSyncfusionToolkit();
            return builder.Build();
        }
    }
}
{% endhighlight %} 
{% endtabs %}

## Step 4: Add a Basic Popup

 1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Popup` namespace into your code.
 2. Initialize `SfPopup` class.
 
{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" %}

<ContentPage   
    . . .
    xmlns:syncfusion="clr-namespace:Syncfusion.Maui.Toolkit.Popup;assembly=Syncfusion.Maui.Toolkit">

    <syncfusion:SfPopup />
</ContentPage>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

using Syncfusion.Maui.Toolkit.Popup;
. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfPopup popup = new SfPopup();
    }
}

{% endhighlight %}
{% endtabs %}

## Step 5: Displaying popup

Display a popup over your view by calling the `Show` method.

Refer to the following code example for displaying popup using Button's Click event.

{% tabs %}

{% highlight xaml tabtitle="MainPage.xaml" %}

<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:local="clr-namespace:GettingStarted"
			 xmlns:syncfusion="clr-namespace:Syncfusion.Maui.Toolkit.Popup;assembly=Syncfusion.Maui.Toolkit"
             x:Class="GettingStarted.MainPage" 
             Padding="0,40,0,0">
     <StackLayout x:Name="mainLayout">
       <Button x:Name="clickToShowPopup" Text="ClickToShowPopup" 
               VerticalOptions="Start" HorizontalOptions="Center"
               Clicked="ClickToShowPopup_Clicked" />
               <syncfusion:SfPopup x:Name="popup" />
     </StackLayout>
</ContentPage>

{% endhighlight %}

{% highlight c# tabtitle="MainPage.xaml.cs" hl_lines="12" %}
namespace GettingStarted
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();
        }

        private void ClickToShowPopup_Clicked(object sender, EventArgs e)
        {
            popup.Show();
        }
    }
}

{% endhighlight %}

{% endtabs %}

## Step 6: Running the Application

Press **F5** to build and run the application. Once compiled, click the button to open the Popup.

Here is the result of the previous codes.

![Popup with default appearance](Images/getting-started//maui-popup-with-default-appearance.png)

## Close the popup

To close the popup programmatically, you can call either the `Dismiss` method or set the IsOpen property to false.

Refer to the following code example for dismissing popup.

{% tabs %}
{% highlight c# tabtitle="MainPage.xaml.cs" hl_lines="4 7" %}
    
    private void ClickToDismissPopup_Clicked(object sender, EventArgs e)
    {
        // Dismiss SfPopup from the view.
        sfPopup.Dismiss();

        // Or
        sfPopup.IsOpen = false;
    }
{% endhighlight %} 
{% endtabs %}

## Customize positioning

The .NET MAUI Popup (SfPopup) allows showing the popup content at various positions.

The following list of options is available to position the SfPopup in the desired position:

* `Center Positioning`: Use the `IsOpen` property or `Show` method to display the SfPopup at the center.
* `Absolute Positioning`: Use the `Show(x-position, y-position)` to display the SfPopup at the specified X and y position.
* `Relative Positioning`: Use the `ShowRelativeToView(View, RelativePosition)` to display the SfPopup at any of the 8 positions relative to the specified view.
* `Absolute relative positioning`: Use the `ShowRelativeToView(View, RelativePosition,x position,y position)` to display the SfPopup at an absolute x,y coordinate from the relative position of the specified view.

## Customizing layouts

By default, choose a layout from the following available layouts in the SfPopup by using the `AppearanceMode` property.

* `OneButton`: Shows the SfPopup with one button in the footer view. This is the default value.
* `TwoButton`: Shows the SfPopup with two buttons in the footer view.

Also, customize the entire popup view by loading the templates or custom views for the header, body, and footer.

Refer to the following code example for displaying popup with appearance mode.

{% tabs %}

{% highlight xaml tabtitle="MainPage.xaml" hl_lines="11" %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:local="clr-namespace:GettingStarted"
			 xmlns:syncfusion="clr-namespace:Syncfusion.Maui.Toolkit.Popup;assembly=Syncfusion.Maui.Toolkit"
             x:Class="GettingStarted.MainPage" 
             Padding="0,40,0,0">
     <StackLayout x:Name="mainLayout">
       <Button x:Name="clickToShowPopup" Text="ClickToShowPopup" 
               VerticalOptions="Start" HorizontalOptions="FillAndExpand"
               Clicked="ClickToShowPopup_Clicked" />
        <syncfusion:SfPopup x:Name="popup"  ShowFooter="True" AppearanceMode="TwoButton"/>
     </StackLayout>
</ContentPage>

{% endhighlight %}

{% highlight c# tabtitle="MainPage.xaml.cs" hl_lines="13 14" %}
using Syncfusion.Maui.Toolkit.Popup;

namespace GettingStarted
{
    public partial class MainPage : ContentPage
    {
        SfPopup popup;

        public MainPage()
        {
            InitializeComponent();
            popup = new SfPopup();
            popup.ShowFooter = true;
            popup.AppearanceMode = Syncfusion.Maui.Popup.PopupButtonAppearanceMode.TwoButton;
        }

        private void ClickToShowPopup_Clicked(object sender, EventArgs e)
        {
            popup.Show();
        }
    }
}

{% endhighlight %}

{% endtabs %}

![Popup with Appearance Mode](Images/getting-started//maui-popup-with-appearance-mode.png)

##  Load template view in the popup body

Any view can be added as popup content by using the `ContentTemplate` property to refresh it. Refer to the following code example in which a label is added as popup content. 

{% tabs %}

{% highlight xaml tabtitle="MainPage.xaml" hl_lines="15" %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:local="clr-namespace:GettingStarted"
			 xmlns:syncfusion="clr-namespace:Syncfusion.Maui.Toolkit.Popup;assembly=Syncfusion.Maui.Toolkit"
             x:Class="GettingStarted.MainPage" 
             Padding="0,40,0,0">
    <StackLayout>
        <Button x:Name="clickToShowPopup"
                Text="ClickToShowPopup"
                VerticalOptions="Start"
                HorizontalOptions="FillAndExpand"
                Clicked="ClickToShowPopup_Clicked" />
        <syncfusion:SfPopup x:Name="popup">
            <syncfusion:SfPopup.ContentTemplate>
                <DataTemplate>
                    <Label Text="This is the Customized view for SfPopup"
                           BackgroundColor="SkyBlue"
                           VerticalTextAlignment="Center"
                           HorizontalTextAlignment="Center" />
                </DataTemplate>
            </syncfusion:SfPopup.ContentTemplate>
        </syncfusion:SfPopup>
    </StackLayout>
</ContentPage>

{% endhighlight %}

{% highlight c# tabtitle="MainPage.xaml.cs" hl_lines="23"%}
using Syncfusion.Maui.Toolkit.Popup;

namespace GettingStarted
{
    public partial class MainPage : ContentPage
    {
        DataTemplate templateView;
        Label popupContent;

        public MainPage()
        {
            InitializeComponent();            
            templateView = new DataTemplate(() =>
            {
                popupContent = new Label();
                popupContent.Text = "This is the Customized view for SfPopup";
                popupContent.BackgroundColor = Color.LightSkyBlue;
                popupContent.HorizontalTextAlignment = TextAlignment.Center;
                return popupContent;
            });

            // Adding ContentTemplate of the SfPopup
            popup.ContentTemplate = templateView;
        }

        private void ClickToShowPopup_Clicked(object sender, EventArgs e)
        {
            popup.Show();
        }
    } 
}

{% endhighlight %}

{% endtabs %}

![Popup with custom content](Images/getting-started//maui-popup-with-custom-content.png)