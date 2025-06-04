# Les types d’entreôts de données <a href="../"><img src="../../assets/atomicBi.png" alt="Business intelligence" align="right" height="64px"></a>
1. **Le Data Warehouse (DW) Entreprise**  
Un Data Warehouse d’entreprise est une grande base de données centralisée intègrant des données de l’ensemble de l’organisation, conçu pour servir les besoins analytiques de toute l’entreprise.
2. **Data Mart**  
Un Data Mart est une version plus petite et plus ciblée d’un Data Warehouse. Il répond aux besoins spécifiques d’un département ou d’une unité d’affaires particulière. Pouvant indépendant ou extrait d’un Data Warehouse d’entreprise.
3. **Operational Data Store (ODS)**  
L’ODS est une base de données conçue pour les transactions courantes et les opérations courantes de l’entreprise. Servant souvent de source de données pour les Data Warehouses, il est utilisé pour des rapports en temps réel et des tâches de business intelligence opérationnelle.
4. **Cloud Data Warehouse**  
Ces entrepôts de données sont hébergés dans le cloud, offrant évolutivité, flexibilité et une gestion simplifiée. (E.g. Amazon Redshift, Google BigQuery, Snowflake et Microsoft Azure SQL Data Warehouse).
<!--<div align="center"><a href="#"><img src="../../assets/cloud2.jpg" alt="Cloud"></a></div>-->

5. **Virtual Data Warehouse**  
Un Data Warehouse virtuel ne stocke pas les données physiquement. Utilisant des techniques de virtualisation des données pour intégrer les données provenant de sources variées en temps réel, il et permet l’accès et l’analyse sans nécessiter de copie des données.
6. **Le Data Lake**  
Techniquement différent, un Data Lake est souvent mentionné en parallèle des Data Warehouses. Utilisé pour stocker de grandes quantités de données brutes dans leur format d’origine, il permet une analyse flexible et l’extraction de valeur de divers types de données, notamment structurées, semi-structurées et non structurées.
<!--<div align="center"><a href="#"><img src="../../assets/cloud.jpg" alt="Cloud"></a></div>-->

7. **Le Data Vault**  
Le Data Vault est une méthodologie et une architecture flexible et évolutive construisant des entrepôts de données. Utilisant une approche orientée vers les hubs, les liens et les satellites pour gérer les données historiques et faciliter les changements.
<!--<div align="center"><a href="#"><img src="../../assets/vaultCloud.jpg" alt="Cloud"></a><br><br></div>-->

Chaque type de Data Warehouse a ses avantages et inconvénients, et le choix dépend souvent des besoins spécifiques de l’organisation, de la complexité des données et des exigences analytiques.

