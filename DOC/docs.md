# T# Documentation

## Introduction

T# is a Stack-based programming language designed for building software.
It's similar to Porth and Forth.

## Install & Run
```bash
$ git clone https://github.com/Tsharp-lang/Tsharp
$ cd tsharp
$ go build main.go
$ ./main examples/main.t#
or
$ ./main.exe examples/main.t#
```

## Hello World
```pascal
"Hello World!" print
```
'print' will print the top element of the stack, then remove it.

## Comments
```python
# Sample comment
```

## Import
```python
import "main.t#"
```

## Block
```pascal
block main do
    "Hello World!" print
end

call main
```

'block' is like Function in other languages.

## If Statement
```pascal
if false do
    "Hello World" print
else
    "Hello World else body!" print
end

10 10 == print
20 10 != print
2 10 < print
10 2 > print
```

## Dup
```pascal
"Hello World" dup print print
```
'dup' duplicate element on top of the stack.

## Drop
```pascal
"Hello World" "T# Programming Language" drop print
```
'drop' drops the top element of the stack.

## PrintS
```python
1 2 [1,2,3,4,["a","b","c"]]

printS

# stack length  
#     ↓ 
#    <3>  1 2 [1, 2, 3, 4, ["a", "b", "c"]] <- top
```
'printS' print all stack values. 'printS' won't drop stack value after print.

## For loop
```pascal
for true do
    "Hello World!" print
    break
end
```

## Arithmetic
```pascal
34 35 + print

100 40 - print

200 5 / print

10 2 * print
```

## Variable
```pascal
10 -> x drop

x -> y drop

y print
```

## Type
```python
int # 12345
string # "Hello World!"
bool # true false
type # int string bool type
```

## Typeof
```python
"Hello World" dup typeof print
```

## Rot
```python
1 2 3 rot print print print
```
'rot' rotate top three stack elements.

## Over
```python
1 2 over print print print
```
'over' copy the element below the top of the stack

## append string
```python
"Hello " "World!" + print 
```

## Inc
```python
1 inc print
```
'inc' increment the top element of the stack

## Dec
```python
10 dec print
```
'dec' decrement the top element of the stack

## Exit
```python
"Hello World"
exit
print
```
'exit' will exit the program.

## List
```python
["T#", "Ruby", "Python", "C", "Go", "Julia"] dup print

"V" append dup print

["HTML"] append dup print

[1, 2, 3] append[7]

"Hello World!" append[7][1]

print
```

## FizzBuzz
```pascal
1
for dup 101 < do
    if dup 3 % 0 == do
        if dup 15 % 0 == do
            "FizzBuzz" print
        else
            "Fizz" print
        end
    else
        if dup 5 % 0 == do
            "Buzz" print
        else
            dup print
        end
    end
    inc
end drop
```
