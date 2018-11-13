# classandabc

from  abc import ABC,abstractmethod
from functools import reduce


class parrot:
    specie = "bird"
    def __init__(self,name,age):
        self.name=name
        self.age=age

blu=parrot("blu",10)

print("blue is a {}".format(blu.__class__.specie))

print("blu is a {}".format(blu.age))


class penguin(ABC):
    @abstractmethod
    def bird(self):
        print("penguin")

class swim(penguin):
    def bird(self):
        super().bird()
        print("penguin can swim ")

x=swim()
x.bird()




numbers = [1, 2, 3]

result = map(lambda x:x**2, numbers)
print(list(result))

print(reduce(lambda x,y:x+y,numbers))

