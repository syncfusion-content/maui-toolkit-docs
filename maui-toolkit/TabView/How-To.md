---
layout: post
title: Select tab in .NET MAUI Tab View (SfTabView) | Syncfusion
description: Learn here all about select tab item programmatically in Syncfusion .NET MAUI Tab View (SfTabView) control and more.
platform: maui-toolkit
control: Tab View
documentation: ug
---

# How to select a tab item programmatically? 

## Programmatically select the tab item

You can programmatically select a tab item using the [SelectedIndex](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_SelectedIndex) property of `SfTabView`, as shown in the following code snippet.

{% tabs %}

{% highlight xaml %}
   <tabView:SfTabView x:Name="tabView" SelectedIndex="2"/>
{% endhighlight %}

{% highlight C# %}
SfTabView tabView = new SfTabView();
tabView.SelectedIndex = 2;
{% endhighlight %}
{% endtabs %}

The following image shows the tab item selected programmatically using the `SelectedIndex` property:

![Tab item selected programmatically in .NET MAUI TabView](images/SelectedIndexTabView.png)

## Get the selected tab item

The [IsSelected](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_IsSelected) property indicates whether a tab item is active. You can use this property to determine the selected item in the tab view, as shown in the following code snippet.

{% tabs %}

{% highlight xaml %}
    <tabView:SfTabView x:Name="tabView" SelectionChanged="TabView_SelectionIndexChanged"/>
{% endhighlight %}

{% highlight C# %}

SfTabView tabView = new SfTabView();
tabView.SelectionChanged += TabView_SelectionIndexChanged;
private void TabView_SelectionIndexChanged(object sender, TabSelectionChangedEventArgs e)
{
	SfTabItem tabItem = tabView.Items[e.NewIndex];
	bool isTabItemSelected = tabItem.IsSelected;
	if (isTabItemSelected)
	{
		tabItem.FontSize = 26;
	}
}

{% endhighlight %}

{% endtabs %}

The following image shows a tab item selected in the .NET MAUI TabView:

![Selected tab item in .NET MAUI TabView](images/SelectedIndex.png)