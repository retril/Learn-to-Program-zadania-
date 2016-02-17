# Learn-to-Program-zadania-
# Chapter 1 zadania
puts "I year are" 
puts 365*24 
puts "hours"

puts "In decade are"
puts 10*365*24*60
puts "minutes"

puts "I am "
puts 18*365*24*60*60
puts "seconds old"

puts "a lot "

puts "If I am 1246 million seconds old, how old am I?"
puts 1246000000/60/60/24/365

#Chapter 2 ćw
puts 'Hello, world!'
puts ''
puts 'Good-bye.'

puts 'I like' + 'apple pie.'

puts  12  +  12
puts '12' + '12'
puts '12  +  12'

puts  2  *  5
puts '2 ' *  5
puts '2  *  5'

puts 'You\'re swell!'

puts 'backslash at the end of a string:  \\'
puts 'up\\down'
puts 'up\down'

#Chapter 3
puts '...you can say that again...'

myString = '...you can say that again...'
puts myString

name = 'Szymon'
puts 'My name is ' + name + '.'
puts 'Wow!  ' + name + ' is a really beautiful name!'

composer = 'Mozart'
puts composer + ' was "da bomb", in his day.'

composer = 'Beethoven'
puts 'But I prefer ' + composer + ', personally.'

var = 'just another ' + 'string'
puts var

var = 5 * (1+2)
puts var

var1 = 8
var2 = var1
puts var1
puts var2

puts ''

var1 = 'eight'
puts var1
puts var2

#Chapter 4
puts 'Hello ,What is your name?'
name = gets.chomp
puts 'Okay and your surname?'
names=gets
puts 'Hello ,my friend '+name+' '+names

puts 'What is your favourite number'
number = gets
number = number.to_i+1
puts 'The number is bigger and better than your favourite number '+number.to_s
