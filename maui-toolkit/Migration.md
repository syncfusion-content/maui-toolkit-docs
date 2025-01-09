---
layout: post
title: Migration from Syncfusion® .NET MAUI to Syncfusion® Toolkit for .NET MAUI
description: Describes the necessary changes to easily update the existing Syncfusion® .NET MAUI control to use the new toolkit with minimal code modifications.
platform: maui-toolkit
control: General
documentation: ug
---

# Migration Overview: Syncfusion<sup>®</sup> .NET MAUI to Syncfusion<sup>®</sup> Toolkit for .NET MAUI

To ensure a smooth migration from **Syncfusion<sup>®</sup> .NET MAUI** to the **Syncfusion<sup>®</sup> Toolkit for .NET MAUI** controls, we have designed the Toolkit components to closely resemble those in Syncfusion<sup>®</sup> .NET MAUI. This approach minimizes the changes required during migration, with the primary difference being the use of toolkit-specific namespaces.
By preserving similar APIs and functionality, developers can easily update their existing projects to use the new toolkit with minimal code modifications. Refer to the table below for a detailed overview of the necessary changes:

## XAML Namespaces

<table>
<tr>
<th>Controls</th>
<th>Syncfusion<sup>®</sup> .NET MAUI Namespace</th>
<th>Syncfusion<sup>®</sup> Toolkit for .NET MAUI Namespace</th>
<th>Description</th>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html">SfButton</a></td>
  <td>xmlns: button ="clr-namespace:Syncfusion.Maui.Buttons;assembly=Syncfusion.Maui.Buttons"</td>
  <td>xmlns:button ="clr-namespace:Syncfusion.Maui.Toolkit.Buttons;assembly=Syncfusion.Maui.Toolkit"</td>
  <td>Defines the XAML namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html">SfButton</a> control.</td>
</tr>
<tr>
<td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Calendar.SfCalendar.html">SfCalendar</a></td>
<td>xmlns: calendar ="clr-namespace:Syncfusion.Maui.Calendar;assembly=Syncfusion.Maui.Calendar"</td>
<td>xmlns:calendar="clr-namespace:Syncfusion.Maui.Toolkit.Calendar;assembly=Syncfusion.Maui.Toolkit"</td>
<td>Defines the XAML namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Calendar.SfCalendar.html">SfCalendar</a> control.</td>
</tr>
<tr>
<td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html">SfCarousel</a></td>
<td>xmlns: carousel ="clr-namespace:Syncfusion.Maui.Carousel;assembly=Syncfusion.Maui.Carousel"</td>
<td>xmlns:carousel="clr-namespace:Syncfusion.Maui.Toolkit.Carousel;assembly=Syncfusion.Maui.Toolkit"</td>
<td>Defines the XAML namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html">SfCarousel</a> control.</td>
</tr>
<tr>
<td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html">SfCartesianChart</a>, <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCircularChart.html">SfCircularChart</a>, <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfFunnelChart.html">SfFunnelChart</a>, <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPolarChart.html">SfPolarChart</a>, and <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPyramidChart.html">SfPyramidChart</a></td>
<td>xmlns:chart="clr-namespace:Syncfusion.Maui.Charts;assembly=Syncfusion.Maui.Charts"</td>
<td>xmlns:chart="clr-namespace:Syncfusion.Maui.Toolkit.Charts;assembly=Syncfusion.Maui.Toolkit"</td>
<td>Defines the XAML namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html">SfCartesianChart</a>, <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCircularChart.html">SfCircularChart</a>, <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfFunnelChart.html">SfFunnelChart</a>, <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPolarChart.html">SfPolarChart</a>, and <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPyramidChart.html">SfPyramidChart</a> controls.</td>
</tr>
<tr>
<td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.SfChip.html">SfChip</a></td>
<td>xmlns:chip="clr-namespace:Syncfusion.Maui.Core;assembly=Syncfusion.Maui.Core"</td>
<td>xmlns:chip="clr-namespace:Syncfusion.Maui.Toolkit.Chips;assembly=Syncfusion.Maui.Toolkit"</td>
<td>Defines the XAML namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.SfChip.html">SfChip</a> control.</td>
</tr>
<tr>
<td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html">SfEffectsView</a></td>
<td>xmlns:effectsView="clr-namespace:Syncfusion.Maui.Core;assembly=Syncfusion.Maui.Core"</td>
<td>xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit"</td>
<td>Defines the XAML namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html">SfEffectsView</a> control.</td>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.SfNavigationDrawer.html">SfNavigationDrawer</a></td>
  <td>xmlns:navigationDrawer="clr-namespace:Syncfusion.Maui.NavigationDrawer;assembly=Syncfusion.Maui.NavigationDrawer"</td>
  <td>xmlns:navigationDrawer="clr-namespace:Syncfusion.Maui.Toolkit.NavigationDrawer;assembly=Syncfusion.Maui.Toolkit"</td>
  <td>Defines the XAML namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.SfNavigationDrawer.html">SfNavigationDrawer</a> control.</td>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html">SfNumericEntry</a></td>
  <td>xmlns:numericEntry ="clr-namespace:Syncfusion.Maui.Inputs;assembly=Syncfusion.Maui.Inputs"</td>
  <td>xmlns:numericEntry="clr-namespace:Syncfusion.Maui.Toolkit.NumericEntry;assembly=Syncfusion.Maui.Toolkit"</td>
  <td>Defines the XAML namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html">SfNumericEntry</a> control.</td>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html">SfNumericUpDown</a></td>
  <td>xmlns:numericUpDown ="clr-namespace:Syncfusion.Maui.Inputs;assembly=Syncfusion.Maui.Inputs"</td>
  <td>xmlns:numericUpDown="clr-namespace:Syncfusion.Maui.Toolkit.NumericUpDown;assembly=Syncfusion.Maui.Toolkit"</td>
  <td>Defines the XAML namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html">SfNumericUpDown</a> control.</td>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.PullToRefresh.SfPullToRefresh.html">SfPullToRefresh</a></td>
  <td>xmlns:pullToRefreshControl="clr-namespace:Syncfusion.Maui.PullToRefresh;assembly=Syncfusion.Maui.PullToRefresh"</td>
  <td>xmlns:pullToRefreshControl="clr-namespace:Syncfusion.Maui.Toolkit.PullToRefresh;assembly=Syncfusion.Maui.Toolkit"</td>
  <td>Defines the XAML namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.PullToRefresh.SfPullToRefresh.html">SfPullToRefresh</a> control.</td>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SegmentedControl.SfSegmentedControl.html">SfSegmentedControl</a></td>
  <td>xmlns:segmentedControl="clr-namespace:Syncfusion.Maui.Buttons;assembly=Syncfusion.Maui.Buttons"</td>
  <td>xmlns:segmentedControl="clr-namespace:Syncfusion.Maui.Toolkit.SegmentedControl;assembly=Syncfusion.Maui.Toolkit"</td>
  <td>Defines the XAML namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SegmentedControl.SfSegmentedControl.html">SfSegmentedControl</a>.</td>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Shimmer.SfShimmer.html">SfShimmer</a></td>
  <td>xmlns:shimmer="clr-namespace:Syncfusion.Maui.Shimmer;assembly=Syncfusion.Maui.Core"</td>
  <td>xmlns:shimmer="clr-namespace:Syncfusion.Maui.Toolkit.Shimmer;assembly=Syncfusion.Maui.Toolkit"</td>
  <td>Defines the XAML namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Shimmer.SfShimmer.html">SfShimmer</a> control.</td>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html">SfTabView</a></td>
  <td>xmlns:tabView="clr-namespace:Syncfusion.Maui.TabView;assembly=Syncfusion.Maui.TabView"</td>
  <td>xmlns:tabView="clr-namespace:Syncfusion.Maui.Toolkit.TabView;assembly=Syncfusion.Maui.Toolkit"</td>
  <td>Defines the XAML namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html">SfTabView</a> control.</td>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.SfTextInputLayout.html">SfTextInputLayout</a></td>
  <td>xmlns:inputLayout="clr-namespace:Syncfusion.Maui.Core;assembly=Syncfusion.Maui.Core"</td>
  <td>xmlns:inputLayout="clr-namespace:Syncfusion.Maui.Toolkit.TextInputLayout;assembly=Syncfusion.Maui.Toolkit"</td>
  <td>Defines the XAML namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.SfTextInputLayout.html">SfTextInputLayout</a> control.</td>
</tr>
</table>

## C# Namespaces

<table>
<tr>
<th>Controls</th>
<th>Syncfusion<sup>®</sup> .NET MAUI Namespace</th>
<th>Syncfusion<sup>®</sup> Toolkit for .NET MAUI Namespace</th>
<th>Description</th>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html">SfButton</a></td>
  <td>Syncfusion.Maui.Buttons</td>
  <td>Syncfusion.Maui.Toolkit.Buttons</td>
  <td>Defines the namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Buttons.SfButton.html">SfButton</a> control.</td>
</tr>
<tr>
<td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Calendar.SfCalendar.html">SfCalendar</a></td>
<td>Syncfusion.Maui.Calendar</td>
<td>Syncfusion.Maui.Toolkit.Calendar</td>
<td>Defines the namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Calendar.SfCalendar.html">SfCalendar</a> control.</td>
</tr>
<tr>
<td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html">SfCarousel</a></td>
<td>Syncfusion.Maui.Carousel</td>
<td>Syncfusion.Maui.Toolkit.Carousel</td>
<td>Defines the namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Carousel.SfCarousel.html">SfCarousel</a> control.</td>
</tr>
<tr>
<td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html">SfCartesianChart</a>, <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCircularChart.html">SfCircularChart</a>, <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfFunnelChart.html">SfFunnelChart</a>, <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPolarChart.html">SfPolarChart</a>, and <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPyramidChart.html">SfPyramidChart</a></td>
<td>Syncfusion.Maui.Charts</td>
<td>Syncfusion.Maui.Toolkit.Charts</td>
<td>Defines the namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html">SfCartesianChart</a>, <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCircularChart.html">SfCircularChart</a>, <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfFunnelChart.html">SfFunnelChart</a>, <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPolarChart.html">SfPolarChart</a>, and <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPyramidChart.html">SfPyramidChart</a> controls.</td>
</tr>
<tr>
<td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.SfChip.html">SfChip</a></td>
<td>Syncfusion.Maui.Core</td>
<td>Syncfusion.Maui.Toolkit.Chip</td>
<td>Defines the namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Chips.SfChip.html">SfChip</a> control.</td>
</tr>
<tr>
<td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html">SfEffectsView</a></td>
<td>Syncfusion.Maui.Core</td>
<td>Syncfusion.Maui.Toolkit.EffectsView</td>
<td>Defines the namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html">SfEffectsView</a> control.</td>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.SfNavigationDrawer.html">SfNavigationDrawer</a></td>
  <td>Syncfusion.Maui.NavigationDrawer</td>
  <td>Syncfusion.Maui.Toolkit.NavigationDrawer</td>
  <td>Defines the namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.SfNavigationDrawer.html">SfNavigationDrawer</a> control.</td>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html">SfNumericEntry</a></td>
  <td>Syncfusion.Maui.Inputs</td>
  <td>Syncfusion.Maui.Toolkit.NumericEntry</td>
  <td>Defines the namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericEntry.SfNumericEntry.html">SfNumericEntry</a> control.</td>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html">SfNumericUpDown</a></td>
  <td>Syncfusion.Maui.Inputs</td>
  <td>Syncfusion.Maui.Toolkit.NumericUpDown</td>
  <td>Defines the namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NumericUpDown.SfNumericUpDown.html">SfNumericUpDown</a> control.</td>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.PullToRefresh.SfPullToRefresh.html">SfPullToRefresh</a></td>
  <td>Syncfusion.Maui.PullToRefresh</td>
  <td>Syncfusion.Maui.Toolkit.PullToRefresh</td>
  <td>Defines the namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.PullToRefresh.SfPullToRefresh.html">SfPullToRefresh</a> control.</td>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SegmentedControl.SfSegmentedControl.html">SfSegmentedControl</a></td>
  <td>Syncfusion.Maui.Buttons</td>
  <td>Syncfusion.Maui.Toolkit.SegmentedControl</td>
  <td>Defines the namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SegmentedControl.SfSegmentedControl.html">SfSegmentedControl</a>.</td>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Shimmer.SfShimmer.html">SfShimmer</a></td>
  <td>Syncfusion.Maui.Shimmer</td>
  <td>Syncfusion.Maui.Toolkit.Shimmer</td>
  <td>Defines the namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Shimmer.SfShimmer.html">SfShimmer</a> control.</td>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html">SfTabView</a></td>
  <td>Syncfusion.Maui.TabView</td>
  <td>Syncfusion.Maui.Toolkit.TabView</td>
  <td>Defines the namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html">SfTabView</a> control.</td>
</tr>
<tr>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.SfTextInputLayout.html">SfTextInputLayout</a></td>
  <td>Syncfusion.Maui.Core</td>
  <td>Syncfusion.Maui.Toolkit.TextInputLayout</td>
  <td>Defines the namespace for <a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.SfTextInputLayout.html">SfTextInputLayout</a> control.</td>
</tr>
<tr>
  <td>Common</td>
  <td>Syncfusion.Maui.Core.Hosting</td>
  <td>Syncfusion.Maui.Toolkit.Hosting</td>
  <td>Provides functionality for configure your .NET MAUI application through the AppHostBuilder.</td>
</tr>
</table>

## C# Methods

<table>
<tr>
<th>Controls</th>
<th>Syncfusion<sup>®</sup> .NET MAUI</th>
<th>Syncfusion<sup>®</sup> Toolkit for .NET MAUI</th>
<th>Description</th>
</tr>
<tr>
  <td>Common</td>
  <td><a href="https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.Hosting.AppHostBuilderExtensions.html#Syncfusion_Maui_Core_Hosting_AppHostBuilderExtensions_ConfigureSyncfusionCore_Microsoft_Maui_Hosting_MauiAppBuilder_">ConfigureSyncfusionCore()</a></td>
  <td><a href="https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Hosting.AppHostBuilderExtensions.html#Syncfusion_Maui_Toolkit_Hosting_AppHostBuilderExtensions_ConfigureSyncfusionToolkit_Microsoft_Maui_Hosting_MauiAppBuilder_">ConfigureSyncfusionToolkit()</a></td>
  <td>Configures the implemented handlers in <code>Syncfusion.Maui.Toolkit</code>.</td>
</tr>