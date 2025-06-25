---
layout: post
title: Select Tab in .NET MAUI Tab View (SfTabView) | Syncfusion®
description: Learn all about selecting a tab item programmatically in the Syncfusion® .NET MAUI Tab View (SfTabView) control and more.
platform: maui-toolkit
control: SfTabView
documentation: UG
---

# How to Select a Tab Item Programmatically?

## Programmatically select the tab item

You can use the [SelectedIndex](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_SelectedIndex) property of `SfTabView` to programmatically select a tab item. Below is a code snippet demonstrating how to do this:

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control with a name and set the initially selected tab index to 2 -->
<tabView:SfTabView x:Name="tabView"
				   SelectedIndex="2" />
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();
// Set the selected index of the SfTabView to 2
tabView.SelectedIndex = 2;
{% endhighlight %}
{% endtabs %}

The following image shows the tab item selected programmatically using the `SelectedIndex` property:

![Tab item selected programmatically in .NET MAUI TabView](images/SelectedIndexTabView.png)

## Get the selected tab item

The [IsSelected](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_IsSelected) property indicates whether the tab item is active. This property can be used, as shown in the code snippet below, to check and perform actions on the selected tab item.

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control with a name and an event handler for the SelectionChanged event -->
<tabView:SfTabView x:Name="tabView"
                   SelectionChanged="TabView_SelectionIndexChanged" />
{% endhighlight %}

{% highlight C# %}

// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();
// Subscribe to the SelectionChanged event
tabView.SelectionChanged += TabView_SelectionIndexChanged;

// Event handler for the SelectionChanged event
private void TabView_SelectionIndexChanged(object? sender, TabSelectionChangedEventArgs e)
{
	// Access the selected tab item using the new index
	SfTabItem tabItem = tabView.Items[e.NewIndex];
	
	// Check if the tab item is selected
	bool isTabItemSelected = tabItem.IsSelected;
	
	// If the tab item is selected, set its font size
	if (isTabItemSelected)
	{
		tabItem.FontSize = 26;
	}
}

{% endhighlight %}

{% endtabs %}

The following image shows a tab item selected in the .NET MAUI Tab View:

![Selected tab item](images/SelectedIndex.png)