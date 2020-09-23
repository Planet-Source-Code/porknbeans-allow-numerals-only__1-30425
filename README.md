<div align="center">

## Allow Numerals Only


</div>

### Description

After looking here and a few other places for a simple code that allows only numerals and not to allow text to be pasted into a textbox and with no prevail I figured it out. Not a major thing but for beginners this will help them.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[PorkNBeans](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/porknbeans.md)
**Level**          |Beginner
**User Rating**    |4.0 (28 globes from 7 users)
**Compatibility**  |VB 3\.0, VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[String Manipulation](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/string-manipulation__1-5.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/porknbeans-allow-numerals-only__1-30425/archive/master.zip)





### Source Code

'Just Paste This in the change section of the textbox sub<BR>
<br>
<br>
Private Sub txtText1_Change()<br>
'if an error should occur go to the error handler
<br>
 On Error GoTo txtText1_Change_Err
<br>
'if the text entered is not numeric
<br>
100 If Not IsNumeric(txtText1.Text) Then
<br>
'display the message box warning
<br>
102 MsgBox "Only Numerals Are Allowed", vbOKOnly + vbExclamation, "Numerals Only"
<br>
 End If
<br>
 Exit Sub
<br>
'after handling the error and showing what line the error occured in if any
<br>
' then resume the next action
<br>
<br>
txtText1_Change_Err:
<br>
 MsgBox Err.Description & vbCrLf & _
<br>
"in Project1.Form1.txtText1_Change " & _
<br>
 "at line " & Erl
<br>
 Resume Next
<br>
End Sub
<br>
<br>
you could easily have the textbox clear out by adding txt.text ="" but that is so basic I figured no need to add it.
Please if theres no code like this and it does indeed help you at least give me a vote for my time sharing this.

