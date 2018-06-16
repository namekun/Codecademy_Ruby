# *Learn Ruby by Codecademy*



# 1.Introduction to Ruby



## 1)Learn RUBY!

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



## 2)PUTTING THE FORM IN FORMATTER

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

# 2.Control Flow in Ruby



## 3)CONTROL FLOW IN RUBY

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

unless hungry# = if !hungry 즉, 조건이 참이 아닐때.
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



## 4)THITH MEANTH WAR!

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



# 3.Looping With Ruby!



## 5)LOOPS & ITERATORS

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

````ruby
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

object.each { |item| # object배열 혹은 해쉬의 값이 item이라는 변수에 들어간다. 
  # 들어간 변수로 무언가를 한다.
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



## 6) REDACTED

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



# 4.Arrays and Hashes



## 7) DATA STRUCTURE

1. Array

````ruby
array = [5, 7, 9, 2, 0]
array[2]
# returns "9", since "9"
# is at index 2
=begin
        +---+---+---+---+---+
array   | 5 | 7 | 9 | 2 | 0 |
        +---+---+---+---+---+
index     0   1   2   3   4
=end
````

2. Arrays_Non_numbers

`````ruby
string_array = ["i want sleep all day", "So tired"]
`````

3. Array of Array

````ruby
multi_d_array = [[0,0,0,0],[0,0,0,0],[0,0,0,0],[0,0,0,0]]

multi_d_array.each { |x| puts "#{x}\n" }
=begin
= multi_d_array.each do |x| 
	puts "#{x}\n"
end
=end
````

4. Hash

````ruby
my_hash = { "name" => "Eric",
  "age" => 26,
  "hungry?" => true # key => value
}

puts my_hash["name"]
puts my_hash["age"]
puts my_hash["hungry?"]
````

5. Using Hash.new

````ruby
# hash를 손쉽게 생성하는 방법도 있다!
pets = Hash.new # 이때, hash는 반드시 capitalized되어야한다. 아니면 루비가 뭔지 모르거든!
#이렇게 생성된 해쉬는 비어있는 상태이다. 그니까 pets = {} 랑 똑같은거
````

6. Adding to a hash

````ruby
#위의 코드에 이어 진행한다.
pets["zzong"] = "dog"
# zzong이라는 키에 'dog'라는 값을 넣어서 hash 생성
print pets["zzong"]
# => dog
````

7. (Re)Introduction to Iteration

````ruby
#array의 경우
friends = ["Milhouse", "Ralph", "Nelson", "Otto"]
#hash의 경우
family = { "Homer" => "dad",
  "Marge" => "mom",
  "Lisa" => "sister",
  "Maggie" => "sister",
  "Abe" => "grandpa",
  "Santa's Little Helper" => "dog"
}

friends.each { |x| puts "#{x}" }
=begin
Milhouse
Ralph
Nelson
Otto
=end
family.each { |x, y| puts "#{x}: #{y}" }
=begin
Homer: dad
Marge: mom
Lisa: sister
Maggie: sister
Abe: grandpa
Santa's Little Helper: dog
=end
````

8. Iteration over Arrays

```Ruby
languages = ["HTML", "CSS", "JavaScript", "Python", "Ruby"]
languages.each { |x| puts x}
```

9. Iterating Over Multidimensional Arrays

```ruby
s = [["ham", "swiss"], ["turkey", "cheddar"], ["roast beef", "gruyere"]]

s.each do |sub_array| 
  puts sub_array
  sub_array.each do |y|
    puts y
  end
end

=begin
결과물 : 
["ham", "swiss"] (sub_array)
ham (Y)
swiss (Y)
["turkey", "cheddar"]
turkey
cheddar
["roast beef", "gruyere"]
roast beef
gruyere
=end
```

10. Iterating Over Hashes

````ruby
secret_identities = {
  "The Batman" => "Bruce Wayne",
  "Superman" => "Clark Kent",
  "Wonder Woman" => "Diana Prince",
  "Freakazoid" => "Dexter Douglas"
}
  
secret_identities.each do |movie, actor|
  puts "#{movie}: #{actor}"
end
````



## 8)CREATE A HISTOGRAM

1. 코드의 완성

*scripts.rb*

````ruby
puts "Text please: "
text = gets.chomp

words = text.split(" ")
frequencies = Hash.new(0)
words.each { |word| frequencies[word] += 1 } 
frequencies = frequencies.sort_by {|a, b| b } 
frequencies.reverse! # 정렬시킨것을 뒤집습니다.
frequencies.each { |word, frequency| puts word + " " + frequency.to_s }
````

2. Hash's Default Value

````ruby
 # Hash.new(default value) -> 해쉬안에 아무것도 없는데 값을 내놓으라고 하면 default value가 나옵니다.
h = Hash.new("nothing here")

puts h
# {}

puts h["kitty"]
# nothing here 출력.
````

3. make Hash by .each method

````ruby
# Hash에 Word와 해당 word의 count 값을 매칭시켜 넣어줍니다. 
words.each { |word| frequencies[word] += 1 } 
=begin
출력 결과
 input? :
fds dsf fsd a a
{"fds"=>1, "dsf"=>1, "fsd"=>1, "a"=>2}
=end
````

4. Sorting the Hash!

```ruby
#아래의 sort_by 메소드는 b를 기준으로 정렬시켜줍니다.
frequencies = frequencies.sort_by {|a, b| b } 
```



# 5.Block and Sorting



## 9) METHODS, BLOCKS, SORTING

1. Why Methods?

- 코드에 문제가 있으면 프로그램을 잘 구성한 경우 버그를 찾아 수정하는 것이 훨씬 쉽습니다. 특정 작업을 별도의 method에 할당하면 이 조직에 도움이 됩니다. 
- 특정 작업을 별도의 method(컴퓨터 과학자는 이를 separtion of concerns라고 합니다.)에 할당하면 프로그램이 중복되지 않고 코드 재사용이 용이해 집니다. 이는 한 프로그램에서 매번 다시 쓰지 않고 같은 방법을 반복해서 사용할 수 있을 뿐만 아니라 다른 프로그램에서도 사용할 수 있다는 것입니다. 
- **객체**에 대해 자세히 알게 되면 루비의 method를 사용하여 많은 흥미로운 것들을 배울 수 있습니다. 

2. Method Syntax

* method는 보통`def`(`define`의 줄임말)라고 쓰여집니다. 
* head에 `def`라는 키워드를 포함하여, method의 이름, 그리고 method에서 사용할 인수(arguments)를 씁니다.
* body에는 method에서 수행할 code를 씁니다. 만약 `if`, `for`, `elsif`, `else` 를 사용한다면 스페이스바 두칸정도 들여쓰기를 해줍니다.
* method역시 `end`로 끝마칩니다.

```ruby
def puts_1_to_10
  (1..10).each { |i| puts i }
end

puts_1_to_10  # Method call
```

3. 2-way to call the Method 

```ruby
def puts_1_to_10
  (1..10).each { |i| puts i }
end

puts_1_to_10  # Method call 

def cubertino(n)
  puts n ** 3
end

cubertino(8) # Method call 
```

4.  splat arguments 

* 만약, Method에 arguments(전달인자)를 한번에 여러개를 넣고싶다면 다음과 같이 해당 arguments 앞에 `*`를 붙여주면 됩니다. 이것은 한개이상의 arguments를 받을 수 있음을 말해주기 때문입니다.

``` ruby
def what_up(greeting, *friends)
  friends.each { |friend| puts "#{greeting}, #{friend}!" }
end

what_up("What up", "Ian", "Zoe", "Zenas", "Eleanor")

=begin
출력결과:
What up, Ian!
What up, Zoe!
What up, Zenas!
What up, Eleanor!
=end
```

5. Block은 이름없는 Method와 같습니다.

* 대부분 당신이 작업한 Method는 이름이 정의 되어있습니다. 그게 당신이 했던, 다른 사람이 했던지요!(예를 들면 [array].sort(), "string".downcase같은 것들이요!)

* Block을 이름을 갖고 있지않은 Method를 만드는 방법이라고 생각해도 됩니다.

  (이것은 자바스크립트의 anonymous function 또는 파이썬의 lambdas와 비슷해요)

* Block은 do-end 키워드 또는 {} 으로 정의 됩니다.

```ruby
1.times do
  puts "I'm a code block!"
end

1.times { puts "As am I!" }
```

6. Block과 Method의 차이?

* 그러나, Block과 Method에는 차이가 있습니다. 
* Method는 한번 만들면 계속 쓸수있지만, Block은 한번쓰면 끝입니다. 아래의 예시처럼 each가 끝나면 그대로 거기서 끝!

```ruby
# method that capitalizes a word
def capitalize(string) 
  puts "#{string[0].upcase}#{string[1..-1]}" #string을 배열처럼 쓸 수도 있네요? 띠용? 
end

capitalize("ryan") # prints "Ryan"
capitalize("jane") # prints "Jane"

# block that capitalizes each string in the array
["ryan", "jane"].each {|string| puts "#{string[0].upcase}#{string[1..-1]}"} # prints "Ryan", then "Jane"
```

7. Code Block을 사용해봅시다.

- 메소드는 블록을 매개변수로 가질 수 있습니다. 이는 마치 `.each`가 블록을 매개변수로 받은 뒤, 반복적인 작업을 진행하는 것과 같습니다! 그 동안은 `.each`에서 괄호를 생략해왔기 때문에, 아마 여러분은 눈치채지 못했을겁니다. 
- 블록을 메소드에 전달하는 것은 메소드의 특정 작업을 **추상화(abstracting)**하는 좋은 방법이자, 메소드가 호출되었을 때 해당 작업을 정의하는 훌륭한 방법입니다. 추상화는 컴퓨터 과학의 아주 중요한 개념으로, 추상화란 "어떤것을 간단하게 만드는 것"이라고 볼 수 있습니다. 여러분이 새로운 집을 구경하러 간다고 할 때, "콘크리트, 합판, 비닐 슬라이드로 이루어진 구조물을 보러가자!"라고 말하는 건 말 그대로 정신나간 소리처럼 들리죠! 단지 "집을 구경하러 갑시다" 라고 이야기 하는 것이 집의 구성 요소를 모두 다 언급하는 것 보다 훨씬 간단할 겁니다. 이처럼 블록을 이용해서 메소드가 하는 일을 정의하는 것은 (마치 `.each` 처럼) 해당 작업을 단순화 시킵니다. 

```ruby
# The block, {|i| puts i}, is passed the current
# array item each time it is evaluated. This block
# prints the item. 
[1, 2, 3, 4, 5].each { |i| puts i }

# This block prints the number 5 for each item.
# (It chooses to ignore the passed item, which is allowed.)
# Modify the block so it will print each item in the array multiplied by five.
[1, 2, 3, 4, 5].each { |i| puts 5 * i }
```

8. Sort를 해봅시다.

```ruby
my_array = [3, 4, 8, 7, 1, 6, 5, 9, 2]

# 아래에 sort! 메소드를 my_array 배열에 호출하세요.
# my_array 는 [1, 2, 3, 4, 5, 6, 7, 8, 9] 가 되어야 합니다.

my_array.sort
```

9. Foundation

* 알파벳 순에 따라 선반에 진열해야 한다면 어떻게 하시겠습니까?

* 대부분의 정렬 알고리즘들은 우리가 요소의 배열을 정렬할 것이라 가정하는데, 여기엔 배열의 두 요소를 놓고 어느 쪽이 먼저 위치해야 하는지를 판단하는 비교작업이 포함됩니다.
* 앞서 언급한 책을 정렬하는 과정을 예로 들면, 어떤 책이 되었든 간에 두 권을 집어들어 알파벳이 먼저인 책을 항상 선택할 것이고, 정렬을 위한 전략을 고안할 것입니다. 이 "전략"이 바로 이전 예제에서 언급했더 정렬 알고리즘입니다. 우리의 역할은 리스트 안의 두 요소를 어떻게 비교할지를 결정하여, 루비가 어떤 전략을 사용할지 판단하도록 만드는 것입니다. 

```ruby
# 도서관 정렬 코드
books = ["Charlie and the Chocolate Factory", "War and Peace", "Utopia", "A Brief History of Time", "A Wrinkle in Time"]

# 어떻게 이 책들을 알파벳 순으로 정렬(sort)할 수 있을까요? (유심히 보시면 힌트를 찾을 수 있을 겁니다)

books.sort!

puts books
```

10. 복합 비교 연산자(Combined Comparison Operator)

* 루비의 객체를 비교하기 위해 **복합 비교 연산자(Combined Comparison Operator)**라고 불리우는 새로운 연산자를 사용할 수 있습니다. 복합 비교 연산자는 다음과 같이 생겼습니다: `<=>`. 이 연산자는 첫번째 피연산자가 두번째 피연산자와 같다면 0을, 첫번째 피연산자가 *크다면* 1을, 반대로 첫번째 피연산자가 *작다면* -1을 반환합니다.
* `sort` 메소드에 전달된 블록은 1, 0, -1 중 하나의 값만을 반환해야 합니다. 만약 첫번째 블록 매개변수가가 두번째 블록 매개변수보다 먼저 와야 한다면 -1을, 그 반대라면 1을, 두 블럭이 동등하다면(즉, 두 값이 같다면) 0을 반환해야 합니다.

```ruby
book_1 = "A Wrinkle in Time"

book_2 = "A Brief History of Time"

book_1<=>book_2 # book2가 A B~로 시작하기에, book_1보다 먼저와야한다. 그래서 1을 return.

5<=>5 # return 0
```

11. 기술 익혀보기

* 만약 책들을 제목의 알파벳 역순으로 Z-A 까지, 또는 **내림차순**으로 정렬하려면 어떻게 해야 할까요? Ruby의 정렬 메소드는 알파벳 순으로 A-Z 까지, 또는 **오름차순**으로만 작동합니다.
* `sort` 메소드는 기본적으로 값을 오름차순으로 정렬하도록 되어있지만, 프로그래머가 두 번째 인자로 블록을 추가하여 요소들이 어떻게 비교되어야 할 지를 명시할 수 있습니다.

``` ruby
books = ["Charlie and the Chocolate Factory", "War and Peace", "Utopia", "A Brief History of Time", "A Wrinkle in Time"]

# To sort our books in ascending order, in-place
books.sort! do |firstBook, secondBook| 
  firstBook <=> secondBook 
end
# Sort your books in descending order, in-place below
puts books

books.sort! do |firstbook, secondbook|
  secondbook <=> firstbook # 복합 연산자가 반대로 나오기에 자연스레 반대로 정렬!
end

puts books
```

## 10) ORDERING YOUR LIBRARY 

1. What You'll Be Building

```ruby
def alphabetize(arr, rev=false)
  if rev
    arr.sort { |item1, item2| item2 <=> item1 }
  else
    arr.sort { |item1, item2| item1 <=> item2 }
  end
end

books = ["Heart of Darkness", "Code Complete", "The Lorax", "The Prophet", "Absalom, Absalom!"]

puts "A-Z: #{alphabetize(books)}"
puts "Z-A: #{alphabetize(books, true)}"
```

2. result

```ruby
def alphabetize(arr, rev = false)
  if rev 
    arr.sort!
    arr.reverse!
  else
    arr.sort!
  end
end

numbers = [3, 5, 1, 6]
puts alphabetize(numbers)
puts alphabetize(numbers, true)

books = ["Heart of Darkness", "Code Complete", "The Lorax", "The Prophet", "Absalom, Absalom!"]
puts alphabetize(books)
puts alphabetize(books, true)
```

# 6.HASHES AND SYMBOLS

## 12) Hashes and Symbols

1. hash 생성에는 2가지 방법이 있습니다

   *1.hash literal notation*

```ruby
new_hash = { "one" => 1 }
```

​    *2. hash constructor notation* 

     ```ruby
new_hash = Hash.new
     ```

2. hash에서의 반복처리

   hash에서의 반복은 다음과 같이 `.each`문을 통해 처리할 수 있습니다.

   ```ruby
   matz = { "First name" => "Yukihiro",
     "Last name" => "Matsumoto",
     "Age" => 47,
     "Nationality" => "Japanese",
     "Nickname" => "Matz"
   }
   
   matz.each do |key, value|
     puts value
   end
   
   =begin
   result =
   
   Yukihiro
   Matsumoto
   47
   Japanese
   Matz
   
   =end
   ```

3. nil

      만약 존재하지 않는 키를 통해서 접근하고자 한다면 어떻게 될까요?

      많은 언어에서는 아마 에러가 발생할 것입니다. 그러나 루비에서는 당신은 `nil`이라는 특별한 값을 얻을 수 있습니다.

      `false`와 함께, `nil`은 두개의 `true`값이 아닌 것 중에 하나입니다. (모든 다른 객체들은  `if 2`, `if "bacon"` 과 같이 `if`문에서 실행되는 것처럼 진실로 여겨집니다.)

      `false`와 `nil`이 같은 것이 아니라는 것은 매우 중요합니다. `false`의 의미는 `not true`이지만, `nil`은 루비에서 `nothing at all` , 즉 아무것도 없다 라는 의미이거든요.

   ```ruby
   creatures = { "weasels" => 0,
     "puppies" => 6,
     "platypuses" => 3,
     "canaries" => 1,
     "Heffalumps" => 7,
     "Tiggers" => 1
   }
   
   creatures["birds"] # nil
   ```

4. `nil`일 때 출력해줄 기본값 정하기

      - hash를 생성할 때, 입력받은 키값이 nil 값이라면 출력해줄 기본값을 정해줍니다.

      ```ruby
      no_nil_hash = Hash.new("no nil!") # no_nil_hash에 nil값이면 "no nil!"을 출력해준다.
      ```

5. Symbol => `:fdf =>3 ` 이런식으로 사용한다.

   ```ruby
   menagerie = { :foxes => 2,
     :giraffe => 1,
     :weezards => 17,
     :elves => 1,
     :canaries => 4,
     :ham => 1
   }
   ```

6. Symbol과 string이 다른점?

     * key값이 있다는 것.

7. Symbol Syntax

     * 심볼은 다음과 같은 방식으로 선언합니다.

     ```ruby
     :my_symbol
     :my symbol # 이렇게 선언하면 안됩니다.
     ```

8. symbol은 어디에 쓰이는가?

   * hash 키 또는 참조 메소드의 이름으로 사용됩니다.
   * symbol은 다음과 같은 이유로 좋은 hash key를 만들 수 있습니다.
     1. 한번 만들어지면 변경이 불가능합니다. 
     2. 한번에 한개의 심볼만 존재하게 되므로, 메모리가 절약됩니다.
     3. 위의 두가지 이유로 심볼보다 키가 더 빠릅니다.

   ```ruby
   symbol_hash = {
     :one => 1,
     :two => 2,    # Fill in these two blanks!
     :three =>3
   }
   ```

9. symbol => strings

   ```ruby
   strings = ["HTML", "CSS", "JavaScript", "Python", "Ruby"]
   symbols = []
   
   strings.each do |s| 
    symbols.push(s.to_sym)
   end 
   print symbols
   ```

10. `.intern`
       * `.to_sym` 은 `.intern`과 같은 기능을 지닌다.

   ```ruby
   strings = ["HTML", "CSS", "JavaScript", "Python", "Ruby"]
   symbols = []
   
   strings.each do |s| 
    symbols.push(s.intern)
   end 
   print symbols
   ```

11. Hash Rocket!
       * 해쉬 로켓은 => 의 모양이 로켓처럼 생겨서 붙은 별명이다.

   ```ruby
   numbers = {
     :one => 1,
     :two => "two",
     :three => 3,
   }
   ```

12. Hash Rocket 착륙!

       * 그러나 로켓 구문은 루비1.9에서 부터 변경되었습니다. 변경사항은 다음과 같습니다.
         1. 시작 부분이 아니라 기호의 끝에 `:`을 넣습니다.
         2. 더이상 해시 로켓이 필요하지 않습니다!

       ```ruby
       movies = {
         lomantic: 'about_time',
         fantasy: 'Dr.strange',
         }
       ```

13. Hash Search VS String Key

   * 해시검색은 문자열키 검색보다 더 빠릅니다! 다음 결과를 봐주세요

   ```ruby
   require 'benchmark'
   
   string_AZ = Hash[("a".."z").to_a.zip((1..26).to_a)]
   symbol_AZ = Hash[(:a..:z).to_a.zip((1..26).to_a)]
   
   string_time = Benchmark.realtime do
     100_000.times { string_AZ["r"] }
   end
   
   symbol_time = Benchmark.realtime do
     100_000.times { symbol_AZ[:r] }
   end
   
   puts "String time: #{string_time} seconds."
   puts "Symbol time: #{symbol_time} seconds."
   
   #String time: 0.009227719157934189 seconds.
   #Symbol time: 0.0056778742000460625 seconds.
   ```

14. `Select` 문을 사용해보자 

* 특정 기준을 충족하는 어떤 값을 갖고 오고싶다면 `select`문을 사용해야합니다.

```ruby
grades = { alice: 100,
  bob: 92,
  chris: 95,
  dave: 97
}

grades.select { |name, grade| grade <  97 }
# ==> { :bob => 92, :chris => 95 }

grades.select { |k, v| k == :alice }
# ==> { :alice => 100 }
```

15. `.each_key`, `.each_values`

* 두 메소드를 통해 우리는 해시안에 모든 키와 벨류를 좀더 쉽게 불러올 수 있습니다.

```ruby
my_hash = { one: 1, two: 2, three: 3 }

my_hash.each_key { |k| print k, " " }
# ==> one two three

my_hash.each_value { |v| print v, " " }
# ==> 1 2 3
```

## 13) A Night at the Movies

1. 무엇을 만들 것인가?

* 해시에 새 영화를 추가하고, 기존의 영화들을 업데이트하고, 표시하고, 삭제할 수 있는 메소드를 만들고자 한다. 

```ruby
movies = {
  Memento: 3,
  Primer: 4,
  Ishtar: 1
}

puts "What would you like to do?"
puts "-- Type 'add' to add a movie."
puts "-- Type 'update' to update a movie."
puts "-- Type 'display' to display all movies."
puts "-- Type 'delete' to delete a movie."

choice = gets.chomp.downcase
case choice
when 'add'
  puts "What movie do you want to add?"
  title = gets.chomp
  if movies[title.to_sym].nil?
    puts "What's the rating? (Type a number 0 to 4.)"
    rating = gets.chomp
    movies[title.to_sym] = rating.to_i
    puts "#{title} has been added with a rating of #{rating}."
  else
    puts "That movie already exists! Its rating is #{movies[title.to_sym]}."
  end
when 'update'
  puts "What movie do you want to update?"
  title = gets.chomp
  if movies[title.to_sym].nil?
    puts "Movie not found!"
  else
    puts "What's the new rating? (Type a number 0 to 4.)"
    rating = gets.chomp
    movies[title.to_sym] = rating.to_i
    puts "#{title} has been updated with new rating of #{rating}."
  end
when 'display'
  movies.each do |movie, rating|
    puts "#{movie}: #{rating}"
  end
when 'delete'
  puts "What movie do you want to delete?"
  title = gets.chomp
  if movies[title.to_sym].nil?
    puts "Movie not found!"
  else
    movies.delete(title.to_sym)
    puts "#{title} has been removed."
  end
else
  puts "Sorry, I didn't understand you."
end
```



