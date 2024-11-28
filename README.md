# CSS_GRID

## What is CSS Grid?
CSS Grid Layout is a robust system for creating intricate web layouts using a grid format. It enables developers to organize elements into rows and columns, simplifying the creation of responsive designs that adjust to different screen sizes. With CSS Grid, developers have precise control over the positioning and sizing of items within a container, leading to adaptable and efficient layouts.


## Key Grid Properties
| Property                     | Description                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| `display: grid`               | Turns the container into a grid layout, enabling the use of CSS Grid within it.                      |
| `grid-template-columns`       | Specifies how many columns are in the grid and their respective sizes.                               |
| `grid-template-rows`          | Specifies how many rows are in the grid and their respective sizes.                                  |
| `gap`                         | Sets the space between the grid items.                                                               |
| `justify-items`               | Controls the alignment of items along the horizontal (row) axis. Common values: `start`, `end`, `center`, `stretch`. |
| `align-items`                 | Controls the alignment of items along the vertical (column) axis. Common values: `start`, `end`, `center`, `stretch`. |



## HTML Code 

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Electronics List</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<h1>Electronics List</h1>
<div class="container">
    <div class="item electronics-item">
        <h2>Smartphone</h2>
        <p>Features: 5G capable, 128GB storage, 6.5-inch display</p>
        <p>Price: $899</p>
    </div>
    <div class="item electronics-item">
        <h2>Laptop</h2>
        <p>Features: Intel Core i7, 16GB RAM, 512GB SSD</p>
        <p>Price: $1200</p>
    </div>
    <div class="item electronics-item">
        <h2>Smartwatch</h2>
        <p>Features: GPS, heart rate monitor, water-resistant</p>
        <p>Price: $199</p>
    </div>
</div>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Team Members</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<h1>Team Members</h1>
<div class="container">
    <div class="item team-item">
        <h2>Alice Johnson</h2>
        <p>Role: Marketing Specialist</p>
        <p>Experience: 5 years in digital marketing</p>
    </div>
    <div class="item team-item">
        <h2>David Lee</h2>
        <p>Role: Software Developer</p>
        <p>Experience: 3 years in full-stack development</p>
    </div>
    <div class="item team-item">
        <h2>Olivia Brown</h2>
        <p>Role: Data Analyst</p>
        <p>Experience: 4 years in data science</p>
    </div>
</div>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Library Books</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<h1>Library Books</h1>
<div class="container">
    <div class="item book-item">
        <h2>Book 1</h2>
        <p>Title: The Catcher in the Rye</p>
        <p>Author: J.D. Salinger</p>
    </div>
    <div class="item book-item">
        <h2>Book 2</h2>
        <p>Title: The Great Gatsby</p>
        <p>Author: F. Scott Fitzgerald</p>
    </div>
    <div class="item book-item">
        <h2>Book 3</h2>
        <p>Title: Moby Dick</p>
        <p>Author: Herman Melville</p>
    </div>
</div>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sports Teams</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<h1>Sports Teams</h1>
<div class="container">
    <div class="item sports-item">
        <h2>Football Team</h2>
        <p>Members: 25 players</p>
        <p>Coach: John Doe</p>
    </div>
    <div class="item sports-item">
        <h2>Basketball Team</h2>
        <p>Members: 12 players</p>
        <p>Coach: Sarah Smith</p>
    </div>
    <div class="item sports-item">
        <h2>Baseball Team</h2>
        <p>Members: 15 players</p>
        <p>Coach: Mark Johnson</p>
    </div>
</div>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pet List</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<h1>Pet List</h1>
<div class="container">
    <div class="item pet-item">
        <h2>Cat</h2>
        <p>Breed: Siamese</p>
        <p>Age: 3 years</p>
    </div>
    <div class="item pet-item">
        <h2>Dog</h2>
        <p>Breed: Labrador</p>
        <p>Age: 2 years</p>
    </div>
    <div class="item pet-item">
        <h2>Rabbit</h2>
        <p>Breed: Dutch</p>
        <p>Age: 1 year</p>
    </div>
</div>
</body>
</html>




CSS STYLES


body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #fafafa;
}

h1 {
    text-align: center;
    margin: 30px 0;
    color: #4f4f4f;
}

.container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 15px;
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
    justify-content: center;
}

.item {
    background-color: #fff;
    padding: 20px;
    border: 2px solid #ddd;
    border-radius: 10px;
    text-align: center;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
    min-height: 250px;
}

.item:hover {
    transform: scale(1.05);
}

h2 {
    font-size: 1.6em;
    margin-bottom: 12px;
    color: #333;
}

p {
    font-size: 1.1em;
    color: #777;
}

.electronics-item {
    background-color: #e1f5fe;
}

.team-item {
    background-color: #ffe0b2;
}

.book-item {
    background-color: #f3e5f5;
}

.sports-item {
    background-color: #c8e6c9;
}

.pet-item {
    background-color: #fff9c4;
}
