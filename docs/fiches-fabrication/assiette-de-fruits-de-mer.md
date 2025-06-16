``` mermaid
graph TD
    subgraph Réception / Stockage
        A1[Eléments de décor. algues...] --> B1(Froid positif)
        A2[Citrons] --> B1
        A3[Mayonnaise] --> B1
        A4[Palourdes, Praires, Huitres, fraiches] --> B1
        A5[Bigorneaux, moules, frais] --> B1
        A6[Tourteau frais] --> B1
        A7[Langoustines, crevettes, surgelées] --> B2(Froid négatif)
    end

    subgraph Mise en place
        B1 -- Eléments de décor --> C1(Lavage)
        B1 -- Citrons --> C2(Lavage)
        C2 --> C3(Tranchage)
        B1 -- Palourdes, etc. --> C4(Lavage)
        C4 --> C5(Ouverture)
        B1 -- Bigorneaux, etc. --> C6(Lavage)
        B2 -- Langoustines, etc. --> C7(Décongélation)
    end

    subgraph Techniques culinaires
        C6 --> D1(Cuisson 90-100°C : 3 min)
        B1 -- Tourteau --> D2(Cuisson 90-100°C : 15-20 min)
        C7 --> D3(Cuisson 90-100°C : 3 min)
        D1 --> D4(Refroidissement)
        D2 --> D4
        D3 --> D4
        D4 --> D5(Maintien en température < 3°C)
        D5 --> D6(Découpe)
    end

    subgraph Assemblage
        C1 --> E1(Assemblage)
        C3 --> E1
        B1 -- Mayonnaise cf. fiche mayonnaise --> E1
        C5 --> E1
        D6 --> E1
    end

    E1 --> F1(Remise au client)
```