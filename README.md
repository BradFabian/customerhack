# customerhack 
An highly customized saas app that will allow ecommerce brands to have one place to service and view a customers journey. Allow for business specific customization, intergate with an erp, 3pl, PLM, social media, shopify, bigcommerce or weecommerce. This app will allow companies to gather cutsomer information from all touch points of their businesses to create an streamlined wholistic view of their customers journey.

## Pricing Tiers 
More to come

## General Dashboard
- Search funciton to bring up customer, order, product , shipping information
- List All Current Customer cases
- List All active promotions
- List All Products / prices / inventory
- Allow Wismo
- Current appeasment coupons / descriptions
- Escalation contact sheet
- quick view of active support issues
- Top selling highly reveiwed products for upsell
## Ticket Management 
- Create a ticket
- List tickets
- Delete a ticket
- Retrieve a ticket
- Update a ticket
- Add ticket tags
- Remove ticket tags
- List ticket tags
- Set ticket tags
- Delete ticket field value
- Update ticket field value
- List ticket field values
- Update ticket fields values

## Customer Profiles

- List all customers in the database
  - Pagination
  - Select specific fields in result
  - Limit number of results
  - Filter by fields
- Tag Customers
  - High Value
  - Low Value
  - Waiting on order
  - Already-shipped
  - Sentiments/menacing
  - Sentiments/need-human
  - Sentiments/negative
  - Sentiments/offensive
  - Sentiments/positive
  - Sentiments/urgent
- Search customers by first name,last name, email, phone number, order number
  - integrate search to mongdb / ecommerce platforms
- Get single customer
- Create new customer profile
  - Authenticated users only
  - Must have role of "agent", "Manager" or "admin"
  - Field validation via Mongoose
- Update Customer profile
   - Validation on update
- Delete Profile & User
  - Manager only
- View Order History
  - role of "agent" or "manager"
- Update Order History
   - role of "Manager"
- Create Customer Notes
  - role of "agent" or "manager"
  - time stamped
- Update Customer Notes
  - role of "agent" or "manager"
  - time stamped
- Delete Customer Notes
  - time stamped
- Create Gift Card
  - role of "agent" or "manager"
  - time stamped
- Update Gift Card
  - role of "agent" or "manager"
  - time stamped
- View Assigned Tickets
- update Assigned Tickets
  


### Orders

- List all Order associated to a customer
- List all Orders in general
  - Pagination, filtering, etc
- Get single Order
- Update Order
  - admin only
- Delete show
  - admin only
- Apply Upsell and Promotion
- Create Order Notes
  - role of "agent" or "manager"
  - time stamped
- Update Order Notes
  - role of "agent" or "manager"
  - time stamped
- Delete Order Notes
  - time stamped


## Products

- List all products by customer
- List all products in general
  - Pagination, filtering, etc
- Get a single product
- Allow Product Tagging for To sellers, High Upsell value, Recalls, Issues


## Users & Authentication

- Authentication will be ton using JWT/cookies
  - JWT and cookie should expire in 30 days
- User registration
  - Register as a "user" or "publisher"
  - Once registered, a token will be sent along with a cookie (token = xxx)
  - Passwords must be hashed
- User login
  - User can login with email and password
  - Plain text password will compare with stored hashed password.
  - Once logged in, a token will be sent along with a cookie (token = xxx)
- User logout
  - Cookie will be sent to set token = none
- Get user
  - Route to get the currently logged in user (via token)
- Password reset (lost password)
  - User can request to reset password
  - A hashed token will be emailed to the users registered email address
  - A put request can be made to the generated url to reset password
  - The token will expire after 10 minutes
- Update user info
  - Authenticated user only
  - Separate route to update password
- User CRUD
  - Admin only
- Users can only be made admin by updating the database field manually

## Security

- Encrypt passwords and reset tokens
- Prevent NoSQL injections
- Add headers for security (helmet)
- Prevent cross site scripting - XSS
- Add a rate limit for requests of 100 requests per 10 minutes
- Protect against http param polution
- Use cors to make API public (for now)

## Documentation

- Use Postman to create documentation
- Use docgen to create HTML files from Postman
- Add html files as the / route for the api

# Technical Environment
### Front End
NextJS, Tailwind & Algolia

### BDD Testing 
Cucumber, Gherkin

### Back End
Node JS Express MongoDb 



# Serverless Deployment (Digital Ocean or AWS)

- More info to come

# Code Related Suggestions

- NPM scripts for dev and production env
- Config file for important constants
- Use controller methods with documented descriptions/routes
- Error handling middleware
- Authentication middleware for protecting routes and setting user roles
- Validation using Mongoose and no external libraries
- Use async/await (create middleware to clean up controller methods)
- Create a database seeder to import and destroy data

## Future Features and Intergrations Partners
TBD


