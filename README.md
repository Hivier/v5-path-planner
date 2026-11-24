# v5-path-planner

Interactive V5 robot path planner with a 3D field, four robots, and ten scenes.

Open `index.html` locally. No installation or build is required.

To publish the app, open **Settings > Pages**, choose **Deploy from a branch**,
and select **main** and **/(root)**. After the deployment finishes, the app is
available at https://hivier.github.io/v5-path-planner/.

## Controls

- Switch between the 2D path editor and the orbitable 3D field.
- Use the robot button, click a spot, then move the mouse around the heading dial and click to place (snaps to 45° and 90°; arrow keys turn 45°, Enter places, Escape cancels). You can also press, drag, and release.
  Up to two robots per alliance and four total are supported.
- Hold right-click on a robot and move the mouse around it to change its starting heading. Release to finish; Escape reverts.
- Select the active robot to edit, preview, or export its path.
- In the 2D editor, choose **Draw** and drag to add a freehand annotation;
  use **Undo drawing** or **Clear drawings** to remove annotations. Annotations
  appear in both views and are saved per scene, but are not robot paths.
- Choose **Straight path**, then click two different points to append a straight
  segment to the active robot's path. If the first point differs from the path's
  end, a straight connector is added. Press Escape to cancel the first point.
  Choose **Select / waypoints** to resume normal field interactions.
- Click cups, pins, or cup-and-pin assemblies to attach them to the nearest robot.
  Each robot can carry one object; a cup with a pin counts as one. Return the
  active robot's object before picking up another.
- The field includes four black scoring areas plus the central 0, and four
  red/blue scoring areas. Their shapes and positions are approximations.
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
