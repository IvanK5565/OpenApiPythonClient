# openapi_client.DefaultApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**authors_get**](DefaultApi.md#authors_get) | **GET** /authors | Отримати список усіх авторів
[**authors_id_delete**](DefaultApi.md#authors_id_delete) | **DELETE** /authors/{id} | Видалити автора
[**authors_id_get**](DefaultApi.md#authors_id_get) | **GET** /authors/{id} | Отримати деталі конкретного автора
[**authors_id_put**](DefaultApi.md#authors_id_put) | **PUT** /authors/{id} | Оновити інформацію про автора
[**authors_post**](DefaultApi.md#authors_post) | **POST** /authors | Створити нового автора
[**books_get**](DefaultApi.md#books_get) | **GET** /books | Отримати список усіх книг
[**books_id_delete**](DefaultApi.md#books_id_delete) | **DELETE** /books/{id} | Видалити книгу
[**books_id_get**](DefaultApi.md#books_id_get) | **GET** /books/{id} | Отримати деталі конкретної книги
[**books_id_put**](DefaultApi.md#books_id_put) | **PUT** /books/{id} | Оновити інформацію про книгу
[**books_post**](DefaultApi.md#books_post) | **POST** /books | Створити нову книгу


# **authors_get**
> List[Author] authors_get()

Отримати список усіх авторів

### Example


```python
import openapi_client
from openapi_client.models.author import Author
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
    except Exception as e:
        print("Exception when calling DefaultApi->authors_get: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[Author]**](Author.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Успішно отримано список авторів |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authors_id_delete**
> authors_id_delete(id)

Видалити автора

### Example


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
    id = 56 # int | 

    try:
        # Видалити автора
        api_instance.authors_id_delete(id)
    except Exception as e:
        print("Exception when calling DefaultApi->authors_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Автор успішно видалений |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authors_id_get**
> Author authors_id_get(id)

Отримати деталі конкретного автора

### Example


```python
import openapi_client
from openapi_client.models.author import Author
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
    id = 56 # int | 

    try:
        # Отримати деталі конкретного автора
        api_response = api_instance.authors_id_get(id)
        print("The response of DefaultApi->authors_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->authors_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  | 

### Return type

[**Author**](Author.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Успішно отримано деталі автора |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authors_id_put**
> authors_id_put(id, author)

Оновити інформацію про автора

### Example


```python
import openapi_client
from openapi_client.models.author import Author
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
    id = 56 # int | 
    author = openapi_client.Author() # Author | 

    try:
        # Оновити інформацію про автора
        api_instance.authors_id_put(id, author)
    except Exception as e:
        print("Exception when calling DefaultApi->authors_id_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  | 
 **author** | [**Author**](Author.md)|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Інформація про автора успішно оновлена |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authors_post**
> authors_post(author)

Створити нового автора

### Example


```python
import openapi_client
from openapi_client.models.author import Author
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
    author = openapi_client.Author() # Author | 

    try:
        # Створити нового автора
        api_instance.authors_post(author)
    except Exception as e:
        print("Exception when calling DefaultApi->authors_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **author** | [**Author**](Author.md)|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Автор успішно створений |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **books_get**
> List[Book] books_get()

Отримати список усіх книг

### Example


```python
import openapi_client
from openapi_client.models.book import Book
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
        # Отримати список усіх книг
        api_response = api_instance.books_get()
        print("The response of DefaultApi->books_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->books_get: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[Book]**](Book.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Успішно отримано список книг |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **books_id_delete**
> books_id_delete(id)

Видалити книгу

### Example


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
    id = 56 # int | 

    try:
        # Видалити книгу
        api_instance.books_id_delete(id)
    except Exception as e:
        print("Exception when calling DefaultApi->books_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Книга успішно видалена |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **books_id_get**
> Book books_id_get(id)

Отримати деталі конкретної книги

### Example


```python
import openapi_client
from openapi_client.models.book import Book
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
    id = 56 # int | 

    try:
        # Отримати деталі конкретної книги
        api_response = api_instance.books_id_get(id)
        print("The response of DefaultApi->books_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->books_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  | 

### Return type

[**Book**](Book.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Успішно отримано деталі книги |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **books_id_put**
> books_id_put(id, book)

Оновити інформацію про книгу

### Example


```python
import openapi_client
from openapi_client.models.book import Book
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
    id = 56 # int | 
    book = openapi_client.Book() # Book | 

    try:
        # Оновити інформацію про книгу
        api_instance.books_id_put(id, book)
    except Exception as e:
        print("Exception when calling DefaultApi->books_id_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  | 
 **book** | [**Book**](Book.md)|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Інформація про книгу успішно оновлена |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **books_post**
> books_post(book)

Створити нову книгу

### Example


```python
import openapi_client
from openapi_client.models.book import Book
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
    book = openapi_client.Book() # Book | 

    try:
        # Створити нову книгу
        api_instance.books_post(book)
    except Exception as e:
        print("Exception when calling DefaultApi->books_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **book** | [**Book**](Book.md)|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Книга успішно створена |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

