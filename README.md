# v5-path-planner

Interactive V5 robot path planner with a 3D field, four robots, and ten scenes.

Open `index.html` locally. No installation or build is required.

To publish the app, open **Settings > Pages**, choose **Deploy from a branch**,
and select **main** and **/(root)**. After the deployment finishes, the app is
available at https://hivier.github.io/v5-path-planner/.

## Controls

- The left sidebar groups icon tools, playback, scenes, and removal controls.
  Expand **Robot & field settings** for dimensions and image options; project
  downloads and imports are under **Save & export**. On phones, the controls
  sit below the field.
- Switch between the 2D path editor and the orbitable 3D field.
- Use the robot button, click a spot, then move the mouse around the heading dial and click to place (snaps to 45° and 90°; arrow keys turn 45°, Enter places, Escape cancels). You can also press, drag, and release.
  Up to two robots per alliance and four total are supported.
- Hold right-click on a robot and move the mouse around it to change its starting heading. Release to finish; Escape reverts.
- Select the active robot to edit, preview, or export its path.
- In the 2D editor, choose **Draw** and drag to add a freehand annotation;
  use **Undo draw** or **Clear draws** under **Remove & return** to remove annotations. Annotations
  appear in both views and are saved per scene, but are not robot paths.
- Choose **Straight path**, then click two different points to append a straight
  segment to the active robot's path. If the first point differs from the path's
  end, a straight connector is added. Press Escape to cancel the first point.
  Choose **Select** to resume normal field interactions.
- Click cups, pins, or cup-and-pin assemblies to attach them to the nearest robot.
  Each robot can carry one object; a cup with a pin counts as one. Drop or return the
  active robot's object before picking up another.
- Click a carried object to drop it on the ground directly under its robot.
  It stays there when the robot moves, can be picked up again, and its dropped
  position is saved in scenes and project files. Return buttons instead send
  carried objects back to their original positions.
- The field includes four black scoring areas plus the central area, and four
  red/blue scoring areas. Their shapes and positions are approximations.
  Labels now show live **pin counts**, not fixed values or match points.
  A pin counts when its center is inside an area's displayed base and it is not
  carried or covered. The same area boundaries are used in both views.
- Pins have an intrinsic state: `open` (no cup), `cleared` (inside a cup's clear
  side), or `covered` (inside its opaque side). Choose the pin's compartment
  separately from which cup side faces up in the match-loader menu.
  Older cup-and-pin loads default to `cleared`.
- Dropping into a scoring area centers the object on the stack. Objects stack
  in drop order; removing an object settles those above it. A cup with its
  opaque side down makes all pins below it `covered`; a clear-side-down cup
  makes an open pin below it `cleared`. It does not uncover pins already
  hidden by an opaque side. Intrinsically covered pins never count.
  A loose pin dropped onto a cup takes the state of that cup's upward-facing
  compartment: `cleared` for clear or `covered` for opaque.
  Cup orientation, pin compartments, and stack order persist with scenes and
  project files; counts are recalculated from those objects.
- Click corner match loaders to configure or add loads; right-click to edit defaults.
- Click wall toggles to cycle their colors.
- Use scenes 1 through 10 to save different field states. A new scene copies the
  current one. Scene changes animate along saved paths when available, otherwise
  directly between positions.

Changes are autosaved in this browser. Download a project file to back up all
scenes and field images or move them to another browser. CSV export includes
only the active robot's path.

When opening older scenes with multiple objects on one robot, the planner keeps
one and returns the extras to their original positions. Formerly movable
colored scoring markers are restored to the field.

The field geometry is an approximation based on reference images, not official
measurements. Paths and scene transitions do not check collisions or control a
physical robot.
