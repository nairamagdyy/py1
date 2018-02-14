# python: subtract a square game 
#set player to 1  
player=1 
#set number of coins
print("Insert number of coins\n")
coinsnum=int(input())
while( coinsnum>50):
 print('Error,insert again\n')
 coinsnum=int(input())
print("coinsnum = ",coinsnum)
print("Now, start playing")
while True:
    move=int(input())
    if move in [1,4,9,16,25,36,49] and move<=coinsnum and coinsnum-move>=0: 
     coinsnum=coinsnum-move
     print('player',player,'insert',move)
     print('coinsnum = ',coinsnum)
    else:
      print('Error, insert again : ')
      continue
    if coinsnum==0:
      print('player',player,'wins')
      break
    if player==1:
       player=2 
    else:
       player=1
print('game over')
