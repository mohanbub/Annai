<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Foodie</title>
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      margin: 0;
      background-color: #f9f9f9;
      color: #000;
    }
    header {
      background-color: #2196f3; /* Blue */
      color: white;
      padding: 16px;
      text-align: center;
      font-weight: bold;
    }
    .search-box {
      padding: 12px;
    }
    .search-box input {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 12px;
    }
    .restaurant-card {
      background: white;
      margin: 12px;
      padding: 12px;
      border-radius: 12px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .restaurant-info {
      flex-grow: 1;
      margin-left: 12px;
    }
    .restaurant-info h3 {
      margin: 0;
      font-weight: bold;
      color: #2196f3;
    }
    .restaurant-info p {
      margin: 4px 0 0;
      color: #555;
    }
    .order-btn {
      background-color: #e91e63; /* Pink */
      color: white;
      border: none;
      padding: 8px 16px;
      border-radius: 8px;
      cursor: pointer;
    }
    .order-btn:hover {
      background-color: #d81b60;
    }
  </style>
</head>
<body>
  <header>Discover Restaurants</header>

  <div class="search-box">
    <input type="text" placeholder="Search for food or restaurants">
  </div>

  <div class="restaurant-card">
    <span>🍴</span>
    <div class="restaurant-info">
      <h3>Spicy Hub</h3>
      <p>⭐ 4.5 • 30 min delivery</p>
    </div>
    <button class="order-btn">Order</button>
  </div>

  <div class="restaurant-card">
    <span>🍴</span>
    <div class="restaurant-info">
      <h3>Pizza Palace</h3>
      <p>⭐ 4.2 • 25 min delivery</p>
    </div>
    <button class="order-btn">Order</button>
  </div>

  <div class="restaurant-card">
    <span>🍴</span>
    <div class="restaurant-info">
      <h3>Veggie Delight</h3>
      <p>⭐ 4.8 • 20 min delivery</p>
    </div>
    <button class="order-btn">Order</button>
  </div>
</body>
</html>
