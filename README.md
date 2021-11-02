# FP1-S01-Dictionaries-Program
#Simple use of arrays


#____________________________________________________#
#Ben Walz
#FP1-S01 Dictionaries Program
#Student marking system
#____________________________________________________#
#Dict
Student_Marks = {}
#____________________________________________________#
#funcions
def addstudent():
    go = True
    newstudent = input("What is the name of the student? ").lower()
    while go == True:
        marks = input("What are the marks of the student? Please give marks one at a time. Type 'done' when marks are entered. ").lower()
        if marks == 'done':
            go = False
        else:
            Student_Marks[newstudent] = marks
    
    
    print(Student_Marks)
    
    
addstudent() 



