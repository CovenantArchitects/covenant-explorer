🗺️ Repository Structure Map: covenant-explorer (Static Site)

This diagram visualizes the complete structure of the public-facing static site repository, https://github.com/CovenantArchitects/covenant-explorer.

flowchart TB
    %% Style definitions for clarity (Core, Assets, Documentation)
    classDef core fill:#4f46e5, color:#fff, stroke:#4f46e5
    classDef asset fill:#bae6fd, color:#0369a1, stroke:#0369a1
    classDef doc fill:#fde68a, color:#92400e, stroke:#92400e

    %% Define the main repository node (The static site)
    Root[covenant-explorer/ - 13 Total Files]:::core

    %% Define the primary children (Directories and Root Files)
    Root --> Root_Files
    Root --> Images_Dir
    Root --> Map_Files_Dir

    %% Subgraph: Root Files (Core Website Components - 5 Files)
    subgraph Root_Files ["Root Files (Web & Meta)"]
        direction LR
        RF1[CNAME]:::core
        RF2[CONTRIBUTING.md]:::doc
        RF3[GOVERNANCE.md]:::doc
        RF4[README.md]:::doc
        RF5[index.html (Core SPA)]:::core
        Root_Files --> RF1 & RF2 & RF3 & RF4 & RF5
    end
    
    %% Subgraph: Images Directory (Static Assets - 8 Files)
    subgraph Images_Dir ["1. images/ (8 Static Assets)"]
        direction TB
        IMG1[8bbfb44c-1345-46af-8747-89698a1ca267.jpg]:::asset
        IMG2[b6cfa003-4660-42b4-ba5c-f005682d155f.jpg]:::asset
        IMG3[c7e1f035-2c8a-4d64-b0c3-e66a42cb2faf.jpg]:::asset
        IMG4[covenant_architecture.png]:::asset
        IMG5[dfd5611286356.png]:::asset
        IMG6[f03df80d-6c00-4e75-b60c-6184ba2240e6.jpg]:::asset
        IMG7[f8ed0ef3-80db-488b-af2f-f2df4cff0e82.jpg]:::asset
        IMG8[image01101011.png]:::asset
        Images_Dir --> IMG1 & IMG2 & IMG3 & IMG4 & IMG5 & IMG6 & IMG7 & IMG8
    end
    
    %% Subgraph: Map Files Directory (Documentation - 2 Files)
    subgraph Map_Files_Dir ["2. Covenant_Explorer_Repo_Map/ (2 Docs)"]
        direction LR
        MAP1[Covenant_Explorer_Repo_Map.md]:::doc
        MAP2[Covenant_Explorer_Repo_Map.pdf]:::doc
        Map_Files_Dir --> MAP1 & MAP2
    end
