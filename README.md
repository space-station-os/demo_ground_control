# OpenMCT with OpenMCT-ROS Integration

This project demonstrates **integration of [OpenMCT](https://github.com/nasa/openmct)** with **[OpenMCT-ROS](https://github.com/raspberry-pi-os/openmct-ros)** using the [space-station-os/demo_ground_control](https://github.com/space-station-os/demo_ground_control) repository.

## Objective

Enable visualization of **ROS (Robot Operating System)** data streams within the OpenMCT web-based telemetry framework.

---

## Assumptions

Before following this guide, you are assuming that:

- You have **Node.js (>=14.x recommended)** installed.
- You have **ROS (Robot Operating System)** installed and configured.
- You have `rosbridge_websocket` running or plan to use the `demo_ground_control` simulation.
- Your environment supports WebSockets and has no firewall blocking `9090` (the default ROSBridge port).

If these assumptions don’t hold, steps may fail or produce no data.

---

## Installation

### 1. Clone the Demo Ground Control Repository

```bash
git clone https://github.com/space-station-os/demo_ground_control.git
```

---

### 2. Build `openmct-ros`

Navigate to the `openmct-ros` directory inside the cloned project:

```bash
cd demo_ground_control/openmct-ros
```

Install dependencies:

```bash
npm install
```

Build the distribution files:

```bash
npm run build:dist
```

This will generate the `dist` folder containing the plugin files needed by OpenMCT.

---

### 3. Install OpenMCT Dependencies

Navigate to the `openmct` directory:

```bash
cd ../openmct
```

Install the required Node packages:

```bash
npm install
```

---

### 4. Start OpenMCT

Run the development server:

```bash
npm start
```

By default, OpenMCT will be served at:

```
http://localhost:8080/
```

---



