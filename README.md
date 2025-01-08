# skincare-app.
!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Skincare Info</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Skincare Info</h1>
  </header>
  <main>
    <section id="product-list">
      <h2>Daftar Produk Skincare</h2>
      <div id="products"></div>
    </section>
  </main>git init

  <footer>
    <p>&copy; 2025 Skincare App</p>
  </footer>
  <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0;
    background-color: #f9f9f9;
    color: #333;
  }
  
  header {
    background-color: #6db1bf;
    color: #fff;
    padding: 1rem;
    text-align: center;
  }
  
  main {
    padding: 1rem;
  }
  
  #product-list {
    margin: 2rem 0;
  }
  
  #products {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1rem;
  }
  
  .product-card {
    background: #fff;
    padding: 1rem;
    border: 1px solid #ddd;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  
  .product-card h3 {
    margin-top: 0;
    color: #6db1bf;
  }
  
  footer {
    text-align: center;
    padding: 1rem;
    background: #6db1bf;
    color: white;
  }
  const products = [
  {
    name: "Cleanser",
    description: "Membersihkan wajah dari kotoran dan minyak.",
    price: "Rp 100.000",
  },
  {
    name: "Toner",
    description: "Menghidrasi dan menyeimbangkan pH kulit.",
    price: "Rp 80.000",
  },
  {
    name: "Serum Vitamin C",
    description: "Mencerahkan kulit dan mengurangi noda hitam.",
    price: "Rp 150.000",
  },
  {
    name: "Moisturizer",
    description: "Mengunci kelembapan dan menjaga kulit tetap sehat.",
    price: "Rp 120.000",
  },
];

function displayProducts() {
  const productContainer = document.getElementById("products");
  products.forEach((product) => {
    const productCard = document.createElement("div");
    productCard.className = "product-card";
    productCard.innerHTML = `
      <h3>${product.name}</h3>
      <p>${product.description}</p>
      <p><strong>${product.price}</strong></p>
    `;
    productContainer.appendChild(productCard);
  });
}

// Load products on page load
document.addEventListener("DOMContentLoaded", displayProducts);
  
