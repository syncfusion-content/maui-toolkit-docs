---
layout: post
title: Events in .NET MAUI Tab View (SfTabView) Control | Syncfusion®
description: Learn about event support in the Syncfusion® .NET MAUI Tab View (SfTabView) control, its elements and more.
platform: maui-toolkit
control: SfTabView
documentation: UG
---

# Events in .NET MAUI Tab View

This section provides information about the events available in the .NET MAUI Tab View control.

## TabItemTapped event

The [TabItemTapped](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_TabItemTapped) event is triggered whenever a tab is tapped.The [TabItemTappedEventArgs](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.TabItemTappedEventArgs.html) provides the following properties:

* [TabItem](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.TabItemTappedEventArgs.html#Syncfusion_Maui_Toolkit_TabView_TabItemTappedEventArgs_TabItem) : Gets the selected tab item of Tab View control.
* [Cancel](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.TabItemTappedEventArgs.html#Syncfusion_Maui_Toolkit_TabView_TabItemTappedEventArgs_Cancel) : Gets or sets a value indicating whether the event should be canceled.

{% tabs %}

{% highlight xaml %}

<!-- Define the SfTabView control with a name and an event handler for the TabItemTapped event -->
<tabView:SfTabView x:Name="tabView"
                   TabItemTapped="TabView_TabItemTapped" />

{% endhighlight %}

{% highlight C# %}

// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();
// Subscribe to the TabItemTapped event
tabView.TabItemTapped += TabView_TabItemTapped;

// Event handler for the TabItemTapped event
private void TabView_TabItemTapped(object? sender, TabItemTappedEventArgs e)
{
	if (e.TabItem != null)
	{
		// Access the selected tab item property and set its font size
		e.TabItem.FontSize = 26;

		// Cancel the event if needed
		e.Cancel = true;
	}
}

{% endhighlight %}

{% endtabs %}

## SelectionChanging event

The [SelectionChanging](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_SelectionChanging) event notifies before the selection changes, when the tab header is tapped, or when dynamically setting the [SelectedIndex](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html?tabs=tabid-1#Syncfusion_Maui_Toolkit_TabView_SfTabView_SelectedIndex) property of SfTabView. The [SelectionChangingEventArgs](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SelectionChangingEventArgs.html) provides the following properties:

* [Index](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SelectionChangingEventArgs.html#Syncfusion_Maui_Toolkit_TabView_SelectionChangingEventArgs_Index) - Gets the index value of the item that is about to be selected.

* `Cancel` - Gets or sets a boolean value indicating whether the selection of the tab item should be canceled.

{% tabs %}

{% highlight xaml %}

<!-- Define the SfTabView control with a name and an event handler for the SelectionChanging event -->
<tabView:SfTabView x:Name="tabView"
                   SelectionChanging="TabView_SelectionChanging" />
	
{% endhighlight %}

{% highlight C# %}

// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();
// Subscribe to the SelectionChanging event
tabView.SelectionChanging += TabView_SelectionChanging;

// Event handler for the SelectionChanging event
private void TabView_SelectionChanging(object? sender, SelectionChangingEventArgs e)
{
	// Access the index value of the item that is being selected.
	var selectionChangingIndex = e.Index;

	// If we set Cancel to true, the tab item will not be selected.
	e.Cancel = true;
}

{% endhighlight %}

{% endtabs %}

## SelectionChanged event

The [SelectionChanged](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_SelectionChanged) event is used to notify when the selection changes by swiping or dynamically setting the [SelectedIndex](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html?tabs=tabid-1#Syncfusion_Maui_Toolkit_TabView_SfTabView_SelectedIndex) property of SfTabView. The [TabSelectionChangedEventArgs](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.TabSelectionChangedEventArgs.html) provides the following properties:

* [NewValue](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.TabSelectionChangedEventArgs.html#Syncfusion_Maui_Toolkit_TabView_TabSelectionChangedEventArgs_NewIndex) : Gets the index of the currently selected tab item.
* [OldValue](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.TabSelectionChangedEventArgs.html#Syncfusion_Maui_Toolkit_TabView_TabSelectionChangedEventArgs_OldIndex) : Gets the index of the previously selected tab item.
* [Handled](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.TabSelectionChangedEventArgs.html#Syncfusion_Maui_Toolkit_TabView_TabSelectionChangedEventArgs_Handled) : Gets or sets a value indicating whether the `SelectionChanged` event is handled.

{% tabs %}

{% highlight xaml %}

<!-- Define the SfTabView control with a name and an event handler for the SelectionChanged event -->
<tabView:SfTabView x:Name="tabView"
                   SelectionChanged="TabView_SelectionChanged" />
	
{% endhighlight %}

{% highlight C# %}

// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();
// Subscribe to the SelectionChanged event
tabView.SelectionChanged += TabView_SelectionChanged;
			
// Event handler for the SelectionChanged event
private void TabView_SelectionChanged(object? sender, TabSelectionChangedEventArgs e)
{
	// Access the new and old Index
	double newValue = e.NewIndex;
	double oldValue = e.OldIndex;

	// If we set Handled to true, it indicates that the event has been handled.
	e.Handled = true;
}

{% endhighlight %}

{% endtabs %}