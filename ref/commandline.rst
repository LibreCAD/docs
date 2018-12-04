.. _commandline:

Using the Command Line
======================

Introduction
------------

For a quick reference list of commands see `Drawing Tools <tools>`

This is intended for people that want to draw by entering commands. This can be faster and/or more precise than drawing using exclusively a mouse and toolbars.

LibreCAD is designed with emphasis on mouse-clicking input, and some options can be at the moment only selected by clicking, not by typing on command line.


Using the Command line
----------------------

You can press the Space-bar or [Ctrl]-M to activate the command line.

When the command line is active the "Command:" (left of where input appears) turns blue. So now when you press a key you are entering commands.

You press the [Esc] key to leave the command line and another [Esc] to cancel what you have written on the command line.

It is possible to enter a partial command, like "cir" and press [Tab] to have the command completed to circle. If you type too short a segment of a command, such as "c" and press [Tab], the command output will show "ch, circle, cut" because the command segment you typed in isn't unique.

Many commands prompt you on the command line asking for further input. They tell you what input they expect, a point for example, and list other possibilities in the square bracket.  For example if you type command polyline and draw at least two segments you get prompted "Specify next point" or [undo/close]. This means that the program is expecting a point (from the command line or by clicking on drawing area), or you can select the Undo or Close option. You can do that by typing on the command line or by clicking on buttons on the context toolbar called Tool Options.

When there is some value already set and valid, for example when you use command offset, the current value is in sharp brackets, like so: Specify distance <5> or select entity or [Through]. So you see that value for offset is 5 and you can either set a new value by typing it into the command line or using the Tool Options toolbar or you can start drawing parallel entities.

Every command I describe below has a long format and a short format. For example the command for drawing a line has three formats\:

    line
    li
    l

To use the two letter format li you do not have to activate the commandline. Just type li and LibreCAD displays the prompt. If you wish to continue drawing with just mouse input, you click on drawing to enter the point, or click on the tools palette to select the snap mode or whatever.

Clear commands from commands window

To clear the list of commands from the command window - type "clear" in the command line.
Drawing entities
Drawing a point

point
po
Specify location

You type point or po on the command line. LibreCad prompts you to with "Specify Location".

After selecting any desired snapping options on the main toolbar you can respond by clicking with the mouse on the drawing area to enter points. Or you can produce points by entering into the command line:

    10,20[enter] - to place point at coordinates x=10, y=20 from the origin - point x=0, y=0
        @30,40[enter] - to place point at coordinates that are at distance x=30, y=40 from the last drawn point. So x=10+30=40 and y=20+40=60.

    50<45[enter] - to place point at the distance 50 from origin, at 45 angle degree. The positive x axis is at 0 degrees, the positive y axis is at 90 degrees. So degrees are measured at counter clockwise direction from horizontal.

    @60<15[enter] - to place point at the distance 60 at 15 angle degree from the last drawn point.

Drawing a line

line
li
l
Specify first point
Specify next point
Specify next point or [undo]

Produce points as described in the point section. After producing a line segment, any following points create a line segment with the point that precedes them.

If there are at least two segments drawn, you can close the line (draw a segment to the point where you started) by entering close into the command line. To finish drawing lines you press [Esc]

All line segments created can be selected individually. With Polyline all segments are considered a single object that can be selected with one click.
Drawing a polyline

polyline
Specify first point
Specify next point
Specify next point or [undo]
You type polyline on the commandline. LibreCad prompts you to with "Specify first point".

You draw polyline exactly as you would draw a line (see above). The only difference is that all the segments of polyline are a single entity.
Drawing a line or other entity with an offset

offset
o
Specify distance <1> or select entity ot [Through]
You type offset or o on the commandline. LibreCad prompts you to with "Specify distance <1> or select entity ot [Through]". You can enter number from commandline or using Tool Options toolbar, you can select Through option. The default action is to click near an entity, indicating what side you wish to place the offset on. Offset works on lines, polylines (but only on one segment), circles, arcs, polygons (but only on one segment). Offset doesn't work on ellipses, bezier curves (here it kinda-sorta works but not the way you might expect)
Drawing parallel lines

parallel
par
Specify distance <1> or select entity ot [Through]
You type parallel or par on the commandline.

This seems to be the same functionality as offset command.
Drawing an arc

arc
a
Specify startpoint or [center]
Specify second point
Specify endpoint
or
Specify startpoint or [center]
center Specify center
Specify redius
Specify start angle
Specify end angle or [Angle/Chord length]
You type arc or a on the commandline. LibreCAD propmts you "Specify startpoint or [center]". Here you can enter point for center, either by clicking on screen or by typing coordinates or type center and enter center. If you enter start point you are prompted to enter second and third point. LibreCAC draws an arc from the first point through the second point to the third one. If you select "center" you are prompted to enter a center and then radius. After entering radius you are prompted for the starting point. Arcs drawn by center - radius - start point method always go counterclockwise from the start point.
Drawing a circle

circle
ci
Specify center
Specify radius
You type circle or ci on the commandline. LibreCAD propmts you "Specify center". Here you can enter point for center, either by clicking on screen or by typing coordinates or type center and enter center. LibreCAC then prompts you for a radius. Please note than when you use toolbar, there are more possibilities for drawing a circle. Center and point, center and radius (that you enter using tool options toolbar), two opposite points, three points (LibreCAD draws a circle circumscribed to the triangel) and finally Concentric option (that is really just a parallel command in disguise).
Drawing a rectangle

rectangle
rec
rectang
Specify first corner
Specify second corner
You type rectangle or rectang or rec on the commandline. LibreCAD propmts you "Specify first corner". Here you can enter point for one of the corners of the rectangle, either by clicking on screen or by typing coordinates. LibreCAD then prompts you for an opposite corner.
Drawing a text object

text
Specify insertion point
You type text on the commandline. LibreCAD presents a dialog box, where you can select Font, Height, Line spacing, Alignment, and Angle of the text. You type the desired text to the multiline edit box. Above the edit box there are icons that will let you clear, copy or paste text, save text to file or load it from file. Under the edit box there are droplists to help you with entering symbols, such as diameter or unicode characters. After filling in the dialog box, you are presented with prompt "Specify insertion point". You specify a point using any of the above described ways. After entering the point, the text is inserted in place and you are prompted again to "Specify insertion point".
Zooming
Redrawing the screen

regen
rg
zr
You type regen or rg or zr (abbreviation of the Zoom Regen command) on the commandline. LibreCAD redraws the screen. You can use this command, or appropriate icon from the View toolbar to tell LibreCAD to redraw the screen.
Zooming using mousewheel

When zooming in and out around the drawing you will most probably use mainly mousewheel. Just point the cursor to the desired detail and scroll the mousewheel forward to zoom in. Scroll the mousewheel backward to zoom out of the drawing
Zooming keyboard shortcuts

Just like in the original Photoshop and also in Firefox and chroome browsers you can use keyboard shortcuts Ctrl + + and Ctrl + - to zoom in and out of the drawing. This is different than using a mousewheel, because this zoom is always centered in the center of the screen.
Zooming into selected area of the drawing

zw
Specify the first edge
the second edge
You type zw (abbreviation of the Zoom Window command) on the commandline. LibreCAD prompts you to specify the first edge and then the second edge. Then it displays the selected area on the entire drawing window. This is a very traditional way of viewing the drawing details dating many many years back to the times before AutoCAD 10 was released. Nowadays it is often quicker and more comfortable to use mouse with a wheel and zoom in and out by using scrollwheel. By pressing the scrollwheel (or a middle button on mouse) you can also pan around the drawing.
Zooming to display entire drawing

za
the command has no further prompt
You type za (abbreviation of the Zoom All command) on the commandline. LibreCAD sets the zoom factor so that you can see your entire drawing - all the entities.
Zooming to the previous view

zv
the command has no further prompt
You type za (abbreviation of the Zoom preVious command) on the commandline. LibreCAD sets the zoom factor so that you "undo" the last zoom.

Line from rs_commands.cpp: "zv", "zoom - previous", RS2::ActionZoomPrevious;
Panning using mousewheel

When zooming and panning around, the quickest and the most convenient way is to use the mousewheel. Just press it down and you can pan around the drawing in realtime. This is very effective when combined with mousewheel zoom in and zoom out functionality.
Panning

zp
click and drag to pan zoom
You type zp (abbreviation of the ZoomPan command) on the commandline. LibreCAD prompts you to click and drag to pan. This is a very traditional way of panning around the drawing dating many many years back to the times before AutoCAD 10 was released. This command has the big disadvantage that after one grab and drag you are out of the command. So it is much more convenient to use mouse with a wheel and pan with the wheel pressed down you can also zoom in and out by using scrollwheel.
Edit commands
kill

kill
k
the command has no further prompt
This command when called on the command line kills or clears all actions inputed at the command line. At times when you have entered a command, zoomed the drawing, used the command line repetitively besides hitting the ESC key to exit out of the loaded commands you can run the kill command to clear the cache. It does not seem to do anything but if you open up the command line window you will see it clear out all active commands. Most of the time you would not need to use this command but there are times when it seems like the app gets confused at what action to take, using the kill command clears out everything and cleans the slate.

I can't figure out what this command does. Please edit this Wiki if you have any idea what it does.
Undo and Redo using keyboard shortcuts

You can use Ctrl+z and Ctrl+y to undo and redo changes. This is quicker and more convenient than using the next two commands.
Undo

undo
u
the command has no further prompt
You type undo on the commandline. LibreCAD reverts the last change you have made to the drawing. You can repeat the undo command, and every time you use it it takes you one step back through the history of your drawing/edit. Unlike other programs (AutoCAD) the undo command doesn't revert the zoom and pan commands.
Redo

redo
r
the command has no further prompt
You type undo on the commandline. LibreCAD cancels the last undo you have made. When you use the undo, it is easy to do one step too much undo. Using redo you can revert undo. This lets you go back and forth in the edit history.
Drawing dimensions

LibreCad has tools that make drawing dimensions much easier. To modify the default dimensions you can change the preferences. Click on the Drawing menu and select Current drawing preferences. A dialog panel will appear. In the preferences dialog panel select tab Dimensions. Here you can set:

    text height - this is the height of the text of the dimension
    extension line extension - this is the distance that extension line goes over the dimension line
    extension line offset - this is the distance between the beginning of the extension line and the object you are dimensioning. This is important for the readability of the outline of the drawn object.
    extension line gap - this is the distance between the text and the dimension line
    arrow size

Drawing aligned dimension

da
Specify first extension line origin
Specify second extension line origin
Specify dimension line location
You type da (abbreviation for Dimension Aligned) on the commandline. LibreCAD propmts you "Specify first extension line origin". Here you can enter point for the first extension line origin, either by clicking on screen or by typing coordinates typically you use some snap to place the dimension exactly on the point you wish to dimension. LibreCAC then prompts you for the second extension line origin. After specifying the second extension line origin you are propmted for dimesnion line location.
Aligned dimension runs parallel to the line between the two extension line origins.
You use Aligned dimension when you need to indicate the length of the line that runs at the angle. You can also use it for horizontal or vertical lines, but for that you have specialized commands - see below.
You are not given a chance to select a line and have it dimensioned automatically like you can with the AutoCAD.
After issuing command da or clicking on icon or menu you can set other options on the Tool Options toolbar:

    switch on the optional leader (such as diameter sign)
    enter your own text for dimension
    select the optional leader - diameter, plus/minus sign ...
    enter upper and lower tolerances

Drawing Linear dimension

dr
Specify first extension line origin
Specify second extension line origin
Specify dimension line location
You type dr (abbreviation for Dimension lineaR) on the commandline. LibreCAD propmts you "Specify first extension line origin". Here you can enter point for the first extension line origin, either by clicking on screen or by typing coordinates typically you use some snap to place the dimension exactly on the point you wish to dimension. LibreCAC then prompts you for the second extension line origin. After specifying the second extension line origin you are propmted for dimesnion line location.
Linear dimension runs parallel to the line between the two extension line origins.
You use Linear dimension when you need to indicate the length under specific angle. You have to set the angle from the Tool Options toolbar. You can also use it for horizontal or vertical lines, but for that you have specialized commands - see below.
You are not given a chance to select a line and have it dimensioned automatically like you can with the AutoCAD.
After issuing command da or clicking on icon or menu you can set other options on the Tool Options toolbar:

    switch on the optional leader (such as diameter sign)
    enter your own text for dimension
    select the optional leader - diameter, plus/minus sign ...
    enter upper and lower tolerances
    enter the angle for the dimension.

Drawing horizontal dimension

dh
Specify first extension line origin
Specify second extension line origin
Specify dimension line location
You type dh (abbreviation for Dimension Horizontal) on the commandline. LibreCAD propmts you "Specify first extension line origin". Here you can enter point for the first extension line origin, either by clicking on screen or by typing coordinates typically you use some snap to place the dimension exactly on the point you wish to dimension. LibreCAC then prompts you for the second extension line origin. After specifying the second extension line origin you are propmted for dimesnion line location.
Horizontal dimension runs parallel to the x axis.
You use Aligned dimension when you need to indicate the length under specific angle. You have to set the angle from the Tool Options toolbar. You can also use it for horizontal or vertical lines, but for that you have specialized commands - see below.
You are not given a chance to select a line and have it dimensioned automatically like you can with the AutoCAD.
After issuing command da or clicking on icon or menu you can set other options on the Tool Options toolbar:

    switch on the optional leader (such as diameter sign)
    enter your own text for dimension
    select the optional leader - diameter, plus/minus sign ...
    enter upper and lower tolerances
    enter the angle for the dimension.

Command Line Calculator

"cal", use command line as a math expression calculator. Some examples:

   cal 1+1
   cal sin(pi/6)
   cal log(2)

