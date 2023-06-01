# HIP Architecture
A platform designed for the optimized collection, storage, curation, sharing and analysis of multiscale Human intracerebral EEG data at an international level.

## Collaborative Workspace Release 
May 2023 
A secured, private and dedicated space for projects

## Private Workspace Beta Release 
November 2022  
A secured, private and dedicated space for clinical centers contributing to iEEG data collection to upload, store and process their own pseudonymized data.

https://thehip.app/

### Centers Private Workspace 

#### Nextcloud main features
```mermaid
flowchart LR
Nextcloud --> Login -->|Authentication| IAM-Ebrains
Nextcloud --> FileSystem -->|import files| WebDav
FileSystem -->|import files| WebUI
FileSystem -->|import files| Micromed
Nextcloud --> FileBrowser

````

### Web Interface + API Gateway
```mermaid
flowchart LR
NextCloud --> Web-App
Web-App --> API-Gateway
API-Gateway --> S[(State)]
API-Gateway --> Services
Services --> Remote-App-API
Services --> BIDS-Manager
Services --> AuthN/Z
Web-App --> Centers
Web-App --> Center --> Workspace 
Center --> Desktops
Center --> BIDS
BIDS --> Indexation
```

### Remote Apps
```mermaid
flowchart LR
API -->|Start, Stop| Server --> XPra -->|Authentication| IAM-Ebrains
API -->|Start, Stop| App -->|mount User/Center File system| GhostFS
API  --> App-Catalog 

```

## Projects Collaborative Workspace 
An access-restricted space where curated and pseudonymised data can be shared with other accredited data providers.

https://dev.thehip.app/

### Data Management

```mermaid
flowchart LR
BIDS-Tools -->|Index| ElasticSearch
BIDS-Tools -->|Create| BIDS-Dataset --> Private
BIDS-Tools -->|Validate| BIDS-Dataset 
BIDS-Dataset --> Collab
BIDS-Tools -->|Import| Files 

```

### Remote Apps

```mermaid
flowchart LR
Gateway --> API-Private--> Server/App --> XPra -->|AuthN/Z| IAM-Ebrains
Gateway --> API-Collab--> Shared-Server/App --> XPra
API -->|Start, Stop| App -->|mount User/Center File system| GhostFS
 API-Private  --> App-Catalog-1 
API-Collab  --> App-Catalog-2 

```

### Projects

```mermaid
flowchart LR
API-Gateway -->|Authorization| IAM-EBRAINS --> Groups
IAM-EBRAINS --> Members --> Admin
Members --> Users
API-Gateway -->|Retrieve Metadata| FS-API --> GhostFS 
API-Gateway --> Remote-Apps --> Servers
Servers --> Apps --> GhostFS
Servers --> IAM-EBRAINS

```
 
#### Create Project 
```mermaid
sequenceDiagram
    UI->>Gateway: Create Project
    Gateway->>NextCloud: Authenticate
    NextCloud-->>Gateway: Success
    Gateway->>IAM: Authorize
    IAM-->>Gateway: Success
    Gateway->>IAM: Create Group
    Gateway->>IAM: Add User to Group Administrators
    Gateway->>IAM: Add User to Group Members
    Gateway->>IAM: Add Group to Projects Group Members
    IAM-->>Gateway: Success
    Gateway->>Collab: Create Project Folder
    Gateway->>Collab: Chown Project Folder to www-data
    Collab-->>Gateway: Success
    Gateway->>Gateway: Create local mountpoint for distant project folder
    Gateway->>GhostFS: Create User FS API and mount it
    GhostFS-->>Gateway: Success
    Gateway->>Bids-Tools: Create BIDS Dataset
    Bids-Tools-->>Gateway: Success
    Gateway-->>UI: Success
```


