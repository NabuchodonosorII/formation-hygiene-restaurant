``` mermaid
graph TD
    subgraph Réception / Stockage
        A1[Gélatine] --> B1(Température ambiante)
        A2[Eau] --> B1
        A3[Carottes, céleri, poireaux, frais] --> B1
        A4[Bouquet garni] --> B1
        A5[Gîte et jarret] --> B2(Froid positif)
        A6[Os cassés] --> B2
        A7[Pieds de veau] --> B2
        A8[Blanc d'œuf en bric, maigre de bœuf haché] --> B2
    end

    subgraph Mise en place
        B1 -- Carottes, etc. --> C1(Epluchage)
        C1 --> C2(Lavage/égouttage)
        C2 --> C3(Découpe)
        B2 -- Gîte et jarret --> C4(Parage)
        B2 -- Os cassés --> C5(Dégorger / Egouttage)
        B2 -- Pieds de veau --> C6(Parage / lavage)
    end

    subgraph Techniques culinaires
        B1 -- Eau --> D1(Ebullition 100°C : 2 h)
        C3 --> D1
        C4 --> D1
        C5 --> D1
        C6 --> D1
        D1 --> D2(Ecumage / Dégraissage)
        D2 --> D3(Mélange)
        B1 -- Bouquet garni --> D3
        B2 -- Blanc d'oeuf, etc. --> D3
        A1 -- Gélatine --> D3
        D3 --> D4(Ebullition 90°C : 20 min / filtration chinois)
        D4 --> D5(Refroidissement)
        D5 --> D6(Maintien au froid)
        D6 --> D7(Utilisation)
    end
```