# laravel-Basic-interview-1-questions
A collection of Laravel interview questions with answers


# What is Laravel?
# What is MVC Architecture?     
# What is OOP in PHP, and why should we learn it?     
# What is Composer?    
# What is Artisan?    
# What are Migrations in Laravel?     
# What is Eloquent ORM?    
# What is Blade Templating Engine?     
# What is Middleware in Laravel?     
# How do you handle forms in Laravel?     
# Advantages of Using Laravel?    
# What is a Facade in Laravel?    
# What are Service Providers?    


1. What is Laravel?

Laravel is a PHP web application framework that follows the MVC (Model–View–Controller) architecture. It provides tools and features to build secure, scalable, and maintainable web applications faster.

2. What is MVC Architecture?

Model → Handles the data and database logic.

View → Displays the data (the user interface).

Controller → Handles user requests, communicates with the Model, and returns a response (View).

This separation makes applications more organized and maintainable.

3. What is OOP in PHP, and why should we learn it?

OOP (Object-Oriented Programming) is a programming style that uses classes and objects to structure code.

Key concepts: Encapsulation, Inheritance, Polymorphism, Abstraction.

Benefits:
1 Makes code reusable
2 Easier to maintain and scale
3 Encourages clean architecture

Since Laravel is built on OOP principles, understanding OOP is essential.

4. What is Composer?

Composer is a dependency manager for PHP.
It helps install and manage libraries/packages (like Laravel itself) so you don’t have to manually download and update them.

5. What is Artisan?

Artisan is Laravel’s command-line interface (CLI).
It provides commands to speed up development, like:

php artisan serve → starts a server

php artisan make:model → creates a model

php artisan migrate → runs migrations

6. What are Migrations in Laravel?

Migrations are version control for your database schema.
Instead of manually creating tables, you write migration files (PHP code) to define database structure.
Example: add a new column → write migration → run php artisan migrate.

7. What is Eloquent ORM?

Eloquent is Laravel’s Object Relational Mapper (ORM).
It allows you to interact with the database using models and relationships instead of raw SQL.
Example:

$user = User::find(1);  
echo $user->name;


This fetches a user record without writing SQL.

8. What is Blade Templating Engine?

Blade is Laravel’s templating engine for building views.
It provides features like:

Template inheritance (@extends, @section, @yield)

Short syntax for echoing data ({{ $name }})

Conditionals & loops (@if, @foreach)

9. What is Middleware in Laravel?

Middleware acts like a filter for HTTP requests.
Example:

Authentication Middleware → ensures only logged-in users access certain pages.

CSRF Middleware → protects against cross-site request forgery.

10. How do you handle forms in Laravel?

Blade syntax for forms:

<form method="POST" action="/submit">
    @csrf
    <input type="text" name="name">
    <button type="submit">Submit</button>
</form>


CSRF protection is automatically applied with @csrf.

In Controller, handle input using:

$name = $request->input('name');

11. Advantages of Using Laravel

Built-in authentication & authorization

Eloquent ORM for database handling

Blade templating

Artisan CLI

Migrations for database versioning

Middleware for request filtering

Security features (CSRF, XSS protection)

Large community + ecosystem

12. What is a Facade in Laravel?

Facades provide a static interface to Laravel’s classes and services.
Example:

Cache::get('key');  
Route::get('/home', ...);


They look like static methods but internally resolve classes from the service container.

13. What are Service Providers?

Service Providers are the central place to configure and bootstrap application services.
They tell Laravel how to load things like routes, events, middleware, or custom services.
Almost all major Laravel features are bootstrapped through service providers.
