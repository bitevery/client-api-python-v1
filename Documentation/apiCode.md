# ApiCode Module Instruction
The apiCode module operates only one functionaliy: retrieve or create an api code for the client.

## Input Parameter
* username: A username of bitevery account.
* password: The password for the user account

## Output Return
* ApiCode: A string of 32 digits hash code

## Example
``` python
  from bitevery import apiCode
  
  apicode = apiCode.getApiCode($username, $password)
  print apicode
```
```
>>> 0123456789abcdefghijklmnopqrstuvw
```
