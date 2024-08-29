# Creating a GitHub Pages Site

---

[**I. Recap**](#i-recap)

[**II. Markdown vs. HTML/CSS/JS**](#ii-markdown-vs-htmlcssjs)

[**III. Sample HTML Pages**](#iii-sample-html-pages)

[**IV. Posting an HTML page to GitHub**](#iv-posting-an-html-page-to-github)

[**V. Homework**](#v-homework)

---

## I. Recap
- Last time ([GitHub Intro](github-intro.md)) we learned:
  - how to create a new GitHub repository named ***yourGithubId*/IGME-110-Repo**
  - how to create new documents in the respository
  - how to use basic markdown to format text content (headers, bold and italic text, and horizontal rules)
  - how to display display images
  - create hypertext links to web pages

### Demo
- Review of basic markdown covered last time
- How to create folders on a repo and upload files
  - go ahead and grab this ZIP of images -> [images.zip](../_files/images.zip)
  - and we will show you to upload them GitHub, and then link to them/display them from **README.md**

---

## II. Markdown vs. HTML/CSS/JS

- While markdown is a great way to simply and quickly format documents and to add simple interactivity (hypertext links) to them, web pages created with it are lacking many features that are taken for granted on the web today, including:
  - content rich web sites that use visually interesting fonts and animation - check out RIT's home page as an example - https://www.rit.edu/
  - web sites that gather information from users by utilizing forms (e-commerce sites etc)
  - web sites (like Google Docs) that are full blown apps that can replace desktop applications such as Word and Excel
  - web sites that can run games and interactive experiences - here is an IGME-330 project writen in JavaScript that is running on GitHub Pages: https://tonethar.github.io/projects/procedural-flowers/latest/index.html
 
###  HTML/CSS/JS
- To build pages and web sites that go beyond what markdown can do, you need 3 new languages: 
  - HyperText Markup Language (HTML) - a way to add *structure* to a page (this is heading, this is a paragraph, this is a list etc)
  - Cacading Style Sheets (CSS) -  changes the *presentation* (appearance) of a web page
  - JavaScript (JS) - adds *interactivity* to a page
- We're going to cover some of the basics in this course (to help you with your projects), and you'll go much deeper in future courses!
 
### IGM Core Web Classes
- IGME-235 "Intro to Web Tech" - Build web pages, web sites, learn advanced CSS layouts, build a web app, build a web game
  - https://github.com/rit-igm-web/igme-235-shared/blob/main/exercises/projects.md
- IGME-330 "Rich Media I" - Advanced interactivity and procedural drawing (the procedural flower app above is from this course)
- IGME-430 "Rich Media II" (required for New Media Interactive Dev, optional for GDD) - build "full stack" web apps and custom servers

---

## III. Sample HTML Pages
- Go ahead and copy the HTML and create these files on your computer
- You can then open them in Chrome to see how the HTML is rendered
- You can edit their contents in text editors that handle plain text such as VSCode or Notepad++ (but NOT MS Word)
- We will start off by looking at **minimal.html** in the web browser, and then discussing how HTML *tags* work

---

**minimal.html**

```html
<html>
  <head>
    <!-- This shows up in the window title bar -->
    <title>My minimal Color page</title>
  </head>
  <body>
    <!-- Everything here shows up in the browser window -->
    <h1>My Fav Colors!</h1>
    <ol>
      <li>Red</li>
      <li>Green</li>
      <li>Blue</li>
    </ol>
  </body>
</html>
```

---

**links.html**
- This page adds some information that browsers like (e.g. the character set and language) as well as information used by HTML validators (e.g. `<!DOCTYPE html>`
- Also note how we can write a bulleted list in HTML
- And how we create Hypertext links in HTML
  
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Links Page</title>
</head>
<body>
  <h1>Some Links</h1>
  <ul>
    <li><a href="https://en.wikipedia.org/wiki/Taco">Tacos</a></li>
    <li><a href="https://en.wikipedia.org/wiki/Hummus">Hummus</a></li>
  </ul>
</body>
</html>
```

---

**tacos.html**

- This page adds a more content and the beginning of a page layout
- It also adds an image (which you'll have to download yourself - [taco.jpeg](../_files/taco.jpeg))
- Most importantly, we now have CSS styling:
  - here the styling directives are located in the `<style>` tag
  - *CSS selectors* tell the browser which HTML element to apply the style rules to (e.g. `body`, `h1`, `h2` are all CSS "type" selectors)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      background-color: #faf2e4;
      margin: 0 10%;
      font-family: sans-serif;
    }

    h1 {  
      text-align: center;
      font-family: serif;
      font-weight: normal;
      text-transform: uppercase;
      border-bottom: 1px solid #57b1dc;
      margin-top: 30px;}
      
    h2 {  
      color: #d1633c;  
      font-size: 1em;
    }
  </style>
  <title>Taco Tuesday's Restaurant</title>
</head>
<body>
  <h1><img src="images/taco.jpeg" alt="taco" width="175"><br>Taco Tuesday's Restaurant</h1>

<h2>The Restaurant</h2>
<p>The Taco Tuesday Restaurant offers casual breakfast, lunch, dinner and late-night fare in a relaxed atmosphere. The menu features our curated selection of only the finest local tacos.</p>

<h2>The Staff</h2>
<p>Passionate about Food. <em>Dedicated.</em> <b>They love working here 7 days a week!</b> <small>(Apply now! We're always hiring!)</small></p>

<h2>Location and Hours</h2>
<p>West Naragonkshutt, NY;<br>Monday through Sunday 5am to Midnight</p>
</body>
</html>
```

---

**dice-roller.html**

- Finally, here we are using JavaScript to create a simple "Dice Roller" app
- You can see that we are giving some of our HTML elements unique `id` values so that we can reference them in our code
- You can also see some nice button styling
- and CSS *id selectors*
- BTW - as HTML files get larger, we generally start to split them up by moving the JavaScript and CSS to separate files (in this class you won't have to to worry about doing this, unless you really want to)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dice Roller</title>
  <style>
    h1{
      font-family: sans-serif;
    }
    /* https://www.w3schools.com/csS/css3_buttons.asp */
    button {
      background-color: #04AA6D;
      border: none;
      color: white;
      padding: 15px 32px;
      text-align: center;
      text-decoration: none;
      display: inline-block;
      font-size: 16px;
    }

    #btn10{
      background-color: #008CBA;
    }
    
    #btn20{
      background-color: #f44336;
    }
  </style>
</head>
<body>
  <h1>Dice Roller!</h1>
  <div>
    <button id="btn6">D6</button>
    <button id="btn10">D10</button>
    <button id="btn20">D20</button>
  </div>

  <hr>

  <div>The roll is: <span id="numberSpan">???</span></div>
  <script>
    // We are putting the <script> tag at the bottom to make sure that 
    // the HTML page has loaded before we start trying to hook up button events
    
    // The following code is loaded in once, when the HTML page first loads
    
    function showRandomInt(min, max) {
      min = Math.ceil(min);
      max = Math.floor(max);
      let number = Math.floor(Math.random() * (max - min + 1)) + min;
      numberSpan.innerHTML = number;
    }

    btn6.onclick = function(){
      showRandomInt(1, 6);
    };

    btn10.onclick = function(){
      showRandomInt(1, 10);
    };

    btn20.onclick = function(){
      showRandomInt(1, 20);
    };
  </script>
</body>
</html>
```

---

## IV. Posting an HTML page to GitHub
- Here are the instructions: https://pages.github.com/
  - Select "Project site"
  - Select "Start from scratch"
  - Head to your **IGME-110-Repo** from last time
  - When you create an **index.html** file (Step #1) in **IGME-110-Repo**
  - rather than just typing in `<h1>Hello!</h1>` (Step #2), instead use the HTML from **links.html** above
  - Don't forget to save ("Commit") **index.html** (Step #3)
  - For Step #4, click on the **Settings** tab, then click on **Pages**, then select the **main** branch and click the Save button
  - Finally, head to `https://yourGitHubId.github.io/IGME-110-Repo/` to see your page
    - my IGME-110-Repo is at: https://github.com/tonethar/IGME-110-Repo
    - my IGME-110 HTML Web Masterpiece can be viewed at: https://tonethar.github.io/IGME-110-Repo
  - BTW - whenever you update your **index.html** page, it takes a minute or so for the changes to be visible on `https://yourGitHubId.github.io/IGME-110-Repo`
   
---

## V. Homework
- Update **index.html** to display the links (link code written in HTML, NOT markdown!) from your "listicle" (at least 5 of them)
- Head to the myCourses Assignments tab and post the link there in the applicable dropbox - be sure to give me the  `https://yourGitHubId.github.io/IGME-110-Repo/` "web page" version
- If you have some time over the weekend, look over the HTML PDFs that are posted to myCourses
