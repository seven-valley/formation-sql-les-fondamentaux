
# Ajouter des personnes

```sql

INSERT INTO Clients (noCli, nom, prenom, adresse, cpo, ville) VALUES
(20, 'Dubosc', 'Frank', '12 avenue des flots bleus', '76140', 'Petit-Quevilly'),
(21, 'Boon', 'Dany', '22 rue des Ch''tis', '59280', 'Armentières'),
(22, 'Elmaleh', 'Gad', '45 rue du sentier', '75001', 'Paris'),
(23, 'Dujardin', 'Jean', 'rue Brice', '92500', 'Rueil-Malmaison'),
(24, 'Marceau', 'Sophie', 'Boulevard de la Boom', '75010', 'Paris'),
(25, 'Merad', 'Kad', 'Rue du petit nicolas', '91130', 'Ris-Orangis'),
(26, 'Seigner', 'Mathilde', '357 rue du Camping', '75012', 'Paris'),
(27, 'Reno', 'Jean', '78 Boulevard de Léon', '51200', 'Montmirail'),
(28, 'Lanvin', 'Gérard', '84 avenue de l''aile ou la cuisse', '92100', 'Boulogne-Billancourt'),
(29, 'Tautou', 'Audrey', 'rue de Montmartre', '63110', 'Beaumont'),
(30, 'Cotillard', 'Marion', '45 rue de la Même', '13001', 'Marseille'),
(31, 'Duris', 'Romain', '76 rue de l''arnaqueur', '06000', 'Nice'),
(32, 'Depardieu', 'Gérard', '57 rue du conte de Monte-Cristo', '36000', 'Châteauroux'),
(33, 'Youn', 'Michaël', 'rue de la beuze', '92150', 'Suresnes'),
(34, 'Poelvoorde', 'Benoît', '22 rue du Boulet', '22500', 'Paimpol'),
(35, 'Paradis', 'Vanessa', '12 rue des arnaqueurs', '94100', 'Saint-Maur-des-Fossés'),
(36, 'Wilson', 'Lambert', '100 rue de Dieu', '92200', 'Neuilly-sur-Seine'),
(37, 'Garcia', 'José', '65 rue de la vérité', '75001', 'Paris'),
(38, 'Luchini', 'Fabrice', '73 rue de Beaumarchais', '75016', 'Paris'),
(39, 'Baye', 'Nathalie', '33 rue de Vénus', '27150', 'Mainneville'),
(40, 'Magimel', 'Benoît', '47 rue des petits mouchoirs', '33950', 'Lège-Cap-Ferret'),
(41, 'Cluzet', 'François', '7 rue des apprentis', '75018', 'Paris'),
(42, 'Frot', 'Catherine', 'rue Odette', '69110', 'Sainte Foy-lès-Lyon'),
(43, 'Dupontel', 'Albert', '11 impasse de Bernie', '78100', 'Saint-Germain-en-Laye'),
(44, 'Huppert', 'Isabelle', '8 rue des femmes', '75002', 'Paris'),
(45, 'Deneuve', 'Catherine', '12 rue de Rochefort', '50100', 'Cherbourg-Octeville'),
(46, 'de France', 'Cécile', '17 rue de l''auberge espagnole', '08000', 'Charleville-Mézières');
```

# Ajouter le jeux d'essai
```sql
INSERT INTO Fiches VALUES (9909, 20, DATE_SUB(NOW(), INTERVAL 284 DAY), DATE_SUB(NOW(), INTERVAL 282 DAY), 'SO');
INSERT INTO LignesFic VALUES (9909, 1, 'A10', DATE_SUB(NOW(), INTERVAL 284 DAY), DATE_ADD(DATE_SUB(NOW(), INTERVAL 284 DAY), INTERVAL 6 HOUR));
INSERT INTO LignesFic VALUES (9909, 2, 'S01', DATE_SUB(NOW(), INTERVAL 284 DAY), DATE_ADD(DATE_SUB(NOW(), INTERVAL 282 DAY), INTERVAL 6 HOUR));

INSERT INTO Fiches VALUES (9910, 21, DATE_SUB(NOW(), INTERVAL 68 DAY), NULL, 'RE');
INSERT INTO LignesFic VALUES (9910, 1, 'P01', DATE_SUB(NOW(), INTERVAL 68 DAY), DATE_ADD(DATE_SUB(NOW(), INTERVAL 59 DAY), INTERVAL 6 HOUR));
INSERT INTO LignesFic VALUES (9910, 2, 'S01', DATE_SUB(NOW(), INTERVAL 68 DAY), DATE_ADD(DATE_SUB(NOW(), INTERVAL 65 DAY), INTERVAL 6 HOUR));
INSERT INTO LignesFic VALUES (9910, 3, 'A02', DATE_SUB(NOW(), INTERVAL 68 DAY), DATE_ADD(DATE_SUB(NOW(), INTERVAL 66 DAY), INTERVAL 6 HOUR));
INSERT INTO LignesFic VALUES (9910, 4, 'F03', DATE_SUB(NOW(), INTERVAL 68 DAY), DATE_ADD(DATE_SUB(NOW(), INTERVAL 62 DAY), INTERVAL 6 HOUR));
INSERT INTO LignesFic VALUES (9910, 5, 'F22', DATE_SUB(NOW(), INTERVAL 68 DAY), DATE_ADD(DATE_SUB(NOW(), INTERVAL 63 DAY), INTERVAL 6 HOUR));

INSERT INTO Fiches VALUES (9911, 22, DATE_SUB(NOW(), INTERVAL 182 DAY), DATE_SUB(NOW(), INTERVAL 171 DAY), 'SO');
INSERT INTO LignesFic VALUES (9911, 1, 'A04', DATE_SUB(NOW(), INTERVAL 182 DAY), DATE_ADD(DATE_SUB(NOW(), INTERVAL 176 DAY), INTERVAL 6 HOUR));
INSERT INTO LignesFic VALUES (9911, 2, 'A10', DATE_SUB(NOW(), INTERVAL 182 DAY), DATE_ADD(DATE_SUB(NOW(), INTERVAL 177 DAY), INTERVAL 6 HOUR));
INSERT INTO LignesFic VALUES (9911, 3, 'P01', DATE_SUB(NOW(), INTERVAL 182 DAY), DATE_ADD(DATE_SUB(NOW(), INTERVAL 179 DAY), INTERVAL 6 HOUR));

```

## Questions :
  
:one: Liste des clients (nom, prénom, adresse, code postal, ville) ayant au moins une fiche de location en cours.
  
:two: Détail de la fiche de location de M. Dupond Jean de Paris (avec la désignation des articles loués, la date de départ et de retour).
  
:three: Liste de tous les articles (référence, désignation et libellé de la catégorie) dont le libellé de la catégorie contient ski.
  
:four: Calcul du montant de chaque fiche soldée et du montant total des fiches.
  
:five: Calcul du nombre d’articles actuellement en cours de location.
  
:six: Calcul du nombre d’articles loués, par client.
  
:seven: Liste des clients qui ont effectué (ou sont en train d’effectuer) plus de 200€ de location.
  
:eight: Liste de tous les articles (loués au moins une fois) et le nombre de fois où ils ont été loués, triés du plus loué au moins loué.
  
:nine: Liste des fiches (n°, nom, prénom) de moins de 150€.
  
**10**  Calcul de la moyenne des recettes de location de surf (combien peut-on espérer gagner pour une location d'un surf ?).
  
**11**  Calcul de la durée moyenne d'une location d'une paire de skis (en journées entières).
Informations
Les résultats attendus sont présentés dans le fichier TP-module8-resultats_attendus