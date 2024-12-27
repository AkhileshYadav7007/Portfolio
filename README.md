# Personal Portfolio Website
This project is a personal portfolio website built using HTML, CSS, and JavaScript. It showcases my skills, services, projects, and contact information in a visually appealing and user-friendly manner.

Live Demo https://akhileshyadav7007.github.io/Portfolio/

<img width="957" alt="Screenshot 2024-12-27 093224" src="https://github.com/user-attachments/assets/2dada2dc-6d85-4c02-a273-906900b48220" />



<img width="949" alt="image" src="https://github.com/user-attachments/assets/c4e4c499-4f04-4257-a0cd-60d73d1d6963" />


<img width="949" alt="image" src="https://github.com/user-attachments/assets/0ba1cc1f-f0e7-4af9-8ae9-f4df7f90e0bf" />

<img width="949" alt="image" src="https://github.com/user-attachments/assets/0715d31b-ff7b-46f2-b159-886677054e33" />





## Table of Contents
Introduction
Code Explanation
HTML Structure
CSS Styling
JavaScript Functionality
Features
How to Use
Introduction
The portfolio includes:

## A responsive header with navigation links.
An "About Me" section featuring my skills, experience, and education.
A "Services" section showcasing my offerings.
A "Portfolio" section displaying my projects.
A "Contact" section for users to reach out.
Code Explanation
HTML Structure
Header Section (#header)

## Displays the main navigation bar (<nav>) and a welcome message introducing me as a Web Developer.
Includes a responsive menu toggle feature using icons from Font Awesome.
About Section (#about)

### Contains an image (about-col-1) and a text description (about-col-2) of my background.
### Uses tabbed navigation to switch between "Skills," "Experience," and "Education."
Services Section (#services)

### Highlights the services I offer as cards, each with an icon, title, and brief description.
Portfolio Section (#portfolio)

### Displays a grid of project showcases with images, titles, and descriptions, linking to external resources or demo pages.
Contact Section (#contact)

### Includes my contact information, social media links, and a form for sending messages.
### The form integrates Google Apps Script for submission functionality.
Footer

Displays a copyright notice.
CSS Styling
Global Styles

Applies consistent font styles, colors, and box-sizing rules.
Ensures smooth scrolling (html { scroll-behavior: smooth; }).
Header Styling

Sets up the header's background image and responsive layout.
Adds hover effects to navigation links.
About Section Styling

Formats the image with rounded corners and a double border.
Defines styles for tab navigation and active tab states.
Services and Portfolio

Implements grid layouts for services and portfolio items.
Uses hover effects for interactive project descriptions.
Contact Section

Creates a form layout with responsive design.
Styles social media icons for branding consistency.
JavaScript Functionality
Tab Navigation

### Handles the switching between "Skills," "Experience," and "Education" using the opentab function.
javascript
Copy code
function opentab(tabname) {
    for (tablink of tablinks) {
        tablink.classList.remove("active-link");
    }
    for (tabcontent of tabcontents) {
        tabcontent.classList.remove("active-tab");
    }
    event.currentTarget.classList.add("active-link");
    document.getElementById(tabname).classList.add("active-tab");
}
Responsive Menu

Toggles the side menu visibility with the openmenu and closemenu functions.
javascript
Copy code
function openmenu() {
    sidemenu.style.right = "0";
}
function closemenu() {
    sidemenu.style.right = "-200px";
}
Form Submission

Submits contact form data to Google Sheets using the Fetch API.
javascript
Copy code
form.addEventListener('submit', e => {
    e.preventDefault();
    fetch(scriptURL, { method: 'POST', body: new FormData(form) })
        .then(response => {
            msg.innerHTML = "Message sent successfully";
            setTimeout(() => msg.innerHTML = "", 5000);
            form.reset();
        })
        .catch(error => console.error('Error!', error.message));
});
## Features
Responsive Design: Works seamlessly across different screen sizes.
Tabbed Navigation: Displays dynamic content for "Skills," "Experience," and "Education."
Project Showcases: Highlights completed work with project descriptions.
Contact Form Integration: Sends messages to Google Sheets.

### How to Use
Clone this Repository:

bash
Copy code
git clone https://github.com/akhilesh7007/personal-portfolio.git
Open index.html in a browser.

The website should display as intended.
Customize:

Replace images and text in the HTML file.
Update styles in the style.css file.
Deploy:

Use platforms like GitHub Pages, Netlify, or Vercel for deployment.










