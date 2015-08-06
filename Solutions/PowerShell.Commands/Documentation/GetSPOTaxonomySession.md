#Get-SPOTaxonomySession
*Topic automatically generated on: 2015-06-11*

Returns a taxonomy session
##Syntax
```powershell
Get-SPOTaxonomySession [-Web <WebPipeBind>]
```


##Parameters
Parameter|Type|Required|Description
---------|----|--------|-----------
|Web|WebPipeBind|False|The web to apply the command to. Omit this parameter to use the current web.|

##Usage Notes
The object returned is a ClientObject, not all the properties will be loaded by default unless requested through loading them with a context object. Usage Example:
```powershell
$Context = Get-Spocontext
$Session = Get-SPOTaxonomySession
$Store = $Session.GetDefaultKeywordsTermStore()
$Context.Load($Store.Groups)
$Context.ExecuteQuery()
$Store.Groups.Count #show the number of groups in the store.
```
<!-- Ref: B824B21FF036DB705C3C4CD32DC99AD2 -->
