# Bookstore Project Notes

## 1. Project Overview
This project is a simple online bookstore website built using HTML and CSS. It has a framed layout where the top navigation bar, left sidebar, main content area, and footer are loaded from separate files. The website includes pages like Home, Login, Register, Catalogue, and Cart.

The main purpose of this project is to present a basic bookstore interface where users can browse books and navigate between different sections.

---

## 2. Project Structure
- `index.html` – main page that defines the overall layout using frames
- `top.html` – header and navigation bar
- `left.html` – left-side category menu
- `right.html` – default content area
- `home.html` – home page content
- `catalogue.html` – list of books with prices and add-to-cart buttons
- `cse.html` – CSE books page
- `ece.html` – ECE books page
- `mech.html` – Mechanical books page
- `login.html` – login form page
- `register.html` – registration form page
- `cart.html` – shopping cart page
- `footer.html` – creator details
- `style.css` – styling file for the full website

---

## 3. Important Code Snippets and Meaning

### 3.1 Main Layout in `index.html`
```html
<frameset rows="20%,*,7%">
```
This divides the page into three horizontal sections:
- top area
- middle area
- footer area

```html
<frameset cols="25%,*">
```
This divides the middle section into:
- left sidebar
- main content area

```html
<frame src="top.html" name="topFrame" scrolling="no" noresize>
```
This loads the top navigation bar into the top frame.

```html
<frame src="left.html" name="leftFrame">
```
This loads the category menu into the left frame.

```html
<frame src="right.html" name="rightFrame">
```
This loads the main content into the right frame.

---

### 3.2 Linking CSS
```html
<link rel="stylesheet" href="style.css">
```
This connects each HTML page to the CSS file so all pages use the same design.

**Meaning:**
- `rel="stylesheet"` tells the browser it is a stylesheet
- `href="style.css"` points to the CSS file

---

### 3.3 Navigation Bar in `top.html`
```html
<nav>
  <a href="home.html" target="rightFrame">Home</a>
  <a href="login.html" target="rightFrame">Login</a>
  <a href="register.html" target="rightFrame">Register</a>
  <a href="catalogue.html" target="rightFrame">Catalogue</a>
  <a href="cart.html" target="rightFrame">Cart</a>
</nav>
```
This creates the top menu for page navigation.

**Meaning:**
- `<nav>` defines the navigation area
- `<a>` creates links to other pages
- `target="rightFrame"` opens the linked page in the main right section

---

### 3.4 Sidebar in `left.html`
```html
<div class="sidebar">
  <h3>Categories</h3>
  <ul>
    <li><a href="cse.html" target="rightFrame">CSE Books</a></li>
    <li><a href="ece.html" target="rightFrame">ECE Books</a></li>
    <li><a href="mech.html" target="rightFrame">Mechanical Books</a></li>
  </ul>
</div>
```
This creates the left category panel used to navigate between sections.

---

### 3.5 Book Catalogue in `catalogue.html`
```html
<table class="catalogue-table">
```
This creates a table to display books.

```html
<th>Book Image</th>
<th>Book Name</th>
<th>Author Name</th>
<th>Price</th>
<th>Action</th>
```
These are the table headings.

```html
<td><img src="cse images.jpg" alt="Book Image" class="book-img"></td>
```
This shows the book image.

```html
<td>Rs. 3250</td>
```
This displays the price of the book.

```html
<button class="cart-btn">Add to Cart</button>
```
This creates an Add to Cart button.

---

### 3.6 CSS Styling in `style.css`
```css
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background-color: #f5f5f5;
  color: #333;
}
```
This sets the overall page styling.

```css
.sidebar {
  position: fixed;
  left: 0;
  top: 0;
  width: 200px;
  height: 100%;
  background-color: #2c3e50;
}
```
This styles the left sidebar and keeps it fixed on the page.

```css
.catalogue-table {
  width: 100%;
  border-collapse: collapse;
  background: white;
}
```
This makes the book table clean and readable.

```css
.catalogue-table th {
  background-color: #3498db;
  color: white;
}
```
This gives the table header a blue color.

```css
.cart-btn:hover {
  background-color: #2980b9;
}
```
This adds a hover effect to the cart button.

---

### 3.7 Footer in `footer.html`
```html
<footer class="site-footer">
  <p>Created by Devvrat Kumar</p>
  <p>Roll no. 2505110120067</p>
</footer>
```
This section displays the project creator details at the bottom of the page.

---

## 4. Project Summary
This project is a simple bookstore website built using HTML and CSS. It includes a top navigation bar, left-side category menu, book catalogue, login page, registration page, and shopping cart page. The design is simple and easy to understand, making it suitable as a beginner web development project.

The project demonstrates how multiple HTML pages can be connected together and styled using one CSS file.

---

## 5. Important Terms

### HTML
HTML stands for HyperText Markup Language. It is used to create the structure of a webpage.

### CSS
CSS stands for Cascading Style Sheets. It is used to design and style the webpage.

### Frameset
A frameset divides the browser window into separate sections, each showing a different page.

### Table
A table is used to show data in rows and columns, such as book details in the catalogue.

### Form
A form is used to collect user input, such as in the login and registration pages.

### Link
A link connects one page to another or links to an external stylesheet.

### Button
A button is used for actions like login, viewing a cart, or adding a book.

---

## 6. Final Explanation
This bookstore project is a beginner-level front-end project. It teaches the basics of webpage structure, navigation, tables, forms, and CSS styling. It shows how a small website can be built using multiple HTML files and shared stylesheet design.
`