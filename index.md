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
    <title>Array</title>
    <style>
        body {
            font-family: 'Courier New', monospace;
            background: #1e1e1e;
            color: #d4d4d4;
            padding: 20px;
            margin: 0;
        }
        .container {
            max-width: 800px;
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
            white-space: pre-wrap;
            font-size: 14px;
            line-height: 1.6;
        }
        .output-line {
            margin: 5px 0;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Array Output</h2>
        <div class="output" id="output"></div>
    </div>

    <script>
        // Capture console.log output
        const outputDiv = document.getElementById('output');
        const originalLog = console.log;
        console.log = function(...args) {
            const line = document.createElement('div');
            line.className = 'output-line';
            line.textContent = args.join(' ');
            outputDiv.appendChild(line);
            originalLog.apply(console, args);
        };

        // Your code starts here
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
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nested Conditional Challenge</title>
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
        p {
            color: #858585;
            margin-bottom: 20px;
        }
        .output {
            background: #252526;
            border: 1px solid #3e3e42;
            border-radius: 4px;
            padding: 15px;
            margin-top: 20px;
            font-size: 13px;
            line-height: 1.6;
            max-height: 600px;
            overflow-y: auto;
        }
        .output-line {
            margin: 2px 0;
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
        <h2>Code Runner Challenge #3: Nested Conditional</h2>
        <p>Checking numbers 1-50 for divisibility by factors of 50 (1, 2, 5, 10, 25, 50)</p>
        <div class="output" id="output">Loading...</div>
    </div>

    <script>
        // Wait for DOM to be ready
        window.addEventListener('DOMContentLoaded', function() {
            const outputDiv = document.getElementById('output');
            outputDiv.innerHTML = ''; // Clear loading message
            
            // Factors of 50: 1, 2, 5, 10, 25, 50
            const factors = [1, 2, 5, 10, 25, 50];
            
            // Loop through numbers 1-50
            for (let num = 1; num <= 50; num++) {
                // Add number header
                const header = document.createElement('div');
                header.className = 'output-line number-header';
                header.textContent = `Number ${num}:`;
                outputDiv.appendChild(header);
                
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
                outputDiv.appendChild(line);
            }
        });
    </script>
</body>
</html>