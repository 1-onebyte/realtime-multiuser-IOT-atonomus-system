graph TD

%% ================= EDGE LAYER =================
subgraph Edge Layer (Factory Floor)
    S1[Primary Sensor]
    S2[Backup Sensor]
    S3[Load / Stress Sensor]

    ESP[ESP32 Controller\n(Self-Healing Logic)]
    
    LED1[Green LED\nNormal Mode]
    LED2[Yellow LED\nBackup Active]
    LED3[Red LED\nSafe Mode]
    LED4[Blue LED\nAutonomous Mode]
end

S1 --> ESP
S2 --> ESP
S3 --> ESP

ESP --> LED1
ESP --> LED2
ESP --> LED3
ESP --> LED4

%% ================= LOGIC =================
subgraph Decision Engine (Inside ESP32)
    D1[Sensor Health Monitoring]
    D2[Automatic Failover]
    D3[Overload Detection]
    D4[Safe Mode Controller]
    D5[Local Autonomous Control]
end

ESP --> D1
D1 --> D2
D1 --> D3
D3 --> D4
D2 --> D5

%% ================= CLOUD =================
subgraph Cloud Layer
    FB[(Firebase Realtime Database)]
end

ESP -->|JSON Telemetry| FB

%% ================= FRONTEND =================
subgraph Application Layer (Multi-User)
    DASH[Web Dashboard\n(GitHub Pages)]
    USERS[Multiple Users\nJudges / Operators]
end

FB --> DASH
DASH --> USERS

%% ================= FLOW NOTES =================
ESP -.->|Cloud Down| D5
