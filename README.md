# T3A2 Full Stack App

# Sakura Pantry - Japanese Online Grocery Store

## Resources

- [Production site](https://www.google.com.au/)
- [Back-end repo](https://github.com/irene2mana-T3A2-2023/SakuraPantryServer)
- [Front-end repo](https://github.com/irene2mana-T3A2-2023/SakuraPantryClient)
- [Trello board](https://trello.com/b/TE5Q9ZYj/t3a2-%F0%9F%8C%B8sakura-pantry)

## Contributors

- [Mana Misumi](https://github.com/Mana12011207)
- [Irene Nguyen](https://github.com/irenenguyen1017)
- [Ellen Pham](https://github.com/ellenpham)

# R1 - Website description

## Purpose

We were approached by the owner of Sakura Company, a Japanese food wholesaler, to create an online store for Japanese food products.

The web app serves three main purposes:

- To promote and increase access to Japanese food.
- To provide a service to the Japanese community in Australia and to those who love Japanese food products.
- To contribute to business and sales growth for the client, Sakura Company.

### Problem

Prior to having the website, the primary means of obtaining Japanese food was through Japanese supermarkets, mainly located in central areas. This posed geographical constraints for those living in the suburbs. Moreover, limited store numbers and early closing times, often by 5pm, made it challenging for full-time workers to visit. Setting up a physical shop also presented a significant hurdle for Sakura Company, especially with rising rents due to recent unforeseen inflation.

### Solution

The launch of Sakura Pantry is envisioned to address these challenges. Sakura Pantry is an easy-to-use platform for purchasing Japanese food products, accessible to both city dwellers and those in the suburbs, operating 24/7. Unrestricted by the number of shops or closing times, it offers the convenience of online shopping, catering to the busy full-time workforce. By avoiding the need for physical shops, it provides a more cost-efficient means for Sakura Company to offer Japanese food products. In doing so, Sakura Pantry introduces a modern solution to access Japanese food ingredients in response to contemporary demands.

## Functionality/Features

The overall function of the website is to operate as an online store for selling Japanese food products. Below are the MVP features and functionality for the current stage of product development.

### MVP Features

- User authentication and authorisation (Register and Login)
  - Allow users to create account and login.
- Password recovery
  - Allow users to reset password with reset link sent via email.
- Site navigation and responsive design
  - Intuitive and responsive UX/UI design for storefront to attract and engage audience.  
- Search functionality
  - Allow users to search products by keywords.
- Product catalogue
  - Showcase of new arrivals and featured products.
  - Display a list of products when filtered by categories.
- Product details
  - Detailed information about each product, including product descriptions and product stock status.
- Shopping cart
  - Allow users to add products to cart, view items in cart and increase, decrease or remove items from cart.
- Checkout process
  - Allow users to fill out details of delivery and billing information.
- Contact form
  - Allow users to send their enquiries.
- User account view
  - View user profile
  - Change password
  - View order history
- Admin dashboard:
  - Summary view: allow admins to view total users, total products, total orders and total revenue.
  - User management
  - Category management
  - Product management
  - Order management

### MVP Functionality

#### Users

- Guest users without authentication can view products.
- Guest users can add products to cart and will be prompted to register or log in if they wish to proceed to payment.
- Guest users without authentication can Create account to become authenticated users.
- Users with authentication can perform Read operation on their personal account information.
- Users with authentication can perform Create, Read operations on product orders.

#### Admins

- Admins can perform Read operation on users' information.
- Admins can perform CRUD operations on products.
- Admins can perform CRUD operations on product categories.
- Admins can perform Read and Update operations on orders.

### Possible extensions

#### Nice-to-have features

- Sign-up confirmation via email
- Saved login details
- Secure logout
- Calculation for different delivery options
- Billing services/Payment integration
- Order confirmation via email

#### Nice-to-have functionality

- Update and Deactivate operations on user account details for users with authentication.
- Update and Deactivate operations on user account details for admins.

## Target Audience

The app targets shoppers across Australia who are looking for unique and quality Japanese food products, including:

- Japanese people residing in Australia
- Japanese food products lovers

## Tech Stack

The core tech stack is MERN stack.

- Application:
  - Back-end API: NodeJS, ExpressJS, Mongoose
  - Front-end: HTML, CSS, JavaScript, ReactJS, Axios, Tailwind, NextUI
- Database:
  - MongoDB, MongoDB Atlas
- Testing:
  - Jest, Supertest
- Deployment:
  - Back-end API: Heroku
  - Front-end: Netlify
- DevOps:
  - Git
  - GitHub
  - VS Code
- Project Management:
  - Trello
  - Discord
  - Skype
- Design Tools:
  - Draw.io
  - Miro

# R2 - Dataflow Diagram and Sitemap

## Website Sitemap

![Sitemap](./docs/images/sitemap/sitemap.png)

## Dataflow Diagram

![Dataflow Diagram](./docs/images/DFD/Dataflow_Diagram.png)

### Data description

```
User details:
_id
firstName: String
lastName: String
email: String
password: String (hashed)
phone: String
role: String
isActive: Boolean
dateCreated: Date
resetPasswordToken: String (encrypted)
resetPasswordExpires: Boolean
address : {street: String, city: String, state: String, postcode: String}

Product details:
_id
name: String
description: String
price: String
categoryId: referencing _id from Categories collection
stockQuantity: Number
image: String (URL)
productSlug: String

Category details:
_id
name: String
categorySlug: String

Order details:
_id
userId: referencing _id from Categories
products: [{productId: referencing _id from Products, quantity: Number}]
totalPrice: Number
orderDate: Date
status: String
```

# R3 - Application Architecture Diagram

![Application-Architecture-Diagram](./docs/images/AAD/application_architecture_diagram.png)

# R4 - User Stories

We constructed user stories and personas to improve the online store's user experience for Japanese food products. The process involves identifying and embodying customers' unique needs and expectations, including a system administrator at Sakura company.

## Initial Market Research

1. As a busy parent, I want search functionality with a category filtering option to save time searching for the right product.

2. As a busy parent, I want a contact form 24/7 to quickly ask questions or queries about products and services in the online shop, regardless of time or location.

3. As a user, I want to be able to search products by keywords, which allows me to find specific pantry items effortlessly. This will save me time and ensure that I quickly locate the products I'm looking for.

4. As a user, I want a password recovery feature. As I do online shopping daily, I often forget my passwords.

5. As a user, I want a website with a responsive design. I use my smartphone to access websites, search for products and browse information. If a website supports responsive design, the information is organised and intuitive without forcing me to scroll or zoom.

6. As a user, I expect a shopping cart feature on the online shop. The shopping cart allows me to manage several products I purchase at once and shop efficiently, including changing quantities and deleting items.

7. As a user, I expect to see my order history. I can see which products I have purchased and how much I have paid for them, which will help me with my next order.

8. As a user, I want a navigation bar on the online shop. The navigation bar allows me to explore the entire site efficiently and provides easy access to site contents.

9. As a user who loves new discoveries, I want a new arrivals section to give me new suggestions on Japanese products I might enjoy. 

10. As a cooking enthusiast, I want to have an intuitive platform where I can enjoy browsing the different ingredients and products exclusive to Japan.

11. As a non-Japanese user who needs help understanding the Japanese language, I want a website with the products translated into English to understand the product details better.

12. As an administrator, I want to capture store analytics data to inform our development strategy, so I can ensure our resources are effectively aligned with business growth.

13. As an administrator, I want the ability to perform CRUD operations on products and product categories, which will enable me to manage product inventory efficiently and maintain accurate stock listings.

## Follow Up Market (nice to have)

1. As a user, I expect to receive a sign-up confirmation email after the sign-up is complete. This will prevent any unauthorised use of my account.

2. As a user, I want saved login credentials for easy access.

3. As a parent, I need secure logout to prevent accidental purchases from children. 

4. As a user, I expect to be able to choose different delivery options. I can compare different delivery options and choose the best option according to delivery time and price.

5. As a user, I want order confirmation emails to record my order history so I can keep track of stock levels in my pantry. 

6. As a user who often changes residence, I need to easily update my profile to ensure accurate delivery despite frequent changes in residence.

7. As an administrator, I want the ability to efficiently manage users by CRUD performing their information and assisting with account-related matters.

## User Personas

Shizuka finds it challenging to travel to supermarkets where authentic Japanese food products are available whilst caring for her three children. Given the demands of raising her children, she is also looking for ways to save time when shopping for her daily food.

![Shizuka_Kagami](./docs/images/user_personas/Shizuka_Kagami.png)

Ronnie, a user who has recently become addicted to Japanese food, faces difficulties in finding Japanese food products locally. Ronnie seeks a platform that helps discover the latest Japanese food arrivals and is also user-friendly, providing easy access to essential information.

![Ronnie_Campbell](./docs/images/user_personas/Ronnie_Campbell.png)

Not everyone know about the website before stumbling on it while browsing the internet, Jinny is one of those people. She is among numerous random shoppers, who are the potential users of the website. As a first-time user, she expects the design and layout of the website to be appealing and memorable, easy and clear navigation to make her first shopping experience effortless and seamless. This would make her come back to shop the next time. Also, she would love to know the popular products with description in English and recommended list of products that go together to gather ideas for her cooking recipes.

![Jinny_Chang](./docs/images/user_personas/Jinny_Chang.png)

The final user persona focuses on Lara, a system administrator at Sakura Company. She aims to ensure efficient operations and deliver the best user experience. A reliable user database and product inventory management are essential to achieve this goal. The system is expected to be intuitive, easy to understand, and provide easy access to crucial features.

![Lara_Macintosh](./docs/images/user_personas/Lara_Macintosh.png)

# R5 - Wireframes

Miro was used to design and plan wireframes for features of the application. Our web application adopts a consistent structure across all pages, which is divided into three main parts: the header, the body, and the footer.

## Page structure overview

**Header** is a persistent component that appears at the top of every page. It contains the following elements:

- **Logo**: Our company logo is placed prominently in the header, typically in the top left corner. Clicking the logo will always redirect users to the homepage.
- **Search bar**: Central to the header is a search bar that allows users to search for products by entering keywords. Additionally, users have the option to filter their search by categories to refine their results.
- **Sign in/Sign up Links**: To the right of the search bar, users can find links to 'sign-in' or 'sign-up'. These are provided for easy navigation to authentication pages for user account management.
- **Cart Icon**: An icon representing the shopping cart is also present. This icon displays a count of the number of products currently in the user's cart, offering users a quick view of their potential purchases.

**Body** is the central part of each page and is dynamic. Its layout and content will change to align with the specific purpose of the page. For instance, the body on the product details page will contain images and descriptions of products, while on the checkout page, it will display a form for payment information.

**Footer**, like the header, is a static component displayed at the bottom of every page (except the admin dashboard page). It typically contains company information, a contact form, and direct links to the company's social media profiles, such as Facebook and Instagram.

## Wireframe Breakpoint Range

In the context of responsive design, our project utilizes a set of predefined breakpoints to ensure optimal display across various devices. These breakpoints are crucial for the wireframe part of the project as they guide the layout and scaling of content.

- **Desktop screens**: Defined as screens with a width of `1024 pixels or greater`. Our design is tailored to accommodate a wide range of desktop displays, ensuring full functionality and aesthetic integrity on larger screens.
- **Tablet screens**: These are screens that fall `within the range of 768 pixels to 1023 pixels wide`. The design adjusts between these widths to provide a user-friendly experience on tablet devices, balancing touch interaction with readability.
- **Mobile screens**: Classified as any screen with a width of `less than 768 pixels`. Our mobile design prioritizes accessibility and navigability, recognizing the constraints and advantages of smaller touch screens.

For an in-depth look at our wireframe designs, please see the [Wireframe](https://miro.com/app/board/uXjVNNmFIuE=/)

### Homepage

The homepage includes a hero banner, a section for new arrivals, and a section for featured products, all with a sliding effect for seamless responsive design. The layout is minimal yet effective, enabling easy navigation and enhancing the shopping experience from the first interaction.

![Home page](./docs/images/wireframes/homepage.png)

### Sign-in page

The Sign-in page is accessible to all visitors, allowing them to log into the website. Additionally, this page offers links that guide new users to the Sign-up page and provides a redirect to the Forgot Password page for users who need to recover their login credentials.

![Sign-in page](./docs/images/wireframes/sign-in-page.png)

### Sign up page

The Sign-up page enables new visitors to create an account and includes a link for existing users to return to the Sign-in page.

![Sign-up page](./docs/images/wireframes/sign-up-page.png)

### Forgot password page

Users will be directed to the Forgot Password page after clicking the 'Forgot Password' link. They are required to enter their email address and click the 'Send' button to receive a link for resetting their password.

![Forgot Password page](./docs/images/wireframes/forgot-password-page.png)

### Reset password page

Upon clicking the reset password link received via email, users will be prompted to a page where they can establish a new password.

![Reset Password page](./docs/images/wireframes/set-new-password-page.png)

### Search page

The search bar allows users to search for products using keywords or filter products by categories using the drop-down menu. The matching results will be displayed on the search results page.

![Search page](./docs/images/wireframes/search-page.png)

### Product details page

Clicking on a product image or name will direct users to the Product Details page, where they can find more information about the product, view the stock quantity, and increase or decrease the number of items before adding it to their cart

![Product Details page](./docs/images/wireframes/product-details-page.png)

### Shopping cart page

When users click the cart icon in the header, they will be prompted to the Cart page. Here, they can view all the products they have added and can choose to proceed with their purchase by clicking the 'Proceed to checkout' button or continue shopping by clicking the 'Continue shopping' button.

![Shopping Cart Page](./docs/images/wireframes/shopping-cart-page.png)

### Checkout page

Users intent on proceeding to payment must log in or register an account to be taken to the Checkout page after selecting the 'Proceed to Checkout' button on the cart page. They are required to provide delivery address details and credit card information, and must review and confirm the order summary to finalize the payment process.

![Checkout Page](./docs/images/wireframes/checkout-page.png)

### User account page

Authenticated users have access to their personal accounts where they can view their profiles and purchase history. Additionally, they have the option to change their current password in this section.

![User Account Page](./docs/images/wireframes/user-account-page.png)

### Admin dashboard page

The admin dashboard has four pages, which are structured as tabs:

- **Summary**: This tab provides an overview of the business's key metrics, such as the total number of products, orders, and registered users, all consolidated on a single summary screen.
- **Products**: This crucial section is the heart of product management within the admin dashboard, and the admin has the authority to view the entire list of products, add new products, edit existing product details, or remove products from the listing.
- **Categories**: Similar to the Products tab, this section empowers the admin to manage product categories. Here, the admin can view all existing categories, add new categories, update information on current categories, or remove categories as needed. This ensures that the product catalog remains well-organized and easy to navigate.
- **Users**: This tab enables the admin to review the list of all registered users on the platform.
- **Orders**: In this section, the admin is able to overview the list of all orders, and update the status of these orders.
  
![Admin Dashboard Page](docs/images/wireframes/admin-dashboard-page.png)

# R6 - Tasks planning and tracking

View the description of the way tasks are allocated and tracked in the project [here](./task_tracking.md).

Link to project management tool [Trello](https://trello.com/b/TE5Q9ZYj/t3a2-%F0%9F%8C%B8sakura-pantry).
