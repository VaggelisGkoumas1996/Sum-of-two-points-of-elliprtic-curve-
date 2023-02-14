# Sum-of-two-points-of-elliprtic-curve-
def add_points(x_1, y_1, x_2, y_2, a, b):
    # Calculate the slope of the line passing through the two points
    if x_1 == x_2 and y_1 == y_2:
        # If the two points are the same, the slope of the line passing through them is undefined
        # In this case, we use the formula for finding the slope of the tangent line at the point
        m = (3 * x_1**2 + a) / (2 * y_1)
    else:
        m = (y_2 - y_1) / (x_2 - x_1)

    # Calculate the x and y coordinates of the third point
    x_3 = m**2 - x_1 - x_2
    y_3 = m * (x_3 - x_1) + y_1
    print("the m is :",m)
    return (x_3, y_3)

# Test the function with sample points on the curve y^2 = x^3 + a* x + b
#Insert the points of elliptic curves
x_1 = int(input("x_1= "))
y_1 = int(input("y_1= "))
x_2 = int(input("x_2= "))
y_2 = int(input("y_2= "))

#Insert a and b of elliptic curves
a = int(input("a= "))
b = int(input("b= "))

x_3, y_3 = add_points(x_1, y_1, x_2, y_2, a, b)

print("Point 1: ({}, {})".format(x_1, y_1))
print("Point 2: ({}, {})".format(x_2, y_2))
print("Point 3: ({}, {})".format(x_3,-y_3))
