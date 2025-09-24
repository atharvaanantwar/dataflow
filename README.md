# dataflow
```mermaid
graph TD
    %% External Entity
    A[User]

    %% Data Stores
    D1[(Users)]
    D2[(Scenarios)]
    D3[(Legal Domains)]
    D4[(Feedback)]
    D5[(Progress)]

    %% Processes
    P1[1. Register User]
    P2[2. Play Scenario]
    P3[3. Generate Feedback]
    P4[4. Update Progress]

    %% Data Flows
    A -->|User Details| P1
    P1 -->|User Data| D1
    D1 -->|User Data| P2
    D3 -->|Legal Rules| P2
    D2 -->|Scenario Details| P2
    A -->|User Choice| P2
    P2 -->|Updated Scenario| D2
    D2 -->|Scenario Data| P3
    P3 -->|Feedback Data| D4
    D4 -->|Feedback Data| P4
    P4 -->|Progress Data| D5
    D5 -->|Progress Updates| A
    D4 -->|Feedback Details| A

    %% Styling
    classDef entity fill:#f9f,stroke:#333,stroke-width:2px
    classDef process fill:#bbf,stroke:#333,stroke-width:2px
    classDef datastore fill:#bfb,stroke:#333,stroke-width:2px
