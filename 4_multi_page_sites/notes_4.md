# Multi Page Websites

## File Paths

- If we get on a taxi and the driver asks where to go, saying ***"Home"*** often doesn't suffice. Even in movies.
- We gotta give the exact address (absolute path), or at mention a landmark and some navigate home from there (relative path).
- Same as we consult with computers: if you want to find *cat.png*, you need to tell the system exactly where it lives, starting from the root folder (absolute), or guide it from your current spot (relative).
- We can also set your starting point (like picking a landmark) to make things simpler and avoid confusion.
- In (web) projects etc., we often start paths from the *Project* folder, not the root. That way, if folders move around above *Project*, your code still works—shorter, smarter journeys.
- `../essay.docx` means “go up one folder from where you are, then look for essay.docx.”
- `./dog.png` means “look for dog.png right here in the current folder.” More dots (`../../`) mean go up more levels.
- The `.` is your current location (like saying “I’m here”). `..` is one step up. `...` (not standard, but you get the idea) would be two steps up, and so on.

**Bottom line:**
File paths are your map—absolute for the full address, relative for directions from where you are. Get comfy with both, and you’ll never lose your way in your project folders.

## Webpages

- different files within the same project folder for the purpose of deployment on a single domain, with diff purposes like main.html, contact.html, index.html
- use `<a href="./index.html">Index page </a>`

## 4.2 The HTML Boilerplate

- There’s a set structure for writing HTML pages to keep things readable and consistent.
- Think of it as a jumbo, multi-layered sandwich: top bun, lettuce, cheese, tomato, the meat, tomato, lettuce, the base bun...
- In an empty HTML file in VS Code, type `!` and press Enter when the tooltip pops up—-the app types out the whole structure for you.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8"> <!-- Some charsets allow emojis, some don't. Setting a charset 
                tells the browser what characters it can expect right away. -->
    <title>fractalFigment</title> <!-- Displayed in the browser's tab bar -->
  </head>

  <body>
    <h1>This is the actual page content</h1>
  </body>
</html>
```
