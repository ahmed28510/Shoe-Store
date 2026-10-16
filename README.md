# 👟 Shoe Store

A responsive shoe catalog website where users can browse shoes and filter them by **brand, color, size and price**. Built with plain HTML, CSS, Bootstrap 5 and vanilla JavaScript — no frameworks, no backend.

## ✨ Features

- **36 shoes** across 3 brands: Adidas, Nike and Puma
- **Four filters** that work together:
  - **Brand** — Adidas, Nike, Puma
  - **Color** — Black, White, Brown
  - **Size** — Small, Medium, Large, X-Large
  - **Price** — $0–$99, $100–$199, $200–$299, $300+
- **Combine filters** — e.g. *Nike + Black + Large* shows only shoes matching all three
- **Dynamic cards** — product cards are generated with JavaScript from a single data array
- **"No shoes found" message** when nothing matches the selected filters
- **Responsive layout** — 1 card per row on phones, 2 on tablets, 3–4 on desktops
- **Uniform card images** — every image is cropped to the same height so the grid stays neat

## 🛠️ Built With

| Technology | Used for |
|---|---|
| HTML5 | Page structure |
| CSS3 | Custom styling (`style.css`) |
| Bootstrap 5.3 | Navbar, grid, cards, dropdowns |
| JavaScript (ES6) | Rendering cards and filtering |

## 📁 Project Structure

```
Shoes-prodect/
├── index.html          # Main page (navbar, filters, shoe container)
├── style.css           # Custom styles
├── js/
│   └── script.js       # Shoe data, rendering and filter logic
└── assets/
    ├── logo.png        # Store logo / favicon
    ├── adidas/         # Adidas shoe images
    ├── nike/           # Nike shoe images
    └── puma/           # Puma shoe images
```

## 🚀 How to Run

No installation needed.

1. Download or clone the repository:
   ```bash
   git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
   ```
2. Open the project folder.
3. Double-click `index.html` to open it in your browser.

## 🔍 How It Works

1. All shoes are stored in a `shoes` array in `js/script.js`. Each shoe looks like this:
   ```js
   {
     name: "Adidas Campus",
     brand: "adidas",
     price: 65,
     color: "black",
     size: "small",
     image: "./assets/adidas/adidas-black-shoes-1.jpeg",
   }
   ```
2. `randershoes()` loops through a list of shoes and builds a Bootstrap card for each one.
3. When the user clicks **Search**, `searchProducts()` reads the four dropdown values, keeps only the shoes that match every selected filter, and re-renders the cards.
4. Choosing **All** in a dropdown means "don't filter by this option".

### Adding a new shoe

Add one more object to the `shoes` array and put its image in the matching `assets/` folder. Use lowercase values (`"nike"`, `"black"`, `"large"`) so the filters can match it, and a number for the price.

## ⚠️ Limitations

- **Static data** — shoes live in a JavaScript array; there is no database or backend, so products can't be added or edited from the website itself.
- **No shopping features** — there is no cart, checkout, login or payment.
- **Manual search** — results update only when the **Search** button is clicked, not when a dropdown changes.
- **Fixed filter options** — only the brands, colors, sizes and price ranges listed above are supported. Adding a new option means editing both `index.html` and `script.js`.
- **No text search or sorting** — you can't search by name or sort by price.
- **Size is a label** — sizes are Small/Medium/Large/X-Large, not real shoe sizes (e.g. UK 8, EU 42).
- **Prices are in USD only** and are sample values.
- **Needs internet for styling** — Bootstrap is loaded from a CDN, so the page looks unstyled when opened offline.
- **Images** — product images are loaded locally, so the `assets/` folder must be kept next to `index.html`.

## 🔮 Future Improvements

- Filter automatically when a dropdown changes
- Search by shoe name and sort by price
- Add-to-cart and a favorites list
- Real shoe sizes (UK / US / EU)
- Load products from an API or JSON file

## 📚 What I Learned

- Building a responsive layout with Bootstrap's grid and cards
- Rendering HTML dynamically from a JavaScript array
- Filtering data with `filter()` and combining multiple conditions
- Handling button events without reloading the page

## 👤 Author

**Ahmed Ghufran** — Karachi, Pakistan

Created as a web development assignment for the Saylani Modern Web and App Development course.
