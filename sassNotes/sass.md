<!-- Learning SaSS -->

## What is SaSS.

- Stands for Syntactically Awesome Stylesheets
- CSS Preprocessor / Precompiler
- Enhances the functionality of CSS
- Other prepropcessors include Less and Stylus

## How Does Sass Work?

- Sass uses .scss or .sass file extensions
- The browser does NOT read Sass, it must be compiled
- Sass files are compiled to normal CSS files
- There are many different types of Sass compiliers (cli and GUI)

## What does Sass offer?

- Variables
- Nesting => Main reason for using Sass => You can structure your css like your html
- Partials / Imports
- Functions & Mixins
- Conditionals
- Inheritance
- Operators and calculations
- Color functions

## .scss vs .sass

- .scss is usually preferred over .sass as it uses the same syntax as regular css

### 1. Variables and partials

- Variables are defined using the \$ sign
- The variable is assigned with a :

- You can remove variables from the main scss file and store them in a partial inside the main scss folder.
- A partial file starts with an underscore. The underscore tells the compiler not to compile the partial file into a separate file.
- You import the partial into the main scss file using the @import keyword

- --If you use bootstrap and sass, together, every element e.g the buttons, the navbar etc all have their own separate partial file with just those styles.

$primary-color: steelblue;
$secondary-color: skyblue;

### 2. Nesting & Structuring

- The ampersand placeholder represents the name tag being styled.

- You structure your scss just like the html, styles related to a particulat tag are put together under each other.

### Inheritance and Contrast

- To set the style to be inherited, you start with a % and then the name of the styles....for example

---- %btn-shared{
// styles
}

- Then to set the styles to be extended,use an @extend keyword followed by %name-of-styles-to-be-extended

// Example:
.btn {
$-light{
        @extend %btn-shared;
        background-color: $light-color;
color: #333;
}

    $-dark{
        @extend %btn-shared;
        background-color: $dark-color;
    }

}
