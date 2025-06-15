# ROILLING BALL 3D SIMULATION
# MADE BY BETTYE J. TAYLOR 
# CODE IS MADE FOR SIMPLE 3D  SIMULATION TEST IN PYTHON
# CODE WAS COMPLETED IN 2 HOURS 

from vpython import *

# Create a 3D Scene
scene = canvas (title= '3D ROLLING BALL SIMULATION')

# Floor1
#Add "Floor" if Wanted 

# Ball 
ball_radius = 0.5
ball = sphere(pos=vector(-4, ball_radius, 0), radius=ball_radius, color=color.blue, make_trail=True)
ball.velocity = vector(2, 0, 0) # Move in the +x direction

# Simulation Parameters
dt = 0.01
angular_velocity = vector(0, 0, 0)

while True:
    rate(100)

    #Update Position
    ball.pos = ball.pos + ball.velocity * dt

    #Simulate roiling without slipping
    #w = v/R

    omega = cross(vector(0,1,0), ball.velocity) / ball_radius
    dtheta = mag(omega) * dt

    # Ball Rotation 
    ball.rotate(angle=dtheta, axis=omega.norm(), origin=ball.pos)

    # Bounce off the Walls
    if abs (ball.pos.x) > 4.5:
        ball.velocity.x = -ball.velocity.x
