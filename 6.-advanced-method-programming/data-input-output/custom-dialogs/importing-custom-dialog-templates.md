# Importing Custom Dialog Templates

Here is the file location and file type of the templates

<figure><img src="../../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>



here is what is inside the template file

```
     HxPars,CDTemplate    1.KTemplateName1.T11.VUser Output: 2 Buttons2.KTemplateSortName2.T12.V
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
