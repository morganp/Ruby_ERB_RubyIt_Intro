!SLIDE 
# Ruby #

!SLIDE
# Ruby #

* Ruby the main language
* Rails a web development framework
* IRB Interactive Ruby
* ERB Embedded Ruby

!SLIDE small
# [About Ruby][] #
* Created by Yukihiro Matsumoto aka “matz”
* Version 0.95 release in 1995
* Based on: Perl, Smalltalk, Eiffel, Ada, and Lisp

# Ruby Philosophy #

* Follows the principle of least surprise
* A natural language (not a simple one)
* <strong> Rails </strong> promotes convention over configuration 

[About Ruby]: http://www.ruby-lang.org/en/about/

!SLIDE
# Helloworld #

    @@@ ruby
    #!/usr/bin/env ruby  
   
    # Ruby Comment   
    puts "Helloworld!" 


!SLIDE 
# Ruby Control Flow (1)#

    @@@ ruby
    if var == 10
        puts “Variable is 10”
    elsif var == 20
        puts “Variable is 20″
    else
        puts “Variable is other”
    end

    if not var == 10
      print “Variable not 10”
    end

    if var == 1 or var == 2
      print “Variable 1 or 2”
    end

!SLIDE small
# Ruby Control Flow (2) #
Integer case

    @@@ ruby
    i = 8
    case i
    when 1, 2..5
      puts "1..5"
    when 6..10
      puts "6..10"
    end

Case with text

    @@@ ruby
    j = "mat"
    case j
    when 'on', 'the'
      puts "incedantal"
    when /.at/
      puts "begins xat"
    end

[Source](http://www.rubyist.net/~slagell/ruby/control.html)

!SLIDE small
# Ruby Control Loops #
## Traditional For Loop ##

    @@@ ruby
    for i in (0..9)
      puts i
    end

## Idiomatic Ruby ##

    @@@ ruby
    (0..9).each do |i|
      puts i
    end

## Cleaner Syntax ##
'...' instead of -1

    @@@ ruby
    (0...10).each do |i|
      puts i
    end

!SLIDE
# true or false #

Unassigned values are nil.

    @@@ ruby
    1     is true
    0     is true
    ""    is true

    nil   is false
    false is false

## Try it in IRB ##

    @@@ ruby
    puts 'true' if 1

!SLIDE
# Variables #

    @@@ ruby
    A_CONSTANT  = 123
    a_integer   = 12
    a_float     = 12.3
    a_string    = “123.4”
    a_array     = []
    a_hash      = {}

    :a_symbol   => hash #lightweight string

More Info on [strings][], [arrays][] and [hashes][]

[strings]: http://www.ruby-doc.org/core/String.html
[arrays]: http://www.ruby-doc.org/core/Array.html
[hashes]: http://www.ruby-doc.org/core/Hash.html

!SLIDE
# Arrays are Dynamic #
## but not sparse ##

    a_array = [0,1]
    a_array[3] = 3
    puts a_array.inspect
    > [0, 1, nil, 3]


!SLIDE
# Hashes #

    @@@ ruby
    a_hash = {:one => 1, :two => 2}
    puts a_hash[:one]
    > 1

    a_hash[:one] = 3
    puts a_hash[:one]
    > 3

    a_hash[:three] = 1
    puts a_hash
    > {:one=>3, :two=>2, :three=>1}


  

!SLIDE
# Variable Scope (1)#
## Local Variable (no sigil)##
.notes no sigil

    @@@ ruby
    local_variable = 0 

## Instance Variable (@)##
Available within Class, each instance is unique.

    @@@ ruby
    @instance_variable = 0

!SLIDE
# Variable Scope (2)#
## Class Variable (@@) ##
Best Avoided.
Available to all instances of Class, including inheritance.  
Only one version exisits.

    @@@ ruby
    @@class_variable = 0

## Global ($) ##
Available to all, one version exists.
    
    @@@ ruby
    $global_variable = 0 

!SLIDE 
# Summary #
## Variable Types ##
.notes Implicit Typing

    @@@ ruby 
    CONSTANT_VARIABLE  = 0
    a_integer          = 12
    a_float            = 12.3
    a_string           = “123.4”
    a_array            = []
    a_hash             = {}

## Variable Scope ##

    @@@ ruby
    local_variable     = 0 
    @instance_variable = 0
    $gloabl_variable   = 0

!SLIDE
#Summary of Style#

    @@@ ruby
    require 'use_lower_case'
    a_new_var = UseLowerCase.new()

* ClassesAreCamelCase
* variables\_are\_comma\_delimited
* require 'use\_lower\_case'

