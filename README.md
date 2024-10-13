

# Ecommerce Toy Store

**Ecommerce Toy Store** is a user-friendly online platform where customers can explore and purchase a wide variety of toys for children of all ages. It features an easy-to-navigate interface with categories, product details, a shopping cart, and a checkout process. This store was built using Django and provides a seamless shopping experience.

You can view the live site [here](https://yourdeployedlink.com/).

## Table of Contents
  * [User Experience (UX)](#user-experience-ux)
    + [User Stories](#user-stories)
    + [Design](#design)
  * [Features](#features)
    + [Header](#header)
    + [Footer](#footer)
    + [Home Page](#home-page)
    + [Product Pages](#product-pages)
    + [Cart and Checkout](#cart-and-checkout)
  * [Testing](#testing)
  * [Security Features](#security-features)
    + [User Authentication](#user-authentication)
    + [Form Validation](#form-validation)
    + [Database Security](#database-security)
    + [Custom Error Pages](#custom-error-pages)
  * [Deployment](#deployment)
  * [Forking This Repository](#forking-this-repository)
  * [Cloning This Repository](#cloning-this-repository)
  * [Languages and Tools Used](#languages-and-tools-used)
  * [Credits](#credits)
  * [Acknowledgments](#acknowledgments)

## User Experience (UX)

### User Stories
- As a user, I can browse through categories of toys so that I can find the type of toys I want.
- As a user, I can view the details of individual products so that I can make informed purchase decisions.
- As a user, I can add and remove items from the cart.
- As a user, I can proceed to checkout and securely pay for my orders.

### Design
The **Ecommerce Toy Store** is designed with a vibrant and playful aesthetic, which reflects the target audience—parents shopping for toys for their kids. It is responsive, ensuring a smooth experience across different devices.

## Features

### Header
- The header includes the logo, a navigation bar, and links to the shopping cart and user account. 
- The navigation allows users to quickly browse different toy categories, view their cart, or log in.

### Footer
- The footer contains links to the store's social media pages and additional company information.
- Social media icons link to Facebook, Instagram, and Twitter, helping customers stay connected.

### Home Page
- The homepage showcases featured toy collections, categories, and promotional offers.
- A search bar allows users to quickly find specific toys by name.

### Product Pages
- Each product page includes the toy’s image, description, price, and an "Add to Cart" button.
- The toy details include age recommendations, materials, and availability status.

### Cart and Checkout
- Users can view their selected products, update quantities, and proceed to checkout securely.
- The checkout process allows customers to enter shipping and payment information.

## Testing
- HTML and CSS were validated using the W3C Markup Validator and W3C CSS Validator.
- All forms, buttons, and features have been tested to ensure functionality across devices and browsers.

## Security Features

### User Authentication
- Users can register, log in, and manage their accounts. Django's authentication system is used to secure this functionality.
- Users are redirected to the login page if they attempt to access restricted pages.

### Form Validation
- Forms are validated to ensure that incorrect data is not submitted. Users receive feedback if there are issues.

### Database Security
- The database is securely managed, and sensitive information, such as passwords, is encrypted.

### Custom Error Pages
- Custom error pages (404, 500, etc.) provide clear messages to the user if they encounter an error.

## Deployment

### Heroku Deployment:
- The application was deployed on Heroku. Here’s how you can replicate the deployment:
  1. Create a Heroku account and log in.
  2. Create a new app and connect it to the GitHub repository.
  3. Set up environment variables for the database URL, secret key, and other necessary configurations.
  4. Push your code to Heroku, and the app will be automatically deployed.

## Forking This Repository
- Navigate to the repository on GitHub and click on the "Fork" button in the top-right corner.
- This will create a copy of the repository under your GitHub account.

## Cloning This Repository
1. Open the repository.
2. Click the "Code" button and copy the URL.
3. In your terminal, run:
    ```bash
    git clone <repository-url>
    ```

## Languages and Tools Used
- **Languages**: Python, HTML, CSS, JavaScript
- **Frameworks**: Django, Bootstrap
- **Database**: SQLite (Development), PostgreSQL (Production)
- **Deployment**: Heroku
- **Other Tools**: Django Crispy Forms, Django Allauth, Cloudinary for image storage

## Credits
- **W3Schools**, **Stack Overflow**, and **Django Documentation** for various tutorials and code snippets.
- **Bootstrap 4** for the responsive design framework.
- **Cloudinary** for media storage solutions.

## Acknowledgments
Though challenging project.