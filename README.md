SYCS100-Project
===============
def binarySearch(BostonCeltics,MiamiHeat):
    found = False
    low = 0
    high = len(MiamiHeat)-1
    while low<=high and not found:
        middle = (low+high)//2
        if MiamiHeat[middle]==BostonCeltics:
            found = True
        elif MiamiHeat[middle] < BostonCeltics:
            low = middle + 1
        else:
            high = middle-1
        return found

MiamiHeat= [15,24,27,30,35,45,50,55]    
BostonCeltics= [15,20,26,32,35,45,50,80]
if MiamiHeat>=5:
    MiamiHeat = [15,24,27,30,33,35,45,50,55]
    team = int(input("How many points did your team score?"))
    isitFound= binarySearch(BostonCeltics,MiamiHeat)
    if isitFound is True:
        print("is in index")
    else:
        print("-1")
#My Binary Search that uses NBA Teams
#This BinarySearch cuts the list in half by 2 when searching.
