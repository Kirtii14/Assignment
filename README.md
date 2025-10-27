React Figma Assignment

This project is a React application built to replicate a specific UI design provided via Figma. It features two main widgets with interactive elements.

Features

Info Box: Displays text content with animated tabs ("About Me", "Experiences", "Recommended").

Gallery Box: Shows an image carousel.

Clickable "+ ADD IMAGE" button to upload and add new images.

Functional carousel arrow buttons to navigate through images.

Hover effects on images (grayscale to color, lift animation).

Hover effects on buttons.

Pixel-Perfect Styling: Uses inline styles derived from Figma specifications for accurate replication of gradients, shadows, and dimensions.

Note: The layout is currently designed for a fixed width (1728px) and is not fully responsive across all screen sizes.

Setup and Installation

Prerequisites:

Node.js (which includes npm/npx) installed on your system. (Download Node.js)

Steps:

Clone the Repository:

git clone <your-repository-url>
cd <your-repository-name>


Install Dependencies:

npm install


Install Tailwind CSS Dependencies:

npm install -D tailwindcss
npx tailwindcss init


Configure Tailwind CSS:

Update tailwind.config.js to include your source files in the content array:

/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./src/**/*.{js,jsx,ts,tsx}", // Ensure this covers your component files
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}


Add the Tailwind directives to the top of your ./src/index.css file:

@tailwind base;
@tailwind components;
@tailwind utilities;


Ensure ./src/index.css is imported in your ./src/index.js file (Create React App usually does this by default).

Running the Application

Start the Development Server:

npm start


Open your browser and navigate to http://localhost:3000 (or the address shown in your terminal).

Important Note: Carousel Functionality

The gallery starts with 3 images displayed.

The carousel arrow buttons (< and >) will only become active after you add more than 3 images to the gallery using the "+ ADD IMAGE" button. Once you have 4 or more images, you can use the arrows to navigate through them.
