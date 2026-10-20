```mermaid
graph TD
    %% Akteure und Prozessschritte
    A([Start: Presales erstellt Opportunity]) --> B[Erarbeitung Lösungskonzept]
    
    %% Abstimmung Fachabteilung
    B --> C{Service-Spezifikation}
    C --> D[Zuständige Fachabteilung einbinden]
    D --> E{Approval Fachabteilung?}
    E -- Anpassung nötig --> B
    E -- Approved --> F[Erstellung Angebotsdesign]
    
    %% Ressourcenfreigabe
    F --> G[Prüfung durch Manager Fachabteilungen & Projektmanagement]
    G --> H{Ressourcen-Approval erteilt?}
    H -- Anpassung nötig --> F
    H -- Approved --> I[Finales Angebot an Kunden versenden]
    
    %% Abschluss und Übergabe
    I --> J{Vertrag unterschrieben?}
    J -- Abgelehnt / On Hold --> K([Ende: Opportunity verloren])
    J -- Unterschrieben --> L[Planung durch Projektmanagement]
    L --> M([Ende: Projektauftakt])
    
    %% Styling im CANCOM Corporate Design (Rot & Grautöne)
    classDef default fill:#ffffff,stroke:#4a4a4a,stroke-width:1px,color:#333333;
    classDef cancomRed fill:#ffffff,stroke:#DA002D,stroke-width:2px,color:#DA002D;
    classDef cancomSolid fill:#DA002D,stroke:#DA002D,stroke-width:2px,color:#ffffff;
    classDef grayBox fill:#f5f5f5,stroke:#a7a7a7,stroke-width:2px,color:#333333;
    
    %% Zuweisung der Stile
    class A,M cancomSolid;
    class K grayBox;
    class B,D,F,G,L default;
    class C,E,H,J cancomRed;
    class I cancomSolid;

    %% Linienfarbe anpassen
    linkStyle default stroke:#DA002D,stroke-width:2px,color:#333333;
