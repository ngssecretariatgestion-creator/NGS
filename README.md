# Site NGS Secrétariat & Gestion

Site statique (une seule page HTML) prêt à héberger sur GitHub Pages et à relier au nom de domaine www.ngs-secretariat-gestion.fr.

## Contenu du dépôt
- `index.html` — le site complet (toutes les rubriques : Accueil, Nos Services, À Propos, Contact, Mentions Légales, Politique de confidentialité)
- `CNAME` — déclare le nom de domaine personnalisé à GitHub Pages

## Mise en ligne (à faire une fois le dépôt créé sur GitHub)
1. Dans le dépôt GitHub : **Settings → Pages**
2. Source : **Deploy from a branch**, branche `main`, dossier `/ (root)`
3. Enregistrer — GitHub fournit une adresse provisoire du type `https://<utilisateur>.github.io/<depot>/`

## Relier le nom de domaine www.ngs-secretariat-gestion.fr
Chez le bureau d'enregistrement du domaine (là où le domaine a été acheté), ajouter ces enregistrements DNS :

| Type  | Nom / Hôte | Valeur                          |
|-------|------------|----------------------------------|
| CNAME | www        | `<utilisateur>.github.io`       |
| A     | @          | 185.199.108.153                  |
| A     | @          | 185.199.109.153                  |
| A     | @          | 185.199.110.153                  |
| A     | @          | 185.199.111.153                  |

Ensuite, dans **Settings → Pages** du dépôt GitHub, renseigner `www.ngs-secretariat-gestion.fr` comme domaine personnalisé et cocher **Enforce HTTPS** une fois le certificat généré (peut prendre jusqu'à 24h).
