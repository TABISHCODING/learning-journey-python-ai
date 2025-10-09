
### 

Activity: Use Flask-RESTful

This document provides a comprehensive solution and explanation for the graded assignment.

-----

### 

Scenario & Objective

  * **Scenario:** You are a junior Python developer at an online bookstore. Your task is to use Flask-RESTful to build a new API to keep track of all the books. This API will act as a digital library card catalog that other systems can access to help the bookstore manage its inventory.
  * **Objective:** Create a simplified API for an online bookstore using Flask-RESTful that can handle requests for retrieving and managing book information.

-----

### 

Instructions: Step-by-Step Code Solution

This is the complete code that should be run sequentially in a Jupyter Notebook to create the bookstore API.

#### 

1.  Set up Your Development Environment

<!-- end list -->

  * **Run this cell to install the necessary packages:**
    ```python
    !pip install nest_asyncio flask flask_restful
    ```
  * **Run this cell to import the packages into your environment:**
    ```python
    import nest_asyncio
    from flask import Flask, request
    from flask_restful import Api, Resource
    from threading import Thread
    ```

#### 

2.  Define Sample Data

<!-- end list -->

  * **Load this dictionary of books into your session:**
    ```python
    books = [
        {"isbn": "1234567890", "title": "The Great Gatsby", "author": "F. Scott Fitzgerald", "price": 10},
        {"isbn": "0987654321", "title": "1984", "author": "George Orwell", "price": 8.99}
    ]
    ```

#### 

3.  Set Up Flask App and API

<!-- end list -->

  * **Initialize the Flask application and the Flask-RESTful API:**
    ```python
    app = Flask(__name__)
    api = Api(app)
    ```

#### 

4.  Create a Book Resource
    Create a Python class named `Book` that inherits from `Resource`. This single class will handle all HTTP requests for our API.

<!-- end list -->

```python
class Book(Resource):
    # Method to handle GET requests
    def get(self, isbn=None):
        if isbn:
            for book in books:
                if book['isbn'] == isbn:
                    return book, 200
            return {"message": "Book not found"}, 404
        return books, 200
```

  * **Code Explanation (GET):**
      * `def get(self, isbn=None):`: Defines the method that handles `GET` requests. It accepts an optional `isbn` argument.
      * `if isbn:`: Checks if an ISBN was provided in the URL.
      * **If `isbn` exists:** It loops through the `books` list to find a match. If found, it returns that specific book's data and a `200 OK` status code. If not found, it returns an error message with a `404 Not Found` status.
      * **If `isbn` does not exist:** It means the user is requesting the entire collection, so it returns the full `books` list and a `200 OK` status.

<!-- end list -->

```python
    # Method to handle POST requests
    def post(self):
        new_book = request.json
        books.append(new_book)
        return new_book, 201
```

  * **Code Explanation (POST):**
      * `def post(self):`: Defines the method that handles `POST` requests.
      * `new_book = request.json`: Accesses the JSON data sent in the body of the request.
      * `books.append(new_book)`: Adds the new book dictionary to our `books` list.
      * `return new_book, 201`: Returns the newly created book and, importantly, a `201 Created` status code to indicate success.

<!-- end list -->

```python
    # Method to handle PUT requests
    def put(self, isbn):
        for book in books:
            if book['isbn'] == isbn:
                book.update(request.json)
                return book, 200
        return {"message": "Book not found"}, 404
```

  * **Code Explanation (PUT):**
      * `def put(self, isbn):`: Defines the method for `PUT` requests, which requires an `isbn` to identify the book to update.
      * It loops to find the matching book.
      * `book.update(request.json)`: If the book is found, this line updates the existing book's dictionary with the new data sent in the request body.
      * `return book, 200`: Returns the updated book data with a `200 OK` status.

<!-- end list -->

```python
    # Method to handle DELETE requests
    def delete(self, isbn):
        global books
        books = [book for book in books if book['isbn'] != isbn]
        return {"message": "Book deleted"}, 200
```

  * **Code Explanation (DELETE):**
      * `def delete(self, isbn):`: Defines the method for `DELETE` requests, requiring an `isbn`.
      * `global books`: Declares that we intend to modify the global `books` variable.
      * `books = [book for book in books if book['isbn'] != isbn]`: This is a list comprehension that rebuilds the `books` list, including only those books whose ISBN does *not* match the one to be deleted.
      * `return {"message": "Book deleted"}, 200`: Returns a success message with a `200 OK` status.

#### 

5.  Add Endpoints to the API

<!-- end list -->

  * **Connect the `Book` class to the URL patterns:**
    ```python
    api.add_resource(Book, '/books', '/books/<string:isbn>')
    ```
  * **Code Explanation:**
      * `api.add_resource(...)`: This line tells Flask-RESTful that the `Book` class should handle requests for two URL patterns:
          * `/books`: For requests on the entire collection (GET all, POST new).
          * `/books/<string:isbn>`: For requests on a specific item (GET one, PUT, DELETE).

#### 

6.  Run the Application

<!-- end list -->

  * **Write the code to run the Flask application in a separate thread:**
    ```python
    nest_asyncio.apply()

    def run_app():
        app.run(port=5000, debug=False)

    thread = Thread(target=run_app)
    thread.start()

    print("API is running! Test it at http://127.0.0.1:5000/books")
    ```
  * **Code Explanation:**
      * This code runs the Flask app in a background **thread**. This is a special setup required to run a live server inside a Jupyter Notebook without blocking the notebook from running other cells.

-----

### 

Testing the API with Postman

You can use an API client like Postman to test that all your endpoints are working as expected.

  * **Test GET:**
      * **URL:** `http://127.0.0.1:5000/books` (to get all) or `http://127.0.0.1:5000/books/1234567890` (to get one).
  * **Test POST:**
      * **Method:** `POST`, **URL:** `http://127.0.0.1:5000/books`.
      * **Body (raw, JSON):** `{ "isbn": "1112223334", "title": "Brave New World", "author": "Aldous Huxley", "price": 12.99 }`
  * **Test PUT:**
      * **Method:** `PUT`, **URL:** `http://127.0.0.1:5000/books/1112223334`.
      * **Body (raw, JSON):** `{ "title": "Brave New World - Updated Edition", "author": "Aldous Huxley", "price": 14.99 }`
  * **Test DELETE:**
      * **Method:** `DELETE`, **URL:** `http://127.0.0.1:5000/books/1112223334`.

-----

### 

Graded Questions & Answers

#### 

**Question 1**
Which HTTP methods are most commonly used in API testing with Postman?

  * **Correct Answer:** `GET, POST, PUT, DELETE`
  * **Rationale:** These four methods directly correspond to the fundamental CRUD operations (Create, Read, Update, Delete) that form the basis of most RESTful APIs.

#### 

**Question 2**
How do you define a resource in Flask-RESTful?

  * **Correct Answer:** `By creating a class that inherits from Resource`
  * **Rationale:** As shown in the code solution, a resource is defined by creating a Python class that inherits from the `Resource` class provided by the `flask_restful` library.

#### 

**Question 3**
What is the main function used to start a Flask application?

  * **Correct Answer:** `app.run()`
  * **Rationale:** The `app` object is an instance of the `Flask` class. To start the development web server, you call the `.run()` method on this object.

#### 

**Question 4**
Which of the following headers can be included in a `GET` request? (Select all that apply)

  * **Correct Answers:** `Cache-Control`, `Authorization`
  * **Rationale:**
      * `Authorization` is used to send credentials (like an API key) to access protected resources.
      * `Cache-Control` is used to specify caching policies.
      * `Content-Length` and `Content-Type` are headers related to the body of a request, which `GET` requests typically do not have.

#### 

**Question 5**
What is the primary purpose of using REST in web development?

  * **Correct Answer:** `To provide a scalable and stateless communication method between client and server`
  * **Rationale:** REST is an architectural style built on the principles of scalability and **statelessness**, where each request contains all the information needed to process it. This makes the system highly scalable.
