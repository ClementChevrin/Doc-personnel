# Recette
- `<n:PES_Aller>`
{!docs/ORMC/PES_Aller/enveloppe.md!}
{!docs/ORMC/PES_Aller/entetepes.md!}

<a style="background-color:#404040;color:white;border: 1px solid transparent;padding: 0.375rem 0.75rem;font-size: 1rem;line-height: 1.5;border-radius: 0.25rem;" href="#recette">Strucure</a>


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

<style>
    .tree a {
        color: #E74C3C;
        text-decoration: none;
        padding: 2px 6px;
        font-family: SFMono-Regular, Menlo, Monaco, Consolas, Liberation Mono, Courier New, Courier, monospace;
        max-width: 100%;
        background: #fff;
        border: 1px solid #c2c2c2;
        font-size: 75%;
        margin: 8px 0;
        display: inline-block;
    }

    .tree a[title="facultatif"] {
        border-style: dashed;
        border-color: #bdbdbd;
        background: #fafafa;
    }


    .tree div a:first-child {
        margin: 0 0 8px 0;
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
            </div>
            <div>
                <a href="#">TypFic</a>
            </div>
            <div>
                <a href="#">NomFic</a>
            </div>
        </div>
        <div>
            <a href="#">Emetteur</a>
            <div>
                <a href="#">Sigle</a>
            </div>
            <div>
                <a href="#">Adresse</a>
            </div>
        </div>
        <div>
            <a href="#" title="facultatif">Recepteur</a>
            <div>
                <a href="#" title="facultatif">Sigle</a>
            </div>
            <div>
                <a href="#" title="facultatif">Adresse</a>
            </div>
        </div>
    </div>
    <div>
        <a href="#">EnTetePES</a>
        <div>
            <a href="#">DteStr</a>
        </div>
        <div>
            <a href="#">IdPost</a>
        </div>
        <div>
            <a href="#" title="facultatif">LibellePoste</a>
        </div>
        <div>
            <a href="#">IdColl</a>
        </div>
        <div>
            <a href="#" title="facultatif">FinnJur</a>
        </div>
        <div>
            <a href="#">CodCol</a>
        </div>
        <div>
            <a href="#" title="facultatif">CodBud</a>
        </div>
        <div>
            <a href="#" title="facultatif">LibelleColBud</a>
        </div>
    </div>
    <div>
        <a href="#">PES_RecetteAller</a>
        <div>
            <a href="#">EnTeteRecette</a>
            <div>
                <a href="#">IdVer</a>
            </div>
            <div>
                <a href="#" title="facultatif">InfoDematerialisee</a>
            </div>
        </div>
        <div>
            <a href="#">Bordereau</a>
            <div>
                <a href="#">BlocBordereau</a>
            </div>
            <div>
                <a href="#">Piece</a>
            </div>
            <div>
                <a href="#" title="facultatif">PESSignatureGroup</a>
            </div>
        </div>
    </div>
</div>