# UserList
$aChildUsers = [ 'NephewA', 'NephewB' ]  $aUserList = GetSignedInUsers()  For $i = 0 to UBound($aUserList)-1     If Not UserIsActive($aUserList[$i]) Then         For $j = 0 to UBound($aChildUsers)-1             If $aUserList[$i] = $aChildUsers[$j] Then LogOffUser($aUserList[$i])         Next     EndIf Next
