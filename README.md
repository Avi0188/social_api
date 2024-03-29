# social_api

1. **Register User**
   - **Method:** POST
   - **Endpoint:** /api/auth/register
   - **Description:** Registers a new user with provided username, email, and password.
   - **Request Body:**
     - username: Username of the user
     - email: Email address of the user
     - password: Password of the user (will be hashed before saving)
   - **Response:** Returns the registered user object.

2. **Login User**
   - **Method:** POST
   - **Endpoint:** /api/auth/login
   - **Description:** Logs in a user with provided username and password.
   - **Request Body:**
     - username: Username of the user
     - password: Password of the user
   - **Response:** Returns the user object excluding the password.

3. **Create Category**
   - **Method:** POST
   - **Endpoint:** /api/categories
   - **Description:** Creates a new category.
   - **Request Body:**
     - name: Name of the category
   - **Response:** Returns the created category object.

4. **Get All Categories**
   - **Method:** GET
   - **Endpoint:** /api/categories
   - **Description:** Retrieves all categories.
   - **Response:** Returns an array of category objects.

5. **Create Post**
   - **Method:** POST
   - **Endpoint:** /api/posts
   - **Description:** Creates a new post with provided title, username, description, categories, and optional photo.
   - **Request Body:**
     - title: Title of the post
     - username: Username of the author
     - desc: Description of the post
     - categories: Array of category names
     - file: (Optional) Image file for the post
   - **Response:** Returns the created post object.

6. **Update Post**
   - **Method:** PUT
   - **Endpoint:** /api/posts/:id
   - **Description:** Updates an existing post by ID.
   - **Request Parameters:**
     - id: ID of the post to be updated
   - **Request Body:** Updated fields of the post
   - **Response:** Returns the updated post object.

7. **Delete Post**
   - **Method:** DELETE
   - **Endpoint:** /api/posts/:id
   - **Description:** Deletes a post by ID.
   - **Request Parameters:**
     - id: ID of the post to be deleted
   - **Response:** Returns a success message upon successful deletion.

8. **Get Post by ID**
   - **Method:** GET
   - **Endpoint:** /api/posts/:id
   - **Description:** Retrieves a post by ID.
   - **Request Parameters:**
     - id: ID of the post to be retrieved
   - **Response:** Returns the post object.

9. **Get All Posts**
   - **Method:** GET
   - **Endpoint:** /api/posts
   - **Description:** Retrieves all posts. Optionally filters by username or category.
   - **Query Parameters:**
     - user: Username to filter posts by author
     - cat: Category name to filter posts by category
   - **Response:** Returns an array of post objects.

10. **Update User**
    - **Method:** PUT
    - **Endpoint:** /api/users/:id
    - **Description:** Updates an existing user's information by ID.
    - **Request Parameters:**
      - id: ID of the user to be updated
    - **Request Body:** Updated fields of the user
    - **Response:** Returns the updated user object.

11. **Delete User**
    - **Method:** DELETE
    - **Endpoint:** /api/users/:id
    - **Description:** Deletes a user by ID.
    - **Request Parameters:**
      - id: ID of the user to be deleted
    - **Response:** Returns a success message upon successful deletion.

12. **Get User by ID**
    - **Method:** GET
    - **Endpoint:** /api/users/:id
    - **Description:** Retrieves a user by ID.
    - **Request Parameters:**
      - id: ID of the user to be retrieved
    - **Response:** Returns the user object excluding the password.

Response: Returns the user object excluding the password.
