# Templates

## Templates

<div>

<figure><img src="../../../../.gitbook/assets/image (20) (1).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../../../.gitbook/assets/image (21) (1).png" alt=""><figcaption></figcaption></figure>

</div>

Dialog templates can be created for faster and more consistent creation of dialogs.

To that end, a new custom dialog template has been created with updated graphics and functionality. To use:

* Copy the Hamilton1Enu.cdt file to your \HAMILTON\Config folder.&#x20;
* When installed, you will see a new icon called "Hamilton1" whenever you create a new custom dialog.

The new dialog has a Hamilton banner and updated graphics for buttons, grouping, etc. It allows for resizing of checkboxes and radio buttons as font size is increased. It also includes a default return variable for the dialog box.



***



Here is the file location and file type of the templates

<figure><img src="../../../../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



here is what is inside the template file

```
     HxPars,CDTemplate    1.KTemplateName1.T11.VUser Output: 2 Buttons2.KTemplateSortName2.T12.VUser Output 23.KTemplateDescription3.T13.V/Template for an output dialog with two buttons.4.KTemplatePicture4.T14.Vÿd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5.KXaml5.T15.Vÿª<Window Title="Dialog" ResizeMode="NoResize" Background="#FFF5F5F5" Width="300" Height="140" xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" xmlns:hhcdf="clr-namespace:Hamilton.HxCustomDialog.Framework;assembly=Hamilton.HxCustomDialogCore" xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
  <Window.Resources>
    <hhcdf:HxTheme Value="Default" x:Key="HxThemeResourceKey" />
  </Window.Resources>
      <Grid>
        <Grid.RowDefinitions>
            <RowDefinition/>
            <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>
        <Grid Grid.Row="0">
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="Auto"/>
                <ColumnDefinition/>
            </Grid.ColumnDefinitions>
            <hhcdf:HxImageCtrl Grid.Column="0" Width="56" Height="56" VerticalAlignment="Top" Margin="10,10,0,0" Source="$$$ICON_WARNING$$$" Stretch="Fill" Name="image1">
			      <hhcdf:HxImageCtrl.Effect>
			        <DropShadowEffect ShadowDepth="3" Color="#FF000000" Opacity="0.4" BlurRadius="6" />
			      </hhcdf:HxImageCtrl.Effect>
			      </hhcdf:HxImageCtrl>
            <hhcdf:HxCanvasCtrl Grid.Column="1" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" ClipToBounds="True">
                <hhcdf:HxTextBlockCtrl Text="Your message..." TextWrapping="Wrap" Name="textBlock" Width="197" Height="43" Margin="3,3,3,3" Opacity="1" Canvas.Left="7" Canvas.Top="7" />
            </hhcdf:HxCanvasCtrl>
        </Grid>
        <StackPanel Grid.Row="1" Orientation="Horizontal" HorizontalAlignment="Center">
            <hhcdf:HxButtonCtrl Width="78" Height="22" ClosesDialog="True" ReturnValue="1" IsDefault="True" Name="button1" Margin="5,5,5,10" Content="OK"/>
            <hhcdf:HxButtonCtrl Width="78" Height="22" ClosesDialog="True" ReturnValue="2" IsCancel="True" Name="button2" Margin="5,5,5,10" Content="Cancel"/>
        </StackPanel>
    </Grid>
</Window>6.KPictures6.T06.V.C0C6
* $$author=gSA_tfs_vector_build$$valid=2$$time=2022-02-08 15:24$$checksum=375303f1$$length=098$$
```

