_Codeondesign code snippet_
============

### Menu animations

### HTML
```html

<div class="toggle-menu">
    <span class="stroke str_1"></span>
    <span class="stroke str_2"></span>
    <span class="stroke str_3"></span>
</div>
```
### [Sass]() + [Bourbon]()
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
  background-color: $main-color
  margin: 0 0 6px 0
  +position(relative, 0 0 0 10px)
  
+keyframes (animate-str)
  to
    width: 0

```
