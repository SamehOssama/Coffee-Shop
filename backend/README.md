# Coffee Shop Backend

This project is a coffee shop api for udacity's advance web development nanodegree and serves as a test for our knowledge about APIs' authentication and authorization from Module 4 : Identity and Access Management. The users have varying access to actions depending on their role and their permissions from clients to managers. Anyone can access the shop's menu.


- [Getting Started](#getting-started)
  - [Installing Dependencies](#installing-dependencies)
  - [Running the server](#running-the-server)
- [API References](#api-references)
  - [Errors](#errors)
  - [Endpoints](#endpoints)


## Getting Started

----

### Installing Dependencies

#### Python 3.8

Follow instructions to install the latest version of python for your platform in the [python docs](https://docs.python.org/3/using/unix.html#getting-and-installing-the-latest-version-of-python)

#### Virtual Enviornment

We recommend working within a virtual environment whenever using Python for projects. This keeps your dependencies for each project separate and organaized. Instructions for setting up a virual enviornment for your platform can be found in the [python docs](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/)

#### PIP Dependencies

Once you have your virtual environment setup and running, install dependencies by naviging to the `/backend` directory and running:

```bash
pip install -r requirements.txt
```

This will install all of the required packages we selected within the `requirements.txt` file.

##### Key Dependencies

- [Flask](http://flask.pocoo.org/)  is a lightweight backend microservices framework. Flask is required to handle requests and responses.

- [SQLAlchemy](https://www.sqlalchemy.org/) and [Flask-SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com/en/2.x/) are libraries to handle the lightweight sqlite database. Since we want you to focus on auth, we handle the heavy lift for you in `./src/database/models.py`. We recommend skimming this code first so you know how to interface with the Drink model.

- [jose](https://python-jose.readthedocs.io/en/latest/) JavaScript Object Signing and Encryption for JWTs. Useful for encoding, decoding, and verifying JWTS.

## Running the server

From within the `./src` directory first ensure you are working using your created virtual environment.

Each time you open a new terminal session, run:

```bash
export FLASK_APP=api.py;
```

To run the server, execute:

```bash
flask run --reload
```

The `--reload` flag will detect file changes and restart the server automatically.

## API References

----

- Base url: This app is not hosted on a web server, instead, it is hosted locally at the default ```http://127.0.0.1:5000/```
- Authentication: This version of the app doesn't require authentication.

### Errors
HTTP requests always come with a code to determine the response state from `2xx` codes that means success to `4xx` codes that means there was an error with the request.
Here is a list of the expected response codes from this API and their meaning:

| Code    | Text               | Description                                                                       |
| ------- | ------------------ | --------------------------------------------------------------------------------- |
| **200** | OK                 | Everything worked as expected.                                                    |
| **400** | Bad Request        | The request is missing a required parameter.                                      |
| **401** | Unauthorized       | No valid token was presented to the API.                                          |
| **403** | Forbidden          | The API user doesn't have the this permission.                                    |
| **404** | Not found          | The requested resource could not be found.                                        |
| **405** | Method not allowed | The request method is not supported for the requested resource.                   |
| **422** | unprocessable      | The request was well-formed but was unable to be followed due to semantic errors. |

### Endpoints
```html
GET '/drinks'
GET '/drinks-detail'
POST '/drinks'
PATCH '/drinks/drink_id'
DELETE '/drinks/drink_id'
```