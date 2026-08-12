---
layout: post
title: Populating ItemsSource in .NET MAUI Tab View | Syncfusion®
description: Learn about populating ItemsSource in the Syncfusion® .NET MAUI Tab View (SfTabView) control, its elements, and more.
platform: maui-toolkit
control: SfTabView
documentation: UG
---

# Populating ItemsSource in .NET MAUI Tab View

## Step 6: Populate tab items using ItemsSource

The [ItemsSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_ItemsSource) property provides a flexible way to populate the `Tab View` with data from a collection. This approach is particularly useful when you want to bind the tab items to a data source. 

Items can be added to the control using the `ItemsSource` property of [Tab View](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html).

Objects of any class can be provided as items for `Tab View` using `ItemsSource`. The views corresponding to the objects can be set using the [HeaderItemTemplate](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_HeaderItemTemplate) for the header items and [ContentItemTemplate](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_ContentItemTemplate) for the content.

Create a **Model** class for data binding, that implements `INotifyPropertyChanged` to support property change notifications, as shown in the following code example:

{% tabs %}

{% highlight C# %}

namespace TabViewGettingStarted
{
    public class PersonModel : INotifyPropertyChanged
    {
        private string name;
        private string description;

        public event PropertyChangedEventHandler PropertyChanged;

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
                OnPropertyChanged(nameof(Description));
            }
        }
    }
}
{% endhighlight %}

{% endtabs %}

Next, we will create a **ViewModel** class that will serve as the data source for our `Tab View`. This class contains an `ObservableCollection` named `TabItems`, which will hold the data for each tab. The constructor initializes this collection with sample data.

{% tabs %}

{% highlight C# %}
namespace TabViewGettingStarted
{
    public class PersonViewModel : INotifyPropertyChanged
    {
        private ObservableCollection<PersonModel> tabItems;

        public event PropertyChangedEventHandler PropertyChanged;

        protected void OnPropertyChanged(string propertyName)
        {
            var handler = PropertyChanged;
            if (handler != null)
                handler(this, new PropertyChangedEventArgs(propertyName));
        }

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

        public PersonViewModel()
        {
            TabItems = new ObservableCollection<PersonModel>();
            TabItems.Add(new PersonModel() { Name = "Alexandar", Description = "Alexandar is a creative fiction writer with a knack for weaving intricate plots and complex characters. His works span a variety of genres, but he excels in contemporary fiction. With a passion for exploring human emotions, Alexandar’s stories are known for their depth and ability to resonate with readers on a personal level." });
            TabItems.Add(new PersonModel() { Name = "Gabriella", Description = "Create your description here..." });
            TabItems.Add(new PersonModel() { Name = "Clara", Description = "Create your description here..." });
            TabItems.Add(new PersonModel() { Name = "Tye", Description = "Create your description here..." });
            TabItems.Add(new PersonModel() { Name = "Nora", Description = "Create your description here..." });
            TabItems.Add(new PersonModel() { Name = "Sebastian", Description = "Create your description here..." });
        }
    }
}
{% endhighlight %}

{% endtabs %}

Now that we have our **Model** and **ViewModel** set up, we can bind the `TabItems` collection to the `ItemsSource` property of `Tab View`. The following code examples demonstrate how to set up this binding in both XAML and C#:

{% tabs %}

{% highlight xaml %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage . . .
             xmlns:local="clr-namespace:TabViewGettingStarted;assembly=TabViewGettingStarted"
             xmlns:tabView="clr-namespace:Syncfusion.Maui.Toolkit.TabView;assembly=Syncfusion.Maui.Toolkit"
             BackgroundColor="{DynamicResource PageBackgroundColor}">
    <ContentPage.BindingContext>
        <local:PersonViewModel />
    </ContentPage.BindingContext>
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

            PersonViewModel viewModel = new PersonViewModel();
            this.BindingContext = viewModel;

            SfTabView tabView = new SfTabView();
            tabView.ItemsSource = viewModel.TabItems;

            this.Content = tabView;
        }
    }
}

{% endhighlight %}

{% endtabs %}

### HeaderItemTemplate

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

### ContentItemTemplate

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

The following image demonstrates the `Tab View` displaying custom tab headers and content using `HeaderItemTemplate` and `ContentItemTemplate`.

![.NET MAUI Tab View Item Template](images/ItemTemplate.png)