import numpy as np
import matplotlib.pyplot as plt

class Unicycle:
    def __init__(self, x: float, y: float, theta: float, dt: float):
        self.x = x
        self.y = y
        self.theta = theta
        self.dt = dt
        self.x_points = [self.x]
        self.y_points = [self.y]

    def step(self, v: float, w: float, n: int):
        
        for time in np.arange(0,n*self.dt,self.dt):
           
            self.theta = self.theta + w*self.dt
            self.x = self.x + (v*np.cos(self.theta)*self.dt)
            self.y = self.y + (v*np.sin(self.theta)*self.dt)
            self.x_points.append(self.x)
            self.y_points.append(self.y)

        return self.x,self.y,self.theta

    def plot(self, v: float, w: float):
        plt.title(f"Unicycle Model: {v}, {w}")
        plt.xlabel("X-Coordinates")
        plt.ylabel("Y-Coordinates")
        plt.plot(self.x_points, self.y_points, color="red", alpha=0.75)
        plt.grid()
        plt.show() 

if __name__ == "__main__":
    print("Unicycle Model Assignment")

    p1=Unicycle(0,0,0,0.1)
    p1.step(1.0,0.5,25)
    p1.plot(1.0,0.5)

    p2=Unicycle(0,0,1.57,0.2)
    p2.step(0.5,1.0,10)
    p2.plot(0.5,1.0)

    p3=Unicycle(0,0,0.77,0.05)
    p3.step(5.0,4.0,50)
    p3.plot(5.0,4.0)
