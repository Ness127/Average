def average(marks, function):
    '''
    A recursive function that gives you the average mark of a student in a subject.
    
    Parameters:
    ·marks: a tuple where students' marks are saved
    
    ·function: a list which structure is:
        [1º term, operator, 2º term]
        where the 'terms' are:
            -An int which represent the index of the marks saved in the parameter marks
            -A float.
            -A list with the same structure as function.
    
    Returns:
    ·Float : your mark
    '''
    
    #We establish the base case for an expresion like this: [0, '*', 0.5]
    if type(function[0]) is not list and type(function[2]) is not list:
        # If we have we have an type <<int>> it means that is an index of marks
        if type(function[0]) is int:
            return round(eval(f'{marks[function[0]]} {function[1]} {function[2]}'), 2) #Apliess the formula
        # If not it means that we already have acces to marks with an index
        else:
            return round(eval(f'{function[0]} {function[1]} {function[2]}'), 2) #Apliess the formula
    #We establish the general case for an expresion like this: [[0, '*', 0.5], '+', [1, '*', 0.5]]
    else:
        #if the first term is a list it turned into a floar by using the same function
        if type(function[0]) is list:
            first = average(marks, function[0])
            function[0] = first
        #same for the second term
        if type(function[2]) is list:
            second = average(marks, function[2])
            function[2] = second
        #return the final mark by using the same function with the base case
        return average(marks, function)
    
if __name__ == '__main__':    
    marks = (7, 9, 5, 8)
    
    #formula_FC = '1º * 0,1 + 2º * 0,1 + 3º * 0,1 + 4º * 0,7'
    formula_FC = [[[0,  '*' , 0.1], '+', [1,  '*' , 0.1]], '+', [[2,  '*' , 0.1], '+', [3,  '*' , 0.7]]]


 
    print(average(marks, formula_FC))
