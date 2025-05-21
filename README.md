# Program 5: Runge Kutta method of fourth order

<br>

## Date: 21-05-2025
## Name: KARTHIKEYAN S
## Reg No: 212224230116

<br>

## Question:

<br>

Find $$y(0.2)$$, given that $$\frac{dx}{dy} = x + y^2$$ , $$y(0) = 1$$ , using Runge-Kutta fourth order method.

<br>

## Aim:

<br>

To find approximate colution of the first order differential equation by using Runge-Kuttan Method

<br>

## Algorithm:

<br>

Step 1: Define the function $$f(x,y) = x + y ** 2$$

<br>

Step 2: Get the values of $$x_0, y_0, h$$

<br>

Step 3: Compute $$K_1 = h * f (x_0, y_0)$$

<br>

Step 4: Compute $$K_2 = h * f (x_0 + \frac{h}{2} , y_0 + \frac{K_1}{2})$$

<br>

Step 5: Compute $$K_2 = h * f (x_0 + \frac{h}{2} , y_0 + \frac{K_2}{2})$$

<br>

Step 6: Compute $$K_4 = h * f (x_0 + h , y_0 + K_3)$$

<br>

Step 7: Compute $$y = \frac{y_0 + ( K_1 + 2 * K_2 + 2 * K_3 + K_4 )}{6}$$

<br>

Step 8: Print the value of y.

<br>

## Program:

<br>

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

<br>

## Output:

<br>

Enter initial point of x: 0

<br>

Enter initial point of y: 1

<br>

Enter step value h: 0.2

<br>

The value of y using RK method is 1.2735 

<br>

## Result:

<br>

The solution of first order equation is obtained by using Runge-Kutta method.
