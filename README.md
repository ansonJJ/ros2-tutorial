# ROS2 Tutorial

Welcome to the **ROS2 Tutorial** repository, designed to guide beginners through the fundamentals of **ROS2 (Robot Operating System 2)** using practical examples and hands-on exercises. This repository complements the [ROS2 for Beginners](https://www.udemy.com/course/ros2-for-beginners/) Udemy course, targeting **ROS2 Jazzy Jalisco** on **Ubuntu 24.04**. It covers creating ROS2 packages, writing nodes in Python and C++, working with topics and services, and experimenting with the `turtlesim` simulator. All tutorials are structured for clarity, with step-by-step instructions, screenshots, and fact-checked references to ROS2 documentation.

## Repository Structure

The repository is organized into sections, each containing tutorials as Markdown files. Screenshots are stored in the root-level `images/` directory.

```
ros2-tutorial/
├── images/
│   ├── add_two_ints_server_running.png
│   ├── ros2_service_help.png
│   ├── ros2_service_list.png
│   ├── ros2_node_info_add_two_ints_server.png
│   ├── ros2_service_type.png
│   ├── interface_show_add_two_ints.png
│   ├── ros2_service_call_add_two_ints.png
│   ├── rqt_service_caller_add_two_ints.png
│   ├── ros2_service_list_default_add_two_ints.png
│   ├── ros2_service_list_remapped_abc.png
│   ├── client_waiting_add_two_ints.png
│   ├── client_server_remapped_abc.png
│   ├── turtlesim_window_with_trail.png
│   ├── ros2_service_list_turtlesim.png
│   ├── turtlesim_clear_before_after.png
│   ├── turtlesim_spawn_my_turtle.png
│   ├── turtlesim_kill_my_turtle.png
│   ├── turtlesim_teleport_absolute.png
│   └── ...
├── Section 3 - Your First ROS2 Program/
│   ├── 3.1 - ROS2 Workspace Setup Tutorial.md
│   ├── 3.2 - Creating a ROS2 Python Package.md
│   ├── 3.3 - Creating a ROS2 C++ Package.md
│   ├── 3.4 - Writing Your First ROS2 Node in Python.md
│   ├── 3.5 - Writing Your First ROS2 Node in C++.md
│   ├── 3.6 - Compiling and Running ROS2 Nodes.md
│   └── 3.7 - Understanding ROS2 Node Communication.md
├── Section 4 - Introduction to ROS2 Tools/
│   ├── 4.1 - Introspecting Nodes with ROS2 CLI.md
│   ├── 4.2 - Visualizing ROS2 Nodes with RQT Graph.md
│   ├── 4.3 - Logging in ROS2.md
│   ├── 4.4 - Debugging ROS2 Nodes.md
│   └── 4.5 - Discover Turtlesim.md
├── Section 5 - ROS2 Communication/
│   ├── 5.1 - What is a ROS2 Topic.md
│   ├── 5.2 - Writing a Python Publisher.md
│   ├── 5.3 - Writing a Python Subscriber.md
│   ├── 5.4 - Writing a C++ Publisher.md
│   ├── 5.5 - Writing a C++ Subscriber.md
│   ├── 5.6 - Introspecting ROS2 Topics with Command Line Tools.md
│   ├── 5.7 - Renaming ROS2 Topics at Runtime.md
│   ├── 5.8 - Monitoring ROS2 Topics with RQT Graph.md
│   └── 5.9 - Experimenting with ROS2 Topics Using Turtlesim.md
├── Section 6 - ROS2 Services/
│   ├── 6.1 - What is a ROS2 Service.md
│   ├── 6.2 - Writing a Python Service Server.md
│   ├── 6.3 - Writing a Python Service Client (Non-OOP).md
│   ├── 6.4 - Writing a Python Service Client (OOP).md
│   ├── 6.5 - Writing a C++ Service Server.md
│   ├── 6.6 - Writing a C++ Service Client (Non-OOP).md
│   ├── 6.7 - Writing a C++ Service Client (OOP).md
│   ├── 6.8 - Introspecting ROS2 Services with Command Line Tools.md
│   ├── 6.9 - Remapping ROS2 Services at Runtime.md
│   └── 6.10 - Experimenting with ROS2 Services Using Turtlesim.md
└── README.md
```

## Tutorial Overview

### Section 3 - Your First ROS2 Program
- **3.1**: Set up a ROS2 workspace (`~/ros2_ws`) using `colcon`.
- **3.2**: Create a Python package (`my_py_pkg`) with `ros2 pkg create`.
- **3.3**: Create a C++ package (`my_cpp_pkg`) with `ros2 pkg create`.
- **3.4**: Write a simple Python node to print "Hello, ROS2!".
- **3.5**: Write a simple C++ node to print "Hello, ROS2!".
- **3.6**: Compile and run nodes using `colcon build` and `ros2 run`.
- **3.7**: Understand node communication basics in ROS2.

### Section 4 - Introduction to ROS2 Tools
- **4.1**: Introspect nodes using `ros2 node` CLI commands.
- **4.2**: Visualize node connections with RQT Graph.
- **4.3**: Implement logging in ROS2 nodes for debugging.
- **4.4**: Debug nodes using ROS2 tools and techniques.
- **4.5**: Explore the `turtlesim` simulator and its nodes (`turtlesim_node`, `turtle_teleop_key`).

### Section 5 - ROS2 Communication
- **5.1**: Understand ROS2 topics using a radio analogy.
- **5.2**: Create a Python publisher node for the `/robot_news` topic.
- **5.3**: Create a Python subscriber node for the `/robot_news` topic.
- **5.4**: Create a C++ publisher node for the `/robot_news` topic.
- **5.5**: Create a C++ subscriber node for the `/robot_news` topic.
- **5.6**: Introspect ROS2 topics using command-line tools (`ros2 topic`).
- **5.7**: Rename ROS2 topics at runtime using remapping.
- **5.8**: Monitor ROS2 topics using RQT Graph for visualization.
- **5.9**: Experiment with ROS2 topics using `turtlesim` to control a 2D robot.

### Section 6 - ROS2 Services
- **6.1**: Understand ROS2 services using weather and LED control analogies.
- **6.2**: Create a Python service server for adding two integers (`/add_two_ints`).
- **6.3**: Create a non-OOP Python service client to call the `/add_two_ints` service.
- **6.4**: Create an OOP Python service client integrated into a node.
- **6.5**: Create a C++ service server for adding two integers, tested with a Python client.
- **6.6**: Create a non-OOP C++ service client for quick server testing.
- **6.7**: Create an OOP C++ service client integrated into a node for modularity.
- **6.8**: Introspect ROS2 services using command-line tools (`ros2 service`, `ros2 interface`) and RQT Service Caller.
- **6.9**: Remap ROS2 services at runtime to rename services (e.g., `/add_two_ints` to `/abc`) without code changes.
- **6.10**: Experiment with `turtlesim` services (`/clear`, `/spawn`, `/kill`, etc.) using command-line tools.

## Getting Started

### Prerequisites
- **Ubuntu 24.04** (Noble Numbat).
- **ROS2 Jazzy Jalisco** installed (`ros-jazzy-desktop` recommended).
- **Dependencies**: `colcon`, `turtlesim`, `example_interfaces`, `std_srvs`, `rqt`, and `terminator`.
- A code editor (e.g., VS Code).
- Basic familiarity with Linux terminal commands.

### Installation
1. **Install ROS2 Jazzy**:
   Follow the [ROS2 Installation Guide](https://docs.ros.org/en/jazzy/Installation.html):
   ```bash
   sudo apt update
   sudo apt install ros-jazzy-desktop
   source /opt/ros/jazzy/setup.bash
   ```
   Add to `~/.bashrc` for automatic sourcing:
   ```bash
   echo "source /opt/ros/jazzy/setup.bash" >> ~/.bashrc
   ```

2. **Install Dependencies**:
   ```bash
   sudo apt install python3-colcon-common-extensions ros-jazzy-turtlesim ros-jazzy-example-interfaces ros-jazzy-std-srvs ros-jazzy-rqt ros-jazzy-rqt-common-plugins terminator
   ```

3. **Clone the Repository**:
   ```bash
   mkdir -p ~/ros2_tutorial_ws/src
   cd ~/ros2_tutorial_ws/src
   git clone https://github.com/ansonJJ/ros2-tutorial.git
   mv ros2-tutorial/* .
   rmdir ros2-tutorial
   ```

4. **Set Up Workspace**:
   Create a ROS2 workspace and build:
   ```bash
   cd ~/ros2_tutorial_ws
   colcon build --symlink-install
   source install/setup.bash
   ```
   Add to `~/.bashrc`:
   ```bash
   echo "source ~/ros2_tutorial_ws/install/setup.bash" >> ~/.bashrc
   ```

### Usage
1. **Navigate Tutorials**:
   Tutorials are in `Section 3/`, `Section 4/`, `Section 5/`, and `Section 6/`. Start with `3.1` for workspace setup.

2. **Run Examples**:
   - **Nodes**: Use `ros2 run my_py_pkg <node>` or `ros2 run my_cpp_pkg <node>` (e.g., `add_two_ints_server`).
   - **Turtlesim**: Run `ros2 run turtlesim turtlesim_node` and `ros2 run turtlesim turtle_teleop_key`.
   - **CLI Tools**: Use `ros2 node`, `ros2 topic`, `ros2 service`, `ros2 interface` for introspection.
   - **RQT**: Run `rqt` for graphical tools (e.g., Service Caller, Graph).

3. **Follow Tutorials**:
   Each Markdown file includes:
   - Prerequisites
   - Step-by-step instructions
   - Expected outputs
   - Screenshots (in `images/`)
   - Troubleshooting tips
   - Fact-checked references

### Example Commands
- **Run a Node**:
  ```bash
  ros2 run my_py_pkg add_two_ints_server
  ```
- **List Services**:
  ```bash
  ros2 service list
  ```
- **Call a Turtlesim Service**:
  ```bash
  ros2 service call /spawn turtlesim/srv/Spawn "{x: 5.0, y: 5.0, name: 'my_turtle'}"
  ```
- **Run Turtlesim**:
  ```bash
  ros2 run turtlesim turtlesim_node
  ```

## Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a branch: `git checkout -b feature/your-feature`.
3. Add your tutorial or update in the appropriate section (e.g., `Section 6 - ROS2 Services/`).
4. Place screenshots in `images/`.
5. Update `README.md` to reflect changes.
6. Commit: `git commit -m "Add your feature or tutorial"`.
7. Push: `git push origin feature/your-feature`.
8. Open a pull request.

Please ensure tutorials are fact-checked against [ROS2 Documentation](https://docs.ros.org/en/jazzy/index.html) and include screenshots.

## License
This repository is licensed under the [MIT License](LICENSE). See the [LICENSE](LICENSE) file for details.

## Acknowledgments
- [ROS2 Documentation](https://docs.ros.org/en/jazzy/index.html)
- [ROS2 for Beginners Udemy Course](https://www.udemy.com/course/ros2-for-beginners/)
- The ROS2 community for tools like `turtlesim` and `rqt`.

## Contact
For questions or feedback, open an issue on GitHub or contact the repository owner.

Happy learning with ROS2!