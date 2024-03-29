# News Portal Application

This News Portal application allows users to publish and view news articles conveniently. Users can create news articles, categorize them, and view them by category.

## Models

The project includes the following models:

### News

The `News` model represents news articles and contains the following fields:

- `title` (CharField): The title of the news article.
- `content` (TextField): The content of the news article.
- `created_at` (DateTimeField): The date and time when the news article was created.
- `updated_at` (DateTimeField): The date and time when the news article was last updated.
- `photo` (ImageField): An image associated with the news article.
- `is_published` (BooleanField): Indicates whether the news article is published or not.
- `category` (ForeignKey): The category to which the news article belongs.
- `author` (ForeignKey): The author of the news article.

### Category

The `Category` model represents categories for organizing news articles and contains the following fields:

- `title` (CharField): The title of the category.

## Installation

1. Clone the repository to your local machine:

    ```bash
    git clone https://github.com/your-username/news-portal.git
    ```

2. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Apply migrations:

    ```bash
    python manage.py migrate
    ```

4. Run the development server:

    ```bash
    python manage.py runserver
    ```

5. Access the application at [http://localhost:8000/](http://localhost:8000/)

## Technologies Used

- **Django**: The backend framework for building the application.
- **HTML/CSS**: Frontend styling and structure.
- **Bootstrap**: Frontend framework for responsive design.

## Views

The project includes the following views:

- `register`: Allows users to register for an account.
- `user_login`: Allows registered users to log in.
- `user_logout`: Allows logged-in users to log out.
- `HomeNews`: Displays the main page with news articles.
- `NewsByCategory`: Displays news articles filtered by category.
- `ViewNews`: Displays the full content of a news article.
- `CreateNews`: Allows logged-in users to create new news articles.

## Forms

The project includes the following forms:

### UserRegisterForm

Allows users to register for an account with the following fields:

- `username`
- `first_name`
- `last_name`
- `email`
- `password1`
- `password2`

### UserLoginForm

Allows users to log in with the following fields:

- `username`
- `password`

### NewsForm

Allows users to create new news articles with the following fields:

- `title`
- `content`
- `is_published`
- `category`
- 