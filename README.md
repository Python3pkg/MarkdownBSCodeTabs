# MarkdownBSCodeTabs
This python extension will convert markdown into Bootstrap 3 Tabs. This is used in conjuction with [highlight.js](https://highlightjs.org)

## Dependencies
### Front End
* [Bootstrap Version 3.x](http://getbootstrap.com/)
* [highlight.js](https://highlightjs.org)

### Back End
* Python 2.x / 3.y


## Installation
To install the Python Plugin from a Linux/Mac OSX Environment Run: 
```
pip install BSCodeTabs
```

## Usage
Markdown
```markdown
# Some Header

blah blah content

   ` ` `{lang1}
    some code here in lang1
   ` ` `
   ` ` `{lang2}
      some code here in lang2
    ` ` `
  
```

Where **{langX}** is a valid language specifier in hilight.js see the [highlight.js demo](https://highlightjs.org/static/demo/) for examples of language specifiers you can use. Also note that we are using 
     ``` ``` ``` characters - in the above example, characters have been spaced out so it renders correctly on Github.



## For Use in mkdocs

### Configuring your mkdocs.yml
```yml
markdown_extensions:
  - BSCodeTabExtension:
      default_lang: 'javascript'
      show_all_code_as_folders: False
      animate_tab_transitions: False
```
In this example we are setting the default source language to be used when no source language is specified in the 
```javascript
    ```
      // this is javascript be default
      function pressTheRedButton() {
        alert('World End!');
      }
    ```
``` 
block fence



