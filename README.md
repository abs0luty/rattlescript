# RattleScript
Rattlescript is just a fun language written in Rust. We currently don't have explicit plans for it, just that we're going to add whatever we feel like. Tomorrow we might have classes; who knows?!

# Contributing
We have gotten help from multiple people in the Rust discord, and we're happy to accept anyones suggestions. If you feel you have some value to add, go ahead and open a pull request! Just know that we will immediately deny anything that requires the use of external (non-built-in) crates, we just aren't interested in black boxes around here.

# In case you were wondering...
Here's a quick overview of our syntax ripped straight from our test file:
```python
def deco(foo) {
    def wrapper(func) {
        def inner(a, b) {
            print(foo, "input", a, b)
            let res = func(a, b)
            print(foo, "output", res)
        }
        return inner
    }
    return wrapper
}

@deco("      a d d i t i o n "[::2][3:])
def add(a, b) {
    return a + b
}

@deco("subtract"+"ion")
def sub(a, b) {
    return a - b
}

add(3, 4)
sub(5, 6)


@deco("multiplication")
def mul(a, b) => a * b
mul(3,2)

let multiply = |a, b| { return a / b; }

let divide = deco("division")(|a, b| => a / b)
divide(4,2)

let boo = true
let not_boo = true

assert boo == true, "failed"

if boo {
    print("boo is true")
} else if not_boo {
    print("boo is false, but not_boo is true")
} else {
    print("boo is false, and not_boo is false")
}

let boo_lam = || => true

if boo_lam() {
    print("boo_lam is true")
} else {
    print("boo_lam is false")
}

print(true or false, false or true, false and true, true and true)
print(not true)

print(nothing)

print(1==2, 1!=2, 1<2, 1>2, 1<=2, 1>=2)

let a = 0
let b = 1
let n = 0
while n < 10 {
    print(a)
    let c = a + b
    a = b
    b = c
    n = n + 1
}


print("-"*80)
for x in "hello" {
    print(x)
}
print("-"*80)
for x in 0..5 {
    print(x)
}
//print("hello world"

let c = 100_000.25_18
print(c)

print(0b_101, 0o_67, 0x_22B, 0x_15b3)
```
