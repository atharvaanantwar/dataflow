Level 1
```mermaid

graph TD
    A[User]
    D1[(Users)]
    D2[(Scenarios)]
    D3[(Legal Rules)]
    D4[(Feedback)]
    D5[(Progress)]
    P1[1. Register User]
    P2[2. Play Legal Scenario]
    P3[3. Evaluate Legal Choices]
    P4[4. Update User Progress]
    A -->|User Credentials| P1
    P1 -->|User Profile| D1
    D1 -->|User Profile| P2
    D3 -->|Legal Rules| P2
    D2 -->|Scenario Content| P2
    A -->|Scenario Choices| P2
    P2 -->|User Choices| P3
    D2 -->|Scenario Content| P3
    D3 -->|Legal Rules| P3
    P3 -->|Feedback Results| D4
    D4 -->|Feedback Results| P4
    D4 -->|Feedback Summary| A
    P4 -->|Progress Data| D5
    D5 -->|Progress Summary| A




    P2.3 -->|User Choices| P2
