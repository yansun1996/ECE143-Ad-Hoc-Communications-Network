# File Description

* ```Problem_Statement.pdf```: Complete version of Problem statement.

* ```Region_Class.py```: Definition of communication network class, including all pivotal functions for the problem solution.

* ```Example.ipynb```: Tutorial for how to use the Region class and its function in Region_Class.py. (The solutions to all the problems are also included in this Jupyter Notebook)

NOTE: The analysis part of the solution is also included at the bottom of Example.ipynb.

# Analysis of Ad-Hoc Communications Network

You have been asked to help with planning an ad-hoc communications network over a large rectangular region. Each individual tower can monitor a rectangular subsection of a specific width and height. The main problem is that none of the individual towers can provide coverage for the entire region of interest. Communications towers are unreliable and are put up independently and at random. You have no control over where or how big a tower’s footprint is placed. Importantly, due to technical issues such as cross-talk, no individual rectangular subsection can have multiple towers providing coverage for it. That is, there can be no overlap between any pair of rectangular subsections provided by the two respective towers. In any case, the desire is to maximize the coverage area of any available communications tower.

The order of when the towers come online is important. Once a tower has acquired its rectangular section, no subsequent tower can overlap that section. You may assume the following for this problem:

* All rectangular sections have integer-based corners.
* All rectangular sections must be contained in the overall rectangular footprint.
* The height and width of each rectangular section is sampled from a uniform distribution.
* Positions of the windows are also determined by uniform random distribution.
* All footprints must be rectangles (not general polygons).
* When a new tower comes online, if its coverage rectangle intersects the pre-existing composite footprint, then that new tower’s coverage is trimmed such that its maximum remaining coverage area is retained.

Write a detailed Jupyter notebook that implements a solution to this problem such that the user can supply the following overall size of desired coverage footprint and then determine the following:

* Given an overall desired coverage footprint and a sequence of n communications towers, what is the resulting resolved coverage?
* What is the total area of coverage relative to the desired total coverage area of the original footprint? That is, are there any gaps in coverage?
* On average, how many communications towers are required before full coverage is obtained?
