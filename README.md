# sceval-spec

Specification of the (half-)esoteric language _Sceval_.

Sceval is a strange hybrid of imperative and functional programming paradigms. At it's core Sceval is quite imperative which, combined with the way it intuitively provides "scopeobjects", makes for an oddly interesting language.

### Examples


```
# Fibonacci
ffibs=@<n>(
  :a=1 b=1
  i=0@(i<n)~@(
    (i>1)?@(
      h=(a+b)
      a=b
      b=h
    )
    !<("fibs #"+i+"="+n)>print
    i++
  )
)

!<10>ffibs
```
