[![forthebadge](http://forthebadge.com/images/badges/winter-is-coming.svg)](http://forthebadge.com) 

|        🤖        |🤹‍♀️   | 💻  |  🤘🏼 |
| ------------- |:-------------:| -----:| -----:|

# SCSS Template
A simple architectural scss and js template to start new awesome projects 🤩

## Structure
```
┌── fonts
├── .gitignore
├── gulpfile.js
├── img
├── package.json
├── package-lock.json
├── scripts.min.js
├── scripts.min.js.map
├── styles.min.css
├── styles.min.css.map
└── src
    ├── js
    │   ├── events.js
    │   ├── functions.js
    │   └── vendors
    └── scss
        ├── abstracts
        │   ├── _animations.scss
        │   ├── _mixins.scss
        │   └── _variables
        ├── base
        │    ├── _fonts.scss
        │    └── _reset.scss
        ├── components
        ├── layout
        │    ├── _footer.scss
        │    ├── _header.scss
        │    └── _grid.scss  
        ├── pages                    
        ├── styles.scss
        └── vendors
```

## Needs
- An intuitive scss and js structure easy to work with.
- Clone and start using immediately.

## Goals
- Save work time and allow me to focus only on what's important.

## Current Features
- Works with [Gulp](https://gulpjs.com/) task manager.
- Generates map files.
- Autoprefixer, minifier and uglifier included.
- Sass grid generator from [Bootstrap v4.3.1](https://github.com/twbs/bootstrap) made with CSS Flexbox.

## Setup
1. Clone repository or download
2. Personalize your package.json file:
```
  "name": "name",
  "version": "1.0.0",
  "description": "description",
  "main": "index.js",
  "private": true,
  "author": "Robot Juggler"

```
3. In terminal, `cd` to the directory containing your project.
4. Type `npm i`. This should install all dependencies set in package.json.
5. Type `gulp watch`. Gulp will look for changes in your js and css code.
6. Edit your code inside the `src` folder.
7. Your complied and minified css and javascript files will be updated.
8. ⚠️ If you add a new scss file don't forget to add it in `styles.scss`.

## Usage
### Grid

Simple, it works like [Bootstrap](https://www.google.com) 🙌🏼

Use `.container` class to create a new block and `.row` to create a row on it. The columns class start with `col` following by the number of columns you want to include, and the prefix size name of the container you want to apply this column structure.

```
<div class="container">
  <div class="row">
    <div class="col-md-3">
      This is a column
    </div>
    <div class="col-md-4">
      This is a column
    </div>
    <div class="col-md-5">
      This is a column
    </div>
  </div>
</div>
```

You can have a  **full-width** container by applying `container-fluid` class.

Columns can all have same size avoiding the number of columns.

```
<div class="container-fluid">
  <div class="row">
    <div class="col-md">
      This is a column
    </div>
    <div class="col-md">
      This is a column
    </div>
    <div class="col-md">
      This is a column
    </div>
  </div>
</div>
```

### Breakpoints

|                            | Extra small       | Small    | Medium   | Large | Extra large |
| ---------------------------|-------------|----------|----------|-------|-------------|
| **Max window device size** |<576px       |≥576px    |≥768px    |≥992px |≥1200px      |
| **Max container width**    |None (auto)  |540px    |720px     |960px  |1140px       |
| **Class prefix name**      |`.col- `     |`.col-sm-`|`.col-md-`|`.col-lg-`|`.col-xl-`|

### Media Queries

You can add two types of media queries by adding inside the brackets the prefix size name:

#### `mediaquery-down()` 
The styles inside this media query will apply to devices or windows **smaller** than the prefix name selected.

###### SCSS
```
@include mediaquery-down(xs){
	//Here the scss applied to this media query
}
```

###### CSS
```
@media (max-width: 576px) {
      //Here the scss applied to this media query
}
```

#### `mediaquery-up()` 
The styles inside this media query will apply to devices or windows **bigger** than the prefix name selected.

###### SCSS
```
@include mediaquery-up(xs){
	//Here the scss applied to this media query
}
```

###### CSS
```
@media (min-width: 576px) {
      //Here the scss applied to this media query
}
```