# Tip Module Instruction
The tip module supports tip link creation for single or multiple receiver(s) in three formats: URL, HTML and QRCODE

## Input Parameter
* ApiCode (required): the api code of the user ([apiCode docs](apiCode.md))
* Format (optional): URL, HTML and QRCODE. Default is URL.
* Locale (optional): effective only if the format is QRCODE. Default is 'en-us'. The other option is 'zh'.
* Distribution (optional): key-value pair for multiple receivers. See example below.

## Output Return
A string of tip link in desired format. If the format is QRCODE, the return is an address to fetch the image.

## example
### Single Receiver
``` python
  from bitevery import tip
  tip_Single = tip.TipService()
  tip_Single.getTipLink('0123456789abcdefghijklmnopqrstuvw')
```
```
>>> https://www.bitevery.com/tip.php?tid=9999999
```
HTML format
``` python
  tip_Single.setFormat("HTML")
  tip_Single.getTipLink('0123456789abcdefghijklmnopqrstuvw')
```
```
>>> <div id="bitEveryTip2345d"></div></script><script src="https://www.bitevery.com/be-js/tip_button.js"></script><script>tip_btn_setup(6,"6303d",1,30,30);</script>
```
QRCODE format
``` python
  tip_Single.setFormat("QRCODE")
  tip_Single.getTipLink('0123456789abcdefghijklmnopqrstuvw')
```
```
>>> https://www.bitevery.com/restAPI/V1.0/qrcode.php?username=bitevery&tid=9999999&locale=en-us
```
Go to the link above, an image of the qrcode will show up
![QRCODE](image/qr_code_en_us.png)
