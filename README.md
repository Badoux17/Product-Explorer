Product Explorer – TP Jetpack Compose

Application Android construite progressivement au fil des TP 4 à 11. Elle affiche un catalogue local de produits. Les données restent locales du début à la fin.

TP4 – Écran de détail produit

Création du projet Product Explorer et d'un premier écran de détail produit. Utilisation des composants fondamentaux : Text, Button, Icon (avec ajout de la dépendance des icônes Material), Image, Card et OutlinedTextField en lecture seule. L'interface est découpée en petits composables qui reçoivent leurs données en paramètres.

TP5 – Écran d'accueil

Ajout d'un écran d'accueil construit avec les layouts Compose : Column, Row, Box (badge superposé sur un bloc), Spacer et Surface.

TP6 – Catalogue de produits

Affichage d'une liste locale de produits. Le catalogue utilise une LazyColumn pour les produits, une LazyRow pour les catégories et une carte produit réutilisable (ProductListItem).

TP7 – Personnalisation graphique

Personnalisation du thème avec Material Design 3 : palettes de couleurs claire et sombre, formes et typographie personnalisées. Les composants utilisent MaterialTheme pour s'adapter automatiquement au thème, avec des previews claire et sombre.

TP8 – Catalogue interactif

Ajout d'une recherche, d'un filtre « en stock uniquement », de favoris et d'un compteur de produits affichés. Les états sont gérés directement dans l'écran avec remember, mutableStateOf et rememberSaveable.

TP9 – State Hoisting

Réorganisation du code. Les états sont déplacés dans un composable stateful, ProductCatalogContainer. L'écran ProductCatalogScreen devient stateless : il reçoit des valeurs et des callbacks.

TP10 – ViewModel

Déplacement de l'état de l'écran dans ProductCatalogViewModel. Le container récupère le ViewModel avec viewModel() et transmet ses données à l'écran.

TP11 – StateFlow

Regroupement de l'état dans une classe ProductCatalogUiState. Le ViewModel l'expose avec un StateFlow (MutableStateFlow privé) et le met à jour avec update et copy. Le container observe cet état avec collectAsState().

Organisation finale

ProductCatalogViewModel gère l'état, ProductCatalogContainer le relie à Compose, ProductCatalogScreen l'affiche et ProductListItem affiche chaque produit.

Piton Léo M1AL
