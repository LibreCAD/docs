.. User Manual, LibreCAD v2.2.x

.. Default include
.. include:: /inclFiles/notice.rst


.. _snaps:

Snapping
========

Snaps provide the ability to pick precise locations when using a mouse.  Various snap tools are available to allow the user to select different locations on entities or elsewhere in the drawing space when using the grid.

.. csv-table:: 
    :widths: 20, 7, 20, 53
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Menu Item", "Icon", "Command", "Description"
    "Exclusive Snap Mode", |icon01|, "", "**On**: only one snap mode is allowed.  **Off**: multiple snap modes are allowed The snap modes are remembered in each state."
    "Free Snap", |icon02|, "so, os, snapfree", "Allows for the crosshair to move freely while other snap modes are enabled."
    "Snap on Grid", |icon03|, "sg, snapgrid", "Snap to a grid intersection."
    "Snap on Endpoints", |icon04|, "se, snapend", "Snap to the endpoints of a line segment, the quadrants of a circle, a point, or the alignment point of a text or mtext object."
    "Snap on Entity", |icon05|, "sn, np, snaponentity", "Snap to the path of an entity."
    "Snap Center", |icon06|, "sc, snapcenter", "Snap to the center of a circle or ellipse. It will also snap to the foci of an ellipse."
    "Snap Middle", |icon07|, "sm, snapmiddle", "Snap to the middle of a path. Enabling this mode displays a ''Middle points'' input. If you change the value to 2 then you can snap to the trisection points of a line segment."
    "Snap Distance", |icon08|, "sd, snapdist", "If you snap to the endpoint of a line segment then activate ''snap distance'' and input 50, then it will snap to a point 50 units from the endpoint on the line segment. However, it will also snap to a point that is 50 units from the other endpoint."
    "Snap Intersection", |icon09|, "si, snapintersection", "Snap to the intersection of two entities. Note this does not currently work for polylines."
    "Restrict Horizontal", |icon10|, "rh, restricthorizontal", "Restricts the crosshairs to the x-axis (horizontal movement)."
    "Restrict Vertical", |icon11|, "rv, restrictvertical", "Restricts the crosshairs to the y-axis  (vertical movement)."
    "Restrict Orthogonal", |icon12|, "rr, restrictogonal", "Restricts the crosshairs to the x **or** y-axis. (either horizontal **or** vertical movement)."
    "Restrict Nothing", , "rn, restrictnothing", "Turns off restricted cursor movements."
    "Set relative zero position", |icon13|, "rz, setrelativezero", "Manually sets the Relative Zero Point at the selected coordinate."
    "Lock relative zero position", |icon14|, "", "Locks the Relative Zero Point to the current coordinate."


..  Icon mapping:

.. icon00
.. |icon01| image:: /images/icons/exclusive.svg
            :height: 24
            :width: 24
.. |icon02| image:: /images/icons/snap_free.svg
            :height: 24
            :width: 24
.. |icon03| image:: /images/icons/snap_grid.svg
            :height: 24
            :width: 24
.. |icon04| image:: /images/icons/snap_endpoints.svg
            :height: 24
            :width: 24
.. |icon05| image:: /images/icons/snap_entity.svg
            :height: 24
            :width: 24
.. |icon06| image:: /images/icons/snap_center.svg
            :height: 24
            :width: 24
.. |icon07| image:: /images/icons/snap_middle.svg
            :height: 24
            :width: 24
.. |icon08| image:: /images/icons/snap_distance.svg
            :height: 24
            :width: 24
.. |icon09| image:: /images/icons/snap_intersection.svg
            :height: 24
            :width: 24
.. |icon10| image:: /images/icons/restr_hor.svg
            :height: 24
            :width: 24
.. |icon11| image:: /images/icons/restr_ver.svg
            :height: 24
            :width: 24
.. |icon12| image:: /images/icons/restr_ortho.svg
            :height: 24
            :width: 24
.. |icon13| image:: /images/icons/set_rel_zero.svg
            :height: 24
            :width: 24
.. |icon14| image:: /images/icons/lock_rel_zero.svg
            :height: 24
            :width: 24
.. icon15

