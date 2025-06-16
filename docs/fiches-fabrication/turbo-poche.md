``` mermaid
graph TD
    subgraph Réception / Stockage
        A1[Sauce hollandaise] --> B1(Froid positif)
        A2[Citron entier] --> B1
        A3[Lait frais] --> B1
        A4[Turbot entier] --> B1
        A5[Assaisonnement, eau] --> B2(Température ambiante)
    end

    subgraph Mise en place
        B1 -- Citron --> C1(Lavage)
        C1 --> C2(Tranchage)
        B1 -- Lait --> C3(Ebullition)
        C3 --> C4(Refroidissement)
        B1 -- Turbot --> C5(Rinçage)
        C5 --> C6(Habillage)
        C6 --> C7(Lavage / égouttage)
        C7 --> C8(Découpe)
    end

    subgraph Cuisson
        C8 --> D1(Ebullition 80°C : 15 min)
        B2 -- Assaisonnement, eau --> D1
        C4 --> D1
        D1 --> D2(Egouttage)
    end

    subgraph Assemblage
        D2 --> E1(Assemblage)
        B1 -- Sauce hollandaise --> E1
        C2 --> E1
    end

    E1 --> F1(Remise au client immédiate)
```