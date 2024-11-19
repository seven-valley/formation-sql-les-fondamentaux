# CRM Customer  Relationship Management
Gestion des devis et factures d'une entreprise
  
**echelle de Scoville 100 000**  :underage:  
https://fr.wikipedia.org/wiki/%C3%89chelle_de_Scoville  
3 piments :cactus::cactus::cactus:  
  

## Le pitch :
Le client a un projet  
En fonction du projet , nous lui proposons plusieurs devis  
Il valide un devis  
Nous lui envoyons une facture  
  

## Modele relationnel
![crm](../img/11/crm.webp)
## Les Clients
![client](../img/11/client.png)
## Les factures
![facture](../img/11/facture.png)
  
**attention les dates des factures ont été modifiées !** 
   
# les data

```sql
TRUNCATE client;
TRUNCATE projet;
TRUNCATE devis;
TRUNCATE facture;

INSERT INTO client (nom) VALUES 
	('Mairie de Rennes'),
	('Neo Soft'),
	('Sopra'),
	('Accenture'),
	('Amazon');
INSERT INTO projet (nom, client_id) VALUES
	('Création de site internet', 1),
	('Logiciel CRM', 2),
	('Logiciel de devis', 3),
	('Site internet e-commerce', 4),
	('Logiciel ERP', 2),
	('Logiciel gestion de stock',5);

INSERT INTO devis (version,reference, prix, projet_id) VALUES
	('1','DEV2100A', 3000, 1),
	('2','DEV2100B', 5000, 1),
	('1','DEV2100C', 5000, 2),
	('1','DEV2100D', 3000, 3),
	('1','DEV2100E', 5000, 4),
	('1','DEV2100F', 2000, 5),
	('1','DEV2100G', 1000, 6);

INSERT INTO facture (reference,info,total,devis_id,date_crea,date_paiement)	
    VALUES
	('FA001', 'site internet partie 1', 1500, 1, '2023-09-01','2023-10-01'),
	('FA002', 'site internet partie 2', 1500, 1, '2023-09-20',null),
	('FA003', 'logiciel CRM', 5000, 3, '2024-02-01',null),
	('FA004', 'logiciel devis', 3000, 4, '2024-03-03','2024-04-03'),
	('FA005', 'site ecommerce', 5000, 5, '2023-03-01',null),
	('FA006', 'logiciel ERP', 2000, 6, '2023-03-01',null);
```
# Partie 1
1 - Créer la base de données  en 4 étape  
  11 - Créer la table client & Ajouter les données de client  
  12 - Créer la table projet & Ajouter les données de projet  
  13 - Créer la table devis & Ajouter les données de devis    
  14 - Créer la table facture & Ajouter les données de facture  
  
2 - Ajouter les données  
  
# Partie 2
1 - Afficher toutes les factures avec le nom des clients  
2 - Afficher le nombre de factures par client - afficher 0 factures si il n'y a pas de factures  
3 - afficher le chiffre d'affaire par client   
4 - afficher le CA total  
5 - afficher  la somme des factures en attente de paiement  
6 - afficher les factures en retard de paiment 30 jours max  
avec le nombre de jours de retard  

# Partie 3 réaliser un modèle relationnel
  **[OPTIONEL]**  
:shipit:Réaliser le modèle relationnel sur db diagram  et fournir le prompt
  
https://dbdiagram.io/


