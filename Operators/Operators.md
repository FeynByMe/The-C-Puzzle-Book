# Operators

## Basic Arithmetic Operators

>What does the following program print?
> ```C
> main()
> {
>	int x;
>	x  = -3 + 4 * 5 - 6; printf("%d\n",x);
>	x  = 3 + 4 % 5 - 6; printf("%d\n",x);
>	x  = -3 * 4 % - 6 / 5; printf("%d\n",x);
>	x  = ( 7 + 6 ) % 5 / 2; printf("%d\n",x);
>}
>```

The program will print out the following output:

```C
11
1
0
1
```
This exercise excels at teaching us about operator precedence. It forces us yo understand that `C` will not just read your operations from left-to-right. Instead, it has a semi-strict rule of hierarchical operations which it uses to do the computation. 


![The table of hierarchies for the `C`programming language](https://i.stack.imgur.com/XgKf8.png)

Also, one should understand how `C` deals with division of integers when restricted to using integer type variables, as we're doing with `x`in this exercise. 

## Assignment Operators

>What does the following program print?
> ```C
> #define PRINTX printf("%d\n", x)
> 
> main()
> {
>	int x = 2, y, z;
>
>	x  *= 3 + 2; PRINTX;
>	x  *= y = z = 4; PRINTX;
>	x  = y == z; PRINTX;
>	x  == ( y = z ); PRINTX;
>}
>```

The program will print out the following output:

```C
10
40
1
1
```

Wow, that was a strange exercise. I have done some programming in *`C` and there were certainly questions about the language that was asking myself for the first time while I was attempting this. 

In fact, in order to successfully answer this question you must grasp some fundamental notions of how *assignments* work in `C`.  

The program begins by declaring three variable of type integer, one of them with a concrete value of `2`while the other pair, `y`and `z`, are left as unassigned which means, for now, that they "hold" the same integer value. 

In the second statement the program assigns `x` to the product of its current value, `2`, with `2+3`which equals `5`, meaning that `x`is now holding the value `10`.

In the third statement the program assigsn 

