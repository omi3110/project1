# project1
python mini project
import random

print("Ludo King\n")
print("For 'Exit' enter number greater than 6\n")


User_score = 0
CPU_score = 0

while True:
    User = int(input("User: "))
    CPU = random.randint(1, 6)

    if User >= 1 and User <= 6:

        if User > CPU:
            print("CPU:", CPU)
            print("User Win\n")
            User_score += 1

        elif User < CPU:
            print("CPU:", CPU)
            print("CPU Win\n")
            CPU_score += 1

        else:
            print("CPU:", CPU)
            print("Draw\n")
    elif  User > 6:
        break
    else:
        print("Kindly enter number greater than 0\n")


print("User score:", User_score)
print("CPU score:", CPU_score)
print("")

if User_score > CPU_score:
    print("User win by {0} Point".format(User_score - CPU_score))
elif User_score < CPU_score:
    print("CPU win by {0} Point".format(CPU_score - User_score))
else:
    print("Game is Draw")
