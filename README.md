# DSRT 2024 - Managing Urban Traffic and Air Quality: Simulation Techniques and Practical Applications

Welcome to the repository for the **DS-RT 2024** tutorial titled **"Managing Urban Traffic and Air Quality: Simulation Techniques and Practical Applications"**. This repository contains the materials used during the tutorial, including the slides and all necessary files for the practical session.

## Repository Structure

### 1. **Slides/**

- Contains the PDF of the slides used during the presentation.
  - [Tutorial_DSRT-2024.pdf](Slides/Tutorial_DSRT-2024.pdf)

### 2. **SimulationFiles/**

- Contains all the files required for the practical part of the tutorial.
- Includes a **markdown file** with step-by-step commands and instructions to follow during the tutorial.
- Note that the `valencia_full.osm.xml` file is not included in this repository due to its large size. You can download it from personal [OneDrive](https://upvedues-my.sharepoint.com/:u:/g/personal/jdpadper_upv_edu_es/EZoZAAwsPBFBlFU5TknmsYgBjl91LbxwTiUiRVYVIKddTw?e=cmKlAf).

Files include:

- `tutorial-practical-commands.md`: Step-by-step guide for running the simulations.
- **Simulation config files**: `.sumocfg`, `.net.xml`, `.rou.xml`, and other files for running SUMO and GRAL simulations.

## Prerequisites

To successfully run the simulations and follow the tutorial, you'll need to have the following software installed:

- **SUMO (Simulation of Urban Mobility)**: Version **1.19** or higher
  - Download: [SUMO Downloads](https://sumo.dlr.de/docs/Downloads.php)
- **GRAL (Graz Lagrangian Model)**: Version **23.11** or higher
  - Download: [GRAL Repository](https://github.com/GralDispersionModel/GRAL) or register and download from the [GRAL Website](https://gral.tugraz.at/download/).
  - Use the `GRAL.dll` to run the air quality simulations.
- **SUMO2GRAL**: Latest version
  - Download: [SUMO2GRAL GitHub](https://github.com/GRCDEV/SUMO2GRAL)
- **Python**: Version **3.11** or higher
  - Download: [Python Official Site](https://www.python.org/downloads/)
- **.NET SDK**: Version **8** or higher
  - Download: [.NET SDK Downloads](https://dotnet.microsoft.com/en-us/download)

## Getting Started

1. **Clone the repository**:

   ```bash
   git clone https://github.com/yourusername/DSRT2024-Traffic-AirQuality-Tutorial.git
   cd DSRT2024-Traffic-AirQuality-Tutorial
   ```

2. **Install Prerequisites**:

   - **SUMO**:
     - Download and install SUMO from the [SUMO Downloads](https://sumo.dlr.de/docs/Downloads.php) page.
     - Ensure that SUMO is added to your system's PATH environment variable.

   - **GRAL**:
     - Clone the GRAL repository:

       ```bash
       git clone https://github.com/GralDispersionModel/GRAL.git
       ```

     - Follow the build and installation instructions provided in the GRAL repository.

   - **SUMO2GRAL**:

     - Clone the SUMO2GRAL repository:

        ```bash
        git clone https://github.com/GRCDEV/SUMO2GRAL.git
        ```

     - Install **.NET SDK 8** to build and run SUMO2GRAL.
     - Follow the installation guide in the SUMO2GRAL repository.
     
    - **Python**:

        - Download and install Python 3.11 or higher from the [Python Official Site](https://www.python.org/downloads/).
        - Verify the installation by running `python --version` in your terminal.

    - **.NET SDK**:
        - Download and install the .NET SDK version 8 or higher from the [.NET SDK Downloads](https://dotnet.microsoft.com/en-us/download).
         - Verify the installation by running `dotnet --version` in your terminal.

3. **Follow the Practical Commands**:

   - Navigate to the **SimulationFiles/** directory:

    ```bash
     cd SimulationFiles
    ```

   - Open `tutorial-practical-commands.md` and follow the step-by-step instructions to set up and run the simulations.

4. **Explore the Slides**:

   - The slides provide an overview of the key concepts covered in the tutorial.
   - You can find them in the **Slides/** directory:
     - [Tutorial_DSRT-2024.pdf](Slides/Tutorial_DSRT-2024.pdf)

## Tools Used

- **SUMO (Simulation of Urban Mobility)**: For traffic simulation.
- **GRAL (Graz Lagrangian Model)**: For air quality modeling.
- **SUMO2GRAL**: Custom tool developed to integrate SUMO traffic data into GRAL for air quality simulations.

## License

This repository is open-source under the MIT License. Feel free to explore, use, and contribute!
