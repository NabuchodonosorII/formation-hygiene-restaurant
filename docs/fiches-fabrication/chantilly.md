``` mermaid
graph TD
    subgraph Réception / Stockage
        A1[Crème fraiche liquide +30% M.G.] --> B1(Froid positif)
        A2[Gousses de vanille] --> B2(Température ambiante)
        A3[Sucre] --> B2
    end

    subgraph Mise en place
        B2 -- Vanille --> C1(Extraction des graines)
    end

    subgraph Techniques culinaires
        B1 --> D1(Mélange)
        C1 --> D1
        B2 -- Sucre --> D1
        D1 --> D2(Incorporation dans le siphon)
        D2 --> D3(Maintien au froid)
    end

    D3 --> E1(Utilisation)
```