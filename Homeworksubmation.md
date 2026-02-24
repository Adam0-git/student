---
layout: post 
title: Homework Submation Blog
hide: true
show_reading_time: false
permalink: /homework
---
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>JS Text & Links Demo</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 700px;
      margin: 40px auto;
      padding: 20px;
      background: #070707;
      color: #333;
    }
    h1 { color: #2c3e50; }
    .card {
      background: white;
      border-radius: 8px;
      padding: 20px;
      margin: 20px 0;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    }
    a { color: #3498db; text-decoration: none; }
    a:hover { text-decoration: underline; }
    button {
      margin-top: 10px;
      padding: 8px 16px;
      background: #3498db;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover { background: #2980b9; }
    #dynamic-output { margin-top: 12px; font-size: 15px; }
    #link-list { list-style: none; padding: 0; }
    #link-list li { margin: 8px 0; }
  </style>
</head>
<body>

  <h1>JavaScript Text & Links Demo</h1>

  <!-- 1. Static text via innerHTML -->
  <div class="card">
    <h2>1. Display Text with JavaScript</h2>
    <div id="static-text"></div>
    <script>
      document.getElementById("static-text").innerHTML =
        "👋 Hello! This paragraph was written using <strong>JavaScript</strong>.";
    </script>
  </div>

  <!-- 2. Create a link dynamically -->
  <div class="card">
    <h2>2. Create a Link Dynamically</h2>
    <div id="link-container"></div>
    <script>
      const link = document.createElement("a");
      link.href = "github.com/adam0-git";
      link.textContent = "Visit MDN Web Docs";
      link.target = "_blank";
      document.getElementById("link-container").appendChild(link);
    </script>
  </div>

  <!-- 3. Render a list of links -->
  <div class="card">
    <h2>3. Render a List of Links</h2>
    <ul id="link-list"></ul>
    <script>
      const resources = [
        { label: "MDN Web Docs",    url: "https://developer.mozilla.org" },
        { label: "JavaScript.info", url: "https://javascript.info" },
        { label: "W3Schools JS",    url: "https://www.w3schools.com/js/" },
        { label: "Can I Use",       url: "https://caniuse.com" },
      ];

      const list = document.getElementById("link-list");
      resources.forEach(({ label, url }) => {
        const li   = document.createElement("li");
        const a    = document.createElement("a");
        a.href        = url;
        a.textContent = label;
        a.target      = "_blank";
        li.appendChild(a);
        list.appendChild(li);
      });
    </script>
  </div>

  <!-- 4. Dynamic text on button click -->
  <div class="card">
    <h2>4. Update Text on Click</h2>
    <button onclick="updateText()">Click Me</button>
    <div id="dynamic-output">Waiting for click...</div>
    <script>
      const messages = [
        "You clicked! 🎉",
        "Nice one! 👏",
        "Keep going! 🚀",
        "JavaScript is fun! 😄",
      ];
      let clickCount = 0;
      function updateText() {
        const msg = messages[clickCount % messages.length];
        document.getElementById("dynamic-output").textContent = msg;
        clickCount++;
      }
    </script>
  </div>

</body>
</html>