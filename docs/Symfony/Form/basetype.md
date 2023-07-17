# Options Hérité

## Attr
**Type:** *array*
**Valeur par défaut:** `[]`
**Description:**
> Si vous souhaitez ajouter des attributs supplémentaires à une représentation de champ HTML, vous pouvez utiliser l'option `attr`. C'est un tableau associatif avec des attributs HTML comme clés. Cela peut être utile lorsque vous devez définir une classe personnalisée pour un widget

**Exemple:**
```
$builder->add('input', TextareaType::class, [
    'attr' => ['class' => 'myclass'],
]);
```
<a href="#" class="btn btn-neutral float-right">Retour au menu</a>
