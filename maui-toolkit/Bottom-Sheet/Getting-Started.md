---
layout: post
title: Getting started with .NET MAUI Bottom Sheet control | Syncfusion
description: Learn here about getting started with Syncfusion .NET MAUI Bottom Sheet (SfBottomSheet) control in your cross-platform applications.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---

# Getting Started with .NET MAUI Bottom Sheet

This section provides a quick overview of how to get started with the [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html) for .NET MAUI and a walk-through to configure the .NET MAUI Bottom Sheet in a real-time scenario. Follow the steps below to add .NET MAUI Bottom Sheet to your project.

## Prerequisites

Before proceeding, ensure the following are set up:

1. Install [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) or later is installed.
2. Set up a .NET MAUI environment with Visual Studio 2022 (v17.8 or later) or Visual Studio Code. For Visual Studio Code users, ensure that the .NET MAUI workload is installed and configured as described [here.](https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation?view=net-maui-8.0&tabs=visual-studio-code)

## Step 1: Create a New MAUI Project

{% tabcontents %}
{% tabcontent Visual Studio %}

1. Go to **File > New > Project** and choose the **.NET MAUI App** template.
2. Name the project and choose a location. Then, click **Next.**
3. Select the .NET framework version and click **Create.**

{% endtabcontent %}
{% tabcontent Visual Studio Code %}

1. Open the command palette by pressing `Ctrl+Shift+P` and type **.NET:New Project** and enter.
2. Choose the **.NET MAUI App** template.
3. Select the project location, type the project name and press **Enter.**
4. Then choose **Create project.**

{% endtabcontent %}
{% endtabcontents %}

## Step 2: Install the Syncfusion MAUI Toolkit Package

{% tabcontents %}
{% tabcontent Visual Studio %}

1. In **Solution Explorer,** right-click the project and choose **Manage NuGet Packages.**
2. Search for [Syncfusion.Maui.Toolkit](https://www.nuget.org/packages/Syncfusion.Maui.Toolkit/) and install the latest version.
3. Ensure the necessary dependencies are installed correctly, and the project is restored.

{% endtabcontent %}
{% tabcontent Visual Studio Code %}

1. Press <kbd>Ctrl</kbd> + <kbd>`</kbd> (backtick) to open the integrated terminal in Visual Studio Code.
2. Ensure you're in the project root directory where your .csproj file is located.
3. Run the command `dotnet add package Syncfusion.Maui.Toolkit` to install the Syncfusion .NET MAUI Toolkit NuGet package.
4. To ensure all dependencies are installed, run `dotnet restore`.

{% endtabcontent %}
{% endtabcontents %}

## Step 3: Register the handler

In the MauiProgram.cs file, register the handler for Syncfusion Toolkit.

{% tabs %}
{% highlight C# tabtitle="MauiProgram.cs" hl_lines="1 9" %}
using Syncfusion.Maui.Toolkit.Hosting;

public static class MauiProgram
{
    public static MauiApp CreateMauiApp()
    {
        var builder = MauiApp.CreateBuilder();
        builder
            .ConfigureSyncfusionToolkit()
            .UseMauiApp<App>()
            .ConfigureFonts(fonts =>
            {
                fonts.AddFont("OpenSans-Regular.ttf", "OpenSansRegular");
                fonts.AddFont("OpenSans-Semibold.ttf", "OpenSansSemibold");
            });

        return builder.Build();
    }
}

{% endhighlight %}
{% endtabs %} 

## Step 4: Add a Basic BottomSheet

1. To initialize the control, import the `Syncfusion.Maui.Toolkit.BottomSheet` namespace into your code.

2. Initialize [SfBottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html).

{% tabs %}
{% highlight xaml %}

<ContentPage
    xmlns:local="clr-namespace:BottomSheetGettingStarted.ViewModel"
    xmlns:bottomSheet="clr-namespace:Syncfusion.Maui.Toolkit.BottomSheet;assembly=Syncfusion.Maui.Toolkit">
   <Grid>
        <Grid.BindingContext>
            <local:BookViewModel />
        </Grid.BindingContext>
        <ListView ItemsSource="{Binding Books}" ItemTapped="ListView_ItemTapped" HasUnevenRows="True">
            <ListView.ItemTemplate>
                <DataTemplate>
                    <ViewCell>
                        <Grid ColumnDefinitions="*, 60" Padding="10">
                            <VerticalStackLayout>
                                <Label Text="{Binding Title}" FontSize="20" FontAttributes="Bold"/>
                                <Label Text="{Binding Description}" FontSize="14" TextColor="Gray"/>
                            </VerticalStackLayout>
                            <Label Text="{Binding Rating, StringFormat='{}{0} / 5'}" Grid.Column="1" HorizontalOptions="Center" VerticalOptions="Center"/>
                        </Grid>
                    </ViewCell>
                </DataTemplate>
            </ListView.ItemTemplate>
        </ListView>
        <bottomSheet:SfBottomSheet x:Name="bottomSheet" CornerRadius="15, 15, 0, 0" HalfExpandedRatio="0.35" ContentPadding="10">
            <bottomSheet:SfBottomSheet.BottomSheetContent>
                <VerticalStackLayout Spacing="5" x:Name="bottomSheetContent">
                    <Grid ColumnDefinitions="120, *" ColumnSpacing="10">
                        <Label Text="Title:" FontSize="20" FontAttributes="Bold"/>
                        <Label Text="{Binding Title}" FontSize="16" VerticalTextAlignment="Center" Grid.Column="1"/>
                    </Grid>
                    <Grid ColumnDefinitions="120, *" ColumnSpacing="10">
                        <Label Text="Genre:" FontSize="20" FontAttributes="Bold"/>
                        <Label Text="{Binding Genre}" FontSize="16" VerticalTextAlignment="Center" Grid.Column="1"/>
                    </Grid>
                    <Grid ColumnDefinitions="120, *" ColumnSpacing="10">
                        <Label Text="Published:" FontSize="20" FontAttributes="Bold"/>
                        <Label Text="{Binding Published}" FontSize="16" VerticalTextAlignment="Center" Grid.Column="1"/>
                    </Grid>
                    <Grid ColumnDefinitions="120, *" ColumnSpacing="10">
                        <Label Text="Description:" FontSize="20" FontAttributes="Bold"/>
                        <Label Text="{Binding Description}" FontSize="16" VerticalTextAlignment="Center" Grid.Column="1"/>
                    </Grid>
                    <Grid ColumnDefinitions="120, *" ColumnSpacing="10">
                        <Label Text="Price:" FontSize="20" FontAttributes="Bold"/>
                        <Label FontSize="16" VerticalTextAlignment="Center" Grid.Column="1">
                            <Label.FormattedText>
                                <FormattedString>
                                    <Span Text="$" FontAttributes="Bold" />
                                    <Span Text="{Binding Price, StringFormat='{0:F2}'}" />
                                </FormattedString>
                            </Label.FormattedText>
                        </Label>
                    </Grid>
                </VerticalStackLayout>
            </bottomSheet:SfBottomSheet.BottomSheetContent>
        </bottomSheet:SfBottomSheet>
    </Grid>
</ContentPage>
    
{% endhighlight %}
{% highlight c# %}

using Syncfusion.Maui.Toolkit.BottomSheet;

namespace BottomSheetGettingStarted
{
    public partial class MainPage : ContentPage
    {
        SfBottomSheet bottomSheet;
        public MainPage()
        {
            InitializeComponent();

            // Create ViewModel and set BindingContext
            var bookViewModel = new BookViewModel();

            // Main Grid
            var mainGrid = new Grid();
            mainGrid.BindingContext = bookViewModel;

            // ListView for displaying books
            var listView = new ListView
            {
                ItemsSource = bookViewModel.Books,
                HasUnevenRows = true,
                ItemTemplate = new DataTemplate(() =>
                {
                    var grid = new Grid
                    {
                        Padding = new Thickness(10),
                        ColumnDefinitions =
                        {
                            new ColumnDefinition { Width = new GridLength(1, GridUnitType.Star) },
                            new ColumnDefinition { Width = 60 }
                        }
                    };

                    var titleLabel = new Label
                    {
                        FontSize = 20,
                        FontAttributes = FontAttributes.Bold
                    };
                    titleLabel.SetBinding(Label.TextProperty, "Title");

                    var descriptionLabel = new Label
                    {
                        FontSize = 14,
                        TextColor = Colors.Gray
                    };
                    descriptionLabel.SetBinding(Label.TextProperty, "Description");

                    var verticalStackLayout = new VerticalStackLayout();
                    verticalStackLayout.Children.Add(titleLabel);
                    verticalStackLayout.Children.Add(descriptionLabel);

                    var ratingLabel = new Label
                    {
                        HorizontalOptions = LayoutOptions.Center,
                        VerticalOptions = LayoutOptions.Center
                    };
                    ratingLabel.SetBinding(Label.TextProperty, new Binding("Rating", stringFormat: "{0} / 5"));

                    grid.Children.Add(verticalStackLayout);
                    grid.SetColumn(verticalStackLayout, 0);
                    grid.Children.Add(ratingLabel);
                    grid.SetColumn(ratingLabel, 1);

                    return new ViewCell { View = grid };
                })
            };
            listView.ItemTapped += ListView_ItemTapped;

            // Create BottomSheet
            bottomSheet = new SfBottomSheet
            {
                EnableSwiping = true,
                HalfExpandedRatio = 0.35,
                ContentPadding = new Thickness(10)
            };

            // BottomSheet Content
            var bottomSheetContent = new VerticalStackLayout { Spacing = 5 };

            void AddRow(string labelText, string bindingPath, string? stringFormat = null)
            {
                var rowGrid = new Grid
                {
                    ColumnDefinitions =
                    {
                        new ColumnDefinition { Width = 120 },
                        new ColumnDefinition { Width = new GridLength(1, GridUnitType.Star) }
                    },
                    ColumnSpacing = 10
                };

                var label = new Label
                {
                    Text = labelText,
                    FontSize = 20,
                    FontAttributes = FontAttributes.Bold
                };

                var valueLabel = new Label
                {
                    FontSize = 16,
                    VerticalTextAlignment = TextAlignment.Center
                };

                if (stringFormat != null)
                {
                    valueLabel.SetBinding(Label.TextProperty, new Binding(bindingPath, stringFormat: stringFormat));
                }
                else
                {
                    valueLabel.SetBinding(Label.TextProperty, bindingPath);
                }

                rowGrid.Children.Add(label);
                rowGrid.SetColumn(label, 0);
                rowGrid.Children.Add(valueLabel);
                rowGrid.SetColumn(valueLabel, 1);

                bottomSheetContent.Children.Add(rowGrid);
            }

            AddRow("Title:", "Title");
            AddRow("Genre:", "Genre");
            AddRow("Published:", "Published");
            AddRow("Description:", "Description");
            AddRow("Price:", "Price", "${0:F2}");

            bottomSheet.BottomSheetContent = bottomSheetContent;

            // Add ListView and BottomSheet to Main Grid
            mainGrid.Children.Add(listView);
            mainGrid.Children.Add(bottomSheet);

            // Set the Content of the Page
            Content = mainGrid;
        }

        private void ListView_ItemTapped(object? sender, ItemTappedEventArgs e)
        {
            bottomSheet.BottomSheetContent.BindingContext = e.Item;
            bottomSheet.Show();
        }
        
    }
}
{% endhighlight %}
{% endtabs %}

N> Using [Content](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_Content), Place the main content inside the bottom sheet's `Content` property. Without using `Content`, Place the main content outside the [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html), making sure the bottom sheet is the last element in the Grid layout.

![Getting Started Image for BottomSheet](images/gettingStarted.png)