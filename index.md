---
layout: post 
title: Portfolio Home 
hide: true
show_reading_time: false
---

Hi! My name is Adam Ong

### Development Environment

> Coding starts with tools, explore these tools and procedures with a click.

<div style="display: flex; flex-wrap: wrap; gap: 10px;">
    <a href="https://github.com/Open-Coding-Society/student">
        <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
    </a>
    <a href="https://open-coding-society.github.io/student">
        <img src="https://img.shields.io/badge/GitHub%20Pages-327FC7?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Pages">
    </a>
    <a href="https://kasm.opencodingsociety.com/">
        <img src="https://img.shields.io/badge/KASM-0078D4?style=for-the-badge&logo=kasm&logoColor=white" alt="KASM">
    </a>
    <a href="https://vscode.dev/">
        <img src="https://img.shields.io/badge/VSCode-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white" alt="VSCode">
    </a>
</div>

<br>

### Class Progress

> Here is my progress through coding, click to see these online

<div style="display: flex; flex-wrap: wrap; gap: 10px;">
    <a href="{{site.baseurl}}/snake" style="text-decoration: none;">
        <div style="background-color: #b76c4aff; color: black; padding: 10px 20px; border-radius: 5px; font-weight: bold;">
            Snake Game
        </div>
    </a>
    <a href="{{site.baseurl}}/turtle" style="text-decoration: none;">
        <div style="background-color: #693db6ff; color: white; padding: 10px 20px; border-radius: 5px; font-weight: bold;">
            Turtle
        </div>
    </a>
</div>

<br>

<!-- Contact Section -->
### Get in Touch

> Feel free to reach out if you'd like to collaborate or learn more about our work.

<p style="color: #2A7DB1;">Tokyo Japan Tour: <a href="https://www.youtube.com/watch?v=ZPiVqy5n6FM" style="color: #2A7DB1; text-decoration: underline;">Video</a></p>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Combined Code Runner</title>
    <style>
        body {
            font-family: 'Courier New', monospace;
            background: #1e1e1e;
            color: #d4d4d4;
            padding: 20px;
            margin: 0;
        }
        .container {
            max-width: 900px;
            margin: 0 auto;
        }
        h2 {
            color: #4ec9b0;
            margin-bottom: 10px;
        }
        h3 {
            color: #569cd6;
            margin-top: 30px;
            margin-bottom: 10px;
            border-top: 2px solid #3e3e42;
            padding-top: 20px;
        }
        p {
            color: #858585;
            margin-bottom: 20px;
        }
        .output {
            background: #252526;
            border: 1px solid #3e3e42;
            border-radius: 4px;
            padding: 15px;
            margin-top: 10px;
            font-size: 13px;
            line-height: 1.6;
            max-height: 400px;
            overflow-y: auto;
        }
        .output-line {
            margin: 5px 0;
        }
        .number-header {
            color: #569cd6;
            font-weight: bold;
            margin-top: 8px;
        }
        .divisible {
            color: #4ec9b0;
        }
        .not-divisible {
            color: #ce9178;
        }
        .special {
            color: #dcdcaa;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>JavaScript Code Runner</h2>
        
        <!-- First Section: Original Array Code -->
        <h3>Section 1: Mathematical Expressions</h3>
        <div class="output" id="output1"></div>
        
        <!-- Second Section: Nested Conditional Challenge -->
        <h3>Section 2: Nested Conditional Challenge</h3>
        <p>Checking numbers 1-50 for divisibility by factors of 50 (1, 2, 5, 10, 25, 50)</p>
        <div class="output" id="output2">Loading...</div>
    </div>

    <script>
        // ===== SECTION 1: ORIGINAL CODE =====
        const output1 = document.getElementById('output1');
        const originalLog = console.log;
        console.log = function(...args) {
            const line = document.createElement('div');
            line.className = 'output-line';
            line.textContent = args.join(' ');
            output1.appendChild(line);
            originalLog.apply(console, args);
        };

        // Your original code
        let x = 112209;
        let total = x % 2;

        console.log(x + " % 2 = " + total);

        if (x % 2 === 0) {
            console.log(x + " number is even");
        } else {
            console.log(x + " number is odd");
        }

        // Second part
        let x2 = 11222009;
        let y = 1202026;
        let total1 = x2 + y + 2; // total = 10 + 3 + 2 = 15

        console.log("The total is: " + total1); // final output

        // ===== SECTION 2: NESTED CONDITIONAL CHALLENGE =====
        window.addEventListener('DOMContentLoaded', function() {
            const output2 = document.getElementById('output2');
            output2.innerHTML = ''; // Clear loading message
            
            // Factors of 50: 1, 2, 5, 10, 25, 50
            const factors = [1, 2, 5, 10, 25, 50];
            
            // Loop through numbers 1-50
            for (let num = 1; num <= 50; num++) {
                // Add number header
                const header = document.createElement('div');
                header.className = 'output-line number-header';
                header.textContent = `Number ${num}:`;
                output2.appendChild(header);
                
                // Nested conditionals for each factor
                if (num % 1 === 0) {
                    addLine(`  ✓ Divisible by 1`, 'divisible');
                    
                    if (num % 2 === 0) {
                        addLine(`  ✓ Divisible by 2`, 'divisible');
                        
                        if (num % 5 === 0) {
                            addLine(`  ✓ Divisible by 5`, 'divisible');
                            
                            if (num % 10 === 0) {
                                addLine(`  ✓ Divisible by 10`, 'divisible');
                                
                                if (num % 25 === 0) {
                                    addLine(`  ✓ Divisible by 25`, 'divisible');
                                    
                                    if (num % 50 === 0) {
                                        addLine(`  ✓ Divisible by 50 🌟 ALL FACTORS!`, 'special');
                                    } else {
                                        addLine(`  ✗ NOT divisible by 50`, 'not-divisible');
                                    }
                                } else {
                                    addLine(`  ✗ NOT divisible by 25`, 'not-divisible');
                                }
                            } else {
                                addLine(`  ✗ NOT divisible by 10`, 'not-divisible');
                            }
                        } else {
                            addLine(`  ✗ NOT divisible by 5`, 'not-divisible');
                        }
                    } else {
                        addLine(`  ✗ NOT divisible by 2`, 'not-divisible');
                        
                        if (num % 5 === 0) {
                            addLine(`  ✓ Divisible by 5`, 'divisible');
                            
                            if (num % 25 === 0) {
                                addLine(`  ✓ Divisible by 25`, 'divisible');
                            } else {
                                addLine(`  ✗ NOT divisible by 25`, 'not-divisible');
                            }
                        } else {
                            addLine(`  ✗ NOT divisible by 5`, 'not-divisible');
                        }
                    }
                }
            }
            
            function addLine(text, className) {
                const line = document.createElement('div');
                line.className = 'output-line ' + className;
                line.textContent = text;
                output2.appendChild(line);
            }
        });
    </script>
</body>
</html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Array Exercises</title>
    <style>
        body {
            font-family: 'Courier New', monospace;
            background: #1e1e1e;
            color: #d4d4d4;
            padding: 20px;
            margin: 0;
        }
        .container {
            max-width: 900px;
            margin: 0 auto;
        }
        h2 {
            color: #4ec9b0;
            margin-bottom: 20px;
        }
        .output {
            background: #252526;
            border: 1px solid #3e3e42;
            border-radius: 4px;
            padding: 15px;
            margin-top: 20px;
            font-size: 14px;
            line-height: 1.8;
        }
        .output-line {
            margin: 5px 0;
        }
        .header {
            color: #569cd6;
            font-weight: bold;
            margin-top: 15px;
            margin-bottom: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Array Exercises - Running Code</h2>
        <div class="output" id="output"></div>
    </div>

    <script>
        const outputDiv = document.getElementById('output');
        
        function print(text) {
            const line = document.createElement('div');
            line.className = 'output-line';
            line.textContent = text;
            outputDiv.appendChild(line);
        }
        
        function printHeader(text) {
            const line = document.createElement('div');
            line.className = 'output-line header';
            line.textContent = text;
            outputDiv.appendChild(line);
        }

        // ===== EXERCISE 1: ARRAY BASICS - ACCESS ELEMENTS =====
        printHeader("=== Exercise 1: Array Basics - Access Elements ===");

        // Create an array with 5 different items
        const favoriteMovies = ["Inception", "The Matrix", "Interstellar", "The Shawshank Redemption", "Pulp Fiction"];

        // 1. Print the entire array
        print("1. Entire array: " + JSON.stringify(favoriteMovies));

        // 2. Access and print the first element (index 0)
        print("2. First element (index 0): " + favoriteMovies[0]);

        // 3. Access and print the last element
        print("3. Last element: " + favoriteMovies[favoriteMovies.length - 1]);

        // 4. Print the total number of items in the array
        print("4. Total number of items: " + favoriteMovies.length);


        // ===== EXERCISE 2: MODIFY ARRAYS =====
        printHeader("\n=== Exercise 2: Modify Arrays ===");

        // Start with the shopping list
        let shoppingList = ["milk", "eggs", "bread", "cheese"];

        // 1. Print the original array
        print("1. Original array: " + JSON.stringify(shoppingList));

        // 2. Change the second item to "butter"
        shoppingList[1] = "butter";
        print("2. After changing second item to 'butter': " + JSON.stringify(shoppingList));

        // 3. Add "yogurt" to the end using push()
        shoppingList.push("yogurt");
        print("3. After adding 'yogurt' with push(): " + JSON.stringify(shoppingList));

        // 4. Remove "bread" from the array
        const breadIndex = shoppingList.indexOf("bread");
        if (breadIndex > -1) {
            shoppingList.splice(breadIndex, 1);
        }
        print("4. After removing 'bread': " + JSON.stringify(shoppingList));

        // 5. Print the final array
        print("5. Final array: " + JSON.stringify(shoppingList));


        // ===== EXERCISE 3: LOOP THROUGH AN ARRAY =====
        printHeader("\n=== Exercise 3: Loop Through an Array ===");

        // Create an array with 5 numbers
        const numbers = [10, 25, 30, 15, 20];

        print("Array: " + JSON.stringify(numbers));

        // 1. Print each number with a message
        print("\n1. Each number with message:");
        for (let i = 0; i < numbers.length; i++) {
            print("   Number: " + numbers[i]);
        }

        // 2. Print each number multiplied by 2
        print("\n2. Each number multiplied by 2:");
        for (let i = 0; i < numbers.length; i++) {
            print("   " + numbers[i] + " × 2 = " + (numbers[i] * 2));
        }

        // 3. Calculate and print the sum of all numbers
        let sum = 0;
        for (let i = 0; i < numbers.length; i++) {
            sum += numbers[i];
        }
        print("\n3. Sum of all numbers: " + sum);
    </script>
</body>
</html>
def sum_numbers(n):
    """Calculate the sum of all numbers from 1 to n using iteration"""
    total = 0
    for i in range(1, n + 1):
        total += i
    return total

# Test with n = 5
result = sum_numbers(5)
print(f"Sum of numbers from 1 to 5: {result}")
print(f"Expected: 15 (1 + 2 + 3 + 4 + 5 = 15)")

# Additional test cases
print(f"\nSum of numbers from 1 to 10: {sum_numbers(10)}")
print(f"Sum of numbers from 1 to 100: {sum_numbers(100)}")