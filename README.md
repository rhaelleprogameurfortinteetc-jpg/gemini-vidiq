# GitHub Pages — domaine `rhaelle.gg`

Ce dépôt contient le fichier `CNAME` avec le domaine personnalisé. Les enregistrements ci-dessous sont à créer chez le fournisseur DNS qui gère `rhaelle.gg` (registrar ou hébergeur DNS). Les ajouter à GitHub ne modifie pas les DNS du domaine.

## Enregistrements DNS

Pour le domaine racine `rhaelle.gg`, ajoute ces quatre enregistrements **A** :

| Type | Nom / Hôte | Valeur |
|---|---|---|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |

Optionnel : ajoute aussi les enregistrements **AAAA** IPv6 officiels GitHub Pages :

| Type | Nom / Hôte | Valeur |
|---|---|---|
| AAAA | `@` | `2606:50c0:8000::153` |
| AAAA | `@` | `2606:50c0:8001::153` |
| AAAA | `@` | `2606:50c0:8002::153` |
| AAAA | `@` | `2606:50c0:8003::153` |

Pour le sous-domaine `www.rhaelle.gg`, ajoute :

| Type | Nom / Hôte | Valeur |
|---|---|---|
| CNAME | `www` | `rhaelleprogameurfortinteetc-jpg.github.io` |

Supprime les anciens enregistrements A, AAAA ou CNAME contradictoires pour `@` et `www`. Ne crée pas de CNAME pour le domaine racine `rhaelle.gg`.

## Côté GitHub

1. Dans le dépôt, ouvre **Settings → Pages**.
2. Active la publication depuis la branche `main`, dossier `/ (root)`.
3. Dans **Custom domain**, indique `rhaelle.gg` et enregistre.
4. Après la vérification DNS et la publication, active **Enforce HTTPS** si l’option est disponible.

La propagation DNS peut prendre un certain temps. Les DNS ne sont pas configurés par ce fichier : il faut saisir les enregistrements dans le tableau de bord du fournisseur DNS. Vérifie également que ton forfait GitHub autorise Pages pour ce dépôt privé avant de publier.

Documentation officielle : https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site
