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
    final_mark = 0
    number_marks = 0
    go = True
    newstudent = input("What is the name of the student? ").lower()
    while go == True:
        marks = input("What are the marks of the student? Please give marks one at a time. Type 'done' when marks are entered. ").lower()
        if marks == 'done':
            go = False
            
        
        else:
            marks = int(marks)
            final_mark = marks + final_mark
            
            number_marks = number_marks + 1
                
    final_mark = final_mark / number_marks
    
    Student_Marks[newstudent] = final_mark
    print(Student_Marks)
    
    
addstudent() 


#note - make a description in main to describe what it does - gets kids marks and averages
