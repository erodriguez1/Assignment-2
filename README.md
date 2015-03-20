# Assignment-2
Special Relativity and the Semi-Empirical Mass Formula 


#Elizabeth Rodriguez
#Phys 50733: Computational Physics
#Assignment 2

#1: Special Relativity
# A spaceship travels from Earth in a straight line at a (relativistic) speed v to another planet x light years
#away. Write a program to ask the user for the value of x and the speed v as a fraction of the speed of light,
#then print out the time in years that the spaceship takes to reach its destination (a) in the rest frame of an
#observer on Earth and (b) as perceived by a passenger on board the ship. Use your program to calculate the
#answers for a planet 10 light years away with v=0.90c, v=0.98c, v=0.999c. {gamma=1/(sqrt(1-(v^2/c^2)))} (Time dilation factor)
# For full credit: Email your program plus an output of the program in action showing the answers it produces

#(A)

# When v=0.90c
from __future__ import division
import math
x = int(input('Enter the distance (lyrs):')) # The planet is 10 lyrs away
v_1 = float(input('Enter the fraction of the speed of light:'))# In this case v=0.90 with respect to c
t_1 = round(x/v_1,1) # One-way trip that is measured on Earth, if it was round trip the equation becomes t=(2*x)/v
print 'The following spaceship traveled at a distance of',x,'with units in lyrs and a respected fraction of the speed of light',v_1,'the rest frame of an observer on Earth in yrs is',t_1

# When v=0.98c
from __future__ import division
import math
x = int(input('Enter the distance (lyrs):')) # The planet is 10 lyrs away
v_2 = float(input('Enter the fraction of the speed of light:'))# In this case v=0.98 with respect to c
t_2 = round(x/v_2,1) # One-way trip that is measured on Earth, if it was round trip the equation becomes t=(2*x)/v
print 'The following spaceship traveled at a distance of',x,'with units in lyrs and a respected fraction of the speed of light',v_2,'the rest frame of an observer on Earth in yrs is',t_2

# When v=0.999c
from __future__ import division
import math
x = int(input('Enter the distance (lyrs):')) # The planet is 10 lyrs away
v_3 = float(input('Enter the fraction of the speed of light:'))# In this case v=0.999 with respect to c
t_3 = round(x/v_1,1) # One-way trip that is measured on Earth, if it was round trip the equation becomes t=(2*x)/v
print 'The following spaceship traveled at a distance of',x,'with units in lyrs and a respected fraction of the speed of light',v_3,'the rest frame of an observer on Earth in yrs is',t_3

#2: The Semi-Empirical Mass Formula
# In nuclear physics, the semi-empirical mass formula is a formula for calculating the approximate nuclear
#binding energy B of an atomic nucleus with atomic number Z and mass number A. The formula looks like this:
# B=a_1*A-a_2*A^(2/3)-a_3*(Z^2/A^(1/3))-a_4*((A-2Z)^2/A)-a_5/A^(1/2) where, in units of millions of electon
#volts (MeV), the constants are a_1=15.67, a_2=17.23, a_3=0.75, a_4=93.2, and
#a_5= {0 if A is odd, 12.0 if A and Z are both even, -12.0 if A is even and Z is odd}. Write a program that
#takes as its input the values of A and Z, and prints out (a) the binding energy B for the corresponding atom
#and (b) the binding energy per nucleon, which is B/A. Use your program to find the binding energy of an atom
#with A=58 and Z=28. (Hint: The correct answer is around 490 MeV). Also run, A=59 and Z=28 and A=58 and Z=27.
# For full credit: Email your program plus an output of the program in action showing the answers it produces


#(A)

# When A=58 and Z=28
from __future__ import division
import math
a_1= 15.67
a_2= 17.23
a_3= 0.75
a_4= 93.2
a_5= 12.0 #Changes depending what A and Z are
A_1= int(input('Enter mass number, A:')) #Input 58
Z_1= int(input('Enter atomic number, Z:')) #Input 28
B_1= round(a_1*A_1-a_2*A_1**(2/3)-a_3*(Z_1**2/A_1**(1/3))-a_4*((A_1-2*Z_1)**2/A_1)-a_5/A_1**(1/2),1)
print 'The binding energy B (MeV) for the corresponding A=58 and Z=28 is', B_1 #Units are MeV

#(B): Binding energy per nucleon, which is B/A
bepn_1= round(B_1/A_1,3) # The binding energy per nucleon
print 'The binding energy per nucleon is:', bepn_1

# When A=59 and Z=28
from __future__ import division
import math
a_1= 15.67
a_2= 17.23
a_3= 0.75
a_4= 93.2
a_5= 0.00 #Changes depending what A and Z are
A_2= int(input('Enter mass number, A:')) #Input 59
Z_2= int(input('Enter atomic number, Z:')) #Input 28
B_2= round(a_1*A_2-a_2*A_2**(2/3)-a_3*(Z_2**2/A_2**(1/3))-a_4*((A_2-2*Z_2)**2/A_2)-a_5/A_2**(1/2),1)
print 'The binding energy B (MeV) for the corresponding A=59 and Z=28 is', B_2 #Units are MeV

#(B): Binding energy per nucleon, which is B/A
bepn_2= round(B_2/A_2,3) # The binding energy per nucleon
print 'The binding energy per nucleon is:', bepn_2

# When A=58 and Z=27
from __future__ import division
import math
a_1= 15.67
a_2= 17.23
a_3= 0.75
a_4= 93.2
a_5= -12.0 #Changes depending what A and Z are
A_3= int(input('Enter mass number, A:')) #Input 58
Z_3= int(input('Enter atomic number, Z:')) #Input 27
B_3= round(a_1*A_3-a_2*A_3**(2/3)-a_3*(Z_3**2/A_3**(1/3))-a_4*((A_3-2*Z_3)**2/A_3)-a_5/A_3**(1/2),1)
print 'The binding energy B (MeV) for the corresponding A=58 and Z=27 is', B_3 #Units are MeV

#(B): Binding energy per nucleon, which is B/A
bepn_3= round(B_3/A_3,3) # The binding energy per nucleon
print 'The binding energy per nucleon is:', bepn_3
