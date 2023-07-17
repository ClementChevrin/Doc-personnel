# Options Hérité

## Attr
**Nom de champ:** 'attr'<br>
**Type:** *array*<br>
**Valeur par défaut:** `[]`<br>
**Documentation officiel:** [Symfony Docs](https://symfony.com/doc/current/reference/forms/types/form.html#attr)<br>
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
**Documentation officiel:** [Symfony Docs](https://symfony.com/doc/current/reference/forms/types/form.html#auto-initialize)<br>
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
**Documentation officiel:** [Symfony Docs](https://symfony.com/doc/current/reference/forms/types/form.html#block-name)<br>
**Description:**
> Vous permet d'ajouter un nom de bloc personnalisé à ceux utilisés par défaut pour rendre le type de formulaire. Utile par exemple si vous avez plusieurs instances du même formulaire et que vous avez besoin de personnaliser le rendu des formulaires individuellement.

>Si vous définissez par exemple cette option sur `my_custom_name` et que le champ est de type `text`, Symfony utilisera les noms suivants (et dans cet ordre) pour trouver le bloc utilisé pour rendre le widget du champ : `_my_custom_name_widget`, `text_widget` et `form_widget`.

**Exemple:**
```
$builder->add('input', TextareaType::class, [
    'block_name' => "blockName",
]);
```
<a href="#" class="btn btn-neutral float-right">Retour au menu</a>


## BlockPrefix
**Nom de champ:** 'block_prefix'<br>
**Type:** *string*<br>
**Valeur par défaut:** `null`<br>
**Documentation officiel:** [Symfony Docs](https://symfony.com/doc/current/reference/forms/types/form.html#block-prefix)<br>
**Description:**
> Vous permet d'ajouter un préfixe de bloc personnalisé à ceux utilisés par défaut pour rendre le type de formulaire. Utile par exemple si vous avez plusieurs instances du même formulaire et que vous avez besoin de personnaliser le rendu des formulaires individuellement.

**Exemple:**
```
$builder->add('input', TextareaType::class, [
    'block_prefix' => "blockPrefix",
]);
```

## Disabled
**Nom de champ:** 'disabled'<br>
**Type:** *boolean*<br>
**Valeur par défaut:** `false`<br>
**Documentation officiel:** [Symfony Docs](https://symfony.com/doc/current/reference/forms/types/form.html#disabled)<br>
**Description:**
> Si vous ne souhaitez pas qu'un utilisateur modifie la valeur d'un champ, vous pouvez définir l'option `disabled` sur true. Toute valeur soumise sera ignorée.

**Exemple:**
```
$builder->add('input', TextareaType::class, [
    'disabled' => true,
]);
```

## Label
**Nom de champ:** 'label'<br>
**Type:** *string*<br>
**Valeur par défaut:** `null`<br>
**Documentation officiel:** [Symfony Docs](https://symfony.com/doc/current/reference/forms/types/form.html#label)<br>
**Description:**
> Définit l'étiquette qui sera utilisée lors du rendu du champ.

**Exemple:**
```
$builder->add('input', TextareaType::class, [
    'label' => "Input Field",
]);
```

## LabelHtml
**Nom de champ:** 'label_html'<br>
**Type:** *boolean*<br>
**Valeur par défaut:** `false`<br>
**Documentation officiel:** [Symfony Docs](https://symfony.com/doc/current/reference/forms/types/form.html#label-html)<br>
**Description:**
> Par défaut, le contenu de l'option `label` est échappé avant de le rendre dans le modèle. Définissez cette option sur true pour ne pas les échapper, ce qui est utile lorsque l'étiquette contient des éléments HTML.

**Exemple:**
```
$builder->add('input', TextareaType::class, [
    'label_html' => true,
]);
```

## RowAttr
**Nom de champ:** 'row_attr'<br>
**Type:** *array*<br>
**Valeur par défaut:** `[]`<br>
**Documentation officiel:** [Symfony Docs](https://symfony.com/doc/current/reference/forms/types/form.html#row-attr)<br>
**Description:**
> Un tableau associatif des attributs HTML ajoutés à l'élément qui est utilisé pour restituer le type de formulaire row.

**Exemple:**
```
$builder->add('input', TextareaType::class, [
    'row_attr' => ['class' => 'myrow'],
]);
```

## TranslationDomain
**Nom de champ:** 'translation_domain'<br>
**Type:** *string|null|false*<br>
**Valeur par défaut:** `null`<br>
**Documentation officiel:** [Symfony Docs](https://symfony.com/doc/current/reference/forms/types/form.html#translation-domain)<br>
**Description:**
> Il s'agit du domaine de traduction qui sera utilisé pour toute étiquette ou option rendue pour ce champ. Utilisez null pour réutiliser le domaine de traduction du formulaire parent (ou le domaine par défaut du traducteur pour le formulaire racine). Utilisez false pour désactiver les traductions.

**Exemple:**
```
$builder->add('input', TextareaType::class, [
    'translation_domain' => 'messages',
]);
```

## LabelTranslationParameters
**Nom de champ:** 'label_translation_parameters'<br>
**Type:** *array*<br>
**Valeur par défaut:** `[]`<br>
**Documentation officiel:** [Symfony Docs](https://symfony.com/doc/current/reference/forms/types/form.html#label-translation-parameters)<br>
**Description:**
> Le contenu de l'option `label` est traduit avant de l'afficher, il peut donc contenir des espaces réservés de traduction. Cette option définit les valeurs utilisées pour remplacer ces espaces réservés.

**Exemple:**
```
$builder->add('input', TextareaType::class, [
    'label_translation_parameters' => ['%count%' => 10],
]);
```

## AttrTranslationParameters
**Nom de champ:** 'attr_translation_parameters'<br>
**Type:** *array*<br>
**Valeur par défaut:** `[]`<br>
**Documentation officiel:** [Symfony Docs](https://symfony.com/doc/current/reference/forms/types/form.html#attr-translation-parameters)<br>
**Description:**
> Le contenu des valeurs `title` et `placeholder` définies dans l'option 'attr' est traduit avant de l'afficher, il peut donc contenir des espaces réservés de traduction. Cette option définit les valeurs utilisées pour remplacer ces espaces réservés.

**Exemple:**
```
$builder->add('input', TextareaType::class, [
    'attr_translation_parameters' => [];
]);
```

## Priority
**Nom de champ:** 'priority'<br>
**Type:** *integer*<br>
**Valeur par défaut:** `0`<br>
**Documentation officiel:** [Symfony Docs](https://symfony.com/doc/current/reference/forms/types/form.html#priority)<br>
**Description:**
> Les champs sont rendus dans le même ordre qu'ils sont inclus dans le formulaire. Cette option modifie la priorité de rendu des champs, vous permettant d'afficher les champs plus tôt ou plus tard que leur ordre d'origine.

> Cette option n'affectera que l'ordre d'affichage. Plus cette priorité est élevée, plus le champ sera rendu tôt. La priorité peut également être négative et les champs avec la même priorité conserveront leur ordre d'origine.

**Exemple:**
```
$builder->add('input', TextareaType::class, [
    'priority' => 1,
]);
```

