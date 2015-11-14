# Merge sorted arrays in Ruby

Coding exercise.

## Code

```ruby
def merge(a, b)
  if a.nil? || b.nil?
    a || b || []
  elsif a.empty? || b.empty?
    a.any? ? a : b
  else
    if a.first < b.first
      a[0..0] + merge(a[1..a.size], b)
    else
      b[0..0] + merge(a, b[1..b.size])
    end
  end
end
```
