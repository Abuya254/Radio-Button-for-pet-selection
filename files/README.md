# RadioButtonDemo - Pet Selection Application

## Overview
This is a simple web application that demonstrates the use of radio buttons to select a pet type. The application displays five radio button options (Bird, Cat, Dog, Rabbit, Pig) and shows the user's selection using a message box (alert).

## Features
- Five radio buttons for pet selection
- Beautiful, modern UI with gradient design
- Pet icons for visual appeal
- Message box (alert) displays selection
- Inline result display

## How to Run
1. Simply open the `index.html` file in any web browser (Chrome, Firefox, Edge, Safari)
2. No server or installation required

## Source Code

### HTML Structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RadioButtonDemo - Pet Selection</title>
    <style>
        /* CSS Styles for beautiful UI */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0;
            padding: 20px;
        }

        .container {
            background: white;
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
            padding: 40px;
            max-width: 400px;
            width: 100%;
        }

        h1 {
            color: #333;
            text-align: center;
            margin-bottom: 10px;
            font-size: 28px;
        }

        .pet-options {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-bottom: 30px;
        }

        .radio-option {
            display: flex;
            align-items: center;
            padding: 15px 20px;
            background: #f8f9fa;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }

        .radio-option:hover {
            background: #e9ecef;
            transform: translateX(5px);
        }

        .radio-option input[type="radio"] {
            width: 20px;
            height: 20px;
            margin-right: 15px;
            cursor: pointer;
            accent-color: #667eea;
        }

        .submit-btn {
            width: 100%;
            padding: 15px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 18px;
            font-weight: 600;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🐾 RadioButtonDemo 🐾</h1>
        <p class="subtitle">Select your favorite pet</p>
        
        <div class="pet-options">
            <div class="radio-option">
                <input type="radio" id="bird" name="pet" value="Bird">
                <label for="bird"><span class="pet-icon">🐦</span>Bird</label>
            </div>
            
            <div class="radio-option">
                <input type="radio" id="cat" name="pet" value="Cat">
                <label for="cat"><span class="pet-icon">🐱</span>Cat</label>
            </div>
            
            <div class="radio-option">
                <input type="radio" id="dog" name="pet" value="Dog">
                <label for="dog"><span class="pet-icon">🐕</span>Dog</label>
            </div>
            
            <div class="radio-option">
                <input type="radio" id="rabbit" name="pet" value="Rabbit">
                <label for="rabbit"><span class="pet-icon">🐰</span>Rabbit</label>
            </div>
            
            <div class="radio-option">
                <input type="radio" id="pig" name="pet" value="Pig">
                <label for="pig"><span class="pet-icon">🐷</span>Pig</label>
            </div>
        </div>

        <button class="submit-btn" onclick="showSelection()">Show My Selection</button>
    </div>

    <script>
        function showSelection() {
            const petRadios = document.getElementsByName('pet');
            let selectedPet = null;

            for (let radio of petRadios) {
                if (radio.checked) {
                    selectedPet = radio.value;
                    break;
                }
            }

            if (selectedPet) {
                alert("You have selected: " + selectedPet + " 🐾");
            } else {
                alert("Please select a pet! 🐾");
            }
        }
    </script>
</body>
</html>
```

## How to Upload to GitHub

### Step 1: Create a GitHub Account
If you don't have one, go to [github.com](https://github.com) and sign up.

### Step 2: Create a New Repository
1. Click the "+" icon in the top right corner
2. Select "New repository"
3. Repository name: `RadioButtonDemo`
4. Choose "Public"
5. Click "Create repository"

### Step 3: Upload Files
1. On your new repository page, click "uploading an existing file"
2. Drag and drop the `index.html` file
3. Add commit message: "Add RadioButtonDemo application"
4. Click "Commit changes"

### Step 4: Share the URL
Your repository URL will be:
```
https://github.com/YOUR_USERNAME/RadioButtonDemo
```

To view the app live, you can use GitHub Pages:
1. Go to Repository Settings
2. Click "Pages" on the left sidebar
3. Under "Build and deployment", select "main" branch
4. Click Save
5. Your app will be available at: `https://YOUR_USERNAME.github.io/RadioButtonDemo`

## Screenshot
The application features:
- A gradient purple background
- White card with shadow
- Five radio button options with pet icons (🐦 Bird, 🐱 Cat, 🐕 Dog, 🐰 Rabbit, 🐷 Pig)
- A "Show My Selection" button
- When clicked, displays an alert message box showing the selected pet

## Technologies Used
- HTML5
- CSS3 (Gradients, Flexbox, Animations)
- JavaScript (DOM manipulation)

## License
This project is for educational purposes.

