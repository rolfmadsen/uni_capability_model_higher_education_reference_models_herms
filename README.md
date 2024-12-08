# UNI DK Higher Education Reference Models (HERMS) Capability Model

## Full Disclosure

The PlantUML diagram in this repository is an ArchiMate Capability Model based on the 2018 UCISA UK HE Capability Model that you can assess at https://www.ucisa.ac.uk/groups/enterprise-architecture-group/herm.

## Purpose of the Capability Model

The Higher Education Reference Models (HERM) Capability Model provides a structured, standardized representation of the essential capabilities that enable higher education institutions to deliver their value propositions, achieve strategic goals, and respond effectively to changing educational landscapes. By illustrating **what** an organization is capable of doing rather than focusing on **how** it achieves it, the capability model serves as a foundational blueprint for understanding and communicating the institution’s core functions and domains.

In essence, this model:

- Offers a **holistic, “whole of institution” view** of business architecture elements relevant to higher education.
- Acts as a **communication tool** for engaging stakeholders, including business leaders, strategists, and architects.
- Supports **scenario-based planning** and exploration of strategic drivers, goals, and outcomes.
- Facilitates the **exchange of best practices and architectural knowledge** within and between institutions.
- Serves as a **reference point** to accelerate the creation, refinement, and integration of business and data architectures.
- Anchors discussions related to **business effectiveness, maturity assessments, investment priorities, and strategic alignment**.

By focusing on capabilities—discrete logical constructs combining people, processes, information, and technology—institutions can better understand their strengths and weaknesses, evaluate where to invest for improvement, and ensure the alignment of operational execution with strategic objectives.

## Using PlantUML ArchiMate to Create and Expand the Capability Model

### Overview of PlantUML and ArchiMate

**PlantUML** is a text-based diagramming tool that leverages a human-readable, domain-specific language to render diagrams without traditional drag-and-drop interfaces. It integrates seamlessly with version control systems, enabling collaborative, iterative, and traceable changes to models.

**ArchiMate**, on the other hand, is an open, independent enterprise architecture modeling language that supports describing, analyzing, and visualizing architecture across business domains. By combining PlantUML’s textual approach with ArchiMate’s structured modeling concepts, you can quickly produce clear, consistent enterprise architecture diagrams that illustrate how capabilities, processes, applications, and other elements come together to deliver institutional value.

### Creating the HERMS Capability Model with PlantUML ArchiMate

To model the HERMS Capability Model using PlantUML and ArchiMate, you:

1. **Include the ArchiMate Libraries:**  
   PlantUML supports ArchiMate via standard libraries and additional macros from repositories like Archimate-PlantUML. By including these libraries, you gain access to macros that represent ArchiMate concepts such as Strategy Capabilities, Business Services, Application Components, and more.

2. **Define Strategy Capabilities and Groupings:**  
   Each capability can be represented as a `Strategy_Capability(...)` element, often nested within `Grouping(...)` elements to reflect logical domains and sub-domains (e.g., “Teaching & Learning,” “Research,” “Enabling Capabilities”). Nesting capabilities inside parent capabilities or groupings conveys hierarchy and context, making the model easier to navigate and understand.

3. **Leverage Nesting and Themes:**  
   By specifying a `true` parameter in the capability macro, you enable nesting, allowing you to embed subordinate capabilities directly within a higher-level capability. This visually and logically organizes the model, making it intuitive for stakeholders.  
   Applying a theme (e.g., `archimate-standard`) ensures consistent styling, colors, and font choices, leading to a polished and professional presentation of your architecture.

4. **Add Relationships for Depth and Clarity:**  
   Beyond a static capability list, ArchiMate relationships can show how capabilities depend on each other, serve others, or aggregate to form more complex value streams. Using macros like `Rel_Composition(...)` or `Rel_Assignment(...)` clarifies how different parts of the enterprise interact, revealing dependencies, service flows, and contribution to organizational goals.

5. **Iterative Development and Version Control:**  
   Because you’re working with PlantUML’s plain-text format, updates to the model are as simple as editing a line in a code file. This encourages iterative refinement:  
   - Start with a broad set of top-level capabilities.  
   - Add nested capabilities as detail emerges.  
   - Introduce relationships as you clarify interdependencies.  
   - Commit changes to version control, enabling rollback and transparent evolution of the model over time.

6. **Integration with Other Architecture Artifacts:**  
   The HERMS Capability Model can stand alone or integrate into a larger architecture ecosystem. For example, once capabilities are defined, you can link them to business objectives, map them to data and application services, or highlight alignment with strategic initiatives. Over time, the model can be enriched by adding more ArchiMate layers—e.g., Motivation layer elements (to show goals and principles) or Application layer elements (to show how capabilities are realized by IT systems).

### Expanding and Evolving the Model

The beauty of using ArchiMate and PlantUML is that the model is not static. As institutions grow, strategies evolve, or technologies shift, you can:

- **Add New Capabilities:**  
  Introduce new capabilities as the institution ventures into emerging areas or services.

- **Refine Existing Capabilities:**  
  Break down an existing capability into nested sub-capabilities, showing increasingly granular details as needed.

- **Introduce Additional Layers (Business, Application, Technology):**  
  Extend the capability model to link strategic capabilities to business processes, application services, and infrastructure. This presents a full blueprint of how the institution’s goals are operationalized.

- **Conduct Impact Analysis:**  
  By visualizing dependencies and relationships, you can assess the impact of proposed changes. For instance, if you improve one capability, which other capabilities benefit? If a capability is reduced, what are the downstream implications?

- **Scenario-Based Planning and Stakeholder Communication:**  
  With a version-controlled, easily rendered ArchiMate model, you can create scenario branches for “what-if” analyses. Show key stakeholders how a new strategic initiative would fit into the existing capability landscape, or how resource constraints affect certain capabilities.

### Conclusion

The HERMS Capability Model provides a structured starting point for understanding the institution’s abilities and strategic needs in the higher education sector. By pairing it with PlantUML’s ArchiMate support, you gain a flexible, text-based, and collaborative environment to:

- Construct and maintain a comprehensive capability landscape.
- Visually connect capabilities to strategies, processes, and resources.
- Adapt the model over time as strategies evolve and new requirements emerge.

This approach ensures the capability model remains not just a static diagram, but a living, evolving representation of the enterprise’s strategic and operational reality.

## Using PicoWeb with PlantUML in VSCode to Generate SVG Diagrams

For beginners, setting up a local environment to view and generate ArchiMate-based UML diagrams using PlantUML in Visual Studio Code (VSCode) can seem a bit daunting. The good news is that with a few simple steps, you can have a straightforward workflow: write your PlantUML-based ArchiMate code in VSCode, preview and refine it on the fly, and generate clean SVG files for sharing or embedding into documentation.

### Prerequisites

1. **Java Runtime Environment (JRE) or Java Development Kit (JDK)**  
   Ensure that Java is installed on your system since PlantUML requires a Java environment.  
   - Check by running `java -version` in your terminal.
   - If not installed, download from [https://www.java.com/](https://www.java.com/).

2. **PlantUML JAR File**  
   Download the latest PlantUML JAR (e.g., `plantuml-gplv2-1.2024.8.jar`) from [https://plantuml.com/download#latest_release](https://plantuml.com/download#latest_release) and save it in the same folder as your PlantUML model files.

### Steps to Set Up PicoWeb and VSCode Integration

1. **Install PlantUML Extension for VSCode**  
   Use the Jebbs PlantUML extension, which makes editing and previewing PlantUML diagrams directly inside VSCode a breeze.  
   - Go to the Extensions panel in VSCode (`Ctrl+Shift+X` or `Cmd+Shift+X` on macOS).  
   - Search for "PlantUML" by jebbs and install it. Or visit the GitHub repository for the extension at [https://github.com/qjebbs/vscode-plantuml](https://github.com/qjebbs/vscode-plantuml).

2. **Start PicoWeb**  
   PicoWeb is a tiny webserver built into PlantUML that allows the VSCode PlantUML extension to render diagrams locally.  
   - Open a terminal in the folder where `plantuml-gplv2-1.2024.8.jar` is located.  
   - Run:
     ```bash
     java -jar plantuml-gplv2-1.2024.8.jar -picoweb
     ```
   - This starts a local webserver for PlantUML. By default, it listens on `http://localhost:8080/`.

3. **VSCode Settings for Local Rendering**  
   The Jebbs PlantUML extension can be configured to use your local PicoWeb server for rendering instead of relying on external servers.  
   - Press `Ctrl+Shift+P` (or `Cmd+Shift+P` on macOS) in VSCode and type "PlantUML: Preview Current Diagram" to open a diagram preview.  
   - In the extension settings (`File > Preferences > Settings > Extensions > PlantUML`), set the "Plantuml: Server" URL to `http://localhost:8080`. This ensures all rendering requests go to your local PicoWeb instance.

### Generating and Viewing Diagrams

1. **Create a PlantUML ArchiMate Diagram**  
   In VSCode, create a `.puml` file (for example `uni_capability_model.puml`). Include the ArchiMate libraries and define your elements and relationships as explained earlier.

2. **Preview Within VSCode**  
   With the `.puml` file open, press `Alt+D` on Windows/Linux or `Option+D` on macOS to preview the diagram. The PlantUML extension sends your code to PicoWeb, which renders it and returns the diagram right inside the VSCode preview panel.

3. **Generate an SVG File**  
   Once you’re satisfied with your diagram, you can export it as an SVG for embedding in webpages, wikis, or documentation.  
   - In the diagram preview, you’ll see export options (e.g., a small toolbar at the top of the preview).  
   - Choose "Export as SVG" to generate an `.svg` file. Save it to your project directory or any chosen location.
   - Alternatively, you can run PlantUML from the command line to generate the SVG:
     ```bash
     java -jar plantuml-gplv2-1.2024.8.jar -tsvg uni_capability_model.puml
     ```
     This command outputs `uni_capability_model.svg` in the same directory.

### Expanding and Enhancing Your ArchiMate Model

With PicoWeb and VSCode, it’s easy to iterate on your model:

- **Add More ArchiMate Layers:**  
  Start with Strategy Capabilities, then incorporate Business, Application, or Technology layers. As you add elements and relationships, just hit `Alt+D` to preview the updated diagram instantly.
  
- **Refine the Look with Themes and Skinparams:**  
  Apply different themes or fine-tune styling using `skinparam` lines in your `.puml` file for a cleaner or more branded look.

- **Version Control and Collaboration:**  
  Since your PlantUML diagrams are just text, commit them to Git, push changes to a remote repository, and collaborate with peers. Everyone can run PicoWeb locally to preview the diagrams exactly as you do.

- **Continuous Integration and Automated Documentation:**  
  Integrate PlantUML diagram generation into build pipelines or CI/CD. This ensures that up-to-date diagrams are always generated whenever the `.puml` files change, keeping your architectural documentation dynamic and current.

### Conclusion

For beginners, combining PicoWeb, PlantUML, and the VSCode extension provides a powerful, user-friendly workflow. You:

- Write ArchiMate-based capability models in simple text.
- Instantly preview them locally.
- Easily export clean SVG diagrams for sharing.
- Evolve the model as your understanding and requirements grow.

This approach simplifies the process of producing professional, maintainable architectural diagrams that accurately represent your institution’s business capabilities and strategic direction.