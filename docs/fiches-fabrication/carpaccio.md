``` mermaid
graph TD
    subgraph Réception / Stockage
        A1[Huile] --> B1(Température ambiante)
        A2[Assaisonnements] --> B1
        A3[Citron] --> B2(Froid positif)
        A4[Poivrons] --> B2
        A5[Filet ou rond de gîte de bœuf frais] --> B2
    end

    subgraph Mise en place
        B2 -- Citron --> C1(Lavage/égouttage)
        C1 --> C2(Découpe)
        B2 -- Poivrons --> C3(Lavage/égouttage)
        C3 --> C4(Elimination des pédoncules et graines)
        C4 --> C5(Tranchage fin)
        B2 -- Filet de boeuf --> C6(Parage)
        C6 --> C7(Portionnement)
    end

    subgraph Techniques culinaires
        B1 -- Huile, Assaisonnements --> D1(Fabrication marinade)
        C2 --> D1
    end
    
    subgraph Assemblage
        D1 --> E1(Assemblage)
        C5 --> E1
    end

    subgraph Dressage
        C7 --> F1(Dressage)
        E1 --> F1
    end
    
    F1 --> G1(Remise au client immédiate)
```