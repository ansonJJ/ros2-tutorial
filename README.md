# ROS2 Tutorial: Creating a ROS2 Workspace (Jazzy Jalisco)

## Introduction
A ROS2 workspace is a directory where you develop, build, and run ROS2 packages. It organizes your code and dependencies, enabling you to create and manage robotics applications efficiently. In this section, you'll learn how to create a ROS2 workspace using the `colcon` build tool, set it up correctly, and verify it with a simple test. This tutorial assumes you have [ROS2 Jazzy Jalisco installed](https://docs.ros.org/en/jazzy/Installation.html) on Ubuntu 24.04.

## Prerequisites
- Ubuntu 24.04 (physical machine, virtual machine, or WSL2).
- ROS2 Jazzy Jalisco installed and sourced (run `source /opt/ros/jazzy/setup.bash` in your terminal).
- Basic familiarity with Linux commands (e.g., `cd`, `mkdir`, `ls`).
- A text editor (e.g., VS Code, nano, or gedit).

## Step-by-Step Instructions

### Step 1: Create the Workspace Directory
1. Open a terminal (Ctrl+Alt+T).
2. Create a directory for your ROS2 workspace. A common name is `ros2_ws`, but you can choose any name.
   ```bash
   mkdir -p ~/ros2_ws/src
   ```
   - `mkdir -p` creates the directory and its parent directories if they don't exist.
   - `~/ros2_ws` is the workspace root, and `src` is where your packages will reside.

3. Navigate to the workspace directory:
   ```bash
   cd ~/ros2_ws
   ```

### Step 2: Initialize the Workspace
1. Ensure ROS2 Jazzy is sourced in your terminal:
   ```bash
   source /opt/ros/jazzy/setup.bash
   ```
   - This makes ROS2 commands available. Add this line to your `~/.bashrc` file for automatic sourcing:
     ```bash
     echo "source /opt/ros/jazzy/setup.bash" >> ~/.bashrc
     ```

2. Verify that `colcon` (the ROS2 build tool) is available:
   ```bash
   colcon --version
   ```
   - Expected output: A version number (e.g., `0.16.1` or similar). If not found, ensure ROS2 is installed correctly.

### Step 3: Create a Test Package
To test the workspace, create a simple ROS2 package in the `src` directory.

1. Navigate to the `src` directory:
   ```bash
   cd ~/ros2_ws/src
   ```

2. Create a test package named `my_test_package` using Python:
   ```bash
   ros2 pkg create --build-type ament_python my_test_package
   ```
   - `--build-type ament_python` specifies a Python-based package.
   - This creates a directory `my_test_package` with a basic package structure compatible with ROS2 Jazzy.

3. Check the package structure:
   ```bash
   ls my_test_package
   ```
   - Expected output: Files like `package.xml`, `setup.py`, and directories like `my_test_package`, `resource`, and `test`.

### Step 4: Build the Workspace
1. Return to the workspace root:
   ```bash
   cd ~/ros2_ws
   ```

2. Build the workspace using `colcon`:
   ```bash
   colcon build
   ```
   - This compiles all packages in the `src` directory and generates `build`, `install`, and `log` directories.
   - Expected output: A summary like `Summary: 1 package finished`.

3. Source the workspace to make the package available:
   ```bash
   source ~/ros2_ws/install/setup.bash
   ```
   - Add this to `~/.bashrc` for convenience:
     ```bash
     echo "source ~/ros2_ws/install/setup.bash" >> ~/.bashrc
     ```

### Step 5: Verify the Workspace
1. Check if the test package is recognized:
   ```bash
   ros2 pkg list | grep my_test_package
   ```
   - Expected output: `my_test_package`.

2. Verify the workspace structure:
   ```bash
   ls ~/ros2_ws
   ```
   - Expected output: `build  install  log  src`.

### Step 6: Clean Up (Optional)
If you encounter issues or want to start fresh, clean the workspace:
```bash
cd ~/ros2_ws
rm -rf build install log
```
Then rebuild using `colcon build`.

## Example Workspace Structure
After completing the steps, your workspace should look like this:
```
ros2_ws/
├── build/
├── install/
├── log/
└── src/
    └── my_test_package/
        ├── my_test_package/
        ├── resource/
        ├── test/
        ├── package.xml
        └── setup.py
```

## Troubleshooting Tips
- **Command not found (`ros2` or `colcon`)**:
  - Ensure ROS2 is sourced: `source /opt/ros/jazzy/setup.bash`.
  - Verify ROS2 installation: [ROS2 Jazzy Installation Guide](https://docs.ros.org/en/jazzy/Installation.html).
- **Build errors**:
  - Check for typos in `package.xml` or `setup.py`.
  - Ensure all dependencies are installed: `rosdep install --from-paths src --ignore-src -r -y`.
- **Workspace not recognized**:
  - Source the workspace: `source ~/ros2_ws/install/setup.bash`.
  - Verify the `src` directory contains valid packages.

## Next Steps
You now have a functional ROS2 workspace in ROS2 Jazzy! In the next sections, you'll learn how to create Python and C++ packages, build nodes, and explore ROS2 tools like Turtlesim and Rqt.

## Additional Resources
- [ROS2 Jazzy Documentation: Creating a Workspace](https://docs.ros.org/en/jazzy/Tutorials/Beginner-Client-Libraries/Colcon-Tutorial.html)
- [Colcon Documentation](https://colcon.readthedocs.io/en/released/)
- [ROS2 Community Forums](https://answers.ros.org/)