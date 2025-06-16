``` mermaid
graph TD
    subgraph Réception / Stockage
        A1[Purée de fruits surgelée] --> B1(Froid négatif)
        A2[Jaune d'œuf en brique] --> B2(Froid positif)
        A3[Crème fraiche] --> B2
        A4[Sucre] --> B3(Température ambiante)
        A5[Lait] --> B3
        A6[Additifs alimentaires] --> B3
    end

    subgraph Assemblage
        B1 --> C1(Mélange)
        B2 -- Jaune d'oeuf, Crème fraiche --> C1
        B3 -- Sucre, Lait, Additifs --> C1
    end
    
    subgraph Techniques culinaires
        C1 --> D1{Pasteurisation basse 65°C : 30 min <br> ou Pasteurisation haute 82-83°C : à cœur}
        D1 --> D2(Refroidissement)
        D2 --> D3(Aromatisation)
        D3 --> D4(Maturation 6°C : 24h ou 4°C : 48h ou 2°C : 72h)
        D4 --> D5(Glaçage - Foisonnement)
        D5 --> D6(Remplissage et conditionnement)
    end

    D6 --> E1(Maintien au froid négatif <= -18°C)
    E1 --> F1(Remise au client)
```