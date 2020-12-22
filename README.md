# ELECTION_

nomineted_1 = input("Enter first nomineter's name :")
nomineted_2 = input("Enter second nomineter's name :")
nomineted_3 = input("Enter third nomineter's name :")

votes_1 =0
votes_2 =0
votes_3 =0

total_voters = int(input("Total numbers of voter :"))
voter_ID = []
while total_voters >0 :
    voter_ID.append(total_voters)
    total_voters = total_voters - 1
x = 0
while True and x <= len(voter_ID):
    voter = int(input("Enter your voter ID :"))
    if voter in voter_ID :
        x = x +1
        print("You are applicable for voting..")
        print("please wait....")
        voter_ID.remove(voter)
        vote = int(input("Enter your nomineter code : "))
        if vote == 1 :
            votes_1 = votes_1 + 1
            print("Thanking you for voting :",nomineted_1 )
        elif vote == 2 :
            votes_2 = votes_2 + 1
            print("Thanking you for voting :", nomineted_2 )
        elif vote == 3 :
            votes_3 = votes_3 + 1
            print("Thanking you for voting :", nomineted_3 )
        else :
            print("Please Enter the code only show in the list at top")

    else :
        print("You are not applicable for voting ")
        print("Check your voter ID or you have already voted.")
print("1 :", votes_1)
print("2 :", votes_2)
print("3 :", votes_3)
z = dict()
z[nomineted_1] = votes_1
z[nomineted_2] = votes_2
z[nomineted_3] = votes_3
print(z)



