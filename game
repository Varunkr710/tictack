import random
class game:
    def __init__(self):
        self.board=[" " for i in range(9)]
        self.reboard=[i+1 for i in range(9)]
    def printing(self):
         for i in range(9):
           sun="|"+str(self.board[i])+"|"
           print(sun,end=" ")
           if (i+1)%3==0:
              print("\n")
    def reprinting(self):
        for i in range(9):
           sun="["+str(self.reboard[i])+"]"
           print(sun,end=" ")
           if (i+1)%3==0:
              print("\n")
    def empty(self):
        return [i for i in range(9) if self.board[i]==" "]          
    def human(self):
        enter=int(input("Enter the valid number from the board 1 to 9 "))
        while (enter-1) not in self.empty():
            print("You have entered a wrong number please enter correct number ")
            enter=int(input("Please enter correct number "))
        self.board[enter-1]="O"
    def Computer(self):
        com=random.randrange(0,10)
        while com not in self.empty():
            com=random.randrange(0,10)
        self.board[com]="X"
    def running(self):
        count=0
        for i in range(4):        
           self.reprinting()
           self.human()
           self.Computer()
           self.printing()
           count+=1
           mon=self.winner()

           if mon!=False:
               print(mon,"is winner")
               break
        if count==4:
            print("It is tie")           
    def winner(self):
        varun=[]
        a=[]
        for i in range(0,9,3):
            a=self.board[i:i+3]
            if a.count("O")==3:
                return "o","horizontal",i,i+1,i+2
                
            if a.count("X")==3:
                return "x","horizontal",i,i+1,i+2
                
            
        varun=[]    
        for i in range(3):
            varun.append(self.board[i])
            varun.append(self.board[i+3])
            varun.append(self.board[i+6])
            if varun.count("O")==3:
                return "vertical","O",i,i+3,i+6
                
            if varun.count("X")==3:
                return "vertical","X",i,i+3,i+6
            varun=[]    
        varun=[]    
        i=0
        varun.append(self.board[i])
        varun.append(self.board[i+4])
        varun.append(self.board[i+8])
        if varun.count("O")==3:
            return "Diagonal","O",i,i+4,i+8
            
        if varun.count("X")==3:
            return "Diagonal","X",i,i+4,i+8
            
        varun=[]
        i=2
        varun.append(self.board[i])
        varun.append(self.board[i+2])
        varun.append(self.board[i+4])
        if varun.count("O")==3:
            return "Next diagonal","o",i,i+2,i+4
            
        if varun.count("X")==3:
            return "Next diagonal","X",i,i+2,i+4
            
        return False
            
tarun=game()
tarun.running()
