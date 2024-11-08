# Program-5: Runge Kutta method of fourth order

## Question:

Find $$y(0.2)$$, given that $$\frac{dx}{dy} = x + y^2$$ , $$y(0) = 1$$ , using Runge-Kutta fourth order method.

## Aim:

To find approximate colution of the first order differential equation by using Runge-Kuttan Method

## Algorithm:

Step 1: Define the function $$f(x,y) = x + y ** 2$$

Step 2: Get the values of $$x_0, y_0, h$$

Step 3: Compute $$K_1 = h * f (x_0, y_0)$$

Step 4: Compute $$K_2 = h * f (x_0 + \frac{h}{2} , y_0 + \frac{K_1}{2})$$

Step 5: Compute $$K_2 = h * f (x_0 + \frac{h}{2} , y_0 + \frac{K_2}{2})$$

Step 6: Compute $$K_4 = h * f (x_0 + h , y_0 + K_3)$$

Step 7: Compute $$y = \frac{y_0 + ( K_1 + 2 * K_2 + 2 * K_3 + K_4 )}{6}$$

Step 8: Print the value of y.

## Program:
```
def f (x, y):
 return x+y**2
x0=float (input ("Enter initial point of x: "))
y0=float (input ("Enter initial point of y: "))
h=float (input ("Enter step value h: "))
k1=h*f (x0, y0)
k2=h*f (x0+h/2, y0+k1/2)
k3=h*f (x0+h/2, y0+k2/2)
k4=h*f (x0+h, y0+k3)
y=y0+(k1+2*k2+2*k3+k4)/6
print ("The value of y using RK method is %.4f"%y) 
```
## Output:

Enter initial point of x: 0

Enter initial point of y: 1

Enter step value h: 0.2

The value of y using RK method is 1.2735 

## Result:
The solution of first order equation is obtained by using Runge-Kutta method.
