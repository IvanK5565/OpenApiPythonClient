# openapi-client
API для управління книгами та авторами в бібліотеці.

This Python package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1.0.0
- Package version: 1.0.0
- Generator version: 7.12.0
- Build package: org.openapitools.codegen.languages.PythonClientCodegen

## Requirements.

Python 3.8+

## Installation & Usage
### pip install

If the python package is hosted on a repository, you can install directly using:

```sh
pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git`)

Then import the package:
```python
import openapi_client
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import openapi_client
```

### Tests

Execute `pytest` to run the tests.

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python

import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)



# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)

    try:
        # Отримати список усіх авторів
        api_response = api_instance.authors_get()
        print("The response of DefaultApi->authors_get:\n")
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling DefaultApi->authors_get: %s\n" % e)

```

## Documentation for API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**authors_get**](docs/DefaultApi.md#authors_get) | **GET** /authors | Отримати список усіх авторів
*DefaultApi* | [**authors_id_delete**](docs/DefaultApi.md#authors_id_delete) | **DELETE** /authors/{id} | Видалити автора
*DefaultApi* | [**authors_id_get**](docs/DefaultApi.md#authors_id_get) | **GET** /authors/{id} | Отримати деталі конкретного автора
*DefaultApi* | [**authors_id_put**](docs/DefaultApi.md#authors_id_put) | **PUT** /authors/{id} | Оновити інформацію про автора
*DefaultApi* | [**authors_post**](docs/DefaultApi.md#authors_post) | **POST** /authors | Створити нового автора
*DefaultApi* | [**books_get**](docs/DefaultApi.md#books_get) | **GET** /books | Отримати список усіх книг
*DefaultApi* | [**books_id_delete**](docs/DefaultApi.md#books_id_delete) | **DELETE** /books/{id} | Видалити книгу
*DefaultApi* | [**books_id_get**](docs/DefaultApi.md#books_id_get) | **GET** /books/{id} | Отримати деталі конкретної книги
*DefaultApi* | [**books_id_put**](docs/DefaultApi.md#books_id_put) | **PUT** /books/{id} | Оновити інформацію про книгу
*DefaultApi* | [**books_post**](docs/DefaultApi.md#books_post) | **POST** /books | Створити нову книгу


## Documentation For Models

 - [Author](docs/Author.md)
 - [Book](docs/Book.md)


<a id="documentation-for-authorization"></a>
## Documentation For Authorization

Endpoints do not require authorization.


## Author




