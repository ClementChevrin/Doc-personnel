{!docs/ORMC/PES_Aller/enveloppe.md!}
{!docs/ORMC/PES_Aller/entetepes.md!}

# Recette

## EnTeteRecette
### idVer
`Cardinalité`: 1-1
`Description`:	N° de version du PES recette. – Mettre à « 2 ». A défaut rejet du flux.
### nfoDematerialisee
`Cardinalité`: 0-1
`Description`:	Précise si les blocs recette véhiculent des bordereaux & mandats dématérialisées (1) ou non (0).
La valeur (0) n'empêche pas de communiquer des pièces justificatives dématérialisées et leurs références (PJRef)
Si non présent considéré à '0'
La valeur 1 ne peut être autorisée qu'avec une signature électronique. Si valeur= 1 et absence de signature électronique, rejet du flux.
La valeur 0 et la présence d'une signature électronique aboutissent au rejet du flux.

<div class="admonition attention">
    <p class="fisrt admonition-title">Attention</p>
    <p class="last">Test</p>
</div>