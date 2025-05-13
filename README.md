# ROS2 Tutorials Repository

This repository hosts a collection of beginner-friendly tutorials for learning ROS2 (Robot Operating System 2), specifically for ROS2 Jazzy on Ubuntu 24.04. The tutorials are based on the Udemy course [ROS2 for Beginners](https://www.udemy.com/course/ros2-for-beginners/) and provide step-by-step guides with terminal commands and illustrative images. Currently, the repository includes a tutorial on setting up a ROS2 workspace, with more tutorials to be added in the future.

## Purpose

The tutorials are designed for beginners new to ROS2 who want to learn core concepts like workspace setup, package development, and environment configuration. Each tutorial is structured to be clear and practical, making it easy to follow while building ROS2 applications.

## Prerequisites

- **Operating System**: Ubuntu 24.04 (Noble Numbat)
- **ROS2 Installation**: ROS2 Jazzy Jalisco installed in `/opt/ros/jazzy`. Follow the [official ROS2 installation guide](https://docs.ros.org/en/jazzy/Installation.html) if not installed.
- **Development Tools**: Ensure `ros-dev-tools` is installed:
  ```bash
  sudo apt update
  sudo apt install ros-dev-tools
  ```
- **Terminal**: A `bash`-compatible terminal (tutorials use `~/.bashrc` for configuration).
- **Git**: Installed to clone this repository:
  ```bash
  sudo apt install git
  ```

## Installation

1. **Clone the Repository**:
   Clone this repository to your local machine:
   ```bash
   git clone https://github.com/ansonJJ/ros2-tutorial.git
   cd ros2-tutorial
   ```

2. **Verify Files**:
   Ensure the repository contains the `Tutorials` folder, `README.md`, and `LICENSE.txt`:
   ```bash
   ls
   ```
   Expected output:
   ```
   LICENSE.txt  README.md  Tutorials
   ```
   Check the `Tutorials` folder:
   ```bash
   ls Tutorials
   ```
   Expected output:
   ```
   3.1 - ROS2 Workspace Setup Tutorial.md  images
   ```

## Usage

1. **Access the Tutorials**:
   Navigate to the `Tutorials` folder to find markdown files for each tutorial. Currently, the only tutorial is `3.1 - ROS2 Workspace Setup Tutorial.md`. Open it in a markdown viewer or text editor:
   ```bash
   cd Tutorials
   ```
   For the best experience, use a markdown renderer that supports images (e.g., Visual Studio Code, GitHub, or a web-based viewer).

2. **Follow the Tutorial**:
   The current tutorial, "3.1 - ROS2 Workspace Setup Tutorial," covers:
   - Creating a ROS2 workspace (`ros2_ws` with a `src` subdirectory).
   - Building the workspace using `colcon build`.
   - Sourcing the workspace’s `setup.bash` and automating it via `~/.bashrc`.
   - Verifying the setup with `ros2 pkg list`.

   Follow the commands and explanations to set up your ROS2 workspace.

3. **View Images**:
   The tutorial references images in the `Tutorials/images/` directory to illustrate key steps, such as:
   - Workspace directory structure
   - `colcon build` output and directories
   - `install/` directory contents
   - Edited `.bashrc` file
   - `ros2 pkg list` output

   Ensure the `Tutorials/images/` directory contains the images (`ros2_ws_structure.png`, `colcon_build_output.png`, `install_directory.png`, `bashrc_edit.png`, `ros2_pkg_list.png`). If images don’t render, verify that the tutorial markdown uses the correct path (`images/` relative to `Tutorials/`).

4. **Future Tutorials**:
   More tutorials based on the [ROS2 for Beginners](https://www.udemy.com/course/ros2-for-beginners/) course will be added to the `Tutorials` folder. Check back for updates on topics like creating ROS2 packages, writing nodes, and more.

## Directory Structure

```
ros2-tutorial/
├── LICENSE.txt
├── README.md
└── Tutorials/
    ├── 3.1 - ROS2 Workspace Setup Tutorial.md
    └── images/
        ├── ros2_ws_structure.png
        ├── colcon_build_output.png
        ├── install_directory.png
        ├── bashrc_edit.png
        └── ros2_pkg_list.png
```

- `LICENSE.txt`: MIT License for the repository.
- `README.md`: This file, providing an overview and instructions.
- `Tutorials/`: Contains markdown files for each tutorial and an `images/` subdirectory for visuals.
- `Tutorials/images/`: Stores PNG images referenced in the tutorials.

## Contributing

Contributions are welcome to improve existing tutorials or add new ones. To contribute:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature
   ```
3. Make changes (e.g., enhance tutorials, add new markdown files, update images).
4. Commit and push to your fork:
   ```bash
   git commit -m "Add your feature or fix"
   git push origin feature/your-feature
   ```
5. Open a pull request on GitHub to `https://github.com/ansonJJ/ros2-tutorial`.

Please ensure changes maintain the beginner-friendly tone, align with ROS2 Jazzy, and follow the [ROS2 for Beginners](https://www.udemy.com/course/ros2-for-beginners/) course structure.

## License

This project is licensed under the MIT License. See the [LICENSE.txt](LICENSE.txt) file for details.

## Acknowledgments

- [ROS2 for Beginners](https://www.udemy.com/course/ros2-for-beginners/) Udemy course for inspiring the tutorial content.
- [ROS2 Documentation](https://docs.ros.org/en/jazzy/index.html) for official guidelines.
- The ROS2 community for tools like `colcon` and `ros-dev-tools`.