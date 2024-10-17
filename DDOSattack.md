```mermaid
sequenceDiagram
    participant A as Attacker
    participant B as Bots
    participant S as Server
    participant D as Defense

    A->>B: Send attack command
    B->>S: Start attack
    S->>D: Detect attack
    D->>S: Trigger defenses
    D->>B: Block malicious traffic
    S->>D: Report ongoing attack
    D->>S: Mitigate threat
    S-->>B: Drop attack packets

```

## Documentation
First the attacker bends the commands to the Bots.
Which then starts the attack by sending it to the server.
The defense then detects the attack and triggers the dense systems.
The defense blocks all the malicious traffic from the bots.
The Server reports the attacks to the defense and the defense mitigates the threat. The Server may drop attack packets back to the bots.
