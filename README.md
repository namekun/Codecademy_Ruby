# Learn Ruby by Codecademy

## 1.Learn RUBY!

1. Data Types : Numbers, Strings, Booleans

````ruby
my_num =  25  
my_boolean = true   
my_string =  "Ruby" 
puts my_num
puts my_boolean
puts my_string
````

2. Variables

````ruby
my_num = 25 # 변수 선언
````

3. Math

````
#더하기 (+)
#빼기 (-)
#곱하기 (*)
#나누기 (/)
#지수화 (**)
#나머지 (%)
````

4. Puts & Print

````ruby
puts "What's up?" # puts는 println()
print "Oxnard Montalvo" # print는 print() 라고 생각하는 것이 편합니다.
````

5. Everything in Ruby is an Object

- 루비의 모든것은 객체라고 할 수 있습니다. 
- 루비에서의 모든 것에는 메소드가 내장되어있습니다.

6. .length Method

- Method를 사용하는 방법은 뒤에 .을 붙이는 것입니다.
- String에서 글자의 길이를 알려주는 Method '.length'를 사용해봅시다.

````ruby
puts "I Love My Bag".length
````

7. reverse Method

- String의 Method중 하나인 .reverse는 글자의 순서를 거꾸로 뒤집어 주는 Method입니다.

````ruby
"Hi guys".reverse
````

8.  upcase & downcase

````ruby
"hello world".upcase # ==> HELLO WORLD
"HELLO WORLD".downcase # ==> hello world	
````

9. comments

````ruby
# 주석은 이렇게도 할 수 있고
=begin
이렇게도 한꺼번에 할 수 있습니다.
=end
````

10. Naming Conventions

- 지역변수를 선언할때는 몇가지 지켜야할 규칙이 있습니다.
- 소문자로 시작해야합니다.
- 단어간의 구별에는 _를 사용합니다.
- 만약, 변수에 $, @와 같은 기호가 들어가 있다면, 루비는 실행되지 않을 것입니다.



## 2.PUTTING THE FORM IN FORMATTER

What You'll Be Building

*script.rb*

````ruby
print "What's your first name? " # make question
first_name = gets.chomp # Getting Input, 'get' gets input from user, 'chomp' removes that extra line. without 'chomp', you'll get extra blank
first_name.capitalize! # !는 firstname에 capitalize한 값을 저장해준다. 그러므로 다음에 first_name을 다시 불러와도 capitalize된 상태 그대로 나온다. 이것은 upcase와 같은 다른 Method에도 해당.

print "What's your last name? "
last_name = gets.chomp
last_name.capitalize!

print "What city are you from? "
city = gets.chomp
city.capitalize!

print "What state or province are you from? "
state = gets.chomp
state.upcase!

puts "Your name is #{first_name} #{last_name} and you're from #{city}, #{state}!"
````

​	

## 3.CONTROL FLOW IN RUBY

1. *script.rb*

````ruby
print "Integer please: "
#user_num = Integer(gets.chomp)
user_num = gets.chomp.to_i

# python이나 java와 다르게 ruby는 if 문 뒤에 end가 붙어야한다. 잊지말것.
if user_num < 0
  puts "You picked a negative integer!"
elsif user_num > 0 # 다른 언어와 같게 조건은 ==, != 이런식으로 똑같이~
  puts "You picked a positive integer!"
else
  puts "You picked zero!"
end
````

2. unless

````ruby
hungry = false

unless # = if !hungry 즉, 조건이 참이 아닐때.
  puts "I'm writing Ruby programs!"
else
  puts "Time to eat!"
end
````

3. true or false

````ruby
is true = 2 != 3
is false = 2 == 3
````

4. Less Than or Greater Than

````ruby
test_1 = 17 > 16
test_2 = 21 <= 30
test_3 = 9 <= 9
test_4 = -11 < 4
````

5. &&

````ruby
true && true # => true
true && false # => false
false && true # => false
false && false # => false
````

6. ||

````ruby
true || true # => true
true || false # => true
false || true # => true
false || false # => false
````

7. Not

````ruby
!true # => false
!false # => true
````

8. Combine

````ruby
# boolean_1 = (3 < 4 || false) && (false || true)
boolean_1 = true

# boolean_2 = !true && (!true || 100 != 5**2)
boolean_2 = false

# boolean_3 = true || !(true || false)
boolean_3 = true	
````

9. a short hand if/unless statement

````ruby
problem = false
print "Good to go!" unless problem
# 조건문이 단 하나라면, 출력문 뒤에 조건문을 붙여주는 경우도 있다. 
# 이는 unless뿐아니라, if에도 적용될 수 있다.
````



## 4.THITH MEANTH WAR!

1. THTH!!

````ruby
print "Thtring, pleathe!: "
user_input = gets.chomp
user_input.downcase!

if user_input.include? "s"
  user_input.gsub!(/s/, "th")
else
  puts "Nothing to do here!"
end
  
puts "Your string is: #{user_input}"
````

2. Build up MyCode

````ruby
print "노홍철의 발음으로 바꿔드립니다. : "
user_input = gets.chomp
user_input.downcase!

if user_input.include? "s" # .include? 조건 => 해당 변수에 조건을 포함하는가?
   user_input.gsub!(/s/, "th") # .gsub(/바꾸려는것/, "바꾼것"). 해당 string에서 글자를 바꿔준다.
   puts user_input
else 
   puts user_input
end
````



## 5.LOOPS & ITERATORS

1.  The 'While' Loop

````ruby
counter = 1
while counter < 11
  puts counter
  counter = counter + 1
end
````

2. Until Loop

````ruby
counter = 1
until counter > 10 #counter가 10보다 커질때까지
  puts counter
  # Add code to update 'counter' here!
  counter +=1
end
````

3. For Loop

````
for num in 1..15 # 1..15는 1에서 15까지, 1...15는 1에서 14까지
  puts num
end
````

4. Loop Method

````ruby
i = 20
loop do # for, while과 다르게 break로 지정해줘야 한다. loop문의 시작과 끝은 do - end
  i -= 1
  print "#{i}"
  break if i <= 0
end
````

5. Next if

````ruby
i = 20
loop do
  i -= 1
  next if i % 2 != 0 # next if 조건문 으로 한번더 걸러준다. 굳이 두번 if 쓸 이유없다는 소리
  print "#{i}"
  break if i <= 0
end
````

6. Array

```ruby
my_array = [1, 2, 3, 4, 5]
```

7. .each

```ruby
# 집합(배열이나 해시) 안의 요소들을 반복시켜 어떤 작업을 해야한다면, .each 메소드를 사용하면 된다

object.each { |item| 
  # Do something 
}

# {}은 do로 대체해서 사용할 수 있다.
object.each do |item| 
  # Do something 
end
```

8. The .times Iterator

```ruby
# 반복하고싶은 횟수.times{원하는 행동}
10.times{print "getcha"} 
```

9. while, until, for example

````ruby
1-50까지 출력해보자

i = 1
while i < 51 do
  print i 
  i += 1
end

i = 1
until i > 50 do
  print i
  i += 1
end

for i in 1..50 
  print i
end
````

10. Loop example

````ruby
i = 0
loop do
  print "Ruby!"
  break if i == 29
  i += 1
end
````



## 6.REDACTED

1. Split Method

````ruby
# String.split("기준")

puts "Enter some text: "
text = gets.chomp

puts "Enter words to redact: "
redact = gets.chomp

words = text.split(" ")
````

2. Final code

````ruby
puts "Enter some text: "
text = gets.chomp

puts "Enter words to redact: "
redact = gets.chomp

words = text.split(" ") # 공백 기준으로 split

words.each do |words| # 배열 words에 원소가 있는만큼 Loop 돌린다.
   if words.include? redact # words에 redact에 있는 애가 있다면?
    print "REDACTED " # REDACTED를 출력
  else
    print words + " " # 아니라면 그대로 단어를 출력
  end
end
````

