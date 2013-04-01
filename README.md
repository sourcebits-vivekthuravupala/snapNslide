snapNslide
==========
Small plugin allowing the user to select ranged/single slider selections. Exposes an API to allow easy interfacing with 3rd party code.

Useful Stuff
------------

- Properties:
	- snapIncrement : The pixel width of a single increment, between two minor nodes. ( Default value 5 )
	- nodeIncrement : The distance between two major nodes, inclusive. So if this value is 10, then there are 9 increments between two major nodes. ( Default value 10 )
	- Each increment also has the following properties
		- Value : The numeric/string value assigned to this node
		- Label : The label assigned to this node
		- Type  : String denoting whether this node is a [Major] or [Minor] node

- Getters:
	- getValue : Returns the currently selected value, only to be used for single value selections. If a range is selected, this returns false
	- getRange : Returns the selected range as an object { lower, upper }

- Setters:
	- setValue : Accepts a value ( Numeric or string ), to assign to the slider. On success returns true, and on failure returns false
	- setRange : Sets the range, accepts an object { lower, upper }

- Methods:
	- selectAll : Method to automatically select range from the minumum to the maximum
