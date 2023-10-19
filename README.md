# Solar System Simulation and Titan Probe Landing

## Overview
This repository contains the code and resources for a project that simulates the solar system, designs a flight trajectory for a probe from Earth to Titan, and simulates a precise landing on the surface of Titan. The primary objective was to investigate the solar system's simulation, create a flight trajectory for a probe from Earth to Titan, and simulate a precise landing on Titan's surface.

## Essay:
For a detailed understanding of the research and methodologies employed in this project, you can refer to the [essay](https://drive.google.com/file/d/1_NcuvtgqV6aWvxfHzRZZS8Jh8TDFelRb/view?usp=share_link).

## Project Structure
The codebase is structured to include the following components:

- **Interfaces**: Implementation of the interfaces provided in Phase 1.
- **Genetic Algorithm**: Implemented in `GA.java`.
- **Solvers**: Differential equation solvers implemented in Phase 2 are found in `EulerSolver.java`, `RungeKuttaSolver.java`, and `VerletSolver.java`.
- **Fuel System**: Implemented in `FuelSolver.java` and `SolarSystemSolver.java`.
- **Open Loop Controller**: For coordinating the landing of the lander. Relevant files include `Lander.java`, `OpenLoop.java`, `PhysicsEngine.java`, and `RunLanderGuiOpenLoop.java`.
- **Feedback Controller**: Implemented for precise lander landing. Relevant files include `Thruster.java`, `LandSystem.java`, `PID.java`, and `RunLanderGuiClosedLoop.java`.
- **Wind Model**: A realistic wind simulation model implemented in `Wind.java`.
- **Newton Raphson**: Implemented in `NewtonRaphson.java` to refine the results from Phase 2.

## Running the Code

### Using an IDE:
If you're running the code from an IDE, you'll need to adjust the path name of the images in the class you'll be running. For instance, if you're running `RunLaderGuiOpenLoop.java`, navigate to the lines where the images are being opened and change the path to `"src/main/java/solarimages/lander.png"` instead of `"solarimages/lander.png"`.

### Using Command Line:

1. Navigate to the correct folder in your command window: `src/main/java`

2. **Solar System Simulation (`RunSolarSystemSimulation.java`)**: 
   - **What it shows**: This class simulates the solar system and visualizes the rocket's trajectory from Earth to Titan and back.
   - Compile: `javac RunSolarSystemSimulation.java`
   - Run: `java RunSolarSystemSimulation`

3. **Landing Open Loop Controller (`RunLanderGuiOpenLoop.java`)**:
   - **What it shows**: This class provides a 2D animation showing the trajectory of the lander as it approaches Titan using an open-loop control system.
   - Compile: `javac RunLanderGuiOpenLoop.java`
   - Run: `java RunLanderGuiOpenLoop`

4. **Landing Feedback Controller (`RunLanderGuiFeedbackController.java`)**:
   - **What it shows**: This class offers a 2D animation that visualizes the lander's trajectory as it approaches Titan using a feedback control system, which adjusts the lander's path based on real-time data.
   - Compile: `javac RunLanderGuiFeedbackController.java`
   - Run: `java RunLanderGuiFeedbackController`

## Testing
Test classes were created as per the requirements for Phase 2 and are structured following the Gradle conventions. Additionally, two classes, `Test_SaturnCoordinates.java` and `Test_EarthCoordinates.java`, test the accuracy of the ODE solver against NASA's correct coordinate results. To switch between solvers, adjust the comments in the `State.java` file (lines 58-66).
