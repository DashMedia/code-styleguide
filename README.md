# Code Styleguide

## Sass

### File names

All partial sass files are hyphen delimiter seperated starting with an underscore eg: `_this-is-a-file-name.scss`.

File names must be block names in a BEM sence.

### Class names

All class names referanced within a file **MUST** start with the same slug as the file name

```scss
//  _file-name.scss

// Good examples
.file-name{} 
.file-name__element{}
.file-name__element--modifier{}

// Bad examples
.file__element{} // 1
.file-name .something{} // 2
.something .file-name{} // 3
```

1. Use a name based on the file name instead
2. Add a class to the `.something` element which starts with `.file-name` and target that instead
3. Add a modifer class to `.file-name` instead eg: `.file-name--in-something`


#### BEM syntax

```scss
// _block.scss

// Good examples
.block{}
.block--modifier
.block__element--modifier{}
.block__another-element{}
.block__another-element--modifier{}

// Bad examples
.block-thing{}
.block__element__sub-item{}
.block--modifier__element{}
.something-else{}
.block .another{}
```