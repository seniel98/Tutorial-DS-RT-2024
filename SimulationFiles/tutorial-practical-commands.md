# Practical Commands for DS-RT 2024 Tutorial

### **1. Building Traffic Networks with NETCONVERT**

#### Download OSM data

- Go to: [BBBIKE](https://extract.bbbike.org/). Select the area of interest and download the OSM data in OSM XML format.

#### Import OpenStreetMap data into SUMO’s network format

- Documentation: [NETCONVERT](https://sumo.dlr.de/docs/Networks/Import/OpenStreetMap.html)

```bash
netconvert --osm-files valencia_roads.osm.xml -o valencia_roads_original.net.xml  --geometry.remove --ramps.guess --junctions.join --tls.guess-signals --tls.discard-simple --tls.join --tls.default-type actuated
```

---

### **2. Refining Networks with NETEDIT**

- Documentation: [NETEDIT](https://sumo.dlr.de/docs/Netedit/index.html)

After generating the network, refine it using NETEDIT to manually fix issues such as lane directions, traffic signals, and turn restrictions.

---

### **3. Creating Traffic Demand with Random Trips**

#### Generate random trips for Diesel Euro 4 vehicles

- Documentation: [Random Trips](https://sumo.dlr.de/docs/Tools/Trip.html)

**Option 1**: Calls `duarouter` in the background

```bash
python3 $SUMO_HOME/tools/randomTrips.py -n valencia_roads_edited.net.xml --min-distance 1250 --trip-attributes 'departLane="best" departSpeed="max" departPos="random" type="diesel_e4"' --additional-file valencia_trips.add.xml --edge-permission passenger --random --insertion-rate 10000 --route-file valencia_test.rou.xml
```

**Option 2**: Does not use `route-file`. Use `duarouter` to create a `.rou.xml` file.

- Documentation: [Duarouter](https://sumo.dlr.de/docs/duarouter.html)

```bash
duarouter -n valencia_roads_edited.net.xml --route-files trips.trips.xml --additional-files valencia_trips.add.xml --route-steps 3600 -o valencia_test.rou.xml
```

---

### **4. SUMO Simulation**

#### Create a SUMO configuration file

- Documentation: [SUMO Configuration](https://sumo.dlr.de/docs/sumo.html)

#### Run the SUMO simulation in GUI mode

- Documentation: [SUMO GUI](https://sumo.dlr.de/docs/sumo-gui.html)

```bash
sumo-gui -c configuration.sumo.cfg
```

#### Run the SUMO simulation in command-line mode

- Documentation: [SUMO Command Line](https://sumo.dlr.de/docs/Basics/Using_the_Command_Line_Applications.html)

```bash
sumo -c configuration.sumo.cfg
```

---

### **5. Air Quality Analysis with SUMO2GRAL**

- Documentation: [SUMO2GRAL](https://github.com/seniel98/SUMO2GRAL?tab=readme-ov-file#usage)

```bash
python3 /Users/josedaniel/Library/CloudStorage/OneDrive-UPV/Doctorado/scripts/SUMO2GRAL/cli.py -c configuration-nox.sumo2gral.cfg --process all
```
