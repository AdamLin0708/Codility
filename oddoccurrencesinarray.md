# OddOccurrencesInArray

Problem: [https://app.codility.com/programmers/lessons/2-arrays/odd\_occurrences\_in\_array/](https://app.codility.com/programmers/lessons/2-arrays/odd_occurrences_in_array/)

作法：

* 使用hash

Language: Ruby

```
# you can write to stdout for debugging purposes, e.g.
# puts "this is a debug message"

def solution(a)
  # write your code in Ruby 2.2
  
  hash = {}
  
  for i in 0...a.length
    hash[a[i]] = 0
  end
  
  for i in 0...a.length
    hash[a[i]] = hash[a[i]]+1
  end
      
  hash.each do |key, value|
    if value%2 != 0
      return key
    end
  end
  
end
```



