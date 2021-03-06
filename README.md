# <img src="https://raw.githubusercontent.com/DailyFocusApp/dailyfocus/master/client/web/public/dev/images/dailyfocus__logo.png?token=AG6Ezx6WKuJbbXHUr08LgDJ8B_5RJEPbks5X-36LwA%3D%3D" width=100px" /><br />Dailfocus Inc - Styleguide CSS/Sass

**WORK IN PROGRESS. Not finished yet and can contains a bunch of typos**

Styleguide for CSS and Sass made by Dailyfocus Inc and used across all the company projects.

Disclaimer: This styleguide collects a bunch of ideas inspired by other companies styleguide and adapted to our needs. You can see in credits a great bunch of resources.

## Terminology

Our style is a slightly modified version of the BEM methodology.

We understand 3 types of terms:

1. Component: Standalone entity that is meaningful on its own.
   Example: `header`, `container`, `menu`, `checkbox`, `input`, `button`

2. Element: Parts of a Component and have no standalone meaning. They are semantically tied to its Component.
   Example: `header__title`, `menu__items`, `checkbox__options`

3. Modifier: Flags on components or elements. Use them to change appearance or behavior.
   Examples: `disabled`, `highlighted`, `checked`, `fixed`, `size__big`
   Example: `button__pressed`, `button__hover`, `menu__hidden`,

# CSS
### Formatting

Taken from different docs:

* **Indentation:** use soft tabs (2 spaces).
* **Class name:** prefer dashes over camelCasing.
  Good:
  ```css
  .my_class_name {}
  .button {}
  ```
  Bad:
  ```css
  .myClassName {}
  ```
* **Don't use #ID selectors**. They are only good on your javascript. Think in general components when you're writing your CSS.
* When using multiple selectors in a rule declaration, give each selector its own line.
* **Properties:** put a space after the : character (but not before).
* Put a space before the opening brace `{` in rule declarations
* Put closing braces `}` of rule declarations on a new line

### File naming
  Use camelCasing for the file names.

  *Good*
  ```
  header.sass
  chatPlugin.sass
  ```
  *Bad*
  ```
  header.sass
  chat_plugin.sass
  ```

### How to name classes?

Do not create a style for a specific label. For example, this is wrong:
```css
.header h1 {

}
```
Instead, create a style for the title:
```css
.title {

}

.title__big {

}
```

### Examples

Given an example. We want to create our header. And our headder has a left part and a right part.

```html
<div class="header">

  <div class="header__left">
    <div class="logo logo__big">
      <a href="logo__link">
        DailyFocus
      </a>
    </div>
  </div>

  <div class="header__right">

  </div>

</div>
```

```css
.header {
  width: 100%;
  padding: 10px 0;
  background: red;
}

.header__left {
  float: left;
}

.header__right {
  float: right;
}
```

### Adding new components
The idea is to reuse every new component we create
[TO BE DONE...]


### Resources and credits

http://getbem.com/introduction/
http://www.slideshare.net/stubbornella/object-oriented-css/43-How_about_an_example
https://github.com/airbnb/css
