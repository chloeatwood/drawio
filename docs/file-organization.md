# File Organization Guide

This document outlines the structure and organization of the draw.io repository, helping new contributors understand the purpose of each directory and how the project is organized.

## Top-Level Directories

### `/.github`

GitHub-specific configuration and automation files.

- **`ISSUE_TEMPLATE/`** - Templates for creating issues. Helps standardize bug reports and feature requests from contributors.
- **`workflows/`** - GitHub Actions CI/CD workflows. Contains automation for testing, building, and deployment processes.

### `/docs`

Documentation files for the project. Helps developers understand architecture, setup, and contribution guidelines.

- Contains README, guides, and reference material
- Add new documentation files here as the project evolves

### `/etc`

Miscellaneous build tools, utilities, configuration, and external integrations.

- **`build/`** - Build scripts and configuration files for compiling the project
- **`dependencies/`** - External dependencies and version management
- **`docker/`** - Docker configuration files for containerized deployments
- **`imageResize/`** - Utilities for image processing and resizing
- **`integrate/`** - Integration tools and scripts for connecting with external services
- **`propgen/`** - Property generation utilities for mxGraph
  - **`com/mxgraph/properties/`** - Generated property definitions for the mxGraph library

### `/src/main`

Main source code directory containing both backend and frontend code.

## Source Code Organization

### `/src/main/java`

Java backend code for server-side functionality.

- **`com/mxgraph/online/`** - Main Java packages for servlets and server operations
- Used in server deployments (not required for GitHub Pages deployments)
- Handles server-side file operations, integrations, and API endpoints

### `/src/main/webapp`

The core web application containing frontend code and all static assets.

#### Web Configuration

- **`META-INF/`** - Java web application metadata
- **`WEB-INF/`** - Web application configuration and dependencies
  - **`lib/`** - JAR files and Java libraries required by servlets

#### Frontend Code

- **`connect/`** - Connector and integration modules
  - **`common/js/`** - Shared JavaScript utilities for connecting to external services
- **`js/`** - Core JavaScript source code (see detailed breakdown below)

#### Assets and Resources

- **`images/`** - General application images and icons
- **`img/`** - Diagram elements, clipart, and shape libraries organized by category
  - **`clipart/`**, **`computers/`**, **`finance/`**, **`networking/`**, **`people/`**, **`telecommunication/`** - General-purpose diagram elements
  - **`lib/`** - Extensive library of professional icons organized by provider and category:
    - **`active_directory/`** - Active Directory related icons
    - **`allied_telesis/`** - Networking equipment icons with subcategories (buildings, security, storage, switches, wireless, etc.)
    - **`atlassian/`** - Atlassian product icons
    - **`azure2/`** - Microsoft Azure service icons (AI/ML, analytics, compute, databases, security, storage, networking, etc.)
    - **`clip_art/`** - General clip art organized by category
    - **`cumulus/`** - Cumulus networks icons
    - **`dynamics365/`** - Microsoft Dynamics 365 icons
    - **`ibm/`** - IBM service icons (analytics, blockchain, data, infrastructure, security, etc.)
    - **`mscae/`** - Microsoft Cloud Architecture Essentials icons
    - **`sap/`** - SAP system icons

- **`math4/es5/`** - MathJax library for mathematical notation rendering
  - **`fonts/`** - Font files for math rendering (BBM, BBoldx, DSfont, MHchem, TeX fonts in WOFF2 format)
  - **`input/`** - TeX input processing with extensions
  - **`output/`** - Output rendering engines
  - **`ui/`** - User interface components for math

- **`mxgraph/`** - Core mxGraph library (diagramming and graph visualization)
  - **`css/`** - mxGraph stylesheets
  - **`images/`** - mxGraph-specific images
  - **`src/`** - mxGraph source code organized by functionality:
    - **`handler/`** - Event handlers and user interactions
    - **`io/`** - Input/output operations for diagrams
    - **`layout/`** - Layout algorithms (hierarchical layout with model and stage components)
    - **`model/`** - Data model for graphs and diagram structure
    - **`shape/`** - Shape definitions and custom shape implementations
    - **`util/`** - Utility functions
    - **`view/`** - View rendering and display logic

- **`plugins/`** - Third-party and extended plugins
  - **`trees/`** - Tree diagram plugins
  - **`webcola/`** - WebCola layout and constraint-based layout plugins

- **`resources/`** - General application resources
- **`styles/`** - CSS stylesheets and styling
  - **`fonts/`** - Custom fonts for the application

- **`templates/`** - Pre-built diagram templates organized by use case:
  - **`basic/`** - Basic shapes and simple diagrams
  - **`business/`** - Business process and organizational diagrams
  - **`charts/`** - Data visualization and chart templates
  - **`engineering/`** - Technical and engineering diagrams
  - **`flowcharts/`** - Process flowchart templates
  - **`layout/`** - Layout and positioning templates
  - **`maps/`** - Map and geographical diagrams
  - **`network/`** - Network topology diagrams
  - **`other/`** - Miscellaneous templates
  - **`software/`** - Software architecture and deployment diagrams
  - **`tables/`** - Table and data structure templates
  - **`uml/`** - UML and object-oriented design templates
  - **`venn/`** - Venn diagram templates
  - **`wireframes/`** - UI/UX wireframe templates

#### JavaScript Libraries and Modules

The **`js/`** directory contains the main application code and third-party JavaScript libraries:

- **`cryptojs/`** - Cryptography library for secure operations
- **`deflate/`** - Compression library for file optimization
- **`diagramly/`** - *Core draw.io application code*
  - **`graphml/`** - GraphML file format support
  - **`miro/`** - Miro integration
  - **`sidebar/`** - Sidebar UI components
  - **`util/`** - Utility functions
  - **`vsdx/`** - Microsoft Visio VSDX format support
- **`dropbox/`** - Dropbox integration
- **`freehand/`** - Freehand drawing tools
- **`grapheditor/`** - Graph editing functionality
- **`jquery/`** - jQuery library
- **`jszip/`** - ZIP file handling
- **`mermaid/`** - Mermaid diagram language support
- **`onedrive/`** - OneDrive/Microsoft 365 integration
- **`orgchart/`** - Organization chart templates and utilities
- **`rough/`** - Rough.js library for hand-drawn style graphics
- **`sanitizer/`** - HTML and content sanitization for security
- **`simplepeer/`** - WebRTC peer-to-peer communication
- **`spin/`** - Spin.js loading spinner library


## Summary

The draw.io repository is thoughtfully organized to support both users and developers. The extensive categorization of icons and templates makes diagram creation intuitive, while the modular JavaScript architecture and separation of frontend/backend code enables easy maintenance and feature additions. The clear structure reduces onboarding time for new contributors and supports the project's goal of being a versatile diagramming tool for multiple enterprise platforms and use cases.

# Directory Structure Overview (folders only)
```
draw.io/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   └── workflows/
├── docs/
├── etc/
│   ├── build/
│   ├── dependencies/
│   ├── docker/
│   ├── imageResize/
│   ├── integrate/
│   └── propgen/
│       └── com/mxgraph/properties/
└── src/
    └── main/
        ├── java/
        │   └── com/mxgraph/online
        └── webapp/
            ├── META-INF/
            ├── WEB-INF/
            │   └── lib/
            ├── connect/
            │   └── common/
            │       └── js/
            ├── images/
            ├── img/
            │   ├── clipart/
            │   ├── computers/
            │   ├── finance/
            │   ├── google-app/
            │   ├── networking/
            │   ├── people/
            │   ├── telecommunication/
            │   └── lib/
            │       ├── active_directory/
            │       ├── allied_telesis/
            │       │   ├── buildings/
            │       │   ├── computer_and_terminals/
            │       │   ├── media_converters/
            │       │   ├── security/
            │       │   ├── storage/
            │       │   ├── switch/
            │       │   └── wireless/
            │       ├── atlassian/
            │       ├── azure2/
            │       │   ├── ai_machine_learning/
            │       │   ├── analytics/
            │       │   ├── app_services/
            │       │   ├── azure_ecosystem/
            │       │   ├── azure_stack/
            │       │   ├── azure_vmware_solution/
            │       │   ├── blockchain/
            │       │   ├── compute/
            │       │   ├── containers/
            │       │   ├── cxp/
            │       │   ├── databases/
            │       │   ├── devops/
            │       │   ├── general/
            │       │   ├── hybrid_multicloud/
            │       │   ├── identity/
            │       │   ├── integration/
            │       │   ├── internet_of_things/
            │       │   ├── intune/
            │       │   ├── iot/
            │       │   ├── management_governance/
            │       │   ├── menu/
            │       │   ├── migrate/
            │       │   ├── mixed_reality/
            │       │   ├── monitor/
            │       │   ├── networking/
            │       │   ├── other/
            │       │   ├── power_platform/
            │       │   ├── preview/
            │       │   ├── security/
            │       │   ├── storage/
            │       │   └── web/
            │       ├── clip_art/
            │       │   ├── computers/
            │       │   ├── finance/
            │       │   ├── general/
            │       │   ├── networking/
            │       │   ├── people/
            │       │   └── telecommunication/
            │       ├── cumulus/
            │       ├── dynamics365/
            │       ├── ibm/
            │       │   ├── analytics/
            │       │   ├── applications/
            │       │   ├── blockchain/
            │       │   ├── data/
            │       │   ├── devops/
            │       │   ├── infrastructure/
            │       │   ├── management/
            │       │   ├── miscellaneous/
            │       │   ├── security/
            │       │   ├── social/
            │       │   ├── users/
            │       │   └── vpc/
            │       ├── mscae/
            │       │   └── dep/
            │       └── sap/
            ├── js/
            │   ├── cryptojs/
            │   ├── deflate/
            │   ├── diagramly/
            │   │   ├── graphml/
            │   │   ├── miro/
            │   │   ├── sidebar/
            │   │   ├── util/
            │   │   └── vsdx/
            │   ├── dropbox/
            │   ├── freehand/
            │   ├── grapheditor/
            │   ├── jquery/
            │   ├── jszip/
            │   ├── mermaid/
            │   ├── onedrive/
            │   ├── orgchart/
            │   ├── rough/
            │   ├── sanitizer/
            │   ├── simplepeer/
            │   └── spin/
            ├── math4/es5/
            │   ├── fonts/
            │   │   ├── mathjax-bbm-font-extension/
            │   │   │   └── chtml/woff2/
            │   │   ├── mathjax-bboldx-font-extension/
            │   │   │   └── chtml/woff2/
            │   │   ├── mathjax-dsfont-font-extension/
            │   │   │   └── chtml/woff2/
            │   │   ├── mathjax-mhchem-font-extension/
            │   │   │   └── chtml/woff2/
            │   │   └── mathjax-tex-font/
            │   │       └── chtml/woff2/
            │   ├── input/
            │   │   └── tex/extensions/
            │   ├── output/
            │   └── ui/
            ├── mxgraph/
            │   ├── css/
            │   ├── images/
            │   └── src/
            │       ├── handler/
            │       ├── io/
            │       ├── layout/
            │       │   └── hierarchical/
            │       │       ├── model/
            │       │       └── stage/
            │       ├── model/
            │       ├── shape/
            │       ├── util/
            │       └── view/
            ├── plugins/
            │   ├── trees/
            │   └── webcola/
            ├── resources/
            ├── styles/
            │   └── fonts/
            └── templates/
                ├── basic/
                ├── business/
                ├── charts/
                ├── engineering/
                ├── flowcharts/
                ├── layout/
                ├── maps/
                ├── network/
                ├── other/
                ├── software/
                ├── tables/
                ├── uml/
                ├── venn/
                └── wireframes/
```