`#sass` `#css` `#html` `#master-in-software-engineering`

# SASS - Clone Instagram <!-- omit in toc -->

<p>
  <img alt="Version" src="https://img.shields.io/badge/version-1.0-blue.svg?cacheSeconds=2592000" />
</p>

> Sass (which stands for 'Syntactically awesome style sheets) is an extension of CSS that enables you to use things like variables, nested rules, inline imports and more
>
> The purpose of this project is to learn the basics of SASS and put them into practice by building a visual replica of Instagram

## Index <!-- omit in toc -->

- [Requirements](#requirements)
- [Repository](#repository)
- [Technologies used](#technologies-used)
- [Project delivery](#project-delivery)
- [Resources](#resources)

## Requirements

- You must use variables at least once in the project.
- You must use nesting.
- You must use inheritance at least once in the project.
- You cannot use third party libraries for the development of this pill

## Repository

First of all you must fork this project into your GitHub account.

To create a fork on GitHub is as easy as clicking the “fork” button on the repository page.

<img src="https://docs.github.com/assets/images/help/repository/fork_button.jpg" alt="Fork on GitHub" width='450'>

### Installing

In this project you must use the VSCode SASS extension in order to compile SASS into CSS.

First of all you will need to install the extension:

- [Live SASS Compiler](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass)

When the extension is installed correctly, having a SASS file open, you must click on "Watch Sass":

<img src="https://raw.githubusercontent.com/ritwickdey/vscode-live-sass-compiler/master/images/Screenshot/AnimatedPreview.gif" width="600px">

If you want to change some configuration of "Live SASS Compiler" you can check this official resource:

- [Live SASS Compiler Settings](https://github.com/ritwickdey/vscode-live-sass-compiler/blob/master/docs/settings.md)

## Technologies used

\* SASS

\* CSS

\* HTML

## Project delivery

To deliver this project you must follow the steps indicated in the document:

- [Submitting a solution](https://www.notion.so/Submitting-a-solution-524dab1a71dd4b96903f26385e24cdb6)

## Resources

- [SASS documentation](https://sass-lang.com/)
- [W3S SASS](https://www.w3schools.com/sass/)
- [Organizing SASS Projects](https://blog.prototypr.io/how-i-organize-sass-projects-e2d7760df86f)
- [Why don't use @import](https://www.youtube.com/watch?v=CR-a8upNjJ0)

## Question Answers

## What is SASS? What does SASS stand for?
SASS is a cascade style language (could be simplified as a "css on steroids"), and SASS stands for "Syntactically awesome style sheets"

## What is a CSS pre-processor?
It's a scripting language that can expand the default capabilities of CSS, such as using logic in CSS code.
## What does a pre-processor have to do with SASS?
SASS is itself a pre-processor, and it extends CSS' capabilities immensely.
## Why use SASS?
In order to save time, increase efficiency and apply logic into CSS among other extra capabilities.
## SASS has disadvantages? Which are?
SASS has to be compiled first, browsers can't understand it directly, and can't use browser built-in element inspector
## What is a SASS Variable? Explain why are useful
It is a value assigned through $, which can be used throughout the file, which can be imported to other files as well. They can save a lot of repetition and make code maintenance easy.
## Explain the SASS variables property with an example.
$long-range:100px
.navbar{
    width:$long-range;
}
## What is a mixin? Why is it important? Give an example
A mixin lets you use groups of CSS declarations that you want to reuse throughout your site.

@mixin theme($theme: DarkGray) {
  background: $theme;
  box-shadow: 0 0 1px rgba($theme, .25);
  color: #fff;
}

.info {
  @include theme;
}
.alert {
  @include theme($theme: DarkRed);
}
.success {
  @include theme($theme: DarkGreen);
}
## What is SCSS? Give an example
it's a special file type for sass, the code from which will be converted into css
## What is SASS? Give an example
Sass is an older version compared with scss that uses indentation instead of enclosures and ; .
Example:
SASS SYNTAX
$base-color: #c6538c
$border-dark: rgba($base-color, 0.88)

.alert
  border: 1px solid $border-dark
## What is the difference between .scss and .sass syntax.
scss uses enclosures and ; , and sass uses indentation
## In which cases would we use SCSS? And in which cases would we use SASS?
We should mostly use scss, since it's better to code and has all the advantages of sass.
## Explain how traditional CSS and Preprocessed CSS workflows are different.
traditional CSS is directly interpreted by the browser, but Pre-processed CSS must be compiled and converted before it can be understood by the browser.
## Can we create functions with SASS? If it is true, give an example.
Yes, we can!
@function some-func($param) {
    @return (100/$param);
}

/* How to use a function: */
.col-6 { font-size: some-func(5);}

/* The above is the same as: */
.col-6 { font-size: 20; }
## What is nesting? Is it useful? Give an example of nesting
It's basically including sublocks inside of blocks of code. Among others, it can be applied to loops in JS, and it can also be applied in Sass:

nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
## Difference between @use & @import? Give an example
The main difference is that when using "@use" file is only imported once, which when using "@import" it's not necessarely the case.
## How can we import other CSS/SASS files in SASS? Give an example
by using @use:
SCSS SYNTAX
// foundation/_code.scss
code {
  padding: .25em;
  line-height: 0;
}

// new_file.scss
@use 'foundation/code';

//now the file _cose.css has been imported
## Explain the concept of inheritance in SASS.
inheritance allows you to directly apply the set of properties from one selector to another. Unfortunately, you have to inherit them all, it can't be done selectively.
## Why use @extend? Give an example
Extend is perfect when trying to avoid repetition and you want to apply all the set of properties from an object to another one. See an example below:

%message-shared {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

// This CSS won't print because %equal-heights is never extended.
%equal-heights {
  display: flex;
  flex-wrap: wrap;
}

.message {
  @extend %message-shared;
}

.success {
  @extend %message-shared;
  border-color: green;
}
