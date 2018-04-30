KidGesture Dataset

Overview:
This dataset consists of children's touchscreen gestures, each stored as an XML file. The gestures were collected in five different studies:
Study 1 (Smartphone)
Study 2 (Smartphone) 
Study 3 (Smartphone)
Study 4 (Tablet)
Study 5 (Tabletop)

Data Format:
Each gesture is stored as a single XML file. 
In each session, the participant was asked to draw each of 20 gesture types a total of 6 times. The gesture set [Anthony et al., IDC '13] included numbers (2,4,5,7,8),
letters (A,E,K,Q,X), shapes (diamond,circle,line,rectangle,triangle) and symbols (arch,arrowhead,checkmark,heart,plus).


The following is an example of contents of an XML file. The first line is a standard XML heading. The second line opens a Gesture tag and specifies the name,
subject (user ID), number of points, screen width, and screen height. Within the Gesture is a series of Strokes, which are indexed starting at 1, as well as
the duration of the stroke. Each Point within the stroke has an X and Y coordinate as well as the timestamp at which the point was created (in milliseconds).

<?xml version="1.0" encoding="utf-8" standalone="yes"?>
<Gesture Name="line-1" Subject="555" NumPts="40" ScreenWidth="1080" ScreenHeight="1872">
	<Stroke index="1" duration="650.0">
		<Point X="181" Y="503" T="258244" />
		<Point X="185" Y="503" T="258284" />
		<Point X="188" Y="502" T="258294" />
		<Point X="189" Y="502" T="258295" />
		<Point X="192" Y="503" T="258304" />
                                ...
	</Stroke>
	<Stroke index="2" duration="320.0">
		<Point X="171" Y="503" T="258310" />
		<Point X="168" Y="503" T="258320" />
		<Point X="160" Y="502" T="258395" />
		<Point X="155" Y="502" T="258424" />
		<Point X="151" Y="503" T="258428" />
                              ...
	</Stroke>
</Gesture>

Directory structure:
The higest level contains five directories, one for each of the 5 studies, labeled Study-1, Study-2, Study-3, Study-4, and Study-5. Within each of these directories
are two directories: Complete (participants for which all data is present) and Incomplete (participants for which some data is missing). Within each of these
directories there are further directories depending on the study. In Study-1, there is a folder of Visual-Feedback and No-Visual-Feedback. In Study-3, there is a folder
for Abstract-Application or Complex-Application. In Study-4, there is a folder for Pen input and Finger input.


Demographics:
Demographic information, including the gender, age, and grade level (for children) is included in demographics.csv.

If you use our dataset, please cite as following:
[CITATION]