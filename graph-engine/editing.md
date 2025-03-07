# Editing

The Graph Engine’s node editor is designed for flexibility and ease, letting you build and tweak graphs with simple actions. Here’s how to edit your workflows efficiently.

### Adding & Moving Nodes

Add nodes to your canvas in three ways, each with a handy description to guide you:

* **From the Nodes Panel**:
  * Open the Nodes Panel (usually on the left), find a node (e.g., "Add" or "Color to String"), and drag it onto the canvas.
  * **Hover Tip**: Pause over a node in the panel to see its description (e.g., "Adds two numbers together").
* **Through Shift + K Menu**:
  * Press **Shift + K** (Shift + K on Windows) to open a searchable menu.
  * Type to filter nodes (e.g., "color" for color-related nodes), select one, and hit Enter to add it where your cursor is.
  * **Bonus**: Each node shows a description in the menu for quick reference.
* **From the Top Action Bar**:
  * Click the **Nodes Icon** in the toolbar (top of the screen), pick a node from the dropdown, and it lands on the canvas.
* **Moving Nodes**: Click and drag any node to reposition it.&#x20;

### Connecting Nodes

Link nodes to flow data between them using two methods:

* **Drag Method**: Click an output port (right side), drag to a matching input port (left side), and release. A blue edge appears if the types match; a red edge means they don’t.
* **Click Method**: Click an output port, then click an input port. The editor auto-draws a blue edge if compatible. **Tip**: Hover over ports to check types (e.g., "color", "number") if "Port Types" is enabled.

### Disconnecting Nodes

Break connections easily:

* Click an edge (the line between ports), then press **Delete**. The edge vanishes, and data stops flowing.&#x20;

### Split Connections (Pass Through)

Insert a node into an existing connection to modify the flow:

* **Double-Click Method**: Double-click an edge, pick a node from the menu that pops up (e.g., "Log Value"), and it splits the edge, wiring the new node between the original two.

### Duplicate

Make an exact copy without clipboard fuss:

* Right-click a node (or selected nodes) and choose **Duplicate** from the menu. The copy appears nearby, with settings intact but no edges.&#x20;

**Extra Editing Tools**:

* **Zoom & Pan**: Scroll the mouse wheel to zoom in/out, or drag the canvas to pan—great for navigating big graphs.
