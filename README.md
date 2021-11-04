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
    newstudent = input("What is the name of the student? ")
    print("What are the marks of the student? Please give marks one at a time. Type 'done' when marks are entered")
    while go == True:
        marks = input("Marks > ").lower()
        if marks == 'done':
            go = False
        else:
            marks = int(marks)
            final_mark = marks + final_mark
            number_marks = number_marks + 1
    final_mark = final_mark / number_marks
    Student_Marks[newstudent] = final_mark
    print("You added", newstudent, "with an average of", final_mark)
    
    
def removestudent():
    go = True
    print("What student do you want to remove? Type 'done' when student is removed. ")
    while go == True:
        student = input("Student> ")
        if student == 'done' or student == 'Done':
            go = False
        elif student in Student_Marks:
            print("You removed", student)
            del Student_Marks[student]
            go = False
        else:
            print("That student is not in the list")


def printstudents():
    print("Here are your students and they're marks")
    print(Student_Marks)
        
        
    
def main():
    print("""This program makes a list of students and they're averages.
You can add students and there averages
Remove students
Print list
or exit
""")
    
    repeat = 1
    while repeat == 1:
        print("What do you want to do?")
        answear = input("Add, Remove, Print, Exit. ")
        if answear == "add" or answear == "Add":
            addstudent()
        elif answear == "remove" or answear == "Remove":
            removestudent()
        elif answear == "print" or answear == "Print":
            printstudents()
        elif answear == "exit" or answear == "Exit":
            print("Thank you, goodbye")
            repeat = repeat - 1
        else:
            print("That is not an option")
            print(" ")
        
        
        
#Main Code#
#----------------------------------#
main()
        




