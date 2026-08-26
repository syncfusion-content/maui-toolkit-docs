---
layout: post
title: Getting Started with .NET MAUI GridSplitter | Syncfusion®
description: Learn how to get started with the Syncfusion® .NET MAUI GridSplitter control and create resizable pane layouts.
platform: maui-toolkit
control: SfGridSplitter
documentation: UG
---

# Getting Started with .NET MAUI GridSplitter

This section guides you through setting up and configuring the control in your .NET MAUI application. Follow the steps below to create a basic resizable layout with multiple panes.

{% tabcontents %}
{% tabcontent Visual Studio %}

## Prerequisites

Before proceeding, ensure the following are set up:

1. Install .NET 9 SDK or later.
2. Set up a .NET MAUI environment with Visual Studio 2022 v17.12 or later.

## Step 1: Create a new .NET MAUI project

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Then click **Next**.
3. Select the .NET framework version and click **Create**.

## Step 2: Install the Syncfusion® .NET MAUI Toolkit NuGet package

1. In **Solution Explorer**, right-click the project and choose **Manage NuGet Packages**.
2. Search for **Syncfusion.Maui.Toolkit** and install the latest version.
3. Ensure the necessary dependencies are installed correctly and the project is restored.

{% endtabcontent %}

{% tabcontent Visual Studio Code %}

## Prerequisites

Before proceeding, ensure the following are set up:

1. Install .NET 9 SDK or later.
2. Set up a .NET MAUI environment with Visual Studio Code.
3. Ensure that the .NET MAUI workloads are installed.

## Step 1: Create a new .NET MAUI project

1. Open the command palette by pressing `Ctrl+Shift+P`.
2. Type **.NET: New Project** and press Enter.
3. Choose the **.NET MAUI App** template.
4. Select a project location and enter the project name.
5. Choose **Create Project**.

## Step 2: Install the Syncfusion® .NET MAUI Toolkit NuGet package

1. Open the integrated terminal.
2. Navigate to the project folder.
3. Run:

```bash
dotnet add package Syncfusion.Maui.Toolkit