# SmartReco AI – real store + price comparison
Run: `npm install && SERPAPI_KEY=your_key npm start`  ->  http://localhost:3000

- Auth: signup/login/logout, bcrypt hashes, httpOnly JWT cookie, rate-limited, change password
- Store: SQLite catalog with stock, search ("headphones under 25000"), ranking by saved interests/budget
- Cart, wishlist, orders (Cash on Delivery, stock-checked in a transaction), order history
- Price compare: Our Store vs Amazon/Flipkart/others via SerpApi (cached 6h). Without a key it shows real
  Amazon/Flipkart search links with NO prices (nothing is faked).
- "Buy on Amazon/Flipkart" -> /go/:product/:retailer -> logs the click, redirects to the retailer (affiliate tag if set)
- Add products: insert rows into the `products` table (sqlite3 store.db) or extend the seed list in server.js.
