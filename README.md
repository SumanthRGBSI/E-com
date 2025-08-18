Commerce OS - Unified Platform
🚀 Introduction
Commerce OS is a complete, single-file e-commerce and inventory management application designed to serve both Buyers and Vendors. Built with modern web technologies, it provides a seamless, responsive experience that works beautifully on both desktop and mobile devices. This document serves as a guide to its features, architecture, and core functionalities.

✨ Key Features
The application is split into two distinct roles, each with a tailored set of features:

🤵 For Buyers
Product Browsing: A clean, filterable product grid with high-quality placeholder images and essential details.

Dynamic Cart: Add products by unit (e.g., "piece") or by weight (e.g., "kg", "g") with a persistent cart.

Multi-Step Checkout: A guided, modal-based checkout process for shipping, payment, and order confirmation.

Order History & Tracking: View past orders and track their current status through a visual timeline.

Mobile-First Design: A dedicated bottom tab bar for intuitive navigation on mobile devices, with the "Cart" as the central action button.

🏭 For Vendors
Financial Dashboard: At-a-glance view of key metrics like Total Sales, Total Orders, and Products Listed. Features smart number formatting (Lakhs, Crores) to handle large values gracefully.

Sales Analytics: A clean line chart visualizing sales trends over time.

Product Management: Full CRUD (Create, Read, Update, Delete) functionality for the product catalog.

Intelligent Inventory Management:

View stock levels and statuses (In Stock, Low Stock, Out of Stock).

One-click Reordering: Automatically generate a Purchase Order for low-stock items.

Procurement System (Purchase Orders):

Create and send purchase orders to suppliers.

Add multiple products (by piece or weight) to a single PO.

Track the status of POs (Ordered, Shipped, Received).

Automatic Stock Updates: Inventory is automatically replenished when a PO is marked as "Received".

Order Management: View incoming customer orders and update their status.

Responsive Mobile UI: A dedicated bottom tab bar with "Manage Orders" as the central button for on-the-go management.

💻 Tech Stack
This application is built to be self-contained and requires no complex setup.

Frontend: HTML5, Tailwind CSS, Vanilla JavaScript (ES6+)

Icons: Lucide Icons for a modern and clean look.

Charts: Chart.js for the vendor sales analytics dashboard.

Fonts: Inter from Google Fonts for excellent readability.

📂 File Structure
The entire application is contained within a single index.html file.

<head>: Contains metadata, links to external libraries (Tailwind, Lucide, Chart.js), and all CSS styles within <style> tags.

<body>: Contains the HTML structure for all screens (Login, Main App, Modals).

<script>: A single, large script tag at the end of the body contains all the application logic, including:

Mock Database (products, orders, suppliers, etc.)

Application State Management

DOM Element References

UI Configuration and Rendering Functions

Event Handlers and Core Logic

🧠 Core Concepts
State Management
A simple JavaScript object state holds the current user role and the active page. The mockDatabase object acts as our data source, simulating a real database.

UI Rendering
The application is a Single Page Application (SPA). The navigate() function is the core router. It takes a pageId, updates the application state, and calls the appropriate render function for that page. This clears the main content area and injects new HTML, providing a fast and seamless user experience without page reloads.

Modularity
Despite being in one file, the JavaScript code is organized into logical sections:

Core Functions: init, login, logout, navigate.

Render Functions: Separate functions for each view (e.g., renderBuyerProducts, renderVendorDashboard).

Event Handlers & Actions: Functions that respond to user interactions (e.g., addToCart, updateOrderStatus).

Modal & Utility Functions: Reusable functions for modals, toasts, and data formatting.

▶️ How to Run
Save the entire code as an index.html file.

Open the index.html file in any modern web browser (like Chrome, Firefox, or Edge).

The application will start on the login screen. No web server or build process is needed.
