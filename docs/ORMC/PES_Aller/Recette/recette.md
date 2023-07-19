# Recette
## Présentation 
>Les données à échanger entre ordonnateurs et HELIOS sont véhiculées sous forme de fichiers informatique.

>Un ordonnateur a le choix, pour effectuer la transmission et la réception de données et de documents électroniques, de recourir soit à un dispositif de transmission mis en œuvre par un opérateur «tiers de transmission», soit à la passerelle de transmission sécurisée d'Hélios. L'ordonnateur peut assumer directement la fonction de tiers de transmission en mettant en oeuvre un dispositif de transmission. Le recours à un dispositif de transmission par un tiers de transmission est recommandé dans la logique d'interopérabilité des échanges entre administrations.

>La description de l'infrastructure de transfert ainsi que la définition des canaux sont en dehors du cadre de ce document.

>Les fichiers échangés entre l'ordonnateur et HELIOS sont construits selon la syntaxe XML, selon des dispositions décrites dans ce document.

## Structure
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
        border: 1px solid #929292;
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
        margin: 0px 8px 8px 8px;
        border-left: solid 1px rgb(185, 185, 185);
        padding-left: 20px;
        display: flex;
        flex-direction: column;
    }

    .tree div:last-of-type {
        margin: 0px 8px 0px 8px;
    }
</style>

<div class="tree">
    <a href="#n:PES_Aller">n:PES_Aller</a>
    <div>
        <a href="#Enveloppe">Enveloppe</a>
        <div>
            <a href="#Parametres">Parametres</a>
            <div>
                <a href="#Version">Version</a>
                <a href="#TypFic">TypFic</a>
                <a href="#NomFic">NomFic</a>
            </div>
            <a href="#Emetteur">Emetteur</a>
            <div>
                <a href="#Sigle">Sigle</a>
                <a href="#Adresse">Adresse</a>
            </div>
            <a href="#Recepteur" title="facultatif">Recepteur</a>
            <div>
                <a href="#Sigle" title="facultatif">Sigle</a>
                <a href="#Adresse" title="facultatif">Adresse</a>
            </div>
        </div>
        <a href="#EnTetePES">EnTetePES</a>
        <div>
            <a href="#DteStr">DteStr</a>
            <a href="#IdPost">IdPost</a>
            <a href="#LibellePoste" title="facultatif">LibellePoste</a>
            <a href="#IdColl">IdColl</a>
            <a href="#FinJur" title="facultatif">FinJur</a>
            <a href="#CodCol">CodCol</a>
            <a href="#CodBud" title="facultatif">CodBud</a>
            <a href="#LibelleColBud" title="facultatif">LibelleColBud</a>
        </div>
        <a href="#PES_RecetteAller">PES_RecetteAller</a>
        <div>
            <a href="#EnTeteRecette">EnTeteRecette</a>
            <div>
                <a href="#IdVer">IdVer</a>
                <a href="#InfoDematerialisee" title="facultatif">InfoDematerialisee</a>
            </div>
            <a href="#Bordereau">Bordereau</a>
            <div>
                <a href="#BlocBordereau">BlocBordereau</a>
                <div>
                    <a href="#Exer">Exer</a>
                    <a href="#IdBord">IdBord</a>
                    <a href="#DteBordEm">DteBordEm</a>
                    <a href="#TypBord">TypBord</a>
                    <a href="#NbrPce">NbrPce</a>
                    <a href="#MtCumulAnnuel" title="facultatif">MtCumulAnnuel</a>
                    <a href="#MtBordHt">MtBordHt</a>
                    <a href="#MtBordTVA" title="facultatif">MtBordTVA</a>
                    <a href="#DteAsp" title="facultatif">DteAsp</a>
                    <a href="#Objet">Objet</a>
                </div>
                <a href="#Piece">Piece</a>
                <div>
                    <a href="#BlocPiece">BlocPiece</a>
                    <div>
                        <a href="#CodServ" title="facultatif">CodServ</a>
                        <a href="#Affect" title="facultatif">Affect</a>
                        <a href="#IdPce">IdPce</a>
                        <a href="#TypPce">TypPce</a>
                        <a href="#NatPce">NatPce</a>
                        <a href="#IdRol" title="facultatif">IdRol</a>
                        <a href="#DteAsp" title="facultatif">DteAsp</a>
                        <a href="#Edition" title="facultatif">Edition</a>
                        <a href="#ObjPce" title="facultatif">ObjPce</a>
                        <a href="#DebFact" title="facultatif">DebFact</a>
                        <a href="#FinFact" title="facultatif">FinFact</a>
                        <a href="#NumDette" title="facultatif">NumDette</a>
                        <a href="#Per" title="facultatif">Per</a>
                        <a href="#Cle1" title="facultatif">Cle1</a>
                        <a href="#Cle2" title="facultatif">Cle2</a>
                        <a href="#PJRef" title="facultatif">PJRef</a>
                        <a href="#NumeroFacture" title="facultatif">NumeroFacture</a>
                        <a href="#NumeroMarche" title="facultatif">NumeroMarche</a>
                        <a href="#NumeroEngagement" title="facultatif">NumeroEngagement</a>
                        <a href="#CodeService" title="facultatif">CodeService</a>
                        <a href="#NomService" title="facultatif">NomService</a>
                    </div>
                    <a href="#LigneDePiece">LigneDePiece</a>
                    <div>
                        <a href="#BlocLignePiece">BlocLignePiece</a>
                        <div>
                            <a href="#InfoLignePiece">InfoLignePiece</a>
                            <div>
                                <a href="#IdLigne">IdLigne</a>
                                <a href="#ObjLignePce" title="facultatif">ObjLignePce</a>
                                <a href="#CodProdLoc">CodProdLoc</a>
                                <a href="#FinGeo" title="facultatif">FinGeo</a>
                                <a href="#CodEtGeo" title="facultatif">CodEtGeo</a>
                                <a href="#Nature">Nature</a>
                                <a href="#Fonction" title="facultatif">Fonction</a>
                                <a href="#Operation" title="facultatif">Operation</a>
                                <a href="#TxTva" title="facultatif">TxTva</a>
                                <a href="#Majo">Majo</a>
                                <a href="#DteMajo" title="facultatif">DteMajo</a>
                                <a href="#TxMajo" title="facultatif">TxMajo</a>
                                <a href="#CpteTiers" title="facultatif">CpteTiers</a>
                                <a href="#TvaIntraCom">TvaIntraCom</a>
                                <a href="#TVAImportation" title="facultatif">TVAImportation</a>
                                <a href="#MtHT">MtHT</a>
                                <a href="#MtTVA" title="facultatif">MtTVA</a>
                                <a href="#MtNonMajo" title="facultatif">MtNonMajo</a>
                                <a href="#InfoCollBen" title="facultatif">InfoCollBen</a>
                                <a href="#PJRef" title="facultatif">PJRef</a>
                            </div>
                            <a href="#InfoPrelevement">InfoPrelevement</a>
                            <div>
                                <a href="#NatPrel">NatPrel</a>
                                <a href="#PerPrel">PerPrel</a>
                                <a href="#DtePrel">DtePrel</a>
                                <a href="#MtPrel">MtPrel</a>
                            </div>
                            <a href="#InfoPrelevementSEPA">InfoPrelevementSEPA</a>
                            <div>
                                <a href="#NatPrel">NatPrel</a>
                                <a href="#PerPrel">PerPrel</a>
                                <a href="#DtePrel">DtePrel</a>
                                <a href="#MtPrel">MtPrel</a>
                                <a href="#SequencePres">SequencePres</a>
                                <a href="#DateSignMandat">DateSignMandat</a>
                                <a href="#RefUniMdt">RefUniMdt</a>
                                <a href="#LibPrel" title="facultatif">LibPrel</a>
                                <a href="#AncienRUM" title="facultatif">AncienRUM</a>
                                <a href="#AncienICS" title="facultatif">AncienICS</a>
                                <a href="#AncienTiersCreancier" title="facultatif">AncienTiersCreancier</a>
                                <a href="#AncienneBanque" title="facultatif">AncienneBanque</a>
                                <a href="#AncienIBAN" title="facultatif">AncienIBAN</a>
                                <a href="#TitCpteDiff" title="facultatif">TitCpteDiff</a>
                            </div>
                            <a href="#InfoAssure" title="facultatif">InfoAssure</a>
                            <div>
                                <a href="#CodAssDeb">CodAssDeb</a>
                                <a href="#CodAyantDroit" title="facultatif">CodAyantDroit</a>
                            </div>
                            <a href="#RattachPiece" title="facultatif">RattachPiece</a>
                            <div>
                                <a href="#NatPceOrig">NatPceOrig</a>
                                <a href="#ExerRat">ExerRat</a>
                                <a href="#IdPceOrig">IdPceOrig</a>
                                <a href="#IdLigneOrig" title="facultatif">IdLigneOrig</a>
                            </div>
                            <a href="#LiensIdent" title="facultatif">LiensIdent</a>
                            <div>
                                <a href="#IdConv" title="facultatif">IdConv</a>
                                <a href="#IdMarche" title="facultatif">IdMarche</a>
                                <a href="#IdCaution" title="facultatif">IdCaution</a>
                                <a href="#IdEmprunt" title="facultatif">IdEmprunt</a>
                                <a href="#IdActif" title="facultatif">IdActif</a>
                                <a href="#IdRegie" title="facultatif">IdRegie</a>
                            </div>
                        </div>
                        <a href="#Tiers" title="facultatif">Tiers</a>
                        <div>
                            <a href="#InfoTiers">InfoTiers</a>
                            <div>
                                <a href="#IdTiers" title="facultatif">IdTiers</a>
                                <a href="#DteNaissance" title="facultatif">DteNaissance</a>
                                <a href="#NatIdTiers" title="facultatif">NatIdTiers</a>
                                <a href="#DteIdTiers" title="facultatif">DteIdTiers</a>
                                <a href="#RefTiers" title="facultatif">RefTiers</a>
                                <a href="#CatTiers">CatTiers</a>
                                <a href="#NatJur">NatJur</a>
                                <a href="#TypTiers">TypTiers</a>
                                <a href="#Civilite" title="facultatif">Civilite</a>
                                <a href="#Nom">Nom</a>
                                <a href="#ComplNom" title="facultatif">ComplNom</a>
                                <a href="#Prenom" title="facultatif">Prenom</a>
                                <a href="#LieuNaissance" title="facultatif">LieuNaissance</a>
                            </div>
                            <a href="#Adresse">Adresse</a>
                            <div>
                                <a href="#TypAdr">TypAdr</a>
                                <a href="#Adr1" title="facultatif">Adr1</a>
                                <a href="#Adr2">Adr2</a>
                                <a href="#Adr3" title="facultatif">Adr3</a>
                                <a href="#CP">CP</a>
                                <a href="#Ville">Ville</a>
                                <a href="#CodRes">CodRes</a>
                                <a href="#CodPays" title="facultatif">CodPays</a>
                                <a href="#DteAdr" title="facultatif">DteAdr</a>
                            </div>
                            <a href="#CpteBancaire" title="facultatif">CpteBancaire</a>
                            <div>
                                <a href="#IdPayInt">IdPayInt</a>
                                <a href="#IdBancInt" title="facultatif">IdBancInt</a>
                                <a href="#CodeEtab">CodeEtab</a>
                                <a href="#CodeGuic" title="facultatif">CodeGuic</a>
                                <a href="#IdCpte">IdCpte</a>
                                <a href="#CleRib">CleRib</a>
                                <a href="#BIC">BIC</a>
                                <a href="#IBAN" title="facultatif">IBAN</a>
                                <a href="#LibBanc" title="facultatif">LibBanc</a>
                                <a href="#TitCpte" title="facultatif">TitCpte</a>
                                <a href="#DteBanc" title="facultatif">DteBanc</a>
                            </div>
                        </div>
                        <a href="#Recouvrement" title="facultatif">Recouvrement</a>
                        <div>
                            <a href="#TypFlux">TypFlux</a>
                            <a href="#ModRegl">ModRegl</a>
                            <a href="#DteReco">DteReco</a>
                            <a href="#IdEncaissement">IdEncaissement</a>
                            <a href="#MtReco">MtReco</a>
                        </div>
                    </div>
                </div>
                <a href="#PESSignatureGroup" title="facultatif">PESSignatureGroup</a>
                <div>
                </div>
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
    <p class="fisrt admonition-title">Warning</p>
    <p class="last">Warning message</p>
</div>
<div class="admonition error">
    <p class="fisrt admonition-title">Error</p>
    <p class="last">Error message</p>
</div>
<div class="admonition note">
    <p class="fisrt admonition-title">Note</p>
    <p class="last">Note message</p>
</div>