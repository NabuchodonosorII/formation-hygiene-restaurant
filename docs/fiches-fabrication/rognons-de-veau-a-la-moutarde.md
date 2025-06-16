``` mermaid
graph TD
    subgraph Réception / Stockage
        A1[Moutarde pot entamé] --> B1(Froid positif)
        A2[Crème fraiche] --> B1
        A3[Beurre] --> B1
        A4[Rognons de veau frais] --> B1
        A5[Assaisonnement] --> B2(Température ambiante)
        A6[Vin] --> B2
        A7[Huile] --> B2
    end

    subgraph Mise en place
        B1 -- Rognons --> C1(Lavage)
        C1 --> C2(Dégraissage)
    end

    subgraph Techniques culinaires
        C2 --> D1(Rissolage)
        B2 -- Huile --> D1
        D1 --> D2(Egouttage)
        D2 --> D3(Déglaçage)
        B2 -- Vin --> D3
        D3 --> D4(Mélange)
        B1 -- Moutarde, Crème fraiche, Beurre --> D4
        B2 -- Assaisonnement --> D4
        D4 --> D5(Cuisson)
    end
    
    D5 --> E1(Remise au client)
```