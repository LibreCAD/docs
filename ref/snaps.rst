.. User Manual, LibreCAD v2.2.x


.. _snaps:

Snapping
========

Snaps provide the ability to pick precise locations when using a mouse.  Various snap tools are available to allow the user to select different locations on entities or elsewhere in the drawing space when using the grid.

.. csv-table:: 
   :header: "Menu Item", "Icon", "Command", "Description"
   :widths: 40, 10, 20, 110

    "Exclusive Snap Mode", |icon01|, "", "**On**: only one snap mode is allowed.  **Off**: multiple snap modes are allowed The snap modes are remembered in each state."
    "Free Snap", |icon02|, "os, sf", "Allows for the crosshair to move freely while other snap modes are enabled."
    "Snap on Grid", |icon03|, "sg", "Snap to a grid intersection."
    "Snap on Endpoints", |icon04|, "se", "Snap to the endpoints of a line segment, the quadrants of a circle, a point, or the alignment point of a text or mtext object."
    "Snap on Entity", |icon05|, "np, sn", "Snap to the path of an entity."
    "Snap Center", |icon06|, "sc", "Snap to the center of a circle or ellipse. It will also snap to the foci of an ellipse."
    "Snap Middle", |icon07|, "sm", "Snap to the middle of a path. Enabling this mode displays a ''Middle points'' input. If you change the value to 2 then you can snap to the trisection points of a line segment."
    "Snap Distance", |icon08|, "sd", "If you snap to the endpoint of a line segment then activate ''snap distance'' and input 50, then it will snap to a point 50 units from the endpoint on the line segment. However, it will also snap to a point that is 50 units from the other endpoint."
    "Snap Intersection", |icon09|, "si", "Snap to the intersection of two entities. Note this does not currently work for polylines."
    "Restrict Horizontal", |icon10|, "rh", "Restricts the crosshairs to the x-axis (horizontal movement)."
    "Restrict Vertical", |icon11|, "rv", "Restricts the crosshairs to the y-axis  (vertical movement)."
    "Restrict Orthogonal", |icon12|, "rr", "Restricts the crosshairs to the x **or** y-axis. (either horizontal **or** vertical movement)."
    "Restrict Nothing", , "rn", "Turns off restricted cursor movements."
    "Set relative zero position", |icon13|, "", "Manually sets the Relative Zero Point at the selected coordinate."
    "Lock relative zero position", |icon14|, "", "Locks the Relative Zero Point to the current coordinate."


..  Icon mapping:

.. icon00
.. |icon01| image:: /images/icons/exclusive.svg
.. |icon02| image:: /images/icons/snap_free.svg
.. |icon03| image:: /images/icons/snap_grid.svg
.. |icon04| image:: /images/icons/snap_endpoints.svg
.. |icon05| image:: /images/icons/snap_free.svg
.. |icon06| image:: /images/icons/snap_center.svg
.. |icon07| image:: /images/icons/snap_middle.svg
.. |icon08| image:: /images/icons/snap_distance.svg
.. |icon09| image:: /images/icons/snap_intersection.svg
.. |icon10| image:: /images/icons/restr_hor.svg
.. |icon11| image:: /images/icons/restr_ver.svg
.. |icon12| image:: /images/icons/restr_ortho.svg
.. |icon13| image:: /images/icons/set_rel_zero.svg
.. |icon14| image:: /images/icons/lock_rel_zero.svg
.. icon15

