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

<table>
<tr>
<th> Visual Studio </th>
<th> Visual Studio Code </th>
</tr>
<tr>
<td>
<ol>
<li> Go to <b>File > New > Project</b> and choose the <b>.NET MAUI App</b> template.</li>
<li> Name the project and choose a location. Click <b>Next</b>.</li>
<li> Select the .NET framework version and click <b>Create</b>.</li>
</ol>
</td>
<td>
<ol>
<li> Open the command palette by pressing <code>Ctrl + Shift + P</code> and type <b>.NET: New Project</b> and press <b>Enter</b>.</li>
<li> Choose the <b>.NET MAUI App</b> template.</li>
<li> Select the project location, type the project name, and press <b>Enter</b>.</li>
<li> Choose <b>Create project</b>.</li>
</ol>
</td>
</tr>
</table>

## Step 2: Install the Syncfusion .NET MAUI Toolkit package

<table>
<tr>
<th> Visual Studio </th>
<th> Visual Studio Code </th>
</tr>
<tr>
<td>
<ol>
<li> In <b>Solution Explorer</b>, right-click the project and choose <b>Manage NuGet Packages</b>.</li>
<li> Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.</li>
<li> Ensure the necessary dependencies are installed correctly, and the project is restored.</li>
</ol>
</td>
<td>
<ol>
<li> Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (backtick) to open the integrated terminal in Visual Studio Code.</li>
<li> Ensure you're in the project root directory where your <code>.csproj</code> file is located.</li>
<li> Run the command <code>dotnet add package Syncfusion.Maui.Toolkit</code> to install the Syncfusion .NET MAUI Toolkit NuGet package.</li>
<li> To ensure all dependencies are installed, run <code>dotnet restore</code>.</li>
</ol>
</td>
</tr>
</table>

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
<ContentPage 
            ...
            xmlns:tabView="clr-namespace:Syncfusion.Maui.Toolkit.TabView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
        <tabView:SfTabView/> 
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
            SfTabView tabView = new SfTabView();   
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
            x:Class="TabViewMauiSample.MainPage"
            xmlns:tabView="clr-namespace:Syncfusion.Maui.Toolkit.TabView;assembly=Syncfusion.Maui.Toolkit"
            BackgroundColor="{DynamicResource PageBackgroundColor}">
    <ContentPage.Content> 
        <tabView:SfTabView x:Name="tabView">
            <tabView:SfTabView.Items>
                <tabView:SfTabItem Header="Call">
                    <tabView:SfTabItem.Content>
                        <Grid BackgroundColor="Red" />
                    </tabView:SfTabItem.Content>
                </tabView:SfTabItem>

                <tabView:SfTabItem Header="Favorites">
                     <tabView:SfTabItem.Content>
                    <ListView RowHeight="50">
                        <ListView.ItemsSource>
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
                                    <Grid Margin="10,5">
                                        <Label
                                            VerticalOptions="Start"
                                            HorizontalOptions="Start"
                                            TextColor="#666666"
                                            FontSize="16"
                                            Text="{Binding}"/>
                                    </Grid>
                                </ViewCell>
                            </DataTemplate>
                        </ListView.ItemTemplate>
                    </ListView>
                </tabView:SfTabItem.Content>
                </tabView:SfTabItem>

                <tabView:SfTabItem Header="Contacts">
                    <tabView:SfTabItem.Content>
                        <Grid BackgroundColor="Blue"/>
                    </tabView:SfTabItem.Content>
                </tabView:SfTabItem>
            </tabView:SfTabView.Items>
        </tabView:SfTabView>
    </ContentPage.Content>  
</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.TabView;

namespace TabViewMauiSample
{
	public partial class TabView : ContentPage
	{
		public TabView ()
		{
			InitializeComponent ();
            SfTabView tabView = new SfTabView();
            Grid allContactsGrid = new Grid { BackgroundColor = Colors.Red };
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
            Grid contactsGrid = new Grid { BackgroundColor = Colors.Blue };
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

            tabView.Items = tabItems;
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

Create a simple model class that uses `TabItems` collection property to represent the number of data objects. This class implements `INotifyPropertyChanged` to support property change notifications, which is crucial for data binding, as shown in the following code example:

{% tabs %}

{% highlight C# %}

public class Model: INotifyPropertyChanged
{
    private string name;
    public event PropertyChangedEventHandler PropertyChanged;

    protected void OnPropertyChanged(string propertyName)
    {
        var handler = PropertyChanged;
        if (handler != null)
            handler(this, new PropertyChangedEventArgs(propertyName));
    }

    public string Name
    {
        get { return name; }
        set
        {
            name = value;
            OnPropertyChanged(nameof(Name));
        }
    }
}

{% endhighlight %}

{% endtabs %}

Next, we will create a ViewModel class that will serve as the data source for our `SfTabView`. This class contains an `ObservableCollection` named `TabItems`, which will hold the data for each tab. The constructor initializes this collection with sample data.

{% tabs %}

{% highlight C# %}

public class TabItemsSourceViewModel : INotifyPropertyChanged
{
    private ObservableCollection<Model> tabItems;
    public event PropertyChangedEventHandler PropertyChanged;

    protected void OnPropertyChanged(string propertyName)
    {
        var handler = PropertyChanged;
        if (handler != null)
            handler(this, new PropertyChangedEventArgs(propertyName));
    }

    public ObservableCollection<Model> TabItems
    {
        get { return tabItems; }
        set
        {
            tabItems = value;
            OnPropertyChanged(nameof(TabItems));
        }
    }
    public TabItemsSourceViewModel()
    {
        TabItems = new ObservableCollection<Model>();
        TabItems.Add(new Model() { Name = "Alexandar" });
        TabItems.Add(new Model() { Name = "Gabriella" });
        TabItems.Add(new Model() { Name = "Clara"});
        TabItems.Add(new Model() { Name = "Tye" });
        TabItems.Add(new Model() { Name = "Nora" });
        TabItems.Add(new Model() { Name = "Sebastian" });
    }
}

{% endhighlight %}

{% endtabs %}

Now that we have our `Model` and `ViewModel` set up, we can bind the TabItems collection to the `ItemsSource` property of `SfTabView`. The following code examples demonstrate how to set up this binding in both XAML and C#:

{% tabs %}

{% highlight xaml %}
    <ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="ItemTemplateSample.MainPage"
             xmlns:local="clr-namespace:ItemTemplateSample"
             xmlns:tabView="clr-namespace:Syncfusion.Maui.Toolkit.TabView;assembly=Syncfusion.Maui.Toolkit"
             BackgroundColor="{DynamicResource SecondaryColor}" >
    <ContentPage.BindingContext>
        <local:TabItemsSourceViewModel/>
    </ContentPage.BindingContext>
    <tabView:SfTabView ItemsSource="{Binding TabItems}" >
    </tabView:SfTabView>
    </ContentPage>
{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.TabView;

namespace ItemTemplateSample;

public partial class MainPage : ContentPage
{
	public MainPage()
	{
		InitializeComponent();
		TabItemsSourceViewModel model = new TabItemsSourceViewModel();
		this.BindingContext = model;
		SfTabView tabView = new SfTabView();
        tabView.ItemsSource = model.TabItems;
		this.Content = tabView;
    } 
}

{% endhighlight %}

{% endtabs %}

### Header item template

The [HeaderItemTemplate](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_HeaderItemTemplate) property allows you to define a custom appearance for the tab header data items. Here is how you can define a `HeaderItemTemplate`:

{% tabs %}

{% highlight xaml %}
    <ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="ItemTemplateSample.MainPage"
             xmlns:local="clr-namespace:ItemTemplateSample"
             xmlns:tabView="clr-namespace:Syncfusion.Maui.Toolkit.TabView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.BindingContext>
        <local:TabItemsSourceViewModel/>
    </ContentPage.BindingContext>
    <tabView:SfTabView ItemsSource="{Binding TabItems}">
        <tabView:SfTabView.HeaderItemTemplate>
                <DataTemplate>
                    <Label Padding="5,10,10,10" Text="{Binding Name}"/>
                 </DataTemplate>
            </tabView:SfTabView.HeaderItemTemplate>
    </tabView:SfTabView>
    </ContentPage>
    
{% endhighlight %}

{% highlight C# %}

namespace ItemTemplateSample;

public partial class MainPage : ContentPage
{
	public MainPage()
	{
		InitializeComponent();
		TabItemsSourceViewModel model = new TabItemsSourceViewModel();
		this.BindingContext = model;
		SfTabView tabView = new SfTabView();
		tabView.ItemsSource = model.TabItems;
		tabView.HeaderItemTemplate = new DataTemplate(() =>
		{
			var nameLabel = new Label { Padding = new Thickness(5,10,10,10)};
            nameLabel.SetBinding(Label.TextProperty, "Name");
		    
			return nameLabel;
		});
		this.Content = tabView;
    }
}

{% endhighlight %}

{% endtabs %}

### Content item template

The [ContentItemTemplate](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_ContentItemTemplate) property allows you to define a custom layout for the tab content data items. Here is an example of how to set up a `ContentItemTemplate`:

{% tabs %}

{% highlight xaml %}
    <ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="ItemTemplateSample.MainPage"
             xmlns:local="clr-namespace:ItemTemplateSample"
             xmlns:tabView="clr-namespace:Syncfusion.Maui.Toolkit.TabView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.BindingContext>
        <local:TabItemsSourceViewModel/>
    </ContentPage.BindingContext>
    <tabView:SfTabView ItemsSource="{Binding TabItems}">
        <tabView:SfTabView.HeaderItemTemplate>
                <DataTemplate>
                    <Label Padding="5,10,10,10" Text="{Binding Name}"/>
                 </DataTemplate>
            </tabView:SfTabView.HeaderItemTemplate>
             <tabView:SfTabView.ContentItemTemplate>
                <DataTemplate>
                     <Label TextColor="Black" Text="{Binding Name}"/>
               </DataTemplate>
        </tabView:SfTabView.ContentItemTemplate>
    </tabView:SfTabView>
    </ContentPage>
{% endhighlight %}

{% highlight C# %}

namespace ItemTemplateSample;

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        TabItemsSourceViewModel model = new TabItemsSourceViewModel();
        this.BindingContext = model;
        SfTabView tabView = new SfTabView();
        tabView.ItemsSource = model.TabItems;
        tabView.HeaderItemTemplate = new DataTemplate(() =>
        {
            var nameLabel = new Label { Padding = new Thickness(5,10,10,10)};
            nameLabel.SetBinding(Label.TextProperty, "Name");
            
            return nameLabel;
        });
        tabView.ContentItemTemplate = new DataTemplate(() =>
        {
            var nameLabel = new Label { TextColor=Colors.Black };
            nameLabel.SetBinding(Label.TextProperty, "Name");
            return nameLabel;
        });
        this.Content = tabView;
    }
}

{% endhighlight %}

{% endtabs %}

The following image demonstrates the `SfTabView` displaying custom tab headers and content using `HeaderItemTemplate` and `ContentItemTemplate`.

![.NET MAUI Tab View Item Template](images/ItemTemplate.png)

