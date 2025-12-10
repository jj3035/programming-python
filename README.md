def analyst_price(quantity,unitprice,codeclient):
    addi1=quantity*unitprice
    addi2=addi1
    if addi1>500000 and codeclient == "VIP" :
        k=addi1*0.02
        addi2=addi1-k
    elif addi1>500000:
        g=addi1*0.1
        addi2=addi1-g
    elif addi1>200000 and addi1<=500000:
        f=addi1*0.05
        addi2=addi1-f
    return (addi1,addi2)
if __name__=="__main__":
    quantity1=int(input("pick a number"))
    unitprice1=float(input("pick a number"))
    codeclicent1=input("code")
    answer=analyst_price(quantity1,unitprice1,codeclicent1)
    print (answer)
