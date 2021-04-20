**Какие типы переменных есть в Ruby?**
@var - инстансная переменная, значение этих переменных для каждого элемента является индивидуальным
@@var - перенная класса, общая для всех объектов класса, при изменении меняется у всех объектов
$var - глобальная переменная
var - локальная переменная
VAR - константа

**Какая разница между nil и false?**
nil - это значение означающее отсутствие данных, а false - булевое значение

**Перечислите типы данных в Ruby**
Fixnum(<2^30), Bignum, Float, Array, String, Hash, Boolean, Symbol

**Когда используются load и require?**
load и require подключают файл и после выполняют. В отличии от load, require выполнит код единожды даже если файл подключен несколько раз. В случае если файл вылнен вернётся true. В require при повторном выполнении будет возвращено false. Tckb необходимо чтобы код срабатывал каждый раз, когда файл подключается, например при каких-то изменениях, то необходимо использовать load.

**Какие виды условий есть в Ruby?**
```ruby
if condition
  # ...
elsif condition
  # ...
else
  # ...
end

condition ? true : false

unless condition
  # ...
end

... if condition
... unless condition
```

**Какие в Ruby есть циклы?**
```ruby
loop do
  # ...
end

for el in [...]
  # ...
end

until condition
  # ...
end

while condition
  # ...
end

do
  # ...
while condition


```


**Расскажите про операторы `break`, `next`, `redo`, `retry`**

**Какие виды комментариев есть в Ruby?**

**Что такое объект? Как его создать?**

**Расскажите про классы**

**Как объявляются и используются методы?**

**Что такое блок? Какие есть способы для его создания?**

**Расскажите про оператор yield. Что делает амперсанд параметр?**

**Расскажите про лямбды и проки**

**Расскажите про модули. Что такое миксины?**

**Для чего используется глобальная переменная $?**

**Расскажите про строки. Как можно создавать multiline строки? Как можно заморозить строку? Как можно объединять и сравнивать?**

**Расскажите про массивы, способы их создания. Как можно взаимодествовать с эллементами массивов?**

**Расскажите про Хэши**

**Что такое итераторы? Перечислите их**

**Чем отличается super от super()?**

**Чему будут равны val1 и val2? Расскажите почему**
```ruby
val1 = true and false  # подсказка: вывод этого оператора в IRB не является значением val1!
val2 = true && false
```
**В каких условиях в списке ниже будет false?**
```ruby
true    ? "true" : "false"
false   ? "true" : "false"
nil     ? "true" : "false"
1       ? "true" : "false"
0       ? "true" : "false"
"false" ? "true" : "false"
""      ? "true" : "false"
[]      ? "true" : "false"
```

**Напишите функцию соортировки элементов хэша под длине ключей**
```ruby
{ abc: 'hello', 'another_key' => 123, 4567 => 'third' }
```

**Опишите, как работает следующий код?**
```ruby
VAL = 'Global'

module Foo
  VAL = 'Foo Local'

  class Bar
    def value1
      VAL
    end
  end
end

class Foo::Bar
  def value2
    VAL
  end
end

Foo::Bar.new.value1 # => ?
Foo::Bar.new.value2 # => ?
```

**`(a) {p a}["Hello world"]` - это код валидный? Если это так, то что он делает? Обоснуйте свой ответ.**

**`==, ===, eql?, equal?` - расскажите про эти операторы. Когда и как они должны применяться?**

**Чем `+=` отличается от `.concat`?**

**Часто в руби можно увидеть выражения вида `array.map(&:method_name)`. Как это работает?**

**Напишите в одну строку выражение, которое будет выводить последовательность Фиббоначи любой длины, в виде массива**

**Можно ли вызывать приватный метод класса из вне, через объект?**

**Объясните код**
```ruby
class A
  def self.a(b)
    if b > 0
      b * b
    end
  end
end

var1 = A.a(0) # ?
var2 = A.a(2) # ?
```

**Чем `arr.map` отличается от `arr.each`? `arr.collect` - псевдоним для `arr.map`**

**Как можно удалить элемнеты со значение nil из массива?**

**Расскажите, как работает код**
```ruby
class ABC
  def xyz
    puts "xyz in ABC"
  end
end

ABC::new::xyz
ABC::new.xyz
ABC.new::xyz
ABC.new.xyz
```

**Чему будет равна переменная?**
```ruby
upcased = ["one", "two", "three"].map {|n| puts n.upcase }
```

**Расскажите, как работает код?**
```ruby
if false
  foo = 'test'
end

defined? foo # => ?
defined? bar # => ?
```

**Чем отличаются методы класса Object .clone и .dup?**

**Чем отличается extend от include?**

**Какие в Ruby есть типы переменных?**

**Что выведет код?**
```ruby
cool = "Beans"
def dinner_plans()
  puts cool
end

dinner_plans()
```

**Что выведет код?**
```ruby
name = :crank
puts name.inspect()
```

**Что такое класс?**

**Что такое объект?**

**Что делает метод `.class()` ?**

**Что делает метод `.any()` ?**

**Что делает метод `.all()` ?**

**Что делает метод `.ancestors()` ?**

**Что делает метод `.inject()` ?**

**Что делает метод `.fetch()` ?**

**Что вернёт код `['a', 'b'] == ['b', 'a']` ?**

**Создайте массив элементов из первого массива, которых нет во втором**
```ruby
first = ["cool", "busta", "odb"]
second = ["puffy", "cool", "busta"]
```

**Что вернёт код ниже?**
```ruby
browsers = {
  :favorite => :chrome,
  :favorite => :firefox,
  :worst => :internet_explorer
}
browsers[:favorite]
```

**Что иожет использоваться в качестве ключа в хэше?**


**Верните среднее значение обеих ключей вместе**
```ruby
class_grades = {
  :section_one => [88, 74, 64],
  :section_two => [99, 100]
}
```

**Что вернёт код ниже? Почему?**
```ruby
blah = {}
sah = blah
sah[:redwall] = "awesome books!"
sah.object_id == blah.object_id
```

**Что вернёт код ниже? Почему?**
```ruby
haha = {a: 1, b: 2}
bozo = haha.merge!({lala: "word up"})
haha.object_id == bozo.object_id
```

**Что вернёт код ниже? Почему?**
```ruby
blah = {}
sah = blah
sah[:redwall] = "awesome books!"
sah.object_id == blah.object_id
```

**Создайте хэш с дефолтным значением "cheese"**
```ruby
```

**Конвертируйте массив в хэш: `{"bob" => 320, "edgar" => 152, "maria" => 125}`**
```ruby
```

**Сделайте monkey patch класса Hash и добавьте метод `called all_values_even?`, который будет возвращать true если все значениея чётные**
```ruby
```

**Объясните следующее утверждение: "Всё в Ruby это объекты, т.к. в Ruby нет автономных функций, все функции на самом деле методы"**

**Что выведет следующий код? Объясните**
```ruby
class Dude
end

def Dude.motto
  "Cowabunga"
end

p Dude.motto
```

**Как получить константу модуля и класса?**
```ruby
```

**Что такое синглтон методы? Как посмотреть все синглтон методы доступные объекту?**

**Назовите прадигмы ООП**

**Что такое Наследование?**

**Что такое Полиморфизм?**

**Что такое Инкапсуляция?**

**Что делает метод `.ancestors`?**
```ruby
```

****
```ruby
```

****
```ruby
```

****
```ruby
```

****
```ruby
```

****
```ruby
```

****
```ruby
```

[21 Essential Ruby Interview Questions](https://www.toptal.com/ruby/interview-questions)
[Learn Ruby](https://www.codequizzes.com/ruby)
[Ruby Interview Questions](https://www.javatpoint.com/ruby-interview-questions)
