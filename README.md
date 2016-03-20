# client-api-python-v1
Official client API to interact with www.bitevery.com

## Installation
Installation via pip
```
  $pip install bitevery
```
Manual installation
```
  $ git clone https://github.com/bitevery/client-api-python-v1
  $ cd client-api-python-v1
  $ python setup.py install
```
## Module Structure
The main module is called bitevery. The main module consists of the following sub-modules:
* tip
* apiCode ([docs](Documentation/apiCode.md))

## API Code Required
In order to hide the user information in the API calls as much as possible, bitevery requires an API code to access all the service endpoints. API is available by using apiCode module.
