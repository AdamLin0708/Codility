# Binary Gap

Problem: [https://app.codility.com/programmers/lessons/1-iterations/binary\_gap/](https://app.codility.com/programmers/lessons/1-iterations/binary_gap/)

作法：

* 因為要求要 O\(log\(N\)\) 完成，因此用check去存n轉成二進位後有1的index
* 而check最長的長度是 log2\(n\)，因此最多for只會跑 log2\(N\)次

Method: 

* Math.log2: [http://ruby-doc.org/core-1.9.3/Math.html\#method-c-log2](http://ruby-doc.org/core-1.9.3/Math.html#method-c-log2)

Language: Ruby

```
# you can write to stdout for debugging purposes, e.g.
# puts "this is a debug message"

def solution(n)
  # write your code in Ruby 2.2

  check = []

  x = Math.log2(n).to_i
  n = n-2**x  
  check.push(x)

  if n == 0 
    return 0
  else

    while n>0 do
      y = Math.log2(n).to_i
      n = n-2**y
      check.push(y)
    end

  end    

  max = 0

  for i in 0...check.length

    if i == check.length-1
      break
    end

    if check[i]-check[i+1]-1 > max
      max = check[i]-check[i+1]-1
    end

  end

  return max



end
```



