---
layout: post
title: Getting Started with .NET MAUI Text Input Layout control | Syncfusion
description: Learn here about getting started with Syncfusion .NET MAUI Text Input Layout (SfTextInputLayout) control, its elements and more.
platform: maui-toolkit
control: SfTextInputLayout
documentation: ug
keywords: .net maui text input layout, syncfusion text input layout, text input layout maui, .net maui hint label.
---

# Getting Started with .NET MAUI TextInputLayout

This section guides you through setting up and configuring a `TextInputLayout` in your .NET MAUI application. Follow the steps below to add a basic TextInputLayout to your project.

## Prerequisites

Before proceeding, ensure the following are in place:

1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later.
2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.3 or later) or Visual Studio Code. For Visual Studio Code users, ensure that the .NET MAUI workload is installed and configured as described [here](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-8.0&tabs=visual-studio-code).

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

## Step 2: Install the Syncfusion MAUI Toolkit NuGet Package

### Visual Studio

1. In **Solution Explorer**, right-click the project and choose **Manage NuGet Packages**.
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

### Visual Studio Code

1. Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (backtick) to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your `.csproj` file is located.
3. Run the following command to install the Syncfusion MAUI Expander NuGet package:

{% tabs %}
{% highlight sh %}

   dotnet add package Syncfusion.Maui.Toolkit

{% endhighlight %}
{% endtabs %}

4. To ensure all dependencies are installed, run:

{% tabs %}
{% highlight sh %}

   dotnet restore

{% endhighlight %}
{% endtabs %}

## Step 3: Register the Handler

In the **MauiProgram.cs file**, register the handler for Syncfusion Toolkit.

{% highlight c# hl_lines="6 17" %}   
using Microsoft.Maui;
using Microsoft.Maui.Hosting;
using Microsoft.Maui.Controls.Compatibility;
using Microsoft.Maui.Controls.Hosting;
using Microsoft.Maui.Controls.Xaml;
using Syncfusion.Maui.Toolkit.Hosting;

namespace TextInputLayoutSample
{
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
}     

{% endhighlight %}

## Step 4: Add a Basic TextInputLayout

Step 1: Add the NuGet to the project as discussed in the above reference section.

Step 2: Add the namespace as shown in the following code sample.

Add the following namespace to add `.NET MAUI Text Input Layout`.

{% tabs %}

{% highlight xaml %}

    xmlns:inputLayout="clr-namespace:Syncfusion.Maui.Toolkit.TextInputLayout;assembly=Syncfusion.Maui.Toolkit"
	
{% endhighlight %}

{% highlight c# %}

    using Syncfusion.Maui.Toolkit.TextInputLayout;

{% endhighlight %}

{% endtabs %}

### Adding the .NET MAUI Text Input Layout control

Add any input view control such as [Entry](https://learn.microsoft.com/en-us/dotnet/maui/user-interface/controls/entry) and [Editor](https://learn.microsoft.com/en-us/dotnet/maui/user-interface/controls/editor) controls and add hint label (floating label).

## Initialize TextInputLayout

{% tabs %} 

{% highlight xaml %} 

<inputLayout:SfTextInputLayout>
   <Entry />
</inputLayout:SfTextInputLayout>  

{% endhighlight %}

{% highlight C# %} 

var inputLayout = new SfTextInputLayout();
inputLayout.Content = new Entry(); 

{% endhighlight %}

{% endtabs %}

### Adding hint
Floating label for the text input layout can be added by setting the `Hint` property. Visibility of the hint can be collapsed by setting the `ShowHint` property to `false.` By default, this property is set to `true.`

{% tabs %} 

{% highlight xaml %} 

<inputLayout:SfTextInputLayout Hint="Name">
   <Entry />
</inputLayout:SfTextInputLayout>  

{% endhighlight %}

{% highlight C# %} 

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Name"; 
inputLayout.Content = new Entry(); 

{% endhighlight %}

{% endtabs %}

When focusing on the input view, the hint label will be moved to the top position; it will be returned to the original position when proceeding further (on unfocused) without entering any value.

Run the project, and check if you get the following output to ensure that the project has been appropriately configured to add the text input layout control.

![Adding hint](images/GettingStarted/GettingStarted.png)

## Enabling password visibility toggle

The password visibility toggle is used to show or hide the visibility of characters in the input view added to the control. You can enable this toggle by setting the `EnablePasswordVisibilityToggle` property to `true.`

{% tabs %} 

{% highlight xaml %} 

<inputLayout:SfTextInputLayout  Hint="Password" 
                                EnablePasswordVisibilityToggle="true">
    <Entry Text="1234"/>
</inputLayout:SfTextInputLayout>  
 
{% endhighlight %}

{% highlight C# %} 

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Password";
inputLayout.EnablePasswordVisibilityToggle = true;
inputLayout.Content = new Entry() { Text = "1234" }; 

{% endhighlight %}

{% endtabs %}

![Enable password toggling image](images/GettingStarted/PasswordGettingStarted.png)

N> Password visibility toggle can be enabled only for [Entry](https://learn.microsoft.com/en-us/dotnet/maui/user-interface/controls/entry) control.