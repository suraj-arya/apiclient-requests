# apiclient-requests

A very lightweight framework for building web api clients using python.
it uses requests for HTTP calls

### how to install

you can install it from pip

$ pip install apiclient-requests

### how to use

you can build your apiclients on top of this library,
using this as a base class, like shown below

class SimpleClient(APIClient):

    def __init__(self, api_key=None):
        super(SimpleClient, self).__init__(
            base_url='https://localhost:5000/api/v1',
            api_key=api_key,
            auth_header='Authentication')


then you can can define your api calls like this


    def list_products(self):
    
        return self.call('products')


### todos
  - limiting requests to avoid request throttling
  - handle xml response types
  - add other authentication types like OAuth
  - add base classes for calculating signatures
  - go on a leh-laddakh tour on my Royal Enfield