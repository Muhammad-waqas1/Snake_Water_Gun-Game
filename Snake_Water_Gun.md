**# Snake_Water_Gun-Game**
You can run your code using 2 methods:<br>
    1)Using If_Else<br>
    2)Using Mathematical Operations
```
import pyttsx3

# Include Vocals:
def vocals(greet):
    friend=pyttsx3.init()
    voices=friend.getProperty('voices')
    friend.setProperty('voice',voices[0].id)
    if(greet==0):
        friend.say(f"You     Win.")
        f=open("icon.png","rb")
        f.write
        f.close()
    elif(greet==1):
        friend.say(f"You     lose.")
        # friend.say(f"You     Win.")
        f=open("icon.png","rb")
        f.write
        f.close()
    elif(greet==2):
        friend.say(f"Tie.")
        # friend.say(f"You     Win.")
        f=open("icon.png","rb")
        f.write
        f.close()
    elif(greet==3):
        friend.say(f"Please Enter in Upper Case letters.")
    elif(greet==4):
        friend.say(f"Wrong Input!")
    elif(greet==5):
        friend.say(f"Invalid Input!")
    friend.runAndWait()
    friend.stop()
```


# Using If_Else :
```
def using_if():
    user=input("\nEnter 'S' for Snake, 'W' for Water OR 'G' for Gun: ")
    import random as rd


    collect=['S','W','G']
    comp=str(rd.choices(collect))       # print list
    comp_1=str(rd.choice(collect))      # print string
    user_1=list(user)
    # print(user)
    # print(comp)
    # print(comp_1)

    # For Snake

    if(user == "S"):
        if(comp_1=="S"):
            print(f"Computer was also {comp_1}".center(-80))
            print(f"Tie".center(-80))
            vocals(2)
        elif(comp_1=="W"):
            print(f"Computer was {comp_1}".center(-80))
            print("You Win".center(-80))
            vocals(0)
        elif(comp_1=="G"):
            print(f"Computer was {comp_1}".center(-80))
            print("You Loss".center(-80))
            vocals(1)

    # For Water

    elif(user == "W"):
        if(comp_1=="S"):
            print(f"Computer was {comp_1}".center(-80))
            print("You Loss".center(-80))
            vocals(1)
        elif(comp_1=="W"):
            print(f"Computer was also {comp_1}".center(-80))
            print(f"Tie".center(-80))
            vocals(2)
        elif(comp_1=="G"):
            print(f"Computer was {comp_1}".center(-80))
            print("You Win".center(-80))
            vocals(0)
    # For Gun

    elif(user == "G"):
        if(comp_1=="S"):
            print(f"Computer was {comp_1}".center(-80))
            print("You Win".center(-80))
            vocals(0)
        elif(comp_1=="W"):
            print(f"Computer was {comp_1}".center(-80))
            print("You Loss".center(-80))
            vocals(1)
        elif(comp_1=="G"):
            print(f"Computer was also {comp_1}".center(-80))
            print(f"Tie".center(-80))
            vocals(2)
    elif(user == "g") or (user == "w") or (user == "s"):
        print("Please Enter in Upper_Case letters")
        vocals(3)
    else:
        print("Wrong input!")
        vocals(4)
        #     S W G
        # S:  D W L
        # W:  L D W
        # G:  W L D
```
# Using Mathematical Operations:
```
def using_math():
    user_math=int(input("\nEnter '0' for Snake,'1' for Water or '2' for Gun: "))
    if(user_math != 0) and (user_math != 1) and (user_math != 2):
        print("Invalid Input!")
        vocals(5)
    import random as rd

    cont=[["Tie","You Win","You Loss"],["You Loss","Tie","You Win"],["You Win","You Loss","Tie"]]
    collect_math=[0,1,2]
    comp_math=int(rd.choice(collect_math))

    # print(comp_math)
    # print(type(comp_math))
    # print(type(user_math))
    if(user_math == 0):  # Snake
        cont_1=cont[0]
        if(comp_math==0):
            print(f"Computer was also Snake".center(-80))
            print(f"{cont_1[0]}".center(-80))
            vocals(2)
        elif(comp_math==1):
            print("Computer was Water".center(-80))
            print(f"{cont_1[1]}".center(-80))
            vocals(0)
        elif(comp_math==2):
            print("Computer was Gun".center(-80))
            print(f"{cont_1[2]}".center(-80))
            vocals(1)
    elif(user_math == 1):  # Water
        cont_1=cont[1]
        if(comp_math==0):
            print(f"Computer was Snake".center(-80))
            print(f"{cont_1[0]}".center(-80))
            vocals(1)
        elif(comp_math==1):
            print("Computer was also Water".center(-80))
            print(f"{cont_1[1]}".center(-80))
            vocals(2)
        elif(comp_math==2):
            print("Computer was Gun".center(-80))
            print(f"{cont_1[2]}".center(-80))
            vocals(0)
    elif(user_math == 2):  # Gun
        cont_1=cont[2]
        if(comp_math==0):
            print(f"Computer was Snake".center(-80))
            print(f"{cont_1[0]}".center(-80))
            vocals(0)
        elif(comp_math==1):
            print("Computer was Water".center(-80))
            print(f"{cont_1[1]}".center(-80))
            vocals(1)
        elif(comp_math==2):
            print("Computer was also Gun".center(-80))
            print(f"{cont_1[2]}".center(-80))
            vocals(2)

option=int(input("Enter '0' for using_if OR '1' for using_math: "))
if(option==0):
    using_if()
elif(option==1):
    using_math()
else:
    print("Wrong Input!")
    vocals(4)
```
