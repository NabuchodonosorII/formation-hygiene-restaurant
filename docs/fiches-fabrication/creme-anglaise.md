``` mermaid
graph TD
    subgraph Réception / Stockage
        A1[Œufs] --> B1(Froid positif)
        A2[Sucre] --> B2(Température ambiante)
        A3[Lait] --> B2
        A4[Gousses de vanille] --> B2
    end
    
    subgraph Mise en place
        B1 -- Oeufs --> C1(Cassage)
        C1 --> C2(Clarification)
        C2 --> C3(Réservation des jaunes)
        C3 --> D1(Blanchiment)
        B2 -- Sucre --> D1
        
        B2 -- Vanille --> C4(Extraction des graines)
    end

    subgraph Assemblage et Cuisson
        B2 -- Lait --> E1(Ebullition)
        C4 --> E1
        
        E1 --> E2(Mélange)
        D1 --> E2
        
        E2 --> E3(Cuisson 85°C à coeur ou 1 min 30 minimum à 83°C à coeur)
        E3 --> E4(Refroidissement)
    end

    E4 --> F1(Maintien au froid)
    F1 --> G1(Utilisation)
```