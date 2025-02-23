# Wiring-the-house
Wiring the house Solved


Download Link : https://programming.engineering/product/wiring-the-house-solved/

You have decided to build a new house, but you are hoping to save costs by doing some of the work yourself. Specif-ically, you think you are able to do the electrical wiring. The wiring works by using di erent types of junction points and running electrical wires between these junction points. Complicating things slightly, there are several types of junction points:

Breaker Box: This is a special node in from which the electricity is sourced. There will only be one breaker box that supplies electricity to your entire house.

Switch: A switch is a special node that can a ect the current moving along a path from the breaker box, and can be turned o to not allow current to continue past the switch onward.

Light: A light is a node that is controlled by a switch.

Thus, there MUST be exactly one switch between the light and the breaker box. Each light has a speci c switch you want to control it with, and thus that particular switch must be the one between the light and breaker box.

Electrical Outlet: You want your outlets to be ac-tive all of the time. Thus, an outlet must have a path directly to the breaker box with NO switches in between.

Junction Box: A junction box is simply a location that can connect multiple wires together. For exam-ple, one wire from the breaker can go into a junction box, and three wires can fan out of the box to dis-tribute electricity to the house.

Given the layout of the di erent junction points and the cost of wiring them to each other, can you gure out the cheapest way to wire your house? Consider the following when implementing your solution:

Your solution can use either Prim’s or Kruskal’s algorithm. You may need to custom build the associated data structure for each algorithm, so consider this choice carefully.

Your wired house must be a spanning tree (there can be no cycles)

Lights can be wired to one another if they have the same desired switch, as long as the switch is between all those lights and the breaker.

Every type of junction point (breaker, switch, boxes, etc.) must be connected into your wiring.

junction boxes (and outlets) should never be behind switches in your spanning tree. Thus, once your spanning tree reaches a switch, only lights (though many of them potentially) will be behind the switch.

Attention! In past semesters, we posted a help document with some advice and hints at this link (you are welcome to take a look at it):

https://bit.ly/3iwXrEL

Input

The input le will begin with one line containing integers J and C, the number of junction points and the number of possible connections respectively. The next J lines will each specify the name of a junction point along with the type (breaker, switch, light, outlet, box). When a switch is listed, the lights that need to be behind that switch will be always listed next to indicate this dependency. There will only be one breaker box. The next C lines specify the connections by providing the name of two junction points and the cost between them.

Output

Output the cost of the minimum wiring for the house that adheres to all of the constraints

Sample Input

6 8
			

b1
	

breaker
	

j1
	

box
		

s1
	

switch
	

l1
	

light
	

l2
	

light
	

Sample Output

o1
	

outlet

b1
	

j1
	

5
	

7

b1
	

o1
	

1

j1
	

s1
	

1
	

j1
	

o1
	

2
	

o1
	

l1
	

1
	

l1
	

l2
	

2
	

s1
	

l1
	

6
	

s1
	

l2
	

1
	
Solution
