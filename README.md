<div align="center">

## Api Any Calls/Declarations


</div>

### Description

This is not really a code contribution, but a small tip on API parameter lists.

Ever seen an Api Function which expects parameters of type 'Any' ? . For example

domain/user maintenance calls in the Nt Networking Api or similar (Add Users/Groups etc..).

These parameters usually (in the C/C++ base code) are probably expecting string pointers ,

an other example is in the case of the AddGroup Api call in the NetApi.Dll, where it

expects the name of the server in one of the parameters in the list.

How you actually pass the pointer is by:-

eg.

'###

' Api Function for example:-

' ApiFunction(sArgument as Any) As Long

'

Dim strAnyString As String

Dim strPass() As Byte

Dim lRet As Long

strAnyString = "String as argument"

strPass = strAnyString

lRet = ApiFunction(strPass(0))

'###

What we're basically doing is getting the string to pass, assigning it to another

variable array of type 'byte', then passing the first array segment to the Api function.

Easy enough?

Hope you understood all that !

Robert Dick
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Robert Dick](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/robert-dick.md)
**Level**          |Unknown
**User Rating**    |5.0 (15 globes from 3 users)
**Compatibility**  |VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Windows API Call/ Explanation](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/windows-api-call-explanation__1-39.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/robert-dick-api-any-calls-declarations__1-4501/archive/master.zip)





### Source Code

#

