---
layout: post
title: Getting Started with .NET MAUI Chips control | Syncfusion
description: Learn here about getting started with Syncfusion<sup>®</sup> Toolkit for .NET MAUI Chips control, its elements and more.
platform: maui-toolkit
control: Chips
documentation: ug
---

# Getting Started with .NET MAUI Chips

This section provides instructions for setting up and configuring Chips control [Chips](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.html) in your .NET MAUI application. Follow the steps below to integrate a basic Chips component into your project.

{% tabcontents %}
{% tabcontent Visual Studio %}

## Prerequisites

Before proceeding, ensure the following are setup:

1. Install [.NET 9 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) or later.
2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.8 or later) or Visual Studio 2026 (v18.0.0 or later).

## Step 1: Create a New .NET MAUI Project

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Then, click **Next**.
3. Select the .NET framework version and click **Create**.

## Step 2: Install the Syncfusion<sup>®</sup> .NET MAUI Toolkit Package

1. In **Solution Explorer**, right-click the project and choose **Manage NuGet Packages**.
2. Search for [Syncfusion.Maui.Toolkit](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.html) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

## Step 3: Register the Handler 

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

## Step 4: Add a .NET MAUI Chips control

Step 1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Chips` namespace into your code.

Step 2. Initialize `SfChip` class.

{% tabs %}

{% highlight xaml %}
	
	xmlns:ChipControl="clr-namespace:Syncfusion.Maui.Toolkit.Chips;assembly=Syncfusion.Maui.Toolkit"
       
{% endhighlight %}

{% highlight c# %}

    using Syncfusion.Maui.Toolkit.Chips;

{% endhighlight %}

{% endtabs %}

Step 3: Set the control to content in `ContentPage.`

**For SfChip**

{% tabs %}

{% highlight xaml %}

<ContentPage.Content>    
    <chip:SfChip x:Name="chips" />
</ContentPage.Content>

{% endhighlight %}

{% highlight c# %}
          
SfChip chips = new SfChip(); 
Content = chips;  

{% endhighlight %}

{% endtabs %}

**For SfChipGroup**

Initialize an empty [`SfChipGroup`] as shown in the following code snippet

{% tabs %}

{% highlight xaml %}

<ContentPage.Content>
	<Grid>
		<chip:SfChipGroup/>
	</Grid>
</ContentPage.Content>

{% endhighlight %}

{% highlight c# %}

	Grid grid = new Grid();
	SfChipGroup chipGroup = new SfChipGroup();
	grid.Children.Add(chipGroup);
	this.Content = grid;
		
{% endhighlight %}

{% endtabs %}

{% endtabcontent %}
{% tabcontent Visual Studio Code %}

## Prerequisites

Before proceeding, ensure the following are set up:

1. Install [.NET 9 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) or later is installed.
2. Set up a .NET MAUI environment with Visual Studio Code.
3. Ensure that the .NET MAUI extension is installed and configured as described [here.](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-9.0&tabs=visual-studio-code)

## Step 1: Create a New .NET MAUI Project

1. Open the Command Palette by pressing **Ctrl+Shift+P** and type **.NET:New Project** and press Enter.
2. Choose the **.NET MAUI App** template.
3. Select the project location, type the project name and press **Enter**.
4. Then choose **Create project**

## Step 2: Install the Syncfusion<sup>®</sup> .NET MAUI Toolkit Package

1. Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (backtick) to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your .csproj file is located.
3. Run the command `dotnet add package Syncfusion.Maui.Toolkit` to install the Syncfusion<sup>®</sup> .NET MAUI Toolkit NuGet package.
4. To ensure all dependencies are installed, run `dotnet restore`.

## Step 3: Register the Handler 

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

## Step 4: Add a .NET MAUI Chips control

Step 1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Chips` namespace into your code.

Step 2. Initialize `SfChip` class.

{% tabs %}

{% highlight xaml %}
	
	xmlns:ChipControl="clr-namespace:Syncfusion.Maui.Toolkit.Chips;assembly=Syncfusion.Maui.Toolkit"
       
{% endhighlight %}

{% highlight c# %}

    using Syncfusion.Maui.Toolkit.Chips;

{% endhighlight %}

{% endtabs %}

Step 3: Set the control to content in `ContentPage.`

**For SfChip**

{% tabs %}

{% highlight xaml %}

<ContentPage.Content>    
    <chip:SfChip x:Name="chips" />
</ContentPage.Content>

{% endhighlight %}

{% highlight c# %}
          
SfChip chips = new SfChip(); 
Content = chips;  

{% endhighlight %}

{% endtabs %}

**For SfChipGroup**

Initialize an empty [`SfChipGroup`] as shown in the following code snippet

{% tabs %}

{% highlight xaml %}

<ContentPage.Content>
	<Grid>
		<chip:SfChipGroup/>
	</Grid>
</ContentPage.Content>


{% endhighlight %}

{% highlight c# %}

	Grid grid = new Grid();
	SfChipGroup chipGroup = new SfChipGroup();
	grid.Children.Add(chipGroup);
	this.Content = grid;
		
{% endhighlight %}

{% endtabs %}
{% endtabcontent %}

{% tabcontent JetBrains Rider %}

## Prerequisites

Before proceeding, ensure the following are set up:

1. Ensure you have the latest version of JetBrains Rider.
2. Install [.NET 9 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) or later is installed.
3. Make sure the MAUI workloads are installed and configured as described [here.](https://www.jetbrains.com/help/rider/MAUI.html#before-you-start)

## Step 1: Create a new .NET MAUI Project

1. Go to **File > New Solution,** Select .NET (C#) and choose the .NET MAUI App template.
2. Enter the Project Name, Solution Name, and Location.
3. Select the .NET framework version and click Create.

## Step 2: Install the Syncfusion<sup>®</sup> MAUI Toolkit NuGet Package

1. In **Solution Explorer,** right-click the project and choose **Manage NuGet Packages.**
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored. If not, Open the Terminal in Rider and manually run: `dotnet restore`

## Step 3: Register the Handler 

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

## Step 4: Add a .NET MAUI Chips control

Step 1. To initialize the control, import the `Syncfusion.Maui.Toolkit.Chips` namespace into your code.

Step 2. Initialize `SfChip` class.

{% tabs %}

{% highlight xaml %}
	
	xmlns:ChipControl="clr-namespace:Syncfusion.Maui.Toolkit.Chips;assembly=Syncfusion.Maui.Toolkit"
       
{% endhighlight %}

{% highlight c# %}

    using Syncfusion.Maui.Toolkit.Chips;

{% endhighlight %}

{% endtabs %}

Step 3: Set the control to content in `ContentPage.`

**For SfChip**

{% tabs %}

{% highlight xaml %}

<ContentPage.Content>    
    <chip:SfChip x:Name="chips" />
</ContentPage.Content>

{% endhighlight %}

{% highlight c# %}
          
SfChip chips = new SfChip(); 
Content = chips;  

{% endhighlight %}

{% endtabs %}

**For SfChipGroup**

Initialize an empty [`SfChipGroup`] as shown in the following code snippet

{% tabs %}

{% highlight xaml %}

<ContentPage.Content>
	<Grid>
		<chip:SfChipGroup/>
	</Grid>
</ContentPage.Content>


{% endhighlight %}

{% highlight c# %}

	Grid grid = new Grid();
	SfChipGroup chipGroup = new SfChipGroup();
	grid.Children.Add(chipGroup);
	this.Content = grid;
		
{% endhighlight %}

{% endtabs %}

{% endtabcontent %}
{% endtabcontents %}

## Step 5: Define the view model

Now, define a simple data model of person with the name properties.

{% tabs %}
{% highlight c# tabtitle="C#" %}

//Model class for chips
public class Person
{
	public string Name
	{
		get;
		set;
	}
}

{% endhighlight %}
{% endtabs %}

Next, create a view model class and initialize a collection of persons as shown in the following code sample.

{% tabs %}
{% highlight c# tabtitle="C#" %}

//View model class for chips
public class ViewModel : INotifyPropertyChanged
{
	private ObservableCollection<Person> employees;
	public ObservableCollection<Person> Employees
	{
		get { return employees; }
		set { Employees = value; OnPropertyChanged("Employees"); }
	}

	public ViewModel()
	{
		employees = new ObservableCollection<Person>();
		employees.Add(new Person() { Name = "John" });
		employees.Add(new Person() { Name = "James" });
		employees.Add(new Person() { Name = "Linda" });
		employees.Add(new Person() { Name = "Rose" });
		employees.Add(new Person() { Name = "Mark" });
	}

	public event PropertyChangedEventHandler PropertyChanged;

	public void OnPropertyChanged(string property)
	{
		if (PropertyChanged != null)
		{
			PropertyChanged(this, new PropertyChangedEventArgs(property));
		}
	}
}

{% endhighlight %}
{% endtabs %}

Create an instance of ViewModel class,and then set it as the `BindingContext`. Bind the `ItemsSource` property with a collection, and then set the `DisplayMemberPath` property:

{% tabs %}

{% highlight xaml %}

<ContentPage.BindingContext>
	<local:ViewModel x:Name="viewModel"/>
</ContentPage.BindingContext>
<ContentPage.Content>
	<Grid>
		<chip:SfChipGroup 
			ItemsSource="{Binding Employees}" 
			ChipPadding="8,8,0,0" 
			DisplayMemberPath="Name"
			ChipBackground="white"
			ChipTextColor="Black"
			HorizontalOptions="Start" 
			VerticalOptions="Center">
		</chip:SfChipGroup>  
	</Grid>
</ContentPage.Content>

{% endhighlight %}

{% highlight c# %}

this.BindingContext = new ViewModel();
Grid grid = new Grid();
SfChipGroup chipGroup = new SfChipGroup()
{
	DisplayMemberPath = "Name",
	HorizontalOptions = LayoutOptions.Start,
	VerticalOptions = LayoutOptions.Center,
	ChipTextColor = Colors.Black,
	ChipBackground = Colors.White,
	ChipPadding = new Thickness(8, 8, 0, 0),
};
chipGroup.SetBinding(SfChipGroup.ItemsSourceProperty, "Employees");
grid.Children.Add(chipGroup);
this.Content = grid;
		
{% endhighlight %}

{% endtabs %}

The following screenshot illustrates the result of the above code.

![ChipGroup sample with display member path and itemsSource demo](images/getting-started/getting_started.png)

N> When publishing in AOT mode on iOS, ensure `[Preserve(AllMembers = true)]` is added to the model class to maintain DisplayMemberPath binding
