graph TD
    subgraph Réception / Stockage
        A1[Alcool, Assaisonnement] --> B1(Température ambiante)
        A2[Foie gras entier frais] --> B2(Froid positif)
    end

    subgraph Mise en place
        B2 --> C1(Dénerbage)
    end

    subgraph Techniques culinaires
        C1 --> D1(Mélange)
        A1 --> D1
        D1 --> D2(Maintien en température (< 3°C))
        D2 --> D3(Assemblage)
        D3 --> D4(Cuisson en terrine)
        D4 --> D5(Pressage)
        D5 --> D6(Refroidissement)
    end