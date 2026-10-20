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
    
    %% Styling (ohne Raute-Zeichen um Kopierfehler zu vermeiden)
    classDef default fill:white,stroke:dimgray,stroke-width:1px,color:black;
    classDef cancomRed fill:white,stroke:crimson,stroke-width:2px,color:crimson;
    classDef cancomSolid fill:crimson,stroke:crimson,stroke-width:2px,color:white;
    classDef grayBox fill:whitesmoke,stroke:darkgray,stroke-width:2px,color:black;
    
    %% Zuweisung der Stile
    class A,M cancomSolid;
    class K grayBox;
    class B,D,F,G,L default;
    class C,E,H,J cancomRed;
    class I cancomSolid;

    %% Linienfarbe anpassen
    linkStyle default stroke:crimson,stroke-width:2px,color:black;
