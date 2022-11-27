# Food-Delivery-Backend

## [Deployed URL](https://food-app-api.onrender.com)

## [Frontend Source_code](https://github.com/SaiPraneethPegada/Food-Delivery-Frontend.git)

## API End-Points:

| Method | End point | Description |
| ---- | ---- | ---- |
| POST | /users/signup | Signup requirements -> First Name, Last Name, email(unregistered), password and role(admin or user). |
| POST | /users/login | Login credential requirements -> email and password |

> After successful User login:

| Method | End point | Description |
| ---- | ---- | ---- |
| GET | /all-food | Fetches all the food Items which are added by Admin. |
| POST | /order | User selects min 1 food-item and enters their delivery address to proceed for payment. |
| POST | /payment/verify | If razor pay signature matches with crypto generated signature then selected food order will be placed. |
| GET | /orders/:id | Successful order will have unique ID , will fetch single order details by the id. |
| GET | /ordersByUser/:id | Will fetch all the orders placed by the registered user. |

> After successful Admin login (Only Admin will have access to below API End-points):

| Method | End point | Description |
| ---- | ---- | ---- |
| POST | /add-food | Food requirements -> Food Name, Price, Description, Image URL.  |
| DELETE | /delete-food/:id | Food item can be deleted with unique food ID. |
| PUT | /order-status/:id | Order status update : Ordered -> Placed -> In-Transit -> Delivered. |
| GET | /orders | Fetches all the orders from all the users. |
