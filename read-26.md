## Django

Object-relational mapper
- Define data models in python
- Database access
- Can still write SQL

URLs and views
- Create URLconf. to contain URL map
Templates
- Templating similar to EJS but with Python instead of JavaScript

Forms
- Supports creation and use of forms and generates forms from existing models to create and update data
Authentication
- Handles user accounts, permissions, groups and sessions.
- Supports creation of secure user login/logout

Admin
- Automatic admin interface???
- Reads metadata to provide production-ready interface for easy content management
Internationalization
- Supports text translation and location specific formatting for dates, times, numbers and time zones

Security
- Protects against:
  - Clickjacking
  - Cross-site scripting
  - Cross Site Request Forgery (CSRF)
  - SQL injection
  - Remote code execution

URLs
- While it is possible to process requests from every single URL via a single function, it is much more maintainable to write a separate view function to handle each resource. A URL mapper is used to redirect HTTP requests to the appropriate view based on the request URL. The URL mapper can also match particular patterns of strings or digits that appear in a URL and pass these to a view function as data.

View
- A view is a request handler function, which receives HTTP requests and returns HTTP responses. Views access the data needed to satisfy requests via models, and delegate the formatting of the response to templates.

Models
- Models are Python objects that define the structure of an application's data, and provide mechanisms to manage (add, modify, delete) and query records in the database.

Templates
- A template is a text file defining the structure or layout of a file (such as an HTML page), with placeholders used to represent actual content. A view can dynamically create an HTML page using an HTML template, populating it with data from a model. A template can be used to define the structure of any type of file; it doesn't have to be HTML!