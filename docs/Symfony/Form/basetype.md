# Options Hérité

## Attr
**Nom de champ:** 'attr'<br>
**Type:** *array*<br>
**Valeur par défaut:** `[]`<br>
**Description:**
> Si vous souhaitez ajouter des attributs supplémentaires à une représentation de champ HTML, vous pouvez utiliser l'option `attr`. C'est un tableau associatif avec des attributs HTML comme clés. Cela peut être utile lorsque vous devez définir une classe personnalisée pour un widget

**Exemple:**
```
$builder->add('input', TextareaType::class, [
    'attr' => ['class' => 'myclass'],
]);
```
<a href="#" class="btn btn-neutral float-right">Retour au menu</a>

## AutoInitialize
**Nom de champ:** 'auto_initialize'<br>
**Type:** *boolean*<br>
**Valeur par défaut:** `true`<br>
**Description:**
> Une option interne : définit si le formulaire doit être initialisé automatiquement. Pour tous les champs, cette option ne devrait être que `true` pour les formulaires racine. Vous n'aurez pas besoin de modifier cette option et vous n'aurez probablement pas à vous en soucier.

**Exemple:**
```
$builder->add('input', TextareaType::class, [
    'auto-initialize' => true,
]);
```
<a href="#" class="btn btn-neutral float-right">Retour au menu</a>

## BlockName
**Nom de champ:** 'block_name'<br>
**Type:** *string*<br>
**Valeur par défaut:** `null`<br>
**Description:**
> Vous permet d'ajouter un nom de bloc personnalisé à ceux utilisés par défaut pour rendre le type de formulaire. Utile par exemple si vous avez plusieurs instances du même formulaire et que vous avez besoin de personnaliser le rendu des formulaires individuellement.
>
>Si vous définissez par exemple cette option sur `my_custom_name` et que le champ est de type `text`, Symfony utilisera les noms suivants (et dans cet ordre) pour trouver le bloc utilisé pour rendre le widget du champ : `_my_custom_name_widget`, `text_widget` et `form_widget`.

**Exemple:**
```
$builder->add('input', TextareaType::class, [
    'block_name' => "blockName",
]);
```
<a href="#" class="btn btn-neutral float-right">Retour au menu</a>
