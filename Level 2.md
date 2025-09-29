# level 2
```mermaid
graph TD
    A[User]
    D1[(Users)]
    D2[(Scenarios)]
    D3[(Legal Rules)]
    P2.1[2.1 Select Scenario]
    P2.2[2.2 Present Scenario]
    P2.3[2.3 Capture User Choices]
    D1 -->|User Profile| P2.1
    D2 -->|Available Scenarios| P2.1
    P2.1 -->|Selected Scenario| P2.2
    D3 -->|Legal Rules| P2.2
    P2.2 -->|Scenario Content| A
    A -->|Scenario Choices| P2.3
