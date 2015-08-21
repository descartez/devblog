# Ruby Basics
## `p` vs `puts`

### Setting up the file:

Put the following code into a `.rb` file:

```ruby
string = "hello I am string"
num = 1
```

Now run that file. Nothing will happen. That's because while we've assigned some variables, we haven't told it to _do_ anything with those variables.

### `p` statements
Add on to the file:
```ruby
string = "hello I am string"
num = 1

# this code tests p statements

p string
p num
```
Output should look like:

```
"hello I am string"
1
```

Now change the code so it looks like this:
```ruby
p string = "hello I am string"
p num = 1

# this code tests p statements

# p string
# p num

```
Output should look exactly the same as before. This is because `p` statements can still return a value, even when they are before a variable assignment. Puts statements do the same thing, but with some differences, which we'll get to.

Change the code back to look like this:
```ruby
string = "hello I am string"
num = 1

# this code tests p statements

p string
p num
```

### `puts` statements

Add in some `puts` statements now:
```ruby
string = "hello I am string"
num = 1

# this code tests p statements

p "Some p"
p string
p num

# this code tests puts statements

puts "Now some puts"
puts string
puts num
```

What you should see:
```
"Some p"
"hello I am string"
1
Now some puts
hello I am string
1
```

Notice something? When a `p` statement runs, it returns something very important. It gives information regarding the _data type_ of the thing being given.

Very important if you run _this_:
```ruby
num = 1
num_string = "1"

p num
p num_string
```
Which returns _this_:
```
1
"1"
```
Very important when you're tracking a bug down. So many problems arise from a datatype error. If we're trying to do math, but one of our numbers is a string, the program will break. If we just used `puts` statements, you'd never see it, because `puts` doesn't give us a datatype when printing strings. It would just look like:

```
1
1
```

Which is only half the problem. This is also why we `p` parts of the code we think are broken, rather than `puts`.

The difference between `p` and `puts` is in their intent. If we want to give information, with no regard to the datatype (like error messages), then `puts` is a good start. But if we're debugging, when in doubt, `p` it out. We need as _much_ info as possible.

