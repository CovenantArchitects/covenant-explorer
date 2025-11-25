# Covenant Explorer Repository Structure

```mermaid
flowchart TB
    %% Styles
    classDef core fill:#4f46e5,color:#fff,stroke:#4f46e5,stroke-width:2px
    classDef asset fill:#bae6fd,color:#0369a1,stroke:#0369a1,stroke-width:2px
    classDef doc fill:#fde68a,color:#92400e,stroke:#92400e,stroke-width:2px

    %% Root
    Root["covenant-explorer\\n13 Total Files"]:::core

    %% Main branches
    Root --> RootFiles["Root Files (Web & Meta)\\n5 files"]
    Root --> ImagesDir["images\\n8 Static Assets"]
    Root --> MapDir["Covenant_Explorer_Repo_Map\\n2 Docs"]

    %% Root Files subgraph
    subgraph RootFiles [" "]
        direction TB
        RF1[CNAME]:::core
        RF2[CONTRIBUTING.md]:::doc
        RF3[GOVERNANCE.md]:::doc
        RF4[README.md]:::doc
        RF5["index.html\\nCore SPA"]:::core
    end

    %% Images subgraph
    subgraph ImagesDir [" "]
        direction TB
        IMG1[8bbfb44c-....jpg]:::asset
        IMG2[b6cfa003-....jpg]:::asset
        IMG3[c7e1f035-....jpg]:::asset
        IMG4[covenant_architecture.png]:::asset
        IMG5[dfd5611286356.png]:::asset
        IMG6[f03df80d-....jpg]:::asset
        IMG7[f8ed0ef3-....jpg]:::asset
        IMG8[image01101011.png]:::asset
    end

    %% Map files subgraph
    subgraph MapDir [" "]
        direction TB
        MAP1[Covenant_Explorer_Repo_Map.md]:::doc
        MAP2[Covenant_Explorer_Repo_Map.pdf]:::doc
    end
