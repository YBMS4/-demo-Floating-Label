# (Demo) How did they do it: Floating Label.
 In this repository, you'll discover how libraries like Bootstrap and others create the popular floating label effect — commonly seen in mobile apps.

## What do you need ?

### HTML
 In your **HTML** file, you'll need:
  - A container ```html <div>``` ``(optional)``: Helps control the input's width.
  - A ```html <label class="floating-label check-validation">```: This contains both the **input** and the **label text**. It uses two classes: 
    * **floating-label**: Manages positioning and animation of the label.
    * **check-validation** ``(optional)``: Allows for visual feedback **(valid/invalid)**. ``(You can use JS to toggle the input's ```valid``` attribute based on validation)``. 
  - A ```html <input>```: Obviously ``(can be of type **text**, **email**, **password**)``
  - The **Text** : Use a ```html <span class="label">``` or ```html <div>``` ny element with the class **``label``** works.

### CSS and JS 
 To activate the floating label system::
 - **CSS**: Import ```floatingLabel.css``` into the ```html <head>``` of your app.
 - **JavaScript** ``(optional)``: Import and call the ```js floatingLabelHandler()``` function from ```floatingLabelScript.js``` in a ```html <script type="module">```. It's only used to keep the label floating after the input is populated. Otherwise, the text would return to its original position, but behind the **input's value**. 

 ### Examples:

 1) **HTML**

  ```html
   <div>
        <label for="email" class="floating-label check-validation">
            <input id="email" type="email" name="" required>
            <span class="label">Email</span>
        </label>

        <label for="password" class="floating-label check-validation">
            <input id="password" type="password" name="" required>
            <span class="label">Password</span>
        </label>
    </div>
  ```

  2) **CSS and JS**

  ```html
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="./lib/floatingLabel.css">
    <script type="module" src="script.js" defer></script>
  ```

  **Inside your script**:

  ```js
    import floatingLabelHandler from "./lib/floatingLabelScript.js";

    window.addEventListener("load", () => {
        floatingLabelHandler();
    });
  ```