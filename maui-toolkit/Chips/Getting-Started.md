---
layout: post
title: Getting Started with .NET MAUI Chips control | Syncfusion<sup>®</sup>
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

1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later.
2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.8 or later)

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

{% endtabcontent %}
{% endtabcontents %}

## For SfChip

{% tabs %}

{% highlight xaml %}

<ContentPage.Content>    
    <ChipControl:SfChip x:Name="chips" />
</ContentPage.Content>

{% endhighlight %}

{% highlight c# %}
          
SfChip chips = new SfChip(); 
Content = chips;  

{% endhighlight %}

{% endtabs %}

## For SfChipGroup

Initialize an empty `SfChipGroup` as shown in the following code snippet

{% tabs %}

{% highlight xaml %}

<ContentPage.Content>
	<Grid>
		<ChipControl:SfChipGroup/>
	</Grid>
</ContentPage.Content>


{% endhighlight %}

{% highlight c# %}

using Syncfusion.Maui.Toolkit.Chips;
Grid grid = new Grid();
SfChipGroup chipGroup = new SfChipGroup();
grid.Children.Add(chipGroup);
this.Content = grid;
		
{% endhighlight %}

{% endtabs %}

## Set layout for the control

The chips control creates chip for each object and arranges chips in a `StackLayout` with horizontal orientation. Any layout can be used to arrange the chips in the chips control. In the following example, the `FlexLayout` has been used. 

{% tabs %}

{% highlight xaml %}

<ContentPage.Content>
	<Grid>
		<ChipControl:SfChipGroup DisplayMemberPath="Name">
			<ChipControl:SfChipGroup.ChipLayout>
				<FlexLayout 
					HorizontalOptions="Start" 
					VerticalOptions="Center"/> 
			</ChipControl:SfChipGroup.ChipLayout>
		</ChipControl:SfChipGroup> 
	</Grid>
</ContentPage.Content>

{% endhighlight %}

{% highlight c# %}

using Syncfusion.Maui.Toolkit.Chips;
Grid grid = new Grid();
SfChipGroup chipGroup = new SfChipGroup();
chipGroup.DispalyMemberPath="Name";
grid.Children.Add(chipGroup);
FlexLayout layout = new FlexLayout()
{
	HorizontalOptions = LayoutOptions.Start,
	VerticalOptions = LayoutOptions.Center,
};
chipGroup.ChipLayout = layout;
this.Content = grid;
		
{% endhighlight %}

{% endtabs %}

## Populating business objects

Now, define a simple data model of Employee with the name and image properties. Create a view model class and initialize a collection of Employee as shown in the following code sample.

{% highlight c# %}

namespace Chips
{
	//Model class for chips
	public class Employee
	{
		public string Name
		{
			get;
			set;
		}
	}
}

{% endhighlight %}

{% highlight c# %}

using System.Collections.ObjectModel;
using System.ComponentModel;
namespace Chips
{
	//View model class for chips
	public class ViewModel : INotifyPropertyChanged
	{
		private ObservableCollection<Employee> employees;
		public ObservableCollection<Employee> Employees
		{
			get { return employees; }
			set { Employees = value; OnPropertyChanged("Employees"); }
		}

		public ViewModel()
		{
			employees = new ObservableCollection<Employee>();
			employees.Add(new Employee() { Name = "John" });
			employees.Add(new Employee() { Name = "James" });
			employees.Add(new Employee() { Name = "Linda" });
			employees.Add(new Employee() { Name = "Rose" });
			employees.Add(new Employee() { Name = "Mark" });
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
}

{% endhighlight %}

Create an instance of ViewModel class,and then set it as the `BindingContext`. Bind the `ItemsSource` property with a collection, and then set the `DisplayMemberPath` property:

{% tabs %}

{% highlight xaml %}

<ContentPage.BindingContext>
	<local:ViewModel x:Name="viewModel"/>
</ContentPage.BindingContext>
<ContentPage.Content>
	<Grid>
		<ChipControl:SfChipGroup 
			ItemsSource="{Binding Employees}" 
			ChipPadding="8,8,0,0" 
			DisplayMemberPath="Name"
			ChipBackground="white"
			ChipTextColor="Black"
			HorizontalOptions="Start" 
			VerticalOptions="Center">
		</ChipControl:SfChipGroup>  
	</Grid>
</ContentPage.Content>

{% endhighlight %}

{% highlight c# %}

using Syncfusion.Maui.Toolkit.Chips;
using System.Collections.ObjectModel;
using System.ComponentModel;

Grid grid = new Grid();
SfChipGroup chipGroup = new SfChipGroup();
grid.Children.Add(chipGroup);
this.BindingContext = new ViewModel();
chipGroup.SetBinding(SfChipGroup.ItemsSourceProperty, "Employees");
chipGroup.DisplayMemberPath = "Name";
chipGroup.HorizontalOptions = LayoutOptions.Start;
chipGroup.VerticalOptions = LayoutOptions.Center;
chipGroup.ChipTextColor = Colors.Black;
chipGroup.ChipBackground = Colors.White;
chipGroup.ChipPadding = new Thickness(8, 8, 0, 0);
this.Content = grid;
		
{% endhighlight %}

{% endtabs %}

![ChipGroup sample with display member path and itemsSource demo](images/getting-started/getting_started.png)

N> When publishing in AOT mode on iOS, ensure `[Preserve(AllMembers = true)]` is added to the model class to maintain DisplayMemberPath binding

## Set types of chip group

The functionality of chips control differ based on its [ChipType](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.SfChipGroup.html#Syncfusion_Maui_Toolkit_Chips_SfChipGroup_ChipType) property.
By default type of chips control have Input type. Input chip types have close button, using it chip can be can removed dynamically from children and the layout.

The following code example uses the [Action](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.SfChipsType.html#Syncfusion_Maui_Toolkit_Chips_SfChipsType_Action) type. In Action type, [Command](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.SfChipGroup.html#Syncfusion_Maui_Toolkit_Chips_SfChipGroup_Command) property of [SfChipGroup](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.SfChipGroup.html) is executed when any chip in the group is tapped. Here the Employee name of corresponding chip is set as label text when the Command is executed.

{% tabs %}

{% highlight xaml %}

<ContentPage.BindingContext>
	<local:ViewModel/>
</ContentPage.BindingContext>
<ContentPage.Content>
	<StackLayout>
		<ChipControl:SfChipGroup
			Command="{Binding ActionCommand}" 
			ItemsSource="{Binding Employees}"
			DisplayMemberPath="Name"
			ChipType="Action">
		</ChipControl:SfChipGroup>
		<StackLayout Orientation="Horizontal">
		<Label 
			Text="Name:" 
			FontAttributes="Bold" 
			FontSize="14" />
		<Label 
			Text="{Binding Result}"
			FontAttributes="Bold" 
			FontSize="14" />
		</StackLayout>
	</StackLayout>  
</ContentPage.Content>
{% endhighlight %}
{% highlight c# %}

using System;
using System.Collections.Generic;
using System.Collections.ObjectModel;
using System.ComponentModel;
using System.Windows.Input;

namespace Chips
{
	public class ViewModel :INotifyPropertyChanged
	{
		private ICommand actionCommand;
		private ObservableCollection<Employee> employees;
		private string result;
		public ICommand ActionCommand
    	{
			get { return actionCommand; }
			set { actionCommand = value; }
    	}
    
    	public ObservableCollection<Employee> Employees
    	{
        	get { return employees; }
        	set { Employees = value; OnPropertyChanged("Employees"); }
    	}

		public string Result
		{
			get { return result; }
			set { result = value; OnPropertyChanged("Result"); }
		}

		public ViewModel()
		{
			ActionCommand = new Command(HandleAction);
			employees = new ObservableCollection<Employee>();
			employees.Add(new Employee() { Name = "John" });
			employees.Add(new Employee() { Name = "James" });
			employees.Add(new Employee() { Name = "Linda" });
			employees.Add(new Employee() { Name = "Rose" });
			employees.Add(new Employee() { Name = "Mark" });
		}

		public event PropertyChangedEventHandler PropertyChanged;

		public void OnPropertyChanged(string property)
		{
			if (PropertyChanged != null)
			{
				PropertyChanged(this, new PropertyChangedEventArgs(property));
			}
		}

		private void HandleAction(object obj)
		{
			Result = (obj as Employee).Name.ToString();
		}
	}
}

{% endhighlight %}

{% endtabs %}

![ChipGroup sample with display member path and itemsSource demo](images/getting-started/action.png)


