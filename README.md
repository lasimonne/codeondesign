Codeondesign code snippets
============

###1. Menu animations
    
#### HTML
```html

<div class="toggle-menu">
    <span class="stroke str_1"></span>
    <span class="stroke str_2"></span>
    <span class="stroke str_3"></span>
</div>
```
#### [Sass](http://sass-lang.com/) + [Bourbon](http://bourbon.io/)
``` sass
.toggle-menu
    +size(30px)
    +position(absolute, 20px 0 0 20px)
    cursor: pointer
    z-index: 9999
    &:hover .str_1
        +animation(animate-str 1000ms ease-in-out infinite alternate)
    &:hover .str_2
        +animation(animate-str 1000ms ease-in-out 200ms infinite alternate)
    &:hover .str_3
        +animation(animate-str 1000ms ease-in-out 400ms infinite alternate)
    
.stroke
    width: 30px
    height: 6px
    display: block
    background-color: $main-color
    margin: 0 0 6px 0

+keyframes (animate-str)
    to
        width: 0

```
    
###2. Coming soon!
