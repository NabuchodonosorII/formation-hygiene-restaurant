``` mermaid
graph TD
    subgraph Réception / Stockage
        A1[Vin blanc, Eau] --> B1(Température ambiante)
        A2[Bouquet garni, Assaisonnements] --> B1
        A3[Echalotes, Oignons] --> B1
        A4[Arêtes et têtes de poissons] --> B2(Froid positif)
        A5[Carottes, poireaux, frais] --> B2
        A6[Beurre] --> B2
    end

    subgraph Mise en place
        B1 -- Echalotes, Oignons --> C1(Epluchage)
        C1 --> C2(Découpe)
        B2 -- Arêtes et têtes --> C3(Concassage)
        B2 -- Carottes, poireaux --> C4(Epluchage)
        C4 --> C5(Lavage/égouttage)
        C5 --> C6(Découpe)
    end

    subgraph Techniques culinaires
        B2 -- Beurre --> D1(Faire suer)
        C2 --> D1
        C3 --> D1
        C6 --> D1
        D1 --> D2(Ebullition +90°C : 20 min)
        B1 -- Vin blanc, Eau, Bouquet garni, Assaisonnements --> D2
        D2 --> D3(Filtrage au chinois)
        D3 --> D4(Refroidissement)
        D4 --> D5(Maintien au froid)
        D5 --> D6(Utilisation)
    end
```