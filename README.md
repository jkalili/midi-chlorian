<div align="center">
<img src="https://raw.githubusercontent.com/cpon00/midi-chlorian/main/docs/midichlorianlogo.png" />
</div>

# Introduction

This repository is the home of Midi-Chlorian, a language inspired by the mind of George Lucas. One of our team members had just finished five hours of reading Star Wars wiki articles, and proposed the name SkywalkerScript. After a bit of deliberation, our team settled on Midi-Chlorian, named after the "intelligent microscopic life-forms that lived symbiotically inside the cells of all living things"[[1]](https://starwars.fandom.com/wiki/Midi-chlorian).

Midi-Chlorian is created by [Carter Pon](https://github.com/cpon00), [Adrian Leung](https://github.com/AdrianLearn), [Isaiah Anyimi](https://github.com/ianyimi), and [Jason Kalili](https://github.com/jkalili).


# Shortcuts

-   [ Types ](#types)
-   [ Operational Logic ](#operational-logic)
    -   [ Unary Operators](#unary-operators)
-   [ Comments ](#comments)
-   [ Midi-Chlorian Examples ](#examples)
    -   [Print](#print)
    -   [Variabale Declaration](#variable-declaration)
    -   [If Statements](#if-statements)
    -   [For Loop](#for-loop)
    -   [While Loop](#while-loop)
-   [Example Programs](#example-programs)

# Types

| Type in Javascript | Midi-chlorian |            Declaration                                |
| :----------------: | :-----------: | :----------------------------------------------------:|
|        int         |     cred      |            Cred a = 9                                 |
|        long        |    parsec     |         Parsec b = 900000                             |
|       double       |      ket      |            ket c = 0.5                                |
|      boolean       |   absolute    |         absolute d = true                             |
|        char        | midichlorian  |       midichlorian e = "s"                            |
|       string       | transmission  |  transmission f = "Hello There"                       |
|       array        |     tome      | tome\<transmission> g = ["Execute","Order","66"]      |
|     dictionary     |   holocron    |  holocron\<transmission,cred> g = [exe:34, evc: 32]   |



# Boolean Values

| Javascript | Midi-chlorian |
| :--------: | :-----------: |
|   true     |     light     |
|   false    |     dark      |

# Operational Logic

| Javascript | Midi-chlorian |
| :--------: | :-----------: |
|   a + b    |     a + b     |
|   a - b    |     a - b     |
|   a \_ b   |    a \_ b     |
|   a / b    |     a / b     |
|   a \* b   |    a \* b     |
|   a % b    |     a % b     |
|   a == b   |  a oneWith b  |
|   a != b   | a !oneWith b  |
|   a > b    |     a > b     |
|   a < b    |     a < b     |
|   a <= b   |    a <= b     |
|   a && b   |    a and b    |
|   a or b   |    a or b     |


### Unary Operators

| Operation         | Compatability |
| ----------------- | ------------- |
| increment: `++`   | `Numbers`     |
| decrement: `--`   | `Numbers`     |
| negative: `-`     | `Numbers`     |
| negation: `darth` | `Booleans`    |


# Comments

-   Single Line: `>< comment goes here`
-   Block: `>> comment goes here << `


# Examples

## Print

```
emit ("May the force be with you.")
```

## Variable Declaration

```
cred numberOfSith = 9

```

## If Statements

```
should (i > j) {
    execute i
} orElse {
    execute j
}
```

## For Loop

```
force (cred i = 0; i < 5; i++) {
    should (i onewith 3) {
        unleash >< break from loop
    }
}
```

## While Loop

```
while (i < 3) {
    unleash >< break from loop
}

```

# Example Programs

## Fibonacci

```Javascript
function fibonacci (n) {
    if (n <= 1) {
        return 1
    }
    return fibonacci(n-1) + fibonacci(n-2)
}
```

```
Order fibonacci (cred count) {
    should (count <= 1) {
        execute 1
    }
    execute fibonacci(n-1) + fibonacci(n-2)
}
```

## Returns the Larger of Two Integers

> ### Javascript

```JavaScript
function max (i, j) {
    if (i > j) {
        return i
    } else {
        return j
    }
}
```

> ### Midi-Chlorian

```
order max (cred i, cred j) {
    should (i > j) {
        execute i
    } elseshould {
        execute j
    }
}
```

## Two Sum Leetcode Problem

> ### Javscript

```JavaScript
function twoSum(nums, target) {
    const comp = {};
    for (let i = 0; i < nums.length; i++) {
        if (comp[nums[i]] >= 0) {
            return [comp[nums[i]], i]
        }
        comp[target-nums[i]] = i
    }
}
```

> ### Midi-Chlorian

```
order cred twoSum (tome nums, cred target) {
    const comp = {};
    cred i = 0;
    force (i until nums.length) {
        should (comp[nums[i]] >= 0) {
            execute [comp[nums[i]], i]
        }
        comp[target-nums[i]] = i
    }
}
```
