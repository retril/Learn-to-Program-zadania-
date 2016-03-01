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

words = []
say = gets.chomp
while say != ''
	temp = []
	pushed = false
	words.each do |x|
		if say < x and pushed == false
			temp.push say
			pushed = true
		end
		temp.push x
	end
	if pushed == false
		temp.push say 
	end
	words = temp.clone
	say = gets.chomp
end
puts words

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

#Chapter 8 zadania

def englishNumber number
  if number < 0 
    return 'Please enter a number that isn\'t negative.'
  end
  if number == 0
    return 'zero'
  end
  numString = ''

  onesPlace = ['one',     'two',       'three',    'four',     'five',
               'six',     'seven',     'eight',    'nine']
  tensPlace = ['ten',     'twenty',    'thirty',   'forty',    'fifty',
               'sixty',   'seventy',   'eighty',   'ninety']
  teenagers = ['eleven',  'twelve',    'thirteen', 'fourteen', 'fifteen',
               'sixteen', 'seventeen', 'eighteen', 'nineteen']
 
 left = number
  write = left/1000000
 left = left - write*1000000

 if write > 0
 	milions = englishNumber write
 	numString = numString + milions + ' milion'
	if left > 0
		numString = numString + ' '
	end	
 end
 
 
 write = left/1000
 left = left - write*1000
 if write > 0
 	thousands = englishNumber write
 	numString = numString + thousands + ' thousand'
 	if left > 0
 		numString = numString + ' '
 	end
 end




  write = left/100
  left  = left - write*100

  if write > 0
    hundreds  = englishNumber write
    numString = numString + hundreds + ' hundred'
    if left > 0
      numString = numString + ' '
    end
  end

  write = left/10
  left  = left - write*10

  if write > 0
    if ((write == 1) and (left > 0))
    
      numString = numString + teenagers[left-1]
     
      left = 0
    else
      numString = numString + tensPlace[write-1]
    end

    if left > 0
      numString = numString + '-'
    end
  end

  write = left
  left  = 0

  if write > 0
    numString = numString + onesPlace[write-1]
  end


  numString
end

puts englishNumber(1000)
puts englishNumber(10000)
puts englishNumber(1000000)

def BeerSong beers
beer = beers

while beers > 0 
	if beers == 1
		puts englishNumber(beers)+' bottles of beer on the wall, '+englishNumber(beers)+' bottles of beer.'
		beers = 'no more'
		puts 'Take one down and pass it around, '+beers+' bottles of beer on the wall.'
		beers = 0
	else
		puts englishNumber(beers)+' bottles of beer on the wall, '+englishNumber(beers)+' bottles of beer.'
		beers = beers-1
		puts 'Take one down and pass it around, '+englishNumber(beers)+' bottles of beer on the wall.' 
	end
	puts
end
beers = 'no more'
puts beers.capitalize+' bottles of beer on the wall, '+beers+' bottles of beer. 
Go to the store and buy some more, '+englishNumber(beer)+' bottles of beer on the wall.'	
end

puts BeerSong(1000)

#Chapter 9

born_time = Time.mktime(1997,10,25)
time1b = born_time +1000000000
puts born_time
puts time1b

puts 'When were you born?(year)'
y = gets.chomp
puts 'When were you born?(month)'
m = gets.chomp
puts 'When were you born?(day)'
d = gets.chomp
born_time = Time.mktime(y.to_i,m.to_i,d.to_i)
time = Time.new
age = time - born_time
age = age.to_i/60/60/24/365
puts
puts 'You are '+age.to_s+' years old.'

def BirthdaySpank age
	while age > 0
		puts 'spank!'.capitalize
		age = age -1
	end
end

puts BirthdaySpank(age)

class OrangeTree

  def initialize 
    puts 'You plant an orange tree.'
    @age = 0
    @height = 0
    @heightA = 0
    @oranges = 0
    @endoftree = rand(6) + 8
  end
  
  def height
    if @age == 0
     puts 'Your tree have '+ @height.to_s + ' meters.'
    else
      puts 'Your tree have '+ @height.to_s + ',' + @heightA.to_s + ' meters.'
    end
  end
  
  def oneYearPasses
    if @age == 0 
      puts 'Your tree was recently planted.'
    else
      if @age > 1
        if @oranges > 0
          if @oranges > 1 
            puts 'You lost ' + @oranges.to_s + ' oranges.'
            @oranges = 0
            @oranges = ((rand(4) + 1)*@age) +rand(1)
          else
            puts 'You lost ' + @oranges.to_s + ' orange.'
            @oranges = ((rand(4) + 1)*@age) +rand(1)
          end
        else
          puts 'You pick up all oranges in this year.'
          @oranges = ((rand(4) + 1)*@age) +rand(1)
        end
      else
        @oranges = ((rand(4) + 1)*@age )+rand(1)
      end
    end

    @age = @age +1
    puts 'Your tree grows.' 
    @heightA = rand(8) + 1
    if @age == 1
      @height = 0
      @heightA = rand(5)+1
      while @heightA < 4
        @heightA = rand(5)+1
      end
    else 
      if @height < 5 
        @height = @height + 1
        @heightA = rand(8)+1
        while @heightA < 4
          @heightA = rand(8)+1
        end
      else
        puts 'Your tree can\'t grows more.'
        puts 'Your tree\'s height don\'t change.'
      end
    end
    if @age == @endoftree
      puts 'Your tree dieing... ;('
      puts '...Maybe plant new...'
      puts 'Your tree was ' + @age.to_s + ' years.'
      exit
    end
  end 
  
  def countTheOranges
    if @oranges > 0
      if @oranges > 1
        puts 'Your tree has ' + @oranges.to_s + ' oranges.'
      else
        puts 'Your tree has last orange'
      end  
    else
      puts  'Your tree has no more oranges' 
    end
  end 

  
  def pickAnOrange
    if @oranges > 0
      @oranges = @oranges - 1
      puts 'This orange is so delicious'
    else
      puts 'Your tree has no more oranges'
    end
  end
end  


class Dragon

  def initialize name
    @name = name
    @asleep = false
    @stuffInBelly     = 10  
    @stuffInIntestine =  0  

    puts @name + ' is born.'
  end

  def feed
    puts 'You feed ' + @name + '.'
    @stuffInBelly = 10
    passageOfTime
  end

  def walk
    puts 'You walk ' + @name + '.'
    @stuffInIntestine = 0
    passageOfTime
  end

  def putToBed
    puts 'You put ' + @name + ' to bed.'
    @asleep = true
    3.times do
      if @asleep
        passageOfTime
      end
      if @asleep
        puts @name + ' snores, filling the room with smoke.'
      end
    end
    if @asleep
      @asleep = false
      puts @name + ' wakes up slowly.'
    end
  end

  def toss
    puts 'You toss ' + @name + ' up into the air.'
    puts 'He giggles, which singes your eyebrows.'
    passageOfTime
  end

  def rock
    puts 'You rock ' + @name + ' gently.'
    @asleep = true
    puts 'He briefly dozes off...'
    passageOfTime
    if @asleep
      @asleep = false
      puts '...but wakes when you stop.'
    end
  end

  private

  def hungry?
    @stuffInBelly <= 2
  end

  def poopy?
    @stuffInIntestine >= 8
  end

  def passageOfTime
    if @stuffInBelly > 0
      
      @stuffInBelly     = @stuffInBelly     - 1
      @stuffInIntestine = @stuffInIntestine + 1
    else  
      if @asleep
        @asleep = false
        puts 'He wakes up suddenly!'
      end
      puts @name + ' is starving!  In desperation, he ate YOU!'
      dead = 1
      exit 
    end

    if @stuffInIntestine >= 10
      @stuffInIntestine = 0
      puts 'Whoops!  ' + @name + ' had an accident...'
    end

    if hungry?
      if @asleep
        @asleep = false
        puts 'He wakes up suddenly!'
      end
      puts @name + '\'s stomach grumbles...'
    end

    if poopy?
      if @asleep
        @asleep = false
        puts 'He wakes up suddenly!'
      end
      puts @name + ' does the potty dance...'
    end
  end
end
puts 'Please chose name for your baby dragon'
name = gets.chomp
$pet =Dragon.new name.capitalize
puts
def talktodragon say 
  if say.downcase == 'feed' or say.downcase == 'puttobed' or say.downcase == 'put to bed' or say.downcase == 'walk' or say.downcase == 'toss' or say.downcase == 'rock' or say.downcase == 'help'
    if say.downcase == 'feed'
      $pet.feed
    end
    if say.downcase == 'puttobed' or say.downcase == 'put to bed'
      $pet.putToBed
    end
    if say.downcase == 'walk'
      $pet.walk
    end
    if say.downcase == 'toss'
      $pet.toss
    end
    if say.downcase == 'rock'
      $pet.rock
    end 
    if say.downcase == 'help'
      puts 'You can put this commands to your baby drgon:'
      puts 'feed'
      puts 'put to bed'
      puts 'walk'
      puts 'toss'
      puts 'rock'
    end
  else
    puts 'WRONG COMMAND!'
  end
end
puts 'Let\'s interact with your baby dragon !'
puts
puts 'You can put this commands to your baby drgon:'
puts 'feed'
puts 'put to bed'
puts 'walk'
puts 'toss'
puts 'rock'
puts 'If you do not remember this write help'
puts

dead = 1
while dead == 1
  dead = 1
  say = gets.chomp
  talktodragon say
end
