# Creating a GitHub Pages Site

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

## II. Markdown vs. HTML/CSS/JSS

- While markdown is a great way to simply and quickly format documents and to add simple interactivity (hypertext links) to them, web pages created with it are lacking many features that are taken for granted on the web today, including:
  - content rich web sites that use visually interesting fonts and animation - check out RIT's home page as an example - https://www.rit.edu/
  - web sites that gather information from users by utilizing forms (e-commerce sites etc)
  - web sites (like Google Docs) that are full blown apps that can replace desktop applications such as Word and Excel
  - web sites that can run games and interactive experiences - here is an IGME-330 project writen in JavaScript that is running on GitHub Pages: https://tonethar.github.io/projects/procedural-flowers/latest/index.html
 
###  HTML/CSS/JSS
- To build pages and web sites that go beyond what markdown can do, you need: 
  - HyperText Markup Language - a way to add *structure* to a page (this is heading, this is a paragraph, this is a list etc)
  - Cacading Style SHeets -  changes the presentation (appearance) of a web page
  - JavaScript - adds interactivity to a page
- We're going to cover some of the basics in this course (to help you with your projects), and you'll go much deeper in future courses!
 
### IGM Core Web Classes
- IGME-235 "Intro to Web Tech" - Build web pages, web sites, learn advanced CSS layouts, build a web app, build a web game
- IGME-330 "Rich Media I" - Advanced interactivity and procedural drawing (the procedural flower app above is from this course)
- IGME-430 "Rich Media II" (required for New Media Interactive Dev, optional for GDD) - build "full stack" web apps and custom servers

---

## III. Sample HTML Pages
- Go ahead and copy the HTML and create these files on your computer
- You can then open them in Chrome to see how the HTML is rendered
- You can edit their contents in text editors that handle plain text such as VSCode or Notepad++ (but NOT MS Word)

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

**hello.html**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hello Page</title>
</head>
<body>
  <h1>Hello!</h1>
</body>
</html>
```

---

**tacos.html**

```html
```

---

**dice-roller.html**

```html
```

---

## IV. Posting an HTML page to GitHub
- https://pages.github.com/
