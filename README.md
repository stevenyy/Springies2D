Springies2D
===========
---- Worked together with Kanchan Chauhan

Please see course URL for this project:


Design Plan
============
In order to implement the project, one would have to implement it from main class. Our design contains at most 4 packages and takes advantages of various ways of inheriting. 


Notes from Part 1 Design Meeting:

Required fields:
Spring:
1. m1, m2, rest length, constant k
2. m1, m2, rest length
3. m1, m2

Muscle:
1.m1, m2, rl, amplitude

			Classes, inheritance structure, and packages needed: 

	public abstract class Foo
		field: id1, id2
		Constructor: Foo
		abstract method: connect

	public class Spring extends Foo
		field: rest length, constant
		Constructor: super Foo
		method: implement abstract connect
		 	  springiness
		
	public class Muscle extends Spring  
		field: amplitude
		Constructor: super Spring
		method:  implement abstract connect
		   		expand&contract

	public class Environment
		field: gravity, friction, energy speed
		Constructor:
		method:
			setGravity
			setFriction(bouncingFactor)
			setEnergySpeed


	public abstract class Bar
		field: id, x, y
		Constructor:
		methods:
			Abstract setMove
			Abstract setStationary	

	public class StationaryMass extends Bar
		constructor: super Bar
		method:
			implements Abstract setStationary

	public class MovingMass extends Bar
		field:vx, vy
		constructor:super Bar
		method:
			implements Abstract setMovement
