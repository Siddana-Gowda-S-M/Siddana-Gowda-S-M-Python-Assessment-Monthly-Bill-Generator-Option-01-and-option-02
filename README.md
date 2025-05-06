
 
 Python Assessment: Monthly Bill Generator (Option-01)

 
Project Overview:


The generate monthly bill function calculates monthly billing for items based on their active periods.

Requirements/Task(s):	

1. Input Parsing: The target month (e.g., "2024-11") is split into year and month to determine the billing period (Nov 1-30, 2024).

2. Data Processing: Each item in item list is processed:
	a.	Converts qty and rate to floats if they're strings.
	b.	Parses start date and stop date into datetime objects.
	c.	Invalid entries (missing keys or wrong formats) are skipped.

3. Active Items Filter: Only items active during the target month are considered (i.e., their date    range overlaps with the billing period).

4. Grouping: Items with the same item code, rate, and active period are grouped to avoid  duplication.

5. Billing Calculation:
	a.	For each group, the total quantity is summed.
	b.	If the active period is shorter than the month, the amount is prorated by days.
	c.	The total revenue is the sum of all line item amounts.
 

Conclusion:

This function is production-ready for scenarios requiring prorated billing, balancing accuracy with flexibility. Its modular design allows easy extensions (e.g., discounts, taxes) while maintaining clarity.


Python Assessment: Monthly Bill PDF Invoice Generator (Option-02)

Project Overview:

The generate monthly bill function calculates monthly billing for items based on their active periods and generate output as PDF format.

Requirements/Task(s):

1. Main Issues in Current Code:
	a)	The PDF generation is happening inside the item input loop (incorrect indentation)
	b)	Missing proper page layout and formatting
	c)	No error handling for user inputs
	d)	Limited styling options
	e)	The total amount calculation is inside the item loop
2. Key Improvements Made:
	a)	Fixed indentation so PDF is generated only after all items are collected
	b)	Added input validation with get_valid_input() function
	c)	Improved PDF formatting with better spacing and styling
 	d)	Added page continuation support if items list is long
	e)	Better organized the code structure
	f)	Added proper error handling for numeric inputs
	g)	Ensures at least one item is added before generating PDF

Conclusion: 

The code now properly collects all information first, then generates a well-formatted PDF invoice with proper error handling .
