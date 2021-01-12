# SRA's AutoSim Competition
Simulation Competition for sophomores
--------------------------------------------- Sample Arena --------------------------------------------------------------------------------------------

1. Delete existing sample_arena_urdf and arena_with_qr from src. Add the new ones in src.

2. Change path in line `7` of `launch_in_gz.launch ` (launcg_in_gz.launch is in arena_with_qr -> launch) 
   
   ```
   <arg name="world" default="/home/sanath/catkin_ws/src/arena_with_qr/world/cubes_and_qr_arena.world" />
   ```

3. Change path in line `121` and `143` in `cubes_and_qr.world`(cubes_and_qr.world is in arena_with_qr -> world)

   ```
   <uri>/home/sanath/catkin_ws/src/sample_arena_urdf/meshes/arena_samplenew.dae</uri>
   ```

4. Open terminal from your <workspace> and do
   
   ```
   catkin_make
   source devel/setup.bash
   roslaunch arena_with_qr launch_in_gz.launch
   ```

**NOTE**: If there is a error saying `Error [Converter.cc:127] Unable to convert from SDF version 1.6 to x.x`. Just change the sdf version in line `1` of `cubes_and_qr.world`


---------------------------------------------------- Final Arena --------------------------------------------------------------------------------------

1. Delete existing model and add marker10 to models in .gazebo.

2. Change path in line `7` of `final_arena.launch `
   
   ```
   <arg name="world" default="/home/neha_kurian/catkin_ws/src/arena_with_qr/world/final_arena.world" />
   ```

3. Change path in line `293` and `315` in `final_arena.world`

   ```
	<uri>/home/neha_kurian/catkin_ws/src/final_arena_urdf/meshes/final_arena.dae</uri>
   
   ```

4. Open terminal from your <workspace> and do
   
   ```
   catkin_make
   source devel/setup.bash
   roslaunch arena_with_qr final_arena.launch
   ```

**NOTE**: If there is a error saying `Error [Converter.cc:127] Unable to convert from SDF version 1.6 to x.x`. Just change the sdf version in line `1` of `cubes_and_qr.world`
