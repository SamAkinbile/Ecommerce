

# Ecommerce Toy Store

**Ecommerce Toy Store** is a user-friendly online platform where customers can explore and purchase a wide variety of toys for children of all ages. It features an easy-to-navigate interface with categories, product details, a shopping cart, and a checkout process. This store was built using Django and provides a seamless shopping experience.

You can view the live site [here](https://8000-samakinbile-ecommerce-fxonzcl1uyj.ws.codeinstitute-ide.net/).

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




### Attach the Postgres database:
- In the Resources tab, under add-ons, type in Postgres and select the Heroku Postgres option.
- Copy the DATABASE_URL located in Config Vars in the Settings Tab.
- Go back to your IDE and install 2 more requirements:
    - `pip3 install dj_databse_url`
    - `pip3 install psycopg2-binary` 
- Create requirements.txt file by typing `pip3 freeze --local > requirements.txt`
- Add the DATABASE_URL value and your chosen SECRET_KEY value to the env.py file. 
- In settings.py file import dj_database_url, comment out the default configurations within database settings and add the following: 

```
DATABASES = {
    'default': dj_database_url.parse(os.environ.get('DATABASE_URL'))
}
```
- Run migrations and create a superuser for the new database. 
- Create an if statement in settings.py to run the postgres database when using the app on heroku or sqlite if not

```
    if 'DATABASE_URL' in os.environ:
        DATABASES = {
            'default': dj_database_url.parse(os.environ.get('DATABASE_URL'))
        }
    else:
        DATABASES = {
            'default': {
                'ENGINE': 'django.db.backends.sqlite3',
                'NAME': BASE_DIR / 'db.sqlite3',
            }
    }
```

- Create requirements.txt file by typing `pip3 freeze --local > requirements.txt`
- Create a file named "Procfile" in the main directory and add the following: `web: gunicorn project-name.wsgi:application`
- Add Heroku to the ALLOWED_HOSTS list in settings.py in the format ['app_name.heroku.com', 'localhost']

- Push these changes to Github.

## Forking This Repository
- Locate the repository at this link [EasyShopping](https://github.com/SamAkinbile/Ecommerce)
- Navigate to the repository on GitHub and click on the "Fork" button in the top-right corner.
- This will create a copy of the repository under your GitHub account.

## Cloning this repository
To clone this repository follow the below steps: 

1. Locate the repository at this link [EasyShopping](https://github.com/SamAkinbile/Ecommerce). 
2. Under **'Code'**, see the different cloning options, HTTPS, SSH, and GitHub CLI. Click the prefered cloning option, and then copy the link provided. 
3. Open **Terminal**.
4. In Terminal, change the current working directory to the desired location of the cloned directory.
5. Type **'git clone'**, and then paste the URL copied from GitHub earlier. 
6. Type **'Enter'** to create the local clone. 
## Languages

- Python
- HTML5
- CSS3
- Javascript

## Frameworks - Libraries - Programs Used
- [Django](https://www.djangoproject.com/): Main python framework used in the development of this project
- [Django-allauth](https://django-allauth.readthedocs.io/en/latest/installation.html): authentication library used to create the user accounts
- [JQuery](https://jquery.com/)
- [PostgreSQL](https://www.postgresql.org/) was used as the database for this project.
- [SQLite](https://www.sqlite.org/index.html) - was used as the database during production.
- [Stripe](https://stripe.com/ie) used for the payments system.
- [AWS](https://aws.amazon.com/?nc2=h_lg) used for file storage.
- [Heroku](https://dashboard.heroku.com/login) - was used as the cloud based platform to deploy the site on.
- [Responsinator](http://www.responsinator.com/) - Used to verify responsiveness of website on different devices.
- [Balsamiq](https://balsamiq.com/) - Used to generate Wireframe images.
- [Chrome Dev Tools](https://developer.chrome.com/docs/devtools/) - Used for overall development and tweaking, including testing responsiveness and performance.
- [Font Awesome](https://fontawesome.com/) - Used for icons in information bar.
- [GitHub](https://github.com/) - Used for version control and agile tool.
- [Google Fonts](https://fonts.google.com/) - Used to import and alter fonts on the page.
- [W3C](https://www.w3.org/) - Used for HTML & CSS Validation.
- [Jshint](https://jshint.com/) - used to validate javascript
- [Coolors](https://coolors.co/) - Used to create colour palette.
- [Favicon](https://favicon.io/) - Used to create the favicon.
- [Lucidchart](https://lucid.app/documents#/dashboard) - used to create the database schema design
- [Grammerly](https://app.grammarly.com/) - used to proof read the README.md
- [Techsini](https://techsini.com/multi-mockup/index.php) - Site mockup generator
- [Crispy Forms](https://django-crispy-forms.readthedocs.io/en/latest/) used to manage Django Forms
- [Bootstrap 4.6](https://getbootstrap.com/docs/4.6/getting-started/introduction/): CSS Framework for developing responsiveness and styling
- [Hatchful](https://hatchful.shopify.com/): Used to generate custom logo
- [Tables Generator](https://www.tablesgenerator.com/markdown_tables): Used to convert excel testing tables to markdown
- [Sitemap Generator](www.xml-sitemaps.com): used to create sitemap.xml 
- [Privacy Policy Generator](https://www.privacypolicygenerator.info/): Used to create the site's privacy policy
- [Mailchimp](https://mailchimp.com/?currency=EUR): Used to create the newsletter signup functionality.


## Languages and Tools Used
- **Languages**: Python, HTML, CSS, JavaScript
- **Frameworks**: Django, Bootstrap
- **Database**: SQLite (Development), PostgreSQL (Production)
- **Deployment**: Heroku
- **Other Tools**: Django Crispy Forms, Django Allauth, Cloudinary for image storage

## Credits
- [W3Schools](https://www.w3schools.com/)
- [Django Docs](https://docs.djangoproject.com/en/4.0/)
- [Bootstrap 4.6 Docs](https://getbootstrap.com/docs/4.6/getting-started/introduction/)
- [Stack Overflow](https://stackoverflow.com/)
- [Pexels](https://www.pexels.com/): Imagery on the site was sourced from Pexels.com
- [Unsplashed](https://unsplash.com/): Imagery on the site was sourced from Unsplash
- [Code Institute - Boutique Ado Walkthrough Project](https://github.com/Code-Institute-Solutions/boutique_ado_v1)
- [Stack Overflow](https://stackoverflow.com/questions/19619428/html5-form-validation-pattern-alphanumeric-with-spaces): To prevent form being submitted with whitespace

## Acknowledgments
Though challenging project.