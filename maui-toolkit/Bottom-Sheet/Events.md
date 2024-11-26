---
layout: post
title: Events in .NET MAUI Bottom Sheet control | Syncfusion
description: Learn about Events support in Syncfusion Toolkit for .NET MAUI Bottom Sheet (SfBottomSheet) control, its elements, and more.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---

# Events in .NET MAUI Bottom Sheet (SfBottomSheet)

## StateChanged event

This event occurs when the value or state of the `State` property is changed by sliding the bottom sheet or setting the value to the `State` property using XAML or C# code. The event arguments are of type `StateChangedEventArgs` and expose the following property:

* `NewValue` : Gets the current state of the .NET MAUI Bottom Sheet control.
* `OldValue` : Gets the previous state of the .NET MAUI Bottom Sheet control.

{% tabs %}
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" StateChanged="BottomSheet_StateChanged"/>

{% endhighlight %}
{% highlight c# %}

public MainPage()
{
    InitializeComponent();
    SfBottomSheet bottomSheet = new SfBottomSheet();
    Grid grid = new Grid();
    bottomSheet.BottomSheetContent = grid;
    this.Content = bottomSheet; 
    bottomSheet.StateChanged += BottomSheet_StateChanged;
}

private void BottomSheet_StateChanged(object sender, StateChangedEventArgs args)
{
    // Codes that need to be executed once the Sheet's state value is Changed.
}

{% endhighlight %}
{% endtabs %}