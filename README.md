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

#Chapter 3 ćw
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

#Chapter 4 zadania
puts 'Hello ,What is your name?'
name = gets.chomp
puts 'Okay and your surname?'
names=gets
puts 'Hello ,my friend '+name+' '+names

puts 'What is your favourite number'
number = gets
number = number.to_i+1
puts 'The number is bigger and better than your favourite number '+number.to_s

#Chapter 5 zadania
puts 'WHAT YOU WANT ?'
want = gets.chomp
puts 'WHADDAYA MEAN "'+want.upcase+'"?!?  YOU\'RE FIRED!!'

space = 50.5
puts 'Table of Contents'.center space
puts 'Chapter 1:  Numbers'.ljust(space/2) + 'page 1'.rjust(space/2)
puts 'Chapter 2:  Letters'.ljust(space/2) + 'page 72'.rjust(space/2)
puts 'Chapter 3:  Variables '.ljust(space/2) + 'page 118'.rjust(space/2)

#Chapter 6 zadania
beers = 99
beer = beers	
while beers > 0 
	if beers == 1
		puts beers.to_s+' bottles of beer on the wall, '+beers.to_s+' bottles of beer.'
		beers = 'no more'
		puts 'Take one down and pass it around, '+beers+' bottles of beer on the wall.'
		beers = 0
	else
		puts beers.to_s+' bottles of beer on the wall, '+beers.to_s+' bottles of beer.'
		beers = beers-1
		puts 'Take one down and pass it around, '+beers.to_s+' bottles of beer on the wall.' 
	end
	puts
end
beers = 'no more'
puts beers.capitalize+' bottles of beer on the wall, '+beers.to_s+' bottles of beer. 
Go to the store and buy some more, '+beer.to_s+' bottles of beer on the wall.'	

say = gets.chomp
n = 0
while n != 3
	if say == say.upcase and say != 'BYE'
		t = (rand(1951))
		while t <= 1930
			t = (rand(1951))
		end
		puts 'NO, NOT SINCE '+t.to_s+'!'
		puts 'ANYTHING ELSE!?'
		say = gets.chomp
	else
		puts 'HUH?!  SPEAK UP, SONNY!'	
		say = gets.chomp
	end

	if say == 'BYE'
		n=(n+1)
	else
		n=0
	end	

end

puts 'BYE !'

puts 'Enter starting year.'
year1=gets.chomp
puts 'Enter ending year.'
year2=gets.chomp
if year2.to_f%4 == 0 and year2.to_f/100 != year2.to_i/100 
		year2 = year2
else if year2.to_f/400 == year2.to_i/400 
			year2 = year2
	else
			x=year2.to_i%4
			year2=year2.to_i-x	
	end
end	
puts
puts 'Leap-years beetwen those which You have entered'	
while year1.to_f <= year2.to_f
	if year1.to_i%4 == 0 and year1.to_f/100 != year1.to_i/100 
		puts year1.to_i
		year1=year1.to_i+4
	else if year1.to_f/400 == year1.to_i/400 
			puts year1.to_i
			year1=year1.to_i+4
		else
			r=year1.to_i%4
			r1=4-r
			year1=year1.to_i+r1
		end
	end		
end
puts 'END'

#Chapter 7 zadania

words = []
say= gets.chomp
while say != ''
	words.push say
	say= gets.chomp
end	
puts words.sort

chapters = ['1.Numbers', '2.Letters', '3.Variables']
pages = [1, 72, 118]
space = 50.5 
puts 'Table of Contents'.center space 
puts
chapters_full = []
pages_full = []
n = 0
chapters.each do |ch| 
	
	chapters_full.push 'Chapter '+ ch 
end
pages.each do |p|
	pages_full.push 'page '+ p.to_s

end
n=0
pages_full.each do |pf|
	puts chapters_full[n].ljust(space/2) + pf.rjust(space/2)
	n=n+1
end
