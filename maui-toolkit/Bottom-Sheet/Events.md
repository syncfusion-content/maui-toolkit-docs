---
layout: post
title: Events in .NET MAUI Bottom Sheet control | Syncfusion
description: Learn about event support in Syncfusion Toolkit for .NET MAUI Bottom Sheet (SfBottomSheet) control and more.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---

# Event in .NET MAUI Bottom Sheet (SfBottomSheet)

## StateChanged event

This event occurs when the value of the `State` property is changed by swiping the bottom sheet or setting the value to the State property using XAML or C# code. The event arguments are of type `StateChangedEventArgs` and expose the following property:

* `NewValue` : Gets the current state of the Bottom Sheet.
* `OldValue` : Gets the previous state of the Bottom Sheet.

{% tabs %}
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" StateChanged="OnStateChanged">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>

{% endhighlight %}
{% highlight c# %}

public MainPage()
{
    InitializeComponent();
    SfBottomSheet bottomSheet = new SfBottomSheet();
    Grid grid = new Grid();
    bottomSheet.BottomSheetContent = grid;
    this.Content = bottomSheet; 
    bottomSheet.StateChanged += OnStateChanged;
}

private void OnStateChanged(object sender, StateChangedEventArgs args)
{
    // Codes that need to be executed once the Sheet's state value is Changed.
}

{% endhighlight %}
{% endtabs %}