<div align="center">

## Allow Numerals Only<br/>by PorkNBeans

</div>

### Description

After looking here and a few other places for a simple code that allows only numerals and not to allow text to be pasted into a textbox and with no prevail I figured it out. Not a major thing but for beginners this will help them.

### Source Code

```
'just paste this in the change section of the textbox sub<br>
<br>
<br>
private sub txttext1_change()<br>
'if an error should occur go to the error handler
<br>
 on error goto txttext1_change_err
<br>
'if the text entered is not numeric
<br>
100 if not isnumeric(txttext1.text) then
<br>
'display the message box warning
<br>
102 msgbox "only numerals are allowed", vbokonly + vbexclamation, "numerals only"
<br>
 end if
<br>
 exit sub
<br>
'after handling the error and showing what line the error occured in if any
<br>
' then resume the next action
<br>
<br>
txttext1_change_err:
<br>
 msgbox err.description & vbcrlf & _
<br>
"in project1.form1.txttext1_change " & _
<br>
 "at line " & erl
<br>
 resume next
<br>
end sub
<br>
<br>
you could easily have the textbox clear out by adding txt.text ="" but that is so basic i figured no need to add it.
please if theres no code like this and it does indeed help you at least give me a vote for my time sharing this.
```

