# Email_validation-Code-in-Python-

email=input("Enter Your Email:")
k,j,d=0,0,0
if len(email)>=6:
    if email[0].isalpha():
        if ("@" in email) and (email.count("@")==1):
            if(email[-4]==".") ^ (email[-3]=="."):
                for i in email:
                    if i==i.isspace():
                        k=1
                    elif i.isalpha():
                        if i==i.upper():
                            j=1
                    elif i.isdigit():
                        continue
                    elif i=="_" or i=="." or i=="@":
                        continue
                    else:
                        d=1
                if k==1 or j==1 or d==1:
                    print("Wrong Email, Please Retry that's Can be  Space/Uppercase Error ")
                else:
                    print("That's a Right Email")
            else:
                print("Wrong Email, Please Try again.")                  # If we Missed to write ".com" then,
        else:
            print("Wrong Email, Please Check @ Symbol")
    else:
        print("Wrong Email, Your First Letter should be Alphabate")
else:
    print("Wrong Email , Check Your Email length. It's less ")

