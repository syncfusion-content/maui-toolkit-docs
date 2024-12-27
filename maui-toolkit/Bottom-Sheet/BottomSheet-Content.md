---
layout: post
title: Set Bottom Sheet Content in .NET MAUI Bottom Sheet | Syncfusion
description: Learn here all about setting bottom sheet content support in Syncfusion .NET MAUI Bottom Sheet (SfBottomSheet) control.
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

var verticalStackLayout = new VerticalStackLayout
{
    Padding = new Thickness(20)
};

var button = new Button
{
    Text = "Open Bottom Sheet",
    WidthRequest = 180,
    CornerRadius = 30,
    VerticalOptions = LayoutOptions.Center
};

button.Clicked += OpenBottomSheet;
verticalStackLayout.Children.Add(button);
SfBottomSheet bottomSheet = new SfBottomSheet();
var bottomSheetContent = new Label
{
    Text = "Bottom Sheet Content",
    VerticalOptions = LayoutOptions.Center,
    HorizontalOptions = LayoutOptions.Center,
    FontSize = 14
};

bottomSheet.BottomSheetContent = bottomSheetContent;
bottomSheet.Content = verticalStackLayout;
this.Content = bottomSheet;
  
{% endhighlight %}
{% endtabs %}

{% tabs %}
{% highlight c# %}

private void OpenBottomSheet(object sender, EventArgs e)
{
    bottomSheet.Show();
}

{% endhighlight %}
{% endtabs %}

![BottomSheetContent Image for BottomSheet](images/bottomSheetContent.png)