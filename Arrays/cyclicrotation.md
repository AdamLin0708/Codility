# CyclicRotation

Problem: [https://app.codility.com/programmers/lessons/2-arrays/cyclic\_rotation/ ](https://app.codility.com/programmers/lessons/2-arrays/cyclic_rotation/)

作法：使用Ruby Method

* 注意當a = \[\]時，要處理

Language: Ruby

Method:

* Array unshift: [http://ruby-doc.org/core-2.2.0/Array.html\#method-i-unshift](http://ruby-doc.org/core-2.2.0/Array.html#method-i-unshift)

```
# you can write to stdout for debugging purposes, e.g.
# puts "this is a debug message"

def solution(a, k)
  # write your code in Ruby 2.2
  
  if a.length != 0
    for i in 0...k
      x = a.pop
      a.unshift(x)
    end  
  end
    
  return a
  
end
```









