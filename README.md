
## Ruby Methods Study Guide

### Introduction
* A **method** *is a set of instructions that can be reused in a program*. Ruby comes with a set of predefined methods, but you can also write your own methods. A commony used method, especially when you're first learning Ruby, is `puts`. For instance, `puts "hello world"` will print "hello world" to the screen.
* To make a custom method, write `def`, short for define, add a space, then type the name that you want to call the method. When you are done with your method, finish it off with an `end`. Like this:

```ruby
# basic structure
def method_name
  # code
end

# basic example
def say_hi
  puts "hi"
end
```
* To get a method to run, you must call it. *To call a method, you simply write the name of the method after you've defined it.*

```ruby
def print_alphabet
  puts "abcdefghijklmnopqrstuvwxyz"
end
```
* The code above defines the method `print_alphabet`. This method essentially gives Ruby the instructions for how to print the alphabet but, on its own, it doesn't tell Ruby to _actually_ do it. It's like knowing how to ride a bike, but not physically getting on the bike and moving the pedals with your feet. If we want Ruby to actually execute this code and print "abcd.." to the screen, we have to **call on the method**. *We do this simply by writing the name of the method, in this case `print_alphabet`, anywhere below the `end` keyword.* See the example below:

```ruby
def print_alphabet
  puts "abcdefghijklmnopqrstuvwxyz"
end

print_alphabet
# abcdefghijklmnopqrstuvwxyz
# => nil
```

#### Example: No Arguments

```ruby
def answer_phone
  puts "Hello? Steph speaking."
end

answer_phone
```
The code above will print "Hello? Steph speaking." when it is run.

### Arguments
* **Arguments** make it easy to give methods information.
* To pass one argument to a method, you put parentheses after the name of the method. Within those parentheses, put the variable name that you want to stand for the information you're going to pass in. 

#### Example: One Argument
* For instance:

```ruby
def answer_phone(name)
  puts name
end

answer_phone("Steph")
answer_phone("Vic")
```
* When run, the code above will print "Steph" and then  will print "Vic". We can see that this is more flexible than the code above because the name can change to be any string, instead of being hardcoded as "Steph".

* If we want the method answer_phone to print "Hello this is" followed by the value of name, which in the case above is Steph then Vic, we have to add a `#` symbol and wrap the variable in curly brackets, see below. This is called **string interpolation**.

```ruby
def answer_phone(name)
  puts "Hello, this is #{name}."
end

answer_phone("Steph")
answer_phone("Vic")
```
* When run, the code above will print "Hello, this is Steph.", just like the first method in this overview. It will then print "Hello, this is Vic." 

#### Example: Multiple Arguments
* If we want to pass **multiple arguments** to the method, we *separate those arguments by commas when we define the method AND when we call on the method*.
* When defining the method, it helps to use descriptive words or phrases to describe what order the method is expecting the arguments in.

```ruby
def answer_phone(adjective, name)
  puts "Hello, it is a #{adjective} day at Flatiron School. This is #{name} speaking."
end

answer_phone("beeyootiful", "Steph")
answer_phone("super duper radtastic", "Vic")
```
The code above will print "Hello, it is a beeyootiful day at Flatiron School. This is Steph speaking." and then will print "Hello, it is a super duper radtastic day at Flatiron School. This is Vic speaking."

### Resources

Feel like you're getting the hang of it? Want more practice. Just do these catchup exercises and you'll be a-okay.

1. [Dev HQ](http://www.dev-hq.net/ruby/8--creating-methods) tackles writing your own methods.

2. Ruby Monk explains what [a method is](https://rubymonk.com/learning/books/1-ruby-primer/chapters/19-ruby-methods/lessons/57-being-methodical) and how to [call a method](https://rubymonk.com/learning/books/1-ruby-primer/chapters/19-ruby-methods/lessons/69-new-lesson).

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/hs-ruby-methods-catchup' title='Ruby Methods Study Guide'>Ruby Methods Study Guide</a> on Learn.co and start learning to code for free.</p>
