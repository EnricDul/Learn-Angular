# Learn-Angular
A tutorial to learn Angular's basics.
------

## Les Services :

Un service contient du code réutilisable ou des données que l'on peut partager à travers toute l'application.
Un service Angular possède deux caractéristiques qui le définissent. 

- Singleton (Il n'existe qu'un seul exemplaire de ce service dans toutes l'application).
- Global (Il est accessible dans toute l'application).

Par exemple, dans une application, on trouve souvent un service qui gère les authentifications utilisateurs et un service qui gère la communication avec la base de données. Ces deux services sont susceptibles d'être réutilisés ailleurs dans l'application.

## Les décorateurs Angular :

Angular fournit de nombreux décorateurs. Ils vont permettre de convertir de simples éléments typescript (par exemple: une méthode, une propriété ou un paramètre de méthode) en éléments spéciaux compréhensibles par le framework ou bien de modifier le comportement d'un service.

Ainsi avec le décorateur **@Component**, Angular traitera la classe qui suit comme une **classe de composant**.
Ici, le décorateur **@Component** prend des objets de configuration en paramètre mais nous verrons que certains décorateurs n'en prennent pas.
Pour utiliser un décorateur il suffit de l'importer dans le fichier typescript.

```ts
import { Component } from '@angular/core';   ===> Import du décorateur Component.
```
Ensuite, nous appelons le décorateur comme suit : 

```ts
@Component({                             ===> Un décorateur commence toujours pas un @
  selector: '[componentTag]',            ===> Sélecteur de la balise qui accueillera le composant (Ex:<p>componentTag>Hi</p>)
  templateUrl: './app.component.html',   ===> Chemin vers le fichier HTML
  styleUrls: ['./app.component.css']     ===> Chemin vers le fichier de style
})

export class AppComponent {
  title = 'app';
}
```

**Notez bien que sans les paramètres de @Component, le composant ne fonctionnerait pas**

Comme dis plus haut, il existe d'autres décorateurs très utilisés sur Angular. Voici le listing des plus populaires :

1. @Injectable 





