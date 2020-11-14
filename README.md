# dev-nekoboi's Python Module
A miscellaneous Python module for all of the things that I wish were features of Python without having to program them myself.

---

Currently included commands:
---

```python
prompt(out, condition, err, transform)
```
This function prompts the user to enter an input. `out` is an optional parameter which should be the output value to prompt the user with. `condition` is an optional parameter which, if supplied, should be a funciton which takes in a single input and outputs a boolean. If a condition is supplied, then the user's input **must** meet that condition before it is returned. The user will continue to be prompted until they provide a valid input. `err` is an optional parameter which will be printed in the case that the input which the user provides should not meet the condition supplied. If no condition is supplied, `err` will never be printed and it can therefore be left blank. `transform` is an optional parameter which, if supplied, should be a function that takes a single input and provides an output. If a transform is supplied, the user's input will be passed through said transform before the value of that input is returned from the `prompt()` function.

---

```python
canBe(val, type)
```
This function will return a boolean value of `True` if `val` is an instance of `type` _or_ if `val` can be successfully converted _into_ an instance of `type`, and `False` otherwise. Both parameters are required.

Note: due to the nature of the function definition, it is likely that should either parameter be omitted, the function would return `True`. This has the potential to cause runtime errors, and should be conisdered carefully.
