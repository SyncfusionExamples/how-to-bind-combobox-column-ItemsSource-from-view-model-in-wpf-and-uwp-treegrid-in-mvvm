# how-to-bind-combobox-column-ItemsSource-from-view-model-in-wpf-and-uwp-treegrid-in-mvvm

This example illustrates how to bind the ComboBox column's `ItemsSource` using MVVM in both [WPF TreeGrid](https://www.syncfusion.com/wpf-controls/treegrid) and [UWP TreeGrid](https://www.syncfusion.com/uwp-ui-controls/treegrid)

You can bind the `ItemsSource` from ViewModel to [TreeGridComboBoxColumn](https://help.syncfusion.com/cr/wpf/Syncfusion.UI.Xaml.TreeGrid.TreeGridComboBoxColumn.html) or using `ElementName` binding.

## XAML code:

``` xml
<syncfusion:TreeGridComboBoxColumn AllowEditing="True" 
                                   MappingName="Title"
                                   HeaderText="Title"
                                   ItemsSource="{Binding DataContext.TitleList,
                                                                     ElementName=treeGrid}" />
```

## C# ViewModel:
``` c#
private ObservableCollection<string> titleList;
public ObservableCollection<string> TitleList
{
     get { return titleList; }
     set { titleList = value; }
}
```