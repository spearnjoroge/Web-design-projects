# RESTful API for Inventory Management

## Description

This versatile RESTful API, built using Flask and Python, offers a secure and user-friendly solution for managing inventory. It caters to a broad range of businesses, handling both physical goods and service-based offerings.

## Features

-   **User Authentication:** Secure user access is ensured through registration and token-based authentication with refresh functionality.
-   **Flexible Store Management:** Users can create and manage stores, each with a descriptive name and the ability to hold a list of items. This allows for managing physical products, digital goods, or even service categories within the same system.
-   **Comprehensive Item Management:** Users can create items within specific stores, assigning names and potentially prices (for physical/digital goods) or descriptions (for services). This granular control facilitates detailed inventory tracking, regardless of the item type.
-   **Tailored Data Retrieval:** The API offers flexible data retrieval capabilities. Users can access a complete list of stores and their associated items (including both shoes and services). Additionally, specific stores and their offerings can be retrieved based on store names. Furthermore, users can obtain lists of items within a particular store, enabling targeted inventory checks across physical or service-based offerings.

## Installation

### Prerequisites:

-   Python version 3.7 or later ([https://www.python.org/downloads/](https://www.python.org/downloads/))
-   pip (package installer) - Usually comes bundled with Python

### Steps:
1. Clone the repository:
```Bash
https://github.com/spearnjoroge/RESTful_API_for_Inventory_Management.git
```
2. Create a virtual environment (recommended):
```Bash
python/3 -m venv venv  # Create a virtual environment named 'venv'
```
Install dependencies:
```Bash
pip install -r requirements.txt
```
## Usage

Start the development server:

``` Bash
python app.py
```
This will typically start the server on http://127.0.0.1:5000/. You can adjust the port number if needed.


### Interact with the API:

Use a REST client tool (e.g., Postman, Insomnia, curl) or code in your preferred language to send requests to the API endpoints. Refer to the API Documentation section for details on available endpoints, request methods, expected data formats, and response structures.

## API Documentation

the api uses swagger for its documentation:
```bash
http://127.0.0.1:5000/swagger-ui
```

### Document each endpoint:
| Feature                   | URL                              | Method | Description                                        
|---------------------------|----------------------------------|--------|----------------------------------------------------|
| **User Management**       |                                  |        |                                                    |
| Register User             | `{{url}}/register`               | POST   | Create a new user                                  |
| Login                     | `{{url}}/login`                  | POST   | Authenticate a user                                |
| Logout                    | `{{url}}/logout`                 | POST   | Revoke user's JWT token                            |
| Get User Details          | `{{url}}/user/<id>`              | GET    | Retrieve details of a specific user                |
| Delete User               | `{{url}}/user/<id>`              | DELETE | Delete a specific user                             |
| **Store Management**      |                                  |        |                                                    |
| Create Store Tag          | `{{url}}/store/<id>/tag`         | POST   | Create a new tag within a specific store           |
| Link Item to Store Tag    | `{{url}}/store/<id>/tag/<id>`    | POST   | Link an item to a specific tag within a store      |
| Get List of Store Tags    | `{{url}}/store/<id>/tag`         | GET    | Retrieve all tags associated with a specific store |
| Get Tag Information       | `{{url}}/tag/<id>`               | GET    | Get details of a specific tag                      |
| Unlink Item from Tag      | `{{url}}/store/<id>/tag/<id>`    | DELETE | Unlink an item from a specific tag within a store  |
| Delete Tag                | `{{url}}/tag/<id>`               | DELETE | Delete a specific tag                              |
| Get All Stores            | `{{url}}/store`                  | GET    | Retrieve all stores                                |
| Get Specific Store Details| `{{url}}/store/<id>`             | GET    | Get details of a specific store                    |
| Create New Store          | `{{url}}/store`                  | POST   | Create a new store                                 |
| Delete Store              | `{{url}}/store/<id>`             | DELETE | Delete a specific store                            |
| **Item Management**       |                                  |        |                                                    |
| Get All Items             | `{{url}}/item`                   | GET    | Retrieve all items                                 |
| Get Specific Item Details | `{{url}}/item/<id>`              | GET    | Get details of a specific item                     |
| Create New Item           | `{{url}}/item`                   | POST   | Create a new item                                  |

### License

Specify the license under which your project is distributed. Common open-source licenses include MIT, Apache 2.0, and GPL.

###  Additional Notes
feel free to fork and play with it
