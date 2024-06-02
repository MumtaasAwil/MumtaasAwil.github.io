<!DOCTYPE html>
<html>
<head>
    <title>GitHub Website</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#repos">Repositories</a></li>
                <li><a href="#issues">Issues</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <section id="home">
            <h1>Welcome to My GitHub Website!</h1>
            <p>This is a basic GitHub-style website.</p>
        </section>
        <section id="about">
            <h1>About Me</h1>
            <p>This is a brief description of myself.</p>
        </section>
        <section id="repos">
            <h1>My Repositories</h1>
            <ul>
                <li><a href="#">Repository 1</a></li>
                <li><a href="#">Repository 2</a></li>
                <li><a href="#">Repository 3</a></li>
            </ul>
        </section>
        <section id="issues">
            <h1>Open Issues</h1>
            <ul>
                <li><a href="#">Issue 1</a></li>
                <li><a href="#">Issue 2</a></li>
                <li><a href="#">Issue 3</a></li>
            </ul>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 My GitHub Website</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: #fff;
    padding: 1em;
    text-align: center;
}

nav ul {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: space-between;
}

nav li {
    margin-right: 20px;
}

nav a {
    color: #fff;
    text-decoration: none;
}

nav a:hover {
    color: #ccc;
}

main {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 2em;
}

section {
    background-color: #f7f7f7;
    padding: 2em;
    margin-bottom: 20px;
    border: 1px solid #ddd;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

h1 {
    font-size: 24px;
    margin-top: 0;
}

ul {
    list-style: none;
    margin: 0;
    padding: 0;
}

li {
    margin-bottom: 10px;
}

a {
    text-decoration: none;
    color: #337ab7;
}

a:hover {
    color: #23527c;
}

footer {
    background-color: #333;
    color: #fff;
    padding: 1em;
    text-align: center;
    clear: both;
}

// Add event listener to navigation links
document.querySelectorAll('nav a').forEach(link => {
    link.addEventListener('click', event => {
        event.preventDefault();
        const target = event.target.textContent;
        document.querySelector(`#${target.toLowerCase()}`).scrollIntoView();
    });
});
