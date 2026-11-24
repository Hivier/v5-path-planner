# v5-path-planner

Interactive V5 robot path planner with a 3D field, four robots, and ten scenes.

Run the app at https://hivier.github.io/v5-path-planner/ or open `index.html`
locally. No installation or build is required.

## Controls

- Switch between the 2D path editor and the orbitable 3D field.
- Use the robot button to place a robot and choose its starting heading.
  Up to two robots per alliance and four total are supported.
- Select the active robot to edit, preview, or export its path.
- Click cups, pins, or cup-and-pin assemblies to attach them to the nearest robot.
- Click corner match loaders to configure or add loads; right-click to edit defaults.
- Click wall toggles to cycle their colors.
- Use scenes 1 through 10 to save different field states. A new scene copies the
  current one. Scene changes animate along saved paths when available, otherwise
  directly between positions.

Changes are autosaved in this browser. Download a project file to back up all
scenes and field images or move them to another browser. CSV export includes
only the active robot's path.

The field geometry is an approximation based on reference images, not official
measurements. Paths and scene transitions do not check collisions or control a
physical robot.
