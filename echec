plateau=[[2,3,4,5,6,4,3,2],[1,1,1,1,1,1,1,1],[0,0,0,0,0,0,0,0],[0,0,0,0,0,0,0,0],[0,0,0,0,0,0,0,0],[0,0,0,0,0,0,0,0],[-1,-1,-1,-1,-1,-1,-1,-1],[-2,-3,-4,-5,-6,-4,-3,-2]]

def testmoove(plat,u,v,ub,vb,j):
    x=plat[u][v]
    if x==1 or x==-1:
        if x==1:
            if u+1==ub and((v+1==vb and plat[ub][vb]<0) or (v-1==vb and plat[ub][vb]<0)):
                return 1
            if u+1==ub and v==vb and plat[ub][v]==0:
                return 1
            if (u==1 and v==vb and u+2==ub and plat[u][v+1]==0 and plat[u][v+2]==0):
                return 1
        if x==-1:
            if u-1==ub and((v+1==vb and plat[ub][vb]>0) or (v-1==vb and plat[ub][vb]>0)):
                return 1
            if v==vb and u-1==vb and plat[u][vb]==0:
                return 1
            if u==6 and v==vb and u-2==ub and plat[u][v-1]==0 and plat[u][v-2]==0:
                return 1                    
        return 0
    return 1
    
def game(plat,j):
    print(plat[7][2])
    i=0
    while i<8:
        print(plat[i])
        i=i+1
    x=int(input(': '))
    v=x//10-1
    u=x%10-1
    w=plat[u][v]*j
    if  w<1:
      print('impossible')
      return game(plat,j)
    y=int(input(': '))
    ub=y%10-1
    vb=y//10-1
    if testmoove(plat,u,v,ub,vb,j)==0:
      print('impossible')
      return game(plat,j)
    print(w)
    print(plat[ub][vb])
    plat[ub][vb]=w*j
    plat[u][v]=0
    return game(plat,-j)
game(plateau,1)
