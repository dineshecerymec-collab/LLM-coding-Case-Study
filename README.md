def square_root_bisection(number,tolerence=0.01,iterations = 10):
    if number < 0:
        raise ValueError("Square root of negative number is not defined in real numbers")
    elif number == 1 or number == 0:
        print(f"The square root of {number} is {number}")
        return number
    else:
        high = number
        low = 0
        dec = len(str(tolerence).split('.')[1]) if '.' in str(tolerence) else 0        
        while iterations:
            iterations -= 1         
                        
            mid = (low + high)/2
            
            if abs(mid**2 - number) <= tolerence:
                print(f"The square root of {number} is approximately {mid:{dec}f} ")
                break
            elif mid**2 > number:
                high = mid
            
            else:
                low = mid
        print(mid)

square_root_bisection(0.001, 1e-7, 50)
