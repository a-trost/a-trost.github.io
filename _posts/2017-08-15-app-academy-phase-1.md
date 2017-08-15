---
layout: post
title: "App Academy Prep Work Day 1"
date: 2017-08-15
---
## What’s the same between Ruby and Python?

Coming from knowing some Python and Django, I’m expecting I’ll see a lot of similarities in Ruby/Rails. 
Instead of ‘python’ in the terminal, it’s simply ‘irb’
`print() = puts ()`
Printing numbers and strings are all the same as in python.
`fdiv` divides and gives fractional answers
`%` is still the modulo, giving the remainder, just like in Python.
This helps for even numbers, like 
```
if x % 2 == 0:
	return "Even"
```

variables are named the same way, and take the same format of `variable_name` with underscores and all lowercase.

Reassignment of variables is the same, too. It’s allowed.

`input()` ’s equivalent in ruby seems to be `puts()`
It’s so far unclear if you can give it a string to say first, like in C.

If a method doesn’t take an argument in Ruby, it doesn’t need to have the (), which I’m pretty sure is different from in Python. I like the () because it makes it pretty clear to me that it’s a method. However, it seems to be common practice in Ruby to drop the () because it looks cleaner. Can’t argue with that.

The `int()` function in Python seems to be `.to_i` in Ruby, for ‘turn to integer’. 

Concatenation is alive and well, allowing me to use `+` to combine strings quickly. 
You can do:
```
variable.to_i
"43".to_i
```

Of course, adding strings and ints/floats doesn’t work in Ruby, either. 

#### Changing to string:
`.to_s`

### The Chomp Method
I don’t know of anything in python that does this, save for `end=“”` as an arg for print().
`chomp` is for removing new lines at the end. Interesting to have an entire method just for this purpose. I don’t know which would be better, as an arg or as its own function, that way you can apply it to things other than print().

`name.chomp` does NOT edit the actual string.

And that’s the end of chapter 1. Nothing too crazy or new.
