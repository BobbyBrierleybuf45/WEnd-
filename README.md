# WEnd-
&lt;Constants.au3>  Local $pid = Run("C:\Program Files (x86)\Microsoft Visual Studio\Shared\Python39_64\python.exe myscript.py","",@SW_SHOW,$STDOUT_CHILD + $STDERR_CHILD)  $var = "" While ProcessExists($pid)     $var &amp;= StderrRead($pid)     $var &amp;= StdoutRead($pid)     If @error Then ExitLoop     ConsoleWrite(@crlf &amp; $var &amp; @CRLF) WEnd MsgBox(64, 'Result', $var)  
