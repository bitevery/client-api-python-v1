# Tip Module Instruction
The tip module supports tip link creation for single or multiple receiver(s) in three formats: URL, HTML and QRCODE

## Input Parameter
* ApiCode (required): the api code of the user ([apiCode docs](apiCode.md))
* Format (optional): URL, HTML and QRCODE. Default is URL.
* Locale (optional): effective only if the format is QRCODE. Default is 'en-us'. The other option is 'zh'.
* Distribution (optional): key-value pair for multiple receivers. See example below.

## Output Return
A string of tip link in desired format. If the format is QRCODE, the return is an address to fetch the image.
