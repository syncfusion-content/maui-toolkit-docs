---
layout: post
title: Populating Items in .NET MAUI Chips control | Syncfusion
description: Learn about Populating Items support in Syncfusion Essential Studio .NET MAUI Chips control, its elements and more.
platform: maui-toolkit
control: Chips
documentation: ug
---

# Populating Items in .NET MAUI Chips

[.NET MAUI Chips](https://www.syncfusion.com/maui-controls/maui-chips) can be populated with either business objects and SfChip. This section explain how to populate the chips control with business objects and SfChip.

## Populating business objects as items

Business objects can be populated in Chips using the [`ItemsSource`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.SfChipGroup.html#Syncfusion_Maui_Core_SfChipGroup_ItemsSource) property.
Refer to this `documentation` to know more details about populating the chips control with list of employee details.

## Populating SfChip as items

Chips control also provides support to create and set [`SfChip`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.SfChip.html) as item. It can be achieved using the [`Items`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.SfChipGroup.html#Syncfusion_Maui_Core_SfChipGroup_Items) property.

{% tabs %}

{% highlight xaml %}

<ContentPage.Content>
<Grid>
	<ChipControl:SfChipGroup ChipBackground="Violet">
	<ChipControl:SfChipGroup.Items>
			<ChipControl:SfChip Text="Extra Small"/>
			<ChipControl:SfChip Text="Small"/>
			<ChipControl:SfChip Text="Medium"/>
			<ChipControl:SfChip Text="Large"/>
			<ChipControl:SfChip Text="Extra Large"/>
		</chip:SfChipGroup.Items>
	</ChipControl:SfChipGroup>
</Grid>
</ContentPage.Content>

{% endhighlight %}

{% highlight c# %}

using Syncfusion.Maui.Toolkit.Chips;
Grid grid = new Grid();
var chipGroup = new SfChipGroup(){Type = SfChipsType.Action};
grid.Children.Add(chipGroup);
chipGroup.Items.Add(new SfChip(){Text="Extra Small"});
chipGroup.Items.Add(new SfChip(){Text="Small"});
chipGroup.Items.Add(new SfChip(){Text="Medium"});
chipGroup.Items.Add(new SfChip(){Text="Large"});
chipGroup.Items.Add(new SfChip(){Text="Extra Large"});
chipGroup.ChipBackground = Colors.Violet;
this.Content = grid;
		
{% endhighlight %}

{% endtabs %}

![Collection of items to chip group](images/items/chips_items.png)


