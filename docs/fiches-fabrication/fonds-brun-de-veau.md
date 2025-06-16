``` mermaid
graph TD
    subgraph Réception / Stockage
        A1[Eau, Assaisonnements] --> B1(Température ambiante)
        A2[Plantes aromatiques] --> B1
        A3[Oignons frais] --> B2(Froid positif)
        A4[Os, crosse, jarrets, pieds, <br> morceaux de 2e et 3e <br> catégories de veau] --> B2
        A5[Carottes, poireaux frais] --> B2
        A6[Tomates fraiches] --> B2
    end

    subgraph Mise en place
        B1 -- Plantes aromatiques --> C1(Lavage / égouttage)
        C1 --> C2(Fabrication bouquet garni)
        B2 -- Oignons frais --> C3(Epluchage)
        C3 --> C4(Découpe)
        B2 -- Os, etc. --> C5(Parage)
        C5 --> C6(Concassage)
        B2 -- Carottes, poireaux --> C7(Epluchage)
        C7 --> C8(Lavage / égouttage)
        C8 --> C9(Découpe)
        B2 -- Tomates fraiches --> C10(Lavage / égouttage)
        C10 --> C11(Découpe)
    end

    subgraph Techniques culinaires
        C6 --> D1(Rissolage)
        C4 --> D1
        C9 --> D1
        D1 --> D2(Déglaçage)
        D2 --> D3(Ebullition + de 90-100°C : 4-5h et écumage)
        B1 -- Eau, Assaisonnements --> D3
        C2 --> D3
        C11 --> D3
        D3 --> D4(Filtrage au chinois)
        D4 --> D5(Refroidissement et dégraissage)
        D5 --> D6(Maintien au froid)
        D6 --> D7(Utilisation)
    end
```