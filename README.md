<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Add Items with Price</title>
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      background-color: #f9f9f9;
      margin: 0;
      padding: 20px;
    }
    h1 {
      text-align: center;
      color: #2196f3;
    }
    .form-container {
      max-width: 400px;
      margin: 0 auto;
      background: white;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    input {
      width: 100%;
      padding: 10px;
      margin: 8px 0;
      border: 1px solid #ccc;
      border-radius: 8px;
    }
    button {
      width: 100%;
      padding: 10px;
      background-color: #e91e63;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-weight: bold;
    }
    button:hover {
      background-color: #d81b60;
    }
    ul {
      list-style: none;
      padding: 0;
      margin-top: 20px;
    }
    li {
      background: #fff;
      margin: 8px 0;
      padding: 12px;
      border-radius: 8px;
      display: flex;
      justify-content: space-between;
      box-shadow: 0 1px 3px rgba(0,0,0,0.1);
    }
    .price {
      color: #2196f3;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>Item List</h1>
  <div class="form-container">
    <input type="text" id="itemName" placeholder="Enter item name">
    <input type="number" id="itemPrice" placeholder="Enter price">
    <button onclick="addItem()">Add Item</button>
    <ul id="itemList"></ul>
  </div>

  <script>
    function addItem() {
      const name = document.getElementById('itemName').value;
      const price = document.getElementById('itemPrice').value;

      if (name && price) {
        const li = document.createElement('li');
        li.innerHTML = `<span>${name}</span> <span class="price">₹${price}</span>`;
        document.getElementById('itemList').appendChild(li);

        // Clear inputs
        document.getElementById('itemName').value = '';
        document.getElementById('itemPrice').value = '';
      } else {
        alert("Please enter both item name and price!");
      }
    }
  </script>
</body>
</html>
