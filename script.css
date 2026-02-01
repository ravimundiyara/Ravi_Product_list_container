const products = [
  { name: "Smartphone", price: 15000, rating: 4.5, category: "Electronics" },
  { name: "Laptop", price: 55000, rating: 4.7, category: "Electronics" },
  { name: "Headphones", price: 2000, rating: 4.2, category: "Electronics" },
  { name: "Smartwatch", price: 4000, rating: 4.1, category: "Electronics" },
  { name: "Camera", price: 30000, rating: 4.6, category: "Electronics" },

  { name: "T-Shirt", price: 600, rating: 4.0, category: "Clothing" },
  { name: "Jeans", price: 1200, rating: 4.3, category: "Clothing" },
  { name: "Jacket", price: 2500, rating: 4.4, category: "Clothing" },
  { name: "Shoes", price: 3000, rating: 4.5, category: "Clothing" },
  { name: "Cap", price: 400, rating: 3.9, category: "Clothing" },

  { name: "JavaScript Book", price: 700, rating: 4.8, category: "Books" },
  { name: "HTML Guide", price: 500, rating: 4.2, category: "Books" },
  { name: "CSS Mastery", price: 650, rating: 4.4, category: "Books" },
  { name: "DSA Handbook", price: 900, rating: 4.6, category: "Books" },
  { name: "AI Basics", price: 800, rating: 4.5, category: "Books" },

  { name: "Chair", price: 2200, rating: 4.1, category: "Home" },
  { name: "Table", price: 4500, rating: 4.3, category: "Home" },
  { name: "Lamp", price: 900, rating: 4.0, category: "Home" },
  { name: "Curtains", price: 1500, rating: 4.2, category: "Home" },
  { name: "Wall Clock", price: 1200, rating: 4.4, category: "Home" }
];

const productContainer = document.getElementById("productContainer");
const sortSelect = document.getElementById("sortSelect");
const categorySelect = document.getElementById("categorySelect");

function displayProducts(list) {
  productContainer.innerHTML = "";

  list.forEach(product => {
    const card = document.createElement("div");
    card.className = "product-card";

    card.innerHTML = `
      <h3>${product.name}</h3>
      <p><strong>Price:</strong> ₹${product.price}</p>
      <p><strong>Rating:</strong> ${product.rating}</p>
      <p><strong>Category:</strong> ${product.category}</p>
    `;

    productContainer.appendChild(card);
  });
}

function applyFilterAndSort() {
  let filteredProducts = [...products];

  const category = categorySelect.value;
  if (category !== "all") {
    filteredProducts = filteredProducts.filter(
      product => product.category === category
    );
  }

  const sortValue = sortSelect.value;

  if (sortValue === "price-asc") {
    filteredProducts.sort((a, b) => a.price - b.price);
  } else if (sortValue === "price-desc") {
    filteredProducts.sort((a, b) => b.price - a.price);
  } else if (sortValue === "name-asc") {
    filteredProducts.sort((a, b) => a.name.localeCompare(b.name));
  } else if (sortValue === "name-desc") {
    filteredProducts.sort((a, b) => b.name.localeCompare(a.name));
  } else if (sortValue === "rating-asc") {
    filteredProducts.sort((a, b) => a.rating - b.rating);
  } else if (sortValue === "rating-desc") {
    filteredProducts.sort((a, b) => b.rating - a.rating);
  }

  displayProducts(filteredProducts);
}

sortSelect.addEventListener("change", applyFilterAndSort);
categorySelect.addEventListener("change", applyFilterAndSort);

displayProducts(products);
