``` mermaid
graph TD
    subgraph Réception / Stockage
        A1[Pâte brisée] --> B1(Froid positif)
        A2[Fraises] --> B1
        A3[Œufs coquilles] --> B1
        A4[Sucre] --> B2(Température ambiante)
        A5[Gousse de vanille] --> B2
        A6[Lait UHT non entamé] --> B2
        A7[Farine] --> B2
    end

    subgraph Crème pâtissière
        B2 -- Vanille --> C1(Extraction des graines)
        B2 -- Lait --> C2(Ebullition)
        C1 --> C2
        
        B1 -- Oeufs --> C3(Cassage)
        C3 --> C4(Clarification)
        C4 --> C5(Réservation des jaunes)
        C5 --> C6(Blanchiment)
        B2 -- Sucre --> C6
        
        C2 --> C7(Mélange crème pâtissière)
        C6 --> C7
        B2 -- Farine --> C7
        C7 --> C8(Cuisson 100°C : 2 min)
        C8 --> C9(Refroidissement)
    end

    subgraph Fond de tarte
        B1 -- Pâte cf. fiche pâte feuilletée --> D1(Façonnage)
        D1 --> D2(Cuisson 100°C : 25 min)
        D2 --> D3(Refroidissement)
    end

    subgraph Mise en place Fraises
        B1 -- Fraises --> E1(Lavage / égouttage)
        E1 --> E2(Découpe)
    end

    subgraph Assemblage
        C9 --> F1(Assemblage)
        D3 --> F1
        E2 --> F1
    end
    
    F1 --> G1(Maintien au froid)
    G1 --> H1(Remise au client)
```