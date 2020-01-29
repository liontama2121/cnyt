# cnyt
#  LIBRERIA NUMEROS COMPLEJOS 
from sys import stdin
import math
'''libreria de numeros complejos'''
def suma (c1,c2):
    '''suma de numeros complejos la parte real[] + imaginario[]'''
    sumaN=c1[0]+c2[0]
    sumaI=c1[1]+c1[1]
    return (sumaN,sumaI)

def resta (c1,c2):
    '''resta numeros complejos la parte real[] + imaginario[]'''
    restaN=c1[0]-c2[0]
    restaI=c1[1]-c1[1]
    return (restaN,restaI)
def producto(c1,c2):
    '''multiplica numeros complejos la parte real[] + imaginario[]'''
    productoN=(c1[0]*c2[0]+(-1*c1[1]*c2[1]))
    productoI=c1[0]*c2[1]+c1[1]*c2[0]
    return (productoN,productoI)
def division(c1,c2):
    '''divide numeros complejos la parte real[] + imaginario[]'''
    divD=producto(c1,cambio)
    divDI=producto(c2,cambio)
    divD=list(divD)
    divDI=list(divDI)
    res(divD[0]/divDI[0],divD[1]/divDI[0])
    return(res)
def modulo(c1):
    '''retorna el modulo de un numero complejo'''
    res=(math.sqrt((c1[0]**2)+(c1[1]**2)))
    return(res)     
    
def conjugado(c1):
    '''cambia el simbolo en su parte imaginaria'''
    cambio=(c2[0],-1*c2[1])
    return(cambio)
def polar (c1):
    ''' de carteciano pasa a polar'''
    mod=modulo(c1)
    mod=round(mod,1)
    tan=math.atan2(c1[0],c1[1])
    grados=math.degrees(tan)
    grados=round(grados,0)
    return(mod,grados)
    
    
    



    
def main():
    lis1=[int (x) for x in stdin.readline().strip().split()]
    lis2=[int (x) for x in stdin.readline().strip().split()]
    comando=str(stdin.readline().strip())
    if comando=="+":
         res=suma(lis1,lis2)
         print(str(res[0]) + "+"+str(res[1])+"i")
    elif comando=="-":
         res=resta(lis1,lis2)
         print(str(res[0]) + "-"+str(res[1])+"i")
    elif comando=="*":
         res=producto(lis1,lis2)
         print(str(res[0]) + "*"+str(res[1])+"i")
    elif comando=="/":
        if lis2[0]==0 and lis2[1]==0:
         print("Division imposible")
         main()
        else:
           res=division(lis1,lis2)
           print(res)
    elif comando=="mod":
         res=modulo(lis1)
         res2=modulo(lis2)
         print(str(res),"i")
         print(str(res2),"i")
    elif comando=="cojugado":
         res=conjugado(lis1)
         res2=conjugado(lis2)
         print(res)
         print(res2)
    elif comando=="polar":
        res=polar(lis1)
        res2=polar(lis2)
        print(str(res[0])+"+"+"e^i("+str(res[1])+")")
        print(str(res2[0])+"+"+"e^i("+str(res2[1])+")")
        
         
        
   
    

main()
 

