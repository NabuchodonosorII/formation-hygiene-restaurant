``` mermaid
graph TD
    subgraph Réception / Stockage
        A1[Jambon tranché] --> B1(Froid positif)
        A2[Fromage râpé] --> B1
        A3[Œufs] --> B1
        A4[Sel] --> B2(Température ambiante)
        A5[Eau] --> B2
        A6[Farine de Sarrazin] --> B2
        A7[Huile] --> B2
    end

    subgraph Pâte à galette
        B2 -- Sel, Eau, Farine --> C1(Mélange)
        C1 --> C2(Cuisson)
        B2 -- Huile --> C2
        C2 --> C3(Refroidissement)
        C3 --> C4(Maintien au froid éventuel)
    end

    subgraph Assemblage
        C4 --> D1(Assemblage)
        B1 -- Jambon --> D1
        B1 -- Fromage râpé --> D1
        B1 -- Œufs --> D2(Cassage)
        D2 --> D1
    end

    subgraph Finition
        D1 --> E1(Cuisson / réchauffage)
    end

    E1 --> F1(Remise au client)
```