# pyPHP-LaTeX
Python interpreter in PHP with built-in Mathjax javascript

Example code:
```
from sympy import *
from sympy.printing.mathml import mathml
init_printing(use_unicode=True) # allow LaTeX printing

# independent variables
x, y, z = symbols('x y z', real = True)

# parameters
nu, rho = symbols('nu rho', real = True, constant = True, positive = True)

# dependent variables
u, v, w = symbols('u v w', real = True, cls = Function)

print("$$")
print(latex(diff(u(x,y,z),x)))
print("$$")
```

Note: Without `print("$$")` at two sides of each LaTeX format formula, It will print plain text of LaTeX format formula instead of Mathjax printing.
