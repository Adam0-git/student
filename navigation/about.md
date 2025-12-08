---
layout: post
title: About
permalink: /about/
comments: true
---

## As a conversation Starter
Favorite Video Games:
Limbus Company,
Honkai Star Rail,
Wuthering Waves,
Geometry Dash,

Favorite Anime I watch:
Frieren,
Solo Leveling,
Jujutsu Kaisen,

Favorite Songs:
Hero by Mili,
Compass by Mili,
Through Patches of Violet by Mili,
Frostbite by Ohaikou Music,
Peach Pit and Cyanide by Mili,
In Hell We Live, Lament by Mili feat. KIHOW from MYTH & ROID,
To Your Oblivion by Mili

Here are some places I have lived

<comment>
Flags are made using Wikipedia images
</comment>

<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "0/01/Flag_of_California.svg", "greeting": "Hey", "description": "California - All my life"},

    ];

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

### Journey through Life

Here is what I did at those places

- I was born in San Diego California on November 22 2009. I have lived in Mira Mesa for 5 years and moved to 4S Ranch
- 🏫 I went to Stone Ranch Elementary School in 2015 and graduated in 2022
- 🏫 Then, I went to Oak Valley Middle School from 2022 and then graduated in 2024
- 🎓 Now, I'm a Sophmore in Del Norte High School and will be graduating from Del Norte in 2028

### Culture, Family, and Fun
Family means everything to me

I have been very close to my mom. I unfortunately lost my dad to a heart attack in 2023, and because I have no siblings, I have only my mom to live with. But even still, family is everything and I'm glad to have family close to me. I am lucky that I have many cousins who live close to me, even if they're a lot older than me. 

<comment>
Gallery of pictures of my Family.
</comment>
<div class="image-gallery">
 <img width="2055" height="1510" alt="Image" src="https://github.com/user-attachments/assets/42470b9f-1d9a-4872-be02-089de56df794" />

<img width="1117" height="1501" alt="Image" src="https://github.com/user-attachments/assets/bdcd39f4-505b-4ec6-ba17-9024dcf0671b" />

<img width="1142" height="1482" alt="Image" src="https://github.com/user-attachments/assets/df4a2999-ccf5-4a50-96e9-05de759c5679" />

<img width="1125" height="1496" alt="Image" src="https://github.com/user-attachments/assets/bd81b0e8-e729-4390-a4bd-596d23a974b6" />

<img width="2008" height="1510" alt="Image" src="https://github.com/user-attachments/assets/f47769c1-c9fd-420a-b5ee-a846fd4444d9" />

<img width="1128" height="1508" alt="Image" src="https://github.com/user-attachments/assets/22fbf59e-2d35-4697-8b81-23fd175a3d56" />
