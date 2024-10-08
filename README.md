# assemblylineplanning
Graph Data Science to compute gantt planning from task dependency dataset

![Assembly Line](./images/assemblyline.png)

# How-to
## Neo4j AuraDS instance
1. Spawn an AuraDS instance
2. Connect to https://console.neo4j.io
3. Go to Query > Saved Cypher
4. Import the `./cypher/assemblyline_cypher.csv` file
5. Run the queries one by one

## NeoDash dashboard
1. Connect to https://neodash.graphapp.io
2. Import the `./neodash/assemblyline_dashboard.json`
3. Visualize dynamic gantt dashboards

# Graph model
![Graph Model](./images/graph_model.png)

Let us explain the graph model.
- A `Team` *`PERFORMS`* a `Task` *`AT`* a `Workstation`.
- A `Task` has input and output `Parts`.
- A `Rotorcraft` *`HAS_COMPONENT_ASSEMBLY`* `Parts`.
- A `Part` *`HAS_TYPE`* a `PartType`.