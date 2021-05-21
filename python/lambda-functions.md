## Python Functions

Normal Python functions are defined using the `def` keyword.
e.g

```py
def is_odd_or_div_by_7(n):
    if (n % 7 == 0) or (n % 2 != 0):
        return True
    return False
```

However, you can use lambda functions to define **anonymous** functions.

```py
lambda n: True if (n % 7 == 0) or (n % 2 != 0) else False
```

### Lambda functions syntax

```
lambda arguments: expression
```

The lambda definition does not include a “return” statement, it always contains an expression that is returned.

#### Pitfalls of using lambdas
1. The function can have any number of arguments, but only **one expression**.
1. PEP8 does not allow for the assignment of the lambda fucntion to a variable that you can then re-use.


#### Additional reading
- [PEP8 rule](https://www.flake8rules.com/rules/E731.html)
- [RealPython tutorial](https://realpython.com/python-lambda/)
