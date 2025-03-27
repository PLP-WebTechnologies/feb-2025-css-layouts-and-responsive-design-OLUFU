# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨

ANSWER

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout with Flexbox, Grid, and Media Queries</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1>My Responsive Website</h1>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section class="hero">
            <h2>Welcome to the Hero Section!</h2>
            <p>This is a hero section designed to grab your attention.  It showcases a brief introduction to the website and its purpose.  It adapts well to different screen sizes, thanks to flexbox and media queries.</p>
            <button>Learn More</button>
        </section>

        <section class="grid-container">
            <div class="grid-item">
                <h3>Feature 1</h3>
                <p>Description of Feature 1.  This content will wrap and re-arrange based on screen size.</p>
                <img src="https://via.placeholder.com/150" alt="Feature 1 Image">
            </div>
            <div class="grid-item">
                <h3>Feature 2</h3>
                <p>Description of Feature 2.  This content will wrap and re-arrange based on screen size.</p>
                <img src="https://via.placeholder.com/150" alt="Feature 2 Image">
            </div>
            <div class="grid-item">
                <h3>Feature 3</h3>
                <p>Description of Feature 3.  This content will wrap and re-arrange based on screen size.</p>
                <img src="https://via.placeholder.com/150" alt="Feature 3 Image">
            </div>
        </section>

        <section class="flex-container">
            <div class="flex-item">
                <h3>Article 1</h3>
                <p>Short article snippet. Using Flexbox for equal height columns.</p>
                <a href="#">Read More</a>
            </div>
            <div class="flex-item">
                <h3>Article 2</h3>
                <p>Another short article snippet. Demonstrating Flexbox's column flexibility.</p>
                <a href="#">Read More</a>
            </div>
            <div class="flex-item">
                <h3>Article 3</h3>
                <p>One more short article snippet. Flexbox ensuring equal height and responsive layout.</p>
                <a href="#">Read More</a>
            </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2023 My Responsive Website</p>
    </footer>

</body>
</html>
/* style.css */

/* General Styles */
body {
    font-family: sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
    color: #333;
}

header {
    background-color: #333;
    color: #fff;
    padding: 1rem 0;
    text-align: center;
}

header h1 {
    margin: 0;
}

nav ul {
    padding: 0;
    margin: 0;
    list-style: none;
    display: flex; /* Use Flexbox for Navigation */
    justify-content: center; /* Center the navigation items */
}

nav li {
    margin: 0 1rem;
}

nav a {
    color: #fff;
    text-decoration: none;
}

main {
    padding: 2rem;
}

/* Hero Section Styles */
.hero {
    background-color: #e0e0e0;
    padding: 2rem;
    text-align: center;
    margin-bottom: 2rem;
}

.hero h2 {
    margin-top: 0;
}

button {
    background-color: #333;
    color: #fff;
    padding: 0.75rem 1.5rem;
    border: none;
    cursor: pointer;
}


/* Grid Container Styles */
.grid-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); /* Responsive Grid Layout */
    gap: 1rem;
    margin-bottom: 2rem;
}

.grid-item {
    background-color: #fff;
    padding: 1rem;
    border: 1px solid #ccc;
    text-align: center;
}

.grid-item img {
    max-width: 100%;
    height: auto;
}


/* Flex Container Styles */
.flex-container {
    display: flex;
    flex-wrap: wrap; /* Allow items to wrap to the next line */
    gap: 1rem;
    margin-bottom: 2rem;
}

.flex-item {
    background-color: #fff;
    padding: 1rem;
    border: 1px solid #ccc;
    flex: 1; /* Allow items to grow and shrink equally */
    min-width: 250px; /* Minimum width to prevent too much squeezing */
}

/* Footer Styles */
footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 1rem 0;
}

/* Media Queries for Responsiveness */

/* For tablets and larger phones */
@media (max-width: 768px) {
    nav ul {
        flex-direction: column; /* Stack navigation items on smaller screens */
        align-items: center; /* Center the items */
    }

    nav li {
        margin: 0.5rem 0;
    }

    .grid-container {
        grid-template-columns: 1fr;  /* One column layout on smaller screens */
    }

    .flex-container {
       flex-direction: column;  /* Stack flex items on smaller screens */
    }
}

/* For very small phones */
@media (max-width: 480px) {
    .hero {
        padding: 1rem;
    }

    .hero h2 {
        font-size: 1.5rem;
    }

    .flex-item {
      min-width: 100%; /*Ensure that flex items take the full width on very small screens*/
    }
}
