import random
import numpy as np
import pandas as pd
class Tarafini_sec():
    Q=["R", "L"]
    def __init__(self, stations):
        self.stations= stations

    def ilerleme_yonu(self):
        move = random.choice(self.Q)
        return move
    
    def dmden_yurume(self, adım=None):
        patern=[]
        if adım is None:
            adım=random.choice(self.stations[1:-1])
        elif adım not in self.stations[1:-1]:
            raise ValueError("start_point should be in stations")
              
        patern.append(adım)
        e = self.stations.index(adım)
        while adım not in [self.stations[0], self.stations[-1]]:
            y = self.ilerleme_yonu()
            if y == "R":
                adım=self.stations[e+1]
                patern.append(adım)
       
            elif y == "L":
                adım=self.stations[e-1]
                patern.append(adım)
            e = self.stations.index(adım)
        return patern
Z=["A","B","C","D","E","F","G"]
z=Tarafini_sec(Z)
z.ilerleme_yonu()
z.dmden_yurume()
