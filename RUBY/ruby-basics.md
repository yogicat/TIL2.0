# intro to backend

* Backend usually consists of 3 parts :  a server, an application, and a database
* Backend is the structure that allows information to be shared across accounts or people. It’s the glue that binds the internet together.

- - - -

## Ruby Basics

### interpreted language

’interpreted’ programming language - it can’t run itself directly. It need VM(virtual machine)


When you run `ruby my_program.rb` on your terminal you’re actually loading the`ruby`virtual machine which in turn loads your `my_program.rb`


IRB - Interactive Run Shell
Start IRB y opening Terminal and typing `irb`


**Naming Convention**

* always start with a lowercase letter
* use **snake case** - `students_in_class`, `first_lesson`
* name after the **meaning** of their content, not the type of their contents

---

### String

**Substrings**

```rb
greeting = "hello world!"

greeting[0...4] = "hell"
greeting[0...-4] = "hello wo"
greeting[-4] = "r"
```


**String Methods**

* `.length` - includes spaces and characters.
* `.split` -  returns a new array
* `.sub` - Substitute. Replaces just a single occurange
* `.grub` - Global Substitute. Replaces all occurrences.

```rb
greeting = "Hello Everyone!"
greeting.length
// => 15


greeting.split
// => ["Hello", "Everyone!"]
greeting = "Hello Everyone!"
// greeting은 바뀌지 않는다.
greeting.split("")
// => ["H", "e", "l", "l", "o", " ", "W", "o", "r", "l", "d", "!"]


greting.sub["Everyone", "Friends"]
// => Hello Friends

```


* String Concatenation

```rb
name = "Frank"
puts "Hello " + name + "!"
// => Hello Frank
```


* String Interpolation

```rb
name = "Frank"
puts "Hello #{name}!"
// => Hello Frank!
```

- - - -

### Symbols

- Symbol starts with a colon then one or more letters
- ex) `:flag` or `:best_friend`
- like *named integer*
- Symbols are defined in a global symbol table
- Value cannot change

---

### Numbers

- integers and floats
- Integers have a bunch of methods
- `5.methds` to see methods

```rb
  5.times do
    puts "Hello, World!"
  end
```

---

### Blocks

- A way of bundling up a set of instructions for use elsewhere
- Block starts with `do` and ends with `end`
- For single instruction, use `{`and  `}`

**Block Parameters**

-  `|someparam|` Use pipe characters to spicify a lock parameter.

```rb
  5.times do |i|
    puts "#{i}: hello"
  end
```

```rb
  "hello world".gsub("l"){|el| el.upcase}
  => "heLLo worLd"
```

*`gsub` is using the result of the `block` as the replacement for the original match.*

---

### Arrays

- `<<` add an element to the end of an array. **push**
- `.last` , `.first`
- `.sort` - return a new sorted array (alphabetacla, ascending value)
- `.shuffle`
- `each` -> iterate through each element
- `collect`

```rb
  friends = ["Emmet", "Batman", "Unikitty", "Lucy"]
  friends.each { |a| puts "#{a} is my friend"}
  friends.collect { |a| a + "?" }
```

*more at http://www.ruby-doc.org/core-2.1.2/Array.html*

---

### Hashes

- Hash is a collection of data where each element of data is addressed by a name.
- Like a refrigerator (we don't care about what shelf it's on.)
- Order doesn't matter
- Organize things by *name*
- **Key/Value pairs**
- *Similar* to JS's object
- Can't assign a method as a value! (unlike JS!)


```rb
  # creating hash
  produce = {"apple" => 3, "banana" => 1, "avocado" => 10}

  # creating hash using symbol for key
  produce = {apple: 3, banana: 1, avocado: 10}
```

---

### Nil & Nothingness

nil => nothing!


---


### Objects, Attriutes, Methods

Ruy is an Object Oriented programming language.

**Classes and Instances**

```rb
  class Student
    attr_accessor :first_name, :last_name, :primary_phone_number

    def introduction
      puts "Hi, I'm #{first_name}!"
    end
  end
```

Class itself doesn't represent a student, it's the **idea** of what a student is like. To represent an actual student we create an *instance* of that class.

```rb
  yogicat = Student.new
  yogicat.first_name = "Dahe"
  yogicat.introduction
```

**Method Arguments**

```rb
  class Student
  attr_accessor :first_name, :last_name, :primary_phone_number

    def introduction(target)
      puts "Hi #{target}, I'm #{first_name}!"
    end
  end

  frank = Student.new
  frank.first_name = "Frank"
  frank.introduction('Katrina')
  # => Hi Katrina, I'm Frank.
```

In Ruby, every time you call a method you get a value back. By default, a Ruby method returns the value of the last expression it evaluated.


