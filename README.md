# In-House-Autopilot-for-an-Indoor-Quadcopter

I developed a custom Arm Mbed-based autopilot that enables fully autonomous indoor flight for a quadrotor by combining cascaded PID loops—with derivative filtering and integral anti-windup—to achieve a critically damped 0.5 – 0.8 s settling time. Sensor fusion blends IMU, optical-flow, and barometric data through a complementary filter for attitude and a linear Kalman filter for lateral velocity, while empirically derived inertia, thrust, and drag values feed a realistic six-DOF dynamics model. The real-time C++ control stack—over 3 k lines—runs on an ST-Nucleo F446RE mounted to a custom four-layer PCB that handles sensor and power interfacing, includes fault-tolerant arming logic, and delivers stable position-hold and waypoint tracking in GPS-denied indoor environments, providing a repeatable platform for advanced UAV estimation and control studies.

<!-- Markdown image embed -->
![PCB Connections](images/pcb.gif)

![Demo](images/d12.gif)
