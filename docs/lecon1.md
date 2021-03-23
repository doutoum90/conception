# I- MERISE
## A-Introduction
MERISE est une méthode de conception, de développement et de réalisation de projets informatiques. Elle sépare les données des traitements afin de s'assurer qu'il n'y ai pas des données superflues.

![](../images/MERISE.jpeg)
## C- Le schéma directeur
- objectifs
- stratégie
## D- L'étude préalable

- besoins macro
- les attentes
- traitements
## E- L'étude détaillée
- besoins micro
- les attentes
- traitements
## F- Merise en entreprise
Merise est systémique (vue système)
**Système d'information vs Système d'information informatisée**

```mermaid
graph TD
A[Sous-syteme de Pilotage] --> B[Sous-syteme de d'information]
B --> A
B--> C[Sous-syteme operant]
C --> B
```
- Sous-syteme de Pilotage: reflexion, decision, controle.
- Sous-syteme de d'information: production, memorisation,comm, traitement ....
- Sous-syteme operant : transformation.

**Système d'information vs Système d'information informatisée**
```mermaid
graph LR
A[SI Actuel] -- Merise --> B[SII]
```


**Système d'information informatisée vs Système d'information Organisationnel**
```mermaid
    graph TB
    A[Système d'information informatisée]
    subgraph Système d'information Organisationnel
    A
    end
```

**Séparation données et traitement**
```mermaid
graph TB
    A((SII && SIO))-->B((Données))
    A-->C((Traitement))
    B-->D((Sortie))
    C-->D
    subgraph SIO
        B
        C
    end
```

**Approche par niveau**

```mermaid
    graph TB
    A((SI))--> B[Niveau Conceptuel]
    B-->C[Niveau Organisationnel]
    C-->D[Niveau Logique]
    D-->E[Niveau Physique]

    subgraph SIO
        B
        C
    end

    subgraph SII
     D
     E
    end
```
## B- Cycle d'abstraction (Modelisation)

<table>
    <thead>
        <tr>
            <th>Niveau</th>
            <th>Données</th>
            <th>Traitement</th>
            <th>Domaine</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Niveau Conceptuel</td>
            <td>MCD</td>
            <td>MCT</td>
            <td rowspan=2>SIO</td>
        </tr>
        <tr>
            <td>Niveau Organisationnel</td>
            <td>MOD</td>
            <td>MOT</td>
        </tr>
        <tr>
            <td>Niveau Logique </td>
            <td>MLD</td>
            <td>MLT</td>
            <td rowspan=2>SII</td>
        </tr>
        <tr>
            <td>Niveau Physique</td>
            <td>MPD</td>
            <td>MPT</td>
        </tr>
    </tbody>
</table>



