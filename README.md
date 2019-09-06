# Learning-Outcomes-ruby

## Learning outcomes: https://quizlet.com/186336511/ruby-building-blocks-flash-cards/
## Numbers, Operators and Expressions:
- What’s the difference between an Integer and a Float? /an integer must be a whole, real number. For fractions or  other inexact(Для дробей или других неточных) numbers, we create floating point numbers, or float objects, instead.
To convert a floating point number in Ruby to a Ruby integer, you’d simply wrap the float in an integer, as shown below:

      Integer (950.12)
      => 950
To convert an integer into a floating point number, simply wrap it in float, like so:

      Float (20)
      => 20.0

- Why should you be careful when converting back and forth between integers and floats? / Any arithmetic done with a Float, Ruby will treat the return value as a Float.

- What’s the difference between =, ==, and ===? /
Answer:
        = is an assignment operator
        == checks the equality of 2 values
        === checks the equality and type of 2 values

- How do you do exponents in Ruby? 

        value ** exponent
- What is a range?


      A sequence of numbers between a starting value and an ending value.
- How do you create a range? https://ruby-doc.org/core-2.5.1/Range.html

      (1..10)
      (1...10)
      Range.new(0,2) // (0..2)
      
- What’s the difference between (1..3) and (1...3)?

      (1..3) is inclusive [1,2,3]  and (1...3) is exclusive [1,2] 
- What are three ways to create a range?

      Range.new(0, 2)
      (0..2)
      (0...2)
## Strings:
* What’s the difference between single and double quotes?
  
      Both are essentially the same except string interpolation can only be performed inside double quotes. 
      Not single quotes.
* What is string interpolation?

String Interpolation occurs when you want to plug something else into a string, like a variable.
Simply use the pound symbol and curly braces #{} to do so

      > my_name = "Tiny Tim"
      > my_age = 25
      => "Tiny Tim"
      > my_string = "My name is #{my_name} !"
      => "My name is Tiny Tim!"
      Ruby's ability to run code within a string.
* What are escape characters?

      A string value proceeded with a backslash to represent a special meaning.
* What are line breaks?

      An escape character written as \n. This starts a newline within a string.


* How do you make other things into strings?

      .to_s
* How do you concatenate strings?

      Either the + operator or .concat
* How do you access a specific character or substring?

      string[index] or string[start, end]
* How do you split up strings into arrays?

      .split("")
* How are strings and arrays similar?

      Both can access their elements with square brackets.
* How do you get and clean up user input on the command line?

      .gets.chomp
* What does it mean that strings are “mutable” and why care?

      Mutable means the value can be modified. Not all value types are mutable.
* What is a symbol?

      An immutable object with its name proceeded with a semicolon. 
      They can never be changed. 
      Therefore they make great key names.
* How is a symbol different from a string?

      A string is mutable where as a symbol is immutable.
* What is a Regular Expression (RegEx)?

      A generic computer science method for matching a character or a set of characters in a string.   
* How can you center or right-justify a string?

      "hi".ljust(6,"") => "hi***"
      "hi".rjust(6) => " hi"
      "hi".center(6,"!") => "!!hi!!"
## Arrays:
- What are three ways to create an array?

      Array.new
      array = []
      %w{}
- How do you prepopulate the array with default data?

      Array.new(3) { |e| expression }
- How do you access items in an array?

      array[index]
- How can you access a specific group of items in an array?

      array[start, end]
- How do you modify the items in an array?

      array[index] = value
- How do you combine arrays?

      array + array
- How do you find the values in one array that aren’t in another?

      array1 - array2
      This takes away any and all values that are duplicate 
      in the right array from the left array.
- How do you find values in both arrays?

      [array]&[array]
- What is the difference between push/pop and shift/unshift?

      push appends a value to the end of an array where 
      pop removes the value from the end of the array.
      shift removes a value from the beginning of an array where 
      unshift prepends a value to the beginning.
- What is the shovel operator?

      <<
      It means the same thing as #push
- How is > arr.pop different from > arr[-1]?

      arr.pop is removing the last element of the array.
      arr[-1] is accessing the last element of the array.
- How is pushing or <<ing another array into your array different from just adding them together?

      Pushing prepends the right array as an element to the end of the left array.
      Adding the 2 arrays would concatenate them.
- How do you delete items in an array?

      .delete_at(index)
- Why should you be careful deleting items in an array?

      If you're deleting items inside a loop it will change the index of the other items.
- How can you convert arrays to strings?

      .join(delimeter)
- How can you convert from other data types to arrays?

      .to_a
- How can you figure out if an array contains a particular value?

      .include?(value)
- How do you find the biggest item in an array?

      .max
- How do you find the smallest item in an array?

      .min
- How do you remove any duplicates from your array?

      .uniq
- How do you find out how big an array is?

      .size or .length
- How do you put an array in order?

      .sort
- What are the naming conventions for arrays?

      Array names should be descriptive and plural.
- What should you store in arrays?

      Anything
## Hashes:
- What is a hash? 
        
       "a dictionary."

      A Hash is a dictionary-like collection of unique keys and their values.
      Also called associative arrays, they are similar to Arrays, 
      but where an Array uses integers as its index, a Hash allows you to use any object type.
- What are keys and values?

      
      "key is points to the memory location. Value is what's there"

      Hashes enumerate their values in the order that the corresponding keys were inserted.
- How is a hash similar to an Array?

      "it's still a collection of objects"

      Ruby's arrays and hashes are indexed collections. 
      Both store collections of objects, accessible using a key.
      Both arrays and hashes grow as needed to hold new elements.
      Any particular array or hash can hold objects of differing types; you can have an array containing an integer, a             string, and a floating point number
      Ruby hashes are similar to arrays. 
      A hash literal uses braces rather than square brackets. 
      The literal must supply two objects for every entry: one for the key, the other for the value.
      For example, you might want to map musical instruments to their orchestral sections. You could do this with a hash.
        instSection = {
          'cello'     => 'string',
          'clarinet'  => 'woodwind',
          'drum'      => 'percussion',
          'oboe'      => 'woodwind',
          'trumpet'   => 'brass',
          'violin'    => 'string'
        }
        Hashes are indexed using the same square bracket notation as arrays.
        instSection['oboe']	�	"woodwind"
        instSection['cello']	�	"string"
        instSection['bassoon']	�	nil
        - How is a hash different from an Array?

      With arrays, the key is an integer, whereas hashes support any object as a key.
- What are 3 ways to create a hash?

      Hash.new
      hash = {}
      .to_h
- What is the hash rocket?

      =>
      Assignment operator for key value pairs
      
      In Ruby you can create a Hash by assigning a key to a value with =>, 
      separate these key/value pairs with commas, and enclose the whole thing with curly braces.
- How do you access data in a hash?

      hash_name[key_name]
- How do you change data in a hash?

      hash_name[key_name] = value
- What types of data are good to store in a hash?

      Nuanced or more complex data than what would be put in an array.
      An object that has several different attributes.
- What are options hashes?

      A hash that is the last argument passed to a method.
      link_to 'click here', "http://www.example.com", :id => "my_special_link", :class => "clickable_link"
      
- How do you delete data from a hash?

      hash_name[key_name] = nil
      hash_name.delete(key_name)
- How do you add hashes together?

      hash1.merge(hash2)
- How do you list out all the keys or values?

      hash.keys
      hash.values
- How do you see if the hash contains a key or value?

      hash.key(key_name)
      hash.has_value(value)
- What is a set?

      A hash where all the values are either true or false. 
      Its useful because your computer can search more quickly 
      through this than an array trying to store the same information 
      due to way its set up behind the scenes.
## Dates and Times:  https://www.eriktrautman.com/posts/ruby-explained-dates-and-times
How do you get the current date and time?

      time = Time.now
      
    You can get an object that represents the current time using Time.now
    You can get the current date using Date.today
How do you find just the Year? Month? Hour? Second? Weekday?

    time = Time.now
    time.year
    time.month
    time.hour
    time.sec
    time.day

    The Date.parse method will try to parse any string that looks like a date.
    Date.parse("10/10/2010")  # -> 2010-10-10
    
    If you need something more strict you can use the Date.iso8601 method.
    An iso8601 date has the following format:
    year-month-day
- How do you create a Time specifically for 12/25/2013?

      time = Time.new(2013, 12, 25)
- How do you find how many days have passed between two Time’s?

      ((time1 - time2)/60/60/24).to_i
      "we're converting from seconds to minutes to days"
- What’s the difference between UTC and GMT and Local times?


      "UTC is the universal time"
      "GMT is based on english time"
- How would you find out the time that was 100 seconds ago? 10 days ago?

      "100 seconds ago:" Time.now-100
      "10 days ago:" Time.now - (10*24*60*60)
## Other Random Stuff:  https://www.eriktrautman.com/posts/ruby-explained-other-random-tidbits
- What is nil?

      nil is a special Ruby data type that means "nothing". it`s null
- How do you check if something is nil?

      .nil?
- What’s the difference between nil and blank and empty?

      nil? can be called on all objects and returns true for the nil object and false for anything else.
      empty? is a standard Ruby method on objects like Arrays, Hashes, and Strings. 
      Typically it returns true if the object         contains no elements.
      blank? is not a standard Ruby method but is added to all objects by Rails and returns true for nil, 
      false, empty, or a whitespace string.
- Are the following nil or empty? * " ", "", [], [""], {}
      
      "all empty, not nil"
      
- What’s the difference between puts and p and print?

      puts calls .to_s on the value, appends \n, and prints to the command line. Pretty output
      p calls .inspect on the value and prints to the command line. 
      Informative output print simply prints the value to the command line on 1 single line
      
      "p runs the inspect method"
      "puts runs the to_s method and adds a newline"
        "print runs to_s and doesn't add a new line"
- What does inspect do?

      Returns a string containing a human readable representation of obj.
      "inspect lets you see the innards of an object printed on the screen"
- What do +=, -=, *= and /= do?

        += "calls the + method of the first object and reassigns the memory location to the result"
        -= "is the same thing, but with the - method"
        a *= b "is the same as" a = a * b
        a /= b "is the same as" a = a/b
- What is parallel assignment?

        "when you assign the values of more than one variable at a time"
        a, b = "foo", "bar"
- What’s the easiest way to swap two variables?

      Parallel assignment
      var1, var2 = var2, var1
      
      a, b = b, a



## Conditionals and Flow Control:
- What is a “boolean”?

      A boolean is a value used in a logic statement to say if something is considered 
      true or 
      false.
- What are “truthy” values?

      0 - numeric zero (Integer or otherwise)
      "" - Empty strings
      "\n" - Strings containing only whitespace
      [] - Empty arrays
      {} - Empty hashes
- Are nil, 0, "0", "", 1, [], {} and -1 considered true or false?
      
      We can check using in terminal irb and next code:
      def check_truthy(var_name, var)
        is_truthy = var ? "true" : "false"
          puts "#{var_name} is #{is_truthy}"
        end

      check_truthy("nil", nil)
      check_truthy("0", 0)
      check_truthy("zero", 0)
      check_truthy("empty string", "")
      check_truthy("number one", 1)
      check_truthy("empty array", [])
      check_truthy("empty hash", {})
      check_truthy("number minus one", -1)
      
      // output next:
      nil is false
      0 is true
      zero is true
      empty string is true
      number one is true
      empty array is true
      empty hash is true
      number minus one is true
In Ruby, there are exactly two values which are considered "falsy", 
and will return false when tested as a condition for an if expression. 
      They are:

      nil
      boolean false
      
- When do you use elsif?
- When do you use unless?

            Синтаксис:

            view source
            unless условие [then]
               код
            [else]
               код ]
            end
Выполняет код, если условие false. Если условие true — будет выполнен код из else.
       With an if statement you can check if something is true.
       But when you want to check for “not true” there is two things you can do.
       use unless, which is like if, but it checks for “not true”: 
       
       unless condition
            # ...
       end
       
        Or you can use !:if !condition
            # ...
        end
- What does <=> do?
      Это общий оператор сравнения. 
      Он возвращает либо -1, 0, либо +1 в зависимости от того, 
      меньше ли его получатель, равен или больше его аргумента
      If the other object is not comparable then the <=> operator should return nil
      
      a <=> b :=
      if a < b then return -1
      if a = b then return  0
      if a > b then return  1
      if a and b are not comparable then return nil
      
 The Spaceship Operator <=> is a special one that comes up because it actually gives three different possible outputs depending on whether the left side is greater than, less than, or equal to the right side.

            > 1 <=> 1000
            => -1
            > 1 <=> 1
            => 0
            > 1 <=> -1000
            => 1
      
     The spaceship method is useful when you define it in your own class and include 
     the Comparable module https://ruby-doc.org/core-2.6.4/Comparable.html. 
     
     Your class then gets the >, < , >=, <=, ==, and between? methods for free.

            class Card
              include Comparable
              attr_reader :value

              def initialize(value)
                @value = value
              end

              def <=> (other) #1 if self>other; 0 if self==other; -1 if self<other
                self.value <=> other.value
              end

            end

            a = Card.new(7)
            b = Card.new(10)
            c = Card.new(8)

            puts a > b # false
            puts c.between?(a,b) # true

       #Array#sort uses <=> :
      p [a,b,c].sort 
      => [#<Card:0x0000000242d298 @value=7>, #<Card:0x0000000242d248 @value=8>, #<Card:0x0000000242d270 @value=10>]

- Why might you define your own <=> method?
cause <=> it's actually a method and you can override it in your own classes.
<=> на самом деле это метод, и вы можете переопределить его в своих собственных классах.

Это наиболее часто используется в методах сортировки. 
Представьте, что вы создали класс Person и хотите отсортировать массив объектов Person. 
Сначала вы должны научить Ruby сравнивать двух людей, определив метод # <=> для класса Person:

            def Person
              def <=> (other_person)  # to compare two people, use last names
                self.last_name <=> other_person.last_name
              end
            end # now we can run people_array.sort, woohoo!
- What do || and && and ! do?

|| (the pipe symbol, usually on the same key as the backslash) aka or, 
meaning that if EITHER of the two sides is true, the expression is true (else false)

&& aka and, meaning both sides must be true for the full expression to evaluate to true

! aka not, which reverses the expression from true to false or false to true

            > ( false || true ) && !(true && true ) 
            => false
- What is returned by puts("woah") || true? / return true cause true || true => true
      
      irb(main):001:0> puts("woah") || true
      woah
      => true

- What is ||=?

      it basically expands to thing_a || thing_a = thing_b
Поэтому, если thing_a не был установлен на что-либо, он становится thing_b, 
иначе он сохраняет свое первоначальное значение.
Если thing_a еще не был назначен чему-либо, то это nil, а Ruby проверяет правую часть || чтобы увидеть, может ли это быть true, что включает запуск выражения для установки thing_a = thing_b

Если ему уже присвоено значение, оно просто сохраняет это значение как нормальное.

- What is the ternary operator? // условие ? если_true : если_false
Тернарная операция (от лат. tri — три) — операция, имеющая 3 операнда:
Тернарная условная операция — операция в информатике, возвращающая свой второй или третий операнд в зависимости от логического значения первого операнда.
           
           if a then b else c end === a ? b : c
           
     condition ? do_this_if_true : do_this_if_false

So:

      > true ? puts "I like truth" : puts "not gonna happen"
      "I like truth"
      => nil
- When should you use a case statement?
wWhere you're really just checking to see if something equals any one of a number of clear but different options, a case statement can be a good substitute
It basically lets you construct a chain of logic that says "if x equals option_a, do this, if it equals  option_b, do this, if it equals option_c, do this... and otherwise do this."

            case current_user.energy   # Assume it's an value 1-3
            when 3
                puts "Go run a marathon!"
            when 2
                puts "Go for a walk."
            when 1
                puts "Go take a nap"
            else
                puts "You're only supposed to have energy of 1,2 or 3..."
                
## Iteration:
- What does loop do? 
A loop is really just code that will run a number of times until some condition is met. 

Цикл - это просто код, который будет выполняться несколько раз, пока не будет выполнено какое-либо условие. 
Переменная, как правило, используется для отслеживания того, на какой итерации вы находитесь, 
или для другого увеличения, пока не будет выполнено условие. Это называется индексной переменной.
Цикл - это самый простой способ зацикливания в Ruby, и он не так уж часто используется, потому что другие способы зацикливания намного сексуальнее. 
цикл занимает блок кода, обозначаемый либо {...}, либо do ... end (если он состоит из нескольких строк). 
Это будет продолжаться до тех пор, пока вы не скажете ему прекратить использовать оператор break:

      > loop { puts "this will not stop until you press CTRL+c" }
      this will not stop until you press CTRL+c
      this will not stop until you press CTRL+c
      ... and so on

      > i=0                   # Our index variable
      > loop do
      >   i+=1
      >   print "#{i} "
      >   break if i==10
      > end
      1 2 3 4 5 6 7 8 9 10 => nil
- What are the two ways to denote a block of code?

      loop takes a block of code, denoted by either  { ... } or do ... end (if it's over multiple lines). 
      It will keep looping until you tell it to stop using a break statement
- What is an index variable?
 A variable is typically used to keep track of which iteration you are on or to otherwise increment 
 until the condition is reached
- How do you print out each item of a simple array [1,3,5,7] with:
loop?

            array = [1,3,5,7]
             i=0                   
             loop do
             print "#{array[i]} "
               i+=1
               break if i==array.size
             end
          #output: 3 5 7  => nil

while?

            array = [1,3,5,7]
             i=0
             while i <=array.size
               print "#{array[i]} "
               i+=1
             end
             #output: 1 3 5 7  => nil
for?

            array = [1,3,5,7]
             for arr_number in (0..array.size)
               print "#{arr_number} "
             end
             #output: 0 1 2 3 4 => 0..4
#each?

             array = [1,3,5,7]
             array.each do |array_value|    
               print "#{array_value}! "
             end
             #output: 1! 3! 5! 7! => [1, 3, 5, 7]

#times?

       array = [1,3,5,7]
       array.length.times do |num|
           print "#{num}!"
       end
      #output: 0!1!2!3!=> 4



- What’s the difference between while and until?
until выполняется до тех пор, пока указанное условие ложно

      until is almost identical to while but, 
      instead of running as long as the specified condition is true, 
      it runs as long as the condition is false
- How do you stop a loop?
break will stop the current loop. Often used with an if to specify under what conditions to do that
to stop using a 

      break 
  statement
- How do you skip to the next iteration of a loop?
      
      next 
will jump to the next iteration. Also usually used with an if statement.
- How would you start the loop over again?

      redo 
will let you restart the loop (without evaluating the condition on the first go-through), again usually with some condition
- What are the (basic) differences between situations when you would use while vs #times vs #each?

      #each for any time you want to do stuff with every item in an array or hash, and 
      #times for the simple cases when you just want to do something a fixed number of times.
- What does nesting loops mean and when would you use it?
Вложенные циклы происходят, когда один переходит внутрь другого, 
поэтому вы выполняете весь внутренний цикл для каждой итерации внешнего цикла.

## Blocks, Procs, and Lambdas:
- How is a block like a function?

-How is a block different from a function?

-What are the two ways to declare a block?

-How do you return data from a block?

What happens if you include a return statement in a block?
Why would you use a block instead of just creating a method?
What does yield do?
How do you pass arguments to a block from within a method?
How do you check whether a block was actually passed in?
What is a proc?
What’s the difference between a proc and a block?
When would you use a proc instead of a block?
What is a closure?
What is a lambda?
What’s different between a lambda and a proc?
What is a Method (capital “M”)?
What do Methods basically allow you to do that could probably be pretty interesting when you’re writing some more advanced programs later on?

## Enumerable and Modules:   https://www.eriktrautman.com/posts/ruby-explained-map-select-and-other-enumerable-methods
What is a module?
Why are modules useful?
What does #each do?
What does #each return?
What does #map do?
What does #map return?
What is the difference between #map and #collect?
What does #select do?
What does #select return?
What is the difference between #each #map and #select?
What does #inject do?
When might you use #inject?
How do you check if every item in a hash fulfills a certain criteria?
What about if none of the elements fulfill that criteria?
What (basically) is an enumerator?

## Writing Methods:
How many things should a method ideally do?
What types of things should a method modify?
What should you name a method?
What does self mean?
What do you need to do to create your own Ruby script file?
How would you run a Ruby script from the command line?
How can you check whether your script was being run from the command line?
What is a shebang line?
What does require do?
What does load do?
What is the difference between require and load?
How do you access any parameters that were passed to your script file from the command line?
What does #send do?
When would #send be used that’s different from just running the method on an object ‘normally’?
