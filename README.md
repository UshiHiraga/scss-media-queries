# SCSS Mixins for Media Queries
## Installation
Download and include `media-queries.scss`.

## Usage
SCSS file provides three mixins to control media queries and a map with several breakpoints.

### Avaible mixins
```scss
    // Screen width is in the breakpoint's range.
    @include media($name);

    // Screen width is less than breakpoint's minimum width.
    @include media-lt($name);

    // Screen width is greater than breakpoint's maximum width.
    @include media-gt($name);
```

### Avaible media queries aliases
Edge Devtools consider the following breakpoints:

| Breakpoint name | Minimum width | Maximum width |
| :-------------: | :-----------: | :-----------: |
|    mobile-s     |      0px      |     320px     |
|    mobile-m     |     321px     |     375px     |
|    mobile-l     |     376px     |     425px     |
|     tablet      |     426px     |     768px     |
|     laptop      |     769px     |    1024px     |
|    laptop-l     |    1025px     |    1440px     |
|       4k        |    1441px     |    2560px     |

[Angular Flex Layout MediaQueries](https://github.com/angular/flex-layout/wiki/Responsive-API#mediaqueries-and-aliases) consider the following breakpoints:

| Breakpoint name | Minimum width | Maximum width |
| :-------------: | :-----------: | :-----------: |
|       xs        |      0px      |     599px     |
|       sm        |     600px     |     959px     |
|       md        |     960px     |    1279px     |
|       lg        |    1280px     |    1919px     |
|       xl        |    1920px     |    5000px     |

## Example
```scss
@use "media-queries.scss" as *;

.container {
    @include media("xs") {
        background: blue;
    }

    @include media-lt("mobile-s") {
        color: green;
    }

    @include media-gt("laptop") {
        color: red;
    }
}
```