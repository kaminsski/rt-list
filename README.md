# rt-list
Twitter rt list
import random
import time
import webbrowser

file = open("rt.txt","r",encoding= "utf-8")

l=list()

l1=list()

l2=list()

l3=list()

l22=list()

l33=list()

l4=list()

for i in file: 
    l.append(i)
  
for i in l:
    if i[0]=="@":
        l1.append(i)
      
ouracc=['@dailynft74\n', '@TrendNFT1\n', '@NFTForce74\n', '@rteam199\n', '@Commak4\n', '@nfteamerica\n', '@fastnftpro\n', '@dailymetanft\n', '@NFTtrendy1\n','@ExlusiveNft\n', '@CrazyAPE_nft\n', '@NFTLordKing\n', '@nftlordfirst\n']   


for i in ouracc:
    l1.remove(i)

        
    
random.shuffle(l1)

l2=list((l1[0],l1[1],l1[2],l1[3],l1[4]))

for i in l2:
    i=i[:-1]
    l22.append(i)

random.shuffle(l22)

l3=list((l1[0],l1[1],l1[2]))

for i in l3:
    i=i[:-1]
    l33.append(i)

random.shuffle(l33)

l4=(l1[0])

print("---------------------- Last 5 ----------------------")

time.sleep(3)

print("",l22[0],l22[1],l22[2],l22[3],l22[4])

time.sleep(2)

print("---------------------- Last 3 ----------------------")

time.sleep(2)

print("            ",l33[0],l33[1],l33[2])

time.sleep(2)

print("---------------------- Winner ----------------------")

time.sleep(2)

print("                    ╔═══════════════╗")

print("                     ",l4)

print("                    ╚═══════════════╝")

w=l4[1:]

time.sleep(2)

webbrowser.open('https://twitter.com/'+w)

file.close()
