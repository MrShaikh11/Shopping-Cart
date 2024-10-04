# Shopping Cart with Redux Toolkit

This project is a shopping cart application built using **React**, **Redux Toolkit**, and **Axios**. It features full state management for adding, removing, and managing cart items, as well as fetching product data from an API.

## Features

- **Add to Cart**: Users can add products to the cart, with a notification using `react-toastify`.
- **Remove from Cart**: Remove products from the cart with a notification.
- **Update Cart Quantity**: Adjust product quantities directly within the cart.
- **Cart Total Calculation**: Automatically calculates the total amount and quantity of the cart items.
- **Product Fetching**: Fetches products from an external API using `axios` and `redux-thunk`.
- **Local Storage Persistence**: Cart data persists in `localStorage` across sessions.

## Technologies Used

- **React**: Frontend library for building user interfaces.
- **Redux Toolkit**: For managing global application state.
- **Axios**: For making HTTP requests to the API.
- **React Router DOM**: For client-side routing.
- **React Toastify**: For toast notifications to improve user experience.

## Project Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/shopping-cart.git
   ```
2. Navigate into the project directory:
   cd shopping-cart
3. Install dependencies:
   npm install
4. Start the development server:
   npm start

The application should now be running at http://localhost:3000.

## API

This project interacts with a custom API to fetch product data. The API is expected to be running on `http://localhost:5000`.

- **Get All Products**: Fetches a list of products from the API.

## Code Explanation

### Cart Slice (`cartSlice.js`)

- **State**: The cart slice manages cart items, total quantity, and total amount.
- **Reducers**:
  - `addToCart`: Adds an item to the cart or increases its quantity if it’s already present.
  - `removeFromCart`: Removes an item from the cart.
  - `decreaseCart`: Decreases the quantity of an item in the cart or removes it if the quantity is 1.
  - `clearCart`: Clears all items from the cart.
  - `getTotal`: Calculates the total price and quantity of the cart.

### Product Slice (`productSlice.js`)

- **State**: Manages the list of products and the fetching status (`idle`, `pending`, `success`, `rejected`).
- **Thunks**:
  - `productsFetch`: Asynchronous thunk that fetches product data from the API using `axios`.

## Acknowledgements

This project was developed following a tutorial by **Chaoo Charles**, which helped in setting up the cart functionality and API integration. You can watch the course [here](https://www.youtube.com/playlist?list=PL63c_Ws9ecIRnNHCSqmIzfsMAYZrN71L6).

## License

This project is licensed under the MIT License.
