<div align="center">

## Moving Borderless Forms Without Windows API


</div>

### Description

This an easy way to move a windows form without a border. It does now use the windows API very easy to understand code is very short. Simply click down on the form and move the mouse. the form will move with the mouse alot easier to use instead of the windows API
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Derrick Blake](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/derrick-blake.md)
**Level**          |Intermediate
**User Rating**    |4.8 (38 globes from 8 users)
**Compatibility**  |VB\.NET
**Category**       |[Controls/ Forms/ Dialogs/ Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/controls-forms-dialogs-menus__10-3.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/derrick-blake-moving-borderless-forms-without-windows-api__10-490/archive/master.zip)





### Source Code

```
Dim newPoint As New System.Drawing.Point()
 Dim a As Integer
 Dim b As Integer
 Private Sub Form1_MouseDown(ByVal sender As Object, ByVal e As System.Windows.Forms.MouseEventArgs) Handles MyBase.MouseDown
  a = Me.MousePosition.X - Me.Location.X
  b = Me.MousePosition.Y - Me.Location.Y
 End Sub
 Private Sub Form1_MouseMove(ByVal sender As Object, ByVal e As System.Windows.Forms.MouseEventArgs) Handles MyBase.MouseMove
  If e.Button = MouseButtons.Left Then
   newPoint = Me.MousePosition
   newPoint.X = newPoint.X - (a)
   newPoint.Y = newPoint.Y - (b)
   Me.Location = newPoint
  End If
 End Sub
```

