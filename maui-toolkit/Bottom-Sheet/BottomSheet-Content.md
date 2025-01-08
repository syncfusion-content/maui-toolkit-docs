---
layout: post
title: Set Bottom Sheet Content in .NET MAUI Bottom Sheet | Syncfusion<sup>®</sup>
description: Learn here all about setting bottom sheet content support in Syncfusion<sup>®</sup> .NET MAUI Bottom Sheet (SfBottomSheet) control.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---

# Set Main Content and Bottom Sheet Content in .NET MAUI Bottom Sheet

* The main content of the [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html) is always visible and can be set using the [Content](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_Content) property.

* The `BottomSheet` content is only viewable when the sheet is in the FullExpanded, HalfExpanded, or Collapsed state. Its content can be set as : [BottomSheetContent](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_BottomSheetContent).

{% tabs %}
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" HalfExpandedRatio="0.35" ContentPadding="10">
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
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet
{
    HalfExpandedRatio = 0.35,
    ContentPadding = new Thickness(10)
};

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
  
{% endhighlight %}
{% endtabs %}

{% tabs %}
{% highlight c# %}

private void OnListViewItemTapped(object? sender, ItemTappedEventArgs e)
{
    bottomSheet.BottomSheetContent.BindingContext = e.Item;
    bottomSheet.Show();
}

{% endhighlight %}
{% endtabs %}

![BottomSheetContent Image for BottomSheet](images/bottomSheetContent.png)