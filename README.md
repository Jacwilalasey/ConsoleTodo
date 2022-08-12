# Console-based To-do List - Nested Loops, Else, If practice

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)

## Overview

### The challenge

Users should be able to:

- Utilise 4 functions (New, List, Delete, Quit) 
- View the added/removed items within the devtools console
- Quit the app 

## My process

### Built with

- Semantic HTML5 markup
- JavaScript

### What I learned

I learned how to make nested loops (for within while), using this method to create a continuous loop of prompts that request the user to access one of four functions to add, list, delete a new to-do, or quit the app. I also used this practice to learn more about parseInt, to ensure whatever the user input within the delete index section, it would try to convert to an interger to allow the app to recognise the input:

```while(input !== 'quit'&& input !== 'q') {
    if(input === 'list') {
        console.log('******')
        for (let i = 0; i < todos.length; i++){
            console.log('${i}: ${todos[i]}')
        }
        console.log('******')
    }
    else if (input === 'new'){
        const newTodo = prompt('Ok, what is the new to-do?');
        todos.push(newTodo);
        console.log('${newTodo} added to the list!')        
    } else if (input === 'delete'){
        const index = parseInt(prompt('Ok, enter an index to delete;'));
        if (Number.isNaN(index)) {
            const deleted = todos.splice(index, 1);
            console.log('OK, deleted ${deleted[0]}');
        }
    }
```
