# Recette
## Présentation 
Les données à échanger entre ordonnateurs et HELIOS sont véhiculées sous forme de fichiers informatique.

Un ordonnateur a le choix, pour effectuer la transmission et la réception de données et de documents électroniques, de recourir soit à un dispositif de transmission mis en œuvre par un opérateur «tiers de transmission», soit à la passerelle de transmission sécurisée d'Hélios. L'ordonnateur peut assumer directement la fonction de tiers de transmission en mettant en oeuvre un dispositif de transmission. Le recours à un dispositif de transmission par un tiers de transmission est recommandé dans la logique d'interopérabilité des échanges entre administrations.

La description de l'infrastructure de transfert ainsi que la définition des canaux sont en dehors du cadre de ce document.

Les fichiers échangés entre l'ordonnateur et HELIOS sont construits selon la syntaxe XML, selon des dispositions décrites dans ce document.

## Structure
- `<n:PES_Aller>`
{!docs/ORMC/PES_Aller//enveloppe.md!}
{!docs/ORMC/PES_Aller//entetepes.md!}


<style>
    .tree a {
        color: #E74C3C;
        text-decoration: none;
        padding: 2px 6px;
        font-family: SFMono-Regular, Menlo, Monaco, Consolas, Liberation Mono, Courier New, Courier, monospace;
        width: fit-content;
        background: #fff;
        border: 1px solid #c2c2c2;
        font-size: 75%;
        margin: 0 0 8px 0;
        display: inline-block;
    }

    .tree a[title="facultatif"] {
        border-style: dashed;
        border-color: #bdbdbd;
        background: #fafafa;
    }


    .tree div a:last-child {
        margin: 0;
        display: inline-block;
    }

    .tree div:first-child {
        padding-bottom: 8px;
    }

    .tree a:hover {
        color: #e77a6e;
        text-decoration: none;
    }

    .tree a::before {
        content: "<";
    }

    .tree a::after {
        content: ">";
    }

    .tree div {
        margin: 0px 8px 0px 8px;
        border-left: solid 1px rgb(185, 185, 185);
        padding-left: 20px;
        display: flex;
        flex-direction: column;
    }
</style>

<div class="tree">
    <a href="#">n:PES_Aller</a>
    <div>
        <a href="#">Enveloppe</a>
        <div>
            <a href="#">Parametres</a>
            <div>
                <a href="#">Version</a>
                <a href="#">TypFic</a>
                <a href="#">NomFic</a>
            </div>
            <a href="#">Emetteur</a>
            <div>
                <a href="#">Sigle</a>
                <a href="#">Adresse</a>
            </div>
            <a href="#" title="facultatif">Recepteur</a>
            <div>
                <a href="#" title="facultatif">Sigle</a>
                <a href="#" title="facultatif">Adresse</a>
            </div>
        </div>
        <a href="#">EnTetePES</a>
        <div>
            <a href="#">DteStr</a>
            <a href="#">IdPost</a>
            <a href="#" title="facultatif">LibellePoste</a>
            <a href="#">IdColl</a>
            <a href="#" title="facultatif">FinnJur</a>
            <a href="#">CodCol</a>
            <a href="#" title="facultatif">CodBud</a>
            <a href="#" title="facultatif">LibelleColBud</a>
        </div>
        <a href="#">PES_RecetteAller</a>
        <div>
            <a href="#">EnTeteRecette</a>
            <div>
                <a href="#">IdVer</a>
                <a href="#" title="facultatif">InfoDematerialisee</a>
            </div>
            <a href="#">Bordereau</a>
            <div>
                <a href="#">BlocBordereau</a>
                <a href="#">Piece</a>
                <a href="#" title="facultatif">PESSignatureGroup</a>
            </div>
        </div>
    </div>
</div>


## Balise
### EnTeteRecette
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