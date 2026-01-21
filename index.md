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
    <title>JavaScript Code Runner</title>
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