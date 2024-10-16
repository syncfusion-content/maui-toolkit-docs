---
layout: post
title: Getting started with .NET MAUI Tab View (SfTabView) Control | Syncfusion
description: Learn how to set up, configure, and use the Syncfusion .NET MAUI Tab View (SfTabView) control in your cross-platform applications.
platform: maui-toolkit
control: Tab View control (SfTabView)
documentation: ug
---

# Getting started with .NET MAUI Tab View

This section guides you through setting up and configuring a [SfTabView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html) in your .NET MAUI application. Follow the steps below to add a basic Tab View to your project.

## Prerequisites

Before proceeding, ensure the following are setup:
1. Ensure [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later is installed.
2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.8 or later) or Visual Studio Code. For Visual Studio Code users, ensure that the .NET MAUI workload is installed and configured as described [here](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-8.0&tabs=visual-studio-code).

## Step 1: Create a new .NET MAUI project

### Visual Studio

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Click **Next**.
3. Select the .NET framework version and click **Create**.

### Visual Studio Code

1. Open the command palette by pressing `Ctrl+Shift+P` and type **.NET: New Project** and press **Enter**.
2. Choose the **.NET MAUI App** template.
3. Select the project location, type the project name, and press **Enter**.
4. Choose **Create project**.

## Step 2: Install the Syncfusion .NET MAUI Toolkit package

### Visual Studio

1. In **Solution Explorer**, right-click the project and choose **Manage NuGet Packages**.
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

### Visual Studio Code

1. Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (backtick) to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your .csproj file is located.
3. Run the command `dotnet add package Syncfusion.Maui.Toolkit` to install the Syncfusion .NET MAUI Toolkit NuGet package.
4. To ensure all dependencies are installed, run `dotnet restore`.

## Step 3: Register the handler

In the **MauiProgram.cs** file, register the handler for Syncfusion Toolkit.

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

## Step 4: Add a basic Tab View

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.TabView` namespace into your code.

2. Initialize [SfTabView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html)

{% tabs %}

{% highlight xaml %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="TabViewGettingStarted.MainPage"
             xmlns:local="clr-namespace:TabViewGettingStarted"
             xmlns:tabView="clr-namespace:Syncfusion.Maui.Toolkit.TabView;assembly=Syncfusion.Maui.Toolkit">
    <!-- Define the content of the ContentPage -->
    <ContentPage.Content>
        <!-- Add a SfTabView control to the ContentPage -->
        <tabView:SfTabView />
    </ContentPage.Content>
</ContentPage>
{% endhighlight %}

{% highlight C# %}
using Syncfusion.Maui.Toolkit.TabView;
namespace TabViewGettingStarted
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();
            // Create an instance of the SfTabView control
            SfTabView tabView = new SfTabView();
            // Set the Content property of the ContentPage to the newly created SfTabView instance
            this.Content = tabView;
        }
    }
}
{% endhighlight %}

{% endtabs %}

## Populate tab items in Tab View

Tab items can be added to the control using the [Items](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_Items) property of [SfTabView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html).

The following examples demonstrate how to add tab items to the `SfTabView` control using both XAML and C# approaches.

{% tabs %}
{% highlight xaml %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="TabViewGettingStarted.MainPage"
             xmlns:tabView="clr-namespace:Syncfusion.Maui.Toolkit.TabView;assembly=Syncfusion.Maui.Toolkit"
             BackgroundColor="{DynamicResource PageBackgroundColor}">
    <ContentPage.Content>
        <tabView:SfTabView x:Name="tabView">
            <!-- Define the items (tabs) of the SfTabView -->
            <tabView:SfTabView.Items>
                <!-- First tab item with header "Call" -->
                <tabView:SfTabItem Header="Call">
                    <!-- Content of the "Call" tab: a Grid with a red background -->
                    <tabView:SfTabItem.Content>
                        <Grid BackgroundColor="Red" />
                    </tabView:SfTabItem.Content>
                </tabView:SfTabItem>
                <!-- Second tab item with header "Favorites" -->
                <tabView:SfTabItem Header="Favorites">
                    <tabView:SfTabItem.Content>
                        <!-- Content of the "Favorites" tab: a ListView with predefined items -->
                        <ListView RowHeight="50">
                            <ListView.ItemsSource>
                                <!-- Define an array of strings as the data source for the ListView -->
                                <x:Array Type="{x:Type x:String}">
                                    <x:String>James</x:String>
                                    <x:String>Richard</x:String>
                                    <x:String>Michael</x:String>
                                    <x:String>Alex</x:String>
                                    <x:String>Clara</x:String>
                                </x:Array>
                            </ListView.ItemsSource>
                            <ListView.ItemTemplate>
                                <DataTemplate>
                                    <ViewCell>
                                        <!-- Define the layout for each item in the ListView -->
                                        <Grid Margin="10,5">
                                            <Label VerticalOptions="Start"
                                                   HorizontalOptions="Start"
                                                   TextColor="#666666"
                                                   FontSize="16"
                                                   Text="{Binding}" />
                                        </Grid>
                                    </ViewCell>
                                </DataTemplate>
                            </ListView.ItemTemplate>
                        </ListView>
                    </tabView:SfTabItem.Content>
                </tabView:SfTabItem>
                <!-- Third tab item with header "Contacts" -->
                <tabView:SfTabItem Header="Contacts">
                    <tabView:SfTabItem.Content>
                        <!-- Content of the "Contacts" tab: a Grid with a blue background -->
                        <Grid BackgroundColor="Blue" />
                    </tabView:SfTabItem.Content>
                </tabView:SfTabItem>
            </tabView:SfTabView.Items>
        </tabView:SfTabView>
    </ContentPage.Content>
</ContentPage>
{% endhighlight %}

{% highlight C# %}
using Syncfusion.Maui.Toolkit.TabView;
namespace TabViewGettingStarted
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();

            // Create an instance of the SfTabView control
            SfTabView tabView = new SfTabView();

            // Create a Grid with a red background for the "Call" tab
            Grid allContactsGrid = new Grid { BackgroundColor = Colors.Red };

            // Create a ListView for the "Favorites" tab with predefined items
            var favorites = new ListView
            {
                RowHeight = 50,
                ItemsSource = new string[] { "James", "Richard", "Michael", "Alex", "Clara" },
                ItemTemplate = new DataTemplate(() =>
                {
                    var grid = new Grid
                    {
                        Margin = new Thickness(10, 5)
                    };

                    var label = new Label
                    {
                        VerticalOptions = LayoutOptions.Start,
                        HorizontalOptions = LayoutOptions.Start,
                        TextColor = Color.FromArgb("#666666"),
                        FontSize = 16
                    };
                    label.SetBinding(Label.TextProperty, ".");

                    grid.Children.Add(label);

                    return new ViewCell
                    {
                        View = grid
                    };
                })
            };

            // Create a Grid with a blue background for the "Contacts" tab
            Grid contactsGrid = new Grid { BackgroundColor = Colors.Blue };

            // Create a collection of tab items and add the previously created content to each tab
            var tabItems = new TabItemCollection
            {
                new SfTabItem()
                {
                    Header = "Call",
                    Content = allContactsGrid
                },
                new SfTabItem()
                {
                    Header = "Favorites",
                    Content = favorites
                },
                new SfTabItem()
                {
                    Header = "Contacts",
                    Content = contactsGrid
                }
            };

            // Assign the collection of tab items to the SfTabView
            tabView.Items = tabItems;

            // Set the Content property of the ContentPage to the SfTabView instance
            this.Content = tabView;
        }
    }
}

{% endhighlight %}
{% endtabs %}

N> View [sample](https://github.com/SyncfusionExamples/maui-toolkit-samples/tree/master/TabView/TabViewGettingStarted) in GitHub

## Populate tab items using ItemsSource

The [ItemsSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_ItemsSource) property provides a flexible way to populate the `SfTabView` with data from a collection. This approach is particularly useful when you want to bind the tab items to a data source. 

Items can be added to the control using the `ItemsSource` property of [SfTabView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html).

Objects of any class can be given as items for `SfTabView` by using `ItemsSource`. The views corresponding to the objects can be set using the [HeaderItemTemplate](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_HeaderItemTemplate) for the header items and [ContentItemTemplate](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_ContentItemTemplate) for the content.

Create a **Model** class for data binding, that implements `INotifyPropertyChanged` to support property change notifications, as shown in the following code example:

{% tabs %}

{% highlight C# %}

    public class PersonModel : INotifyPropertyChanged
    {
        private string name;
		private string description;

        // Event to notify when a property value changes
        public event PropertyChangedEventHandler PropertyChanged;

        // Method to raise the PropertyChanged event
        protected void OnPropertyChanged(string propertyName)
        {
            PropertyChangedEventHandler handler = PropertyChanged;
            if (handler != null)
                handler(this, new PropertyChangedEventArgs(propertyName));
        }

        // Property for the person's name
        public string Name
        {
            get { return name; }
            set
            {
                name = value;
                // Notify that the Name property has changed
                OnPropertyChanged(nameof(Name));
            }
        }
		
        // Property for the person's description
        public string Description
        {
            get { return description; }
            set
            {
                description = value;
                // Notify that the Description property has changed
                OnPropertyChanged(nameof(Description));
            }
        }		
    }

{% endhighlight %}

{% endtabs %}

Next, we will create a **ViewModel** class that will serve as the data source for our `SfTabView`. This class contains an `ObservableCollection` named `TabItems`, which will hold the data for each tab. The constructor initializes this collection with sample data.

{% tabs %}

{% highlight C# %}

    public class PersonViewModel : INotifyPropertyChanged
    {
        private ObservableCollection<PersonModel> tabItems;

        // Event to notify when a property value changes
        public event PropertyChangedEventHandler PropertyChanged;

        // Method to raise the PropertyChanged event
        protected void OnPropertyChanged(string propertyName)
        {
            var handler = PropertyChanged;
            if (handler != null)
                handler(this, new PropertyChangedEventArgs(propertyName));
        }

        // Property for the collection of PersonModel items
        public ObservableCollection<PersonModel> TabItems
        {
            get { return tabItems; }
            set
            {
                tabItems = value;
                // Notify that the TabItems property has changed
                OnPropertyChanged(nameof(TabItems));
            }
        }

        // Constructor to initialize the collection with some default values
        public PersonViewModel()
        {
            TabItems = new ObservableCollection<PersonModel>();
            TabItems.Add(new PersonModel() { Name = "Alexandar" , Description = "Alexandar is a creative fiction writer with a knack for weaving intricate plots and complex characters. His works span a variety of genres, but he excels in contemporary fiction. With a passion for exploring human emotions, Alexandar’s stories are known for their depth and ability to resonate with readers on a personal level." });
            TabItems.Add(new PersonModel() { Name = "Gabriella", Description = "Create your description here..." });
            TabItems.Add(new PersonModel() { Name = "Clara" , Description = "Create your description here..." });
            TabItems.Add(new PersonModel() { Name = "Tye" , Description = "Create your description here..." });
            TabItems.Add(new PersonModel() { Name = "Nora" , Description = "Create your description here..." });
            TabItems.Add(new PersonModel() { Name = "Sebastian" , Description = "Create your description here..." });
        }
    }

{% endhighlight %}

{% endtabs %}

Now that we have our **Model** and **ViewModel** set up, we can bind the TabItems collection to the `ItemsSource` property of `SfTabView`. The following code examples demonstrate how to set up this binding in both XAML and C#:

{% tabs %}

{% highlight xaml %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="TabViewGettingStarted.MainPage"
             xmlns:local="clr-namespace:TabViewGettingStarted;assembly=TabViewGettingStarted"
             xmlns:tabView="clr-namespace:Syncfusion.Maui.Toolkit.TabView;assembly=Syncfusion.Maui.Toolkit"
             BackgroundColor="{DynamicResource PageBackgroundColor}">
    <!-- Set the BindingContext of the ContentPage to an instance of PersonViewModel -->
    <ContentPage.BindingContext>
        <local:PersonViewModel />
    </ContentPage.BindingContext>
    <!-- Bind the ItemsSource of the SfTabView to the TabItems property of the PersonViewModel -->
    <tabView:SfTabView ItemsSource="{Binding TabItems}" />
</ContentPage>
{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.TabView;

namespace TabViewGettingStarted
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();

            // Create an instance of the PersonViewModel
            PersonViewModel viewModel = new PersonViewModel();

            // Set the BindingContext of the ContentPage to the PersonViewModel instance
            this.BindingContext = viewModel;

            // Create an instance of the SfTabView control
            SfTabView tabView = new SfTabView();

            // Bind the ItemsSource of the SfTabView to the TabItems property of the PersonViewModel
            tabView.ItemsSource = viewModel.TabItems;

            // Set the Content property of the ContentPage to the SfTabView instance
            this.Content = tabView;
        }
    }
}

{% endhighlight %}

{% endtabs %}

### Header item template

The [HeaderItemTemplate](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_HeaderItemTemplate) property allows you to define a custom appearance for the tab header data items. Here is how you can define a `HeaderItemTemplate`:

{% tabs %}

{% highlight xaml %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="TabViewGettingStarted.MainPage"
             xmlns:local="clr-namespace:TabViewGettingStarted;assembly=TabViewGettingStarted"
             xmlns:tabView="clr-namespace:Syncfusion.Maui.Toolkit.TabView;assembly=Syncfusion.Maui.Toolkit">
    <!-- Set the BindingContext of the ContentPage to an instance of PersonViewModel -->
    <ContentPage.BindingContext>
        <local:PersonViewModel />
    </ContentPage.BindingContext>
    <!-- Bind the ItemsSource of the SfTabView to the TabItems property of the PersonViewModel -->
    <tabView:SfTabView ItemsSource="{Binding TabItems}">
        <!-- Define the template for the header items of the SfTabView -->
        <tabView:SfTabView.HeaderItemTemplate>
            <DataTemplate>
                <!-- Display the Name property of each PersonModel in a Label -->
                <Label Padding="5,10,10,10"
                       Text="{Binding Name}" />
            </DataTemplate>
        </tabView:SfTabView.HeaderItemTemplate>
    </tabView:SfTabView>
</ContentPage>
{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.TabView;
namespace TabViewGettingStarted
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();

            // Create an instance of the PersonViewModel
            PersonViewModel viewModel = new PersonViewModel();

            // Set the BindingContext of the ContentPage to the PersonViewModel instance
            this.BindingContext = viewModel;

            // Create an instance of the SfTabView control
            SfTabView tabView = new SfTabView();

            // Bind the ItemsSource of the SfTabView to the TabItems property of the PersonViewModel
            tabView.ItemsSource = viewModel.TabItems;

            // Define the template for the header items of the SfTabView
            tabView.HeaderItemTemplate = new DataTemplate(() =>
            {
                var nameLabel = new Label { Padding = new Thickness(5, 10, 10, 10) };
                // Bind the Text property of the Label to the Name property of the PersonModel
                nameLabel.SetBinding(Label.TextProperty, "Name");

                return nameLabel;
            });

            // Set the Content of the ContentPage to the SfTabView
            this.Content = tabView;
        }
    }
}

{% endhighlight %}

{% endtabs %}

### Content item template

The [ContentItemTemplate](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_ContentItemTemplate) property allows you to define a custom layout for the tab content data items. Here is an example of how to set up a `ContentItemTemplate`:

{% tabs %}

{% highlight xaml %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="TabViewGettingStarted.MainPage"
             xmlns:local="clr-namespace:TabViewGettingStarted;assembly=TabViewGettingStarted"
             xmlns:tabView="clr-namespace:Syncfusion.Maui.Toolkit.TabView;assembly=Syncfusion.Maui.Toolkit">
    <!-- Set the BindingContext of the ContentPage to an instance of PersonViewModel -->
    <ContentPage.BindingContext>
        <local:PersonViewModel />
    </ContentPage.BindingContext>
    <!-- Bind the ItemsSource of the SfTabView to the TabItems property of the PersonViewModel -->
    <tabView:SfTabView ItemsSource="{Binding TabItems}">
        <!-- Define the template for the header items of the SfTabView -->
        <tabView:SfTabView.HeaderItemTemplate>
            <DataTemplate>
                <!-- Display the Name property of each PersonModel in a Label -->
                <Label Padding="5,10,10,10"
                       Text="{Binding Name}" />
            </DataTemplate>
        </tabView:SfTabView.HeaderItemTemplate>
        <!-- Define the template for the content items of the SfTabView -->
        <tabView:SfTabView.ContentItemTemplate>
            <DataTemplate>
                <!-- Display the Description property of each PersonModel in a Label -->
                <Label TextColor="Black"
                       Text="{Binding Description}" />
            </DataTemplate>
        </tabView:SfTabView.ContentItemTemplate>
    </tabView:SfTabView>
</ContentPage>
{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.TabView;
namespace TabViewGettingStarted
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();

            // Create an instance of the PersonViewModel
            PersonViewModel viewModel = new PersonViewModel();

            // Set the BindingContext of the ContentPage to the PersonViewModel instance
            this.BindingContext = viewModel;

            // Create an instance of the SfTabView control
            SfTabView tabView = new SfTabView();

            // Bind the ItemsSource of the SfTabView to the TabItems property of the PersonViewModel
            tabView.ItemsSource = viewModel.TabItems;

            // Define the template for the header items of the SfTabView
            tabView.HeaderItemTemplate = new DataTemplate(() =>
            {
                var nameLabel = new Label { Padding = new Thickness(5, 10, 10, 10) };
                // Bind the Text property of the Label to the Name property of the PersonModel
                nameLabel.SetBinding(Label.TextProperty, "Name");

                return nameLabel;
            });

            // Define the template for the content items of the SfTabView
            tabView.ContentItemTemplate = new DataTemplate(() =>
            {
                var descriptionLabel = new Label { TextColor = Colors.Black };
                // Bind the Text property of the Label to the Description property of the PersonModel
                descriptionLabel.SetBinding(Label.TextProperty, "Description");
                return descriptionLabel;
            });

            // Set the Content of the ContentPage to the SfTabView
            this.Content = tabView;
        }
    }
}

{% endhighlight %}

{% endtabs %}

The following image demonstrates the `SfTabView` displaying custom tab headers and content using `HeaderItemTemplate` and `ContentItemTemplate`.

![.NET MAUI Tab View Item Template](images/ItemTemplate.png)
