``` mermaid
graph TD
    subgraph Réception / Stockage
        A1[Beurre] --> B1(Froid positif)
        A2[Œufs coquilles] --> B1
        A3[Lait entamé] --> B1
        A4[Assaisonnements] --> B2(Température ambiante)
    end
    
    subgraph Mise en place
        B1 -- Œufs --> C1(Cassage)
    end

    subgraph Assemblage
        C1 --> D1(Mélange)
        B1 -- Lait --> D1
        B2 -- Assaisonnements --> D1
    end

    subgraph Cuisson
        D1 --> E1(Cuisson)
        B1 -- Beurre --> E1
    end
    
    E1 --> F1(Remise au client)
```