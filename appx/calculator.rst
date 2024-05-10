.. User Manual, LibreCAD v2.2.x


.. _calc:

Calculator Operators and Functions
==================================

Typing ``cal`` at the command line will toggle the calculator mode on and off.

.. hint::
    | Trigonometric functions expect angles in *radians*, they are identifiable by the function parameter ``(a)`` in the table! (*radians = degrees*pi/180*)
    | This is not very comfortable for humans, but there is a simple solution to pass angles in degrees.
    | Append the affix ``d`` to the degree value; thus, ``sin(90d)`` is a valid expression and will return the *sinus* of 90°.
    |
    | As the calculator accepts arithmetic expressions and constants, this term will work too: ``sin(90*pi/180)``
    | The part ``90*pi/180`` will be internally calculated and results in ``1.57079632679``, which is 90° in *radians*.
    |
    | And of course, arithmetic expressions can be used for other function parameters too, e.g. to convert imperial to metric values and vice versa.

**Functions**

.. csv-table:: 
    :widths: 10, 70, 20 
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width
    
    "Name", "Function / Operation", "Usage"
    "\+", "addition", "x+y"
    "\-", "subtraction", "x-y"
    "\*", "multiplication", "x*y"
    "/", "division", "x/y"
    "^", "raise x to the power of y", "x^y"
    "sin", "sine function", "sin(a)"
    "cos", "cosine function", "cos(a)"
    "tan", "tangens function", "tan(a)"
    "asin", "arcus sine function", "asin(a)"
    "acos", "arcus cosine function", "acos(a)"
    "atan", "arcus tangens function", "atan(a)"
    "sinh", "hyperbolic sine function", "sinh(a)"
    "cosh", "hyperbolic cosine", "cosh(a)"
    "tanh", "hyperbolic tangens function", "tanh(a)"
    "asinh", "hyperbolic arcus sine function", "asinh(a)"
    "acosh", "hyperbolic arcus tangens function", "acosh(a)"
    "atanh", "hyperbolic arcur tangens function", "atanh(a)"
    "log2", "logarithm to the base 2", "log2(x)"
    "log10", "logarithm to the base 10", "log10(x)"
    "log", "logarithm to base e (2.71828...)", "log(x)"
    "ln", "logarithm to base e (2.71828...)", "ln(x)"
    "exp", "e raised to the power of x", "exp(x)"
    "sqrt", "square root of a value", "sqrt(x)"
    "sign", "sign function -1 if x<0; 1 if x>0", "sign(x)"
    "rint", "round to nearest integer", "rint(x)"
    "abs", "absolute value, negatives become positive", "abs(x)"
    "min", "min of all arguments", "min(x, y, ...n)"
    "max", "max of all arguments", "max(x, y, ...n)"
    "sum", "sum of all arguments", "sum(x, y, ...n)"
    "avg", "mean value of all arguments", "avg(x, y, ...n)"

**Constsants**

.. csv-table:: 
    :widths: 15, 15, 35, 35 
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width
    
    "Name", "Alias", "Constant", "Value"
    "_pi", "pi", "The number π", "3.141592653589793238462643"
    "_e", "", "Euler's number", "2.718281828459045235360287"


.. hint::
    Behind the scenes LibreCAD uses the *muParser library* for the command line and many input boxes. So the above information describes basically the features of *muParser*, which are implemented in LibreCAD.

    For advanced users or the courious ones, you can read more about *muParser* on the inventors website:

    Reference: https://beltoforion.de/en/muparser/index.php#idStart

    But, be aware, that LibreCAD probably does not use the latest version of *muParser*. Also, it is not fully implemented. The *muParser* library has much more capabillities than LibreCAD uses.
