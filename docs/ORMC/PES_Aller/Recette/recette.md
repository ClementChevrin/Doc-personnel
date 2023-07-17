# Recette
- `<n:PES_Aller>`
{!docs/ORMC/PES_Aller/enveloppe.md!}
{!docs/ORMC/PES_Aller/entetepes.md!}

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>


# Recette

## EnTeteRecette
### idVer
**Cardinalité**: 1-1<br>
**Description**:	N° de version du PES recette. – Mettre à « 2 ». A défaut rejet du flux.

### infoDematerialisee
**Cardinalité**: 0-1<br>
**Description**:	Précise si les blocs recette véhiculent des bordereaux & mandats dématérialisées (1) ou non (0).
La valeur (0) n'empêche pas de communiquer des pièces justificatives dématérialisées et leurs références (PJRef)
Si non présent considéré à '0'
La valeur 1 ne peut être autorisée qu'avec une signature électronique. Si valeur= 1 et absence de signature électronique, rejet du flux.
La valeur 0 et la présence d'une signature électronique aboutissent au rejet du flux.

<div class="admonition attention">
    <p class="fisrt admonition-title">Attention</p>
    <p class="last">Test</p>
</div>