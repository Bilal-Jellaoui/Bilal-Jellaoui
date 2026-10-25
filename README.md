<div align="center">

<picture>
  <source media="(max-width: 600px)" srcset="assets/header-m.svg">
  <img src="assets/header.svg" width="100%" alt="Bilal Jellaoui · Data Science · Data Analyst · Machine Learning · AI. AI, Deep Learning, NLP, Big Data & Streaming : I build data-driven systems from raw data to deployment. Disponible pour un stage PFE de 6 mois à partir de février 2027.">
</picture>

**Étudiant en Master Big Data, IA & Applications Avancées (2025–2027)**<br>
Université Ibn Tofaïl · Faculté des Sciences de Kénitra 🇲🇦

<a href="https://github.com/Bilal-Jellaoui/Bilal-Jellaoui/raw/main/CV_Bilal_Jellaoui.pdf"><img src="assets/btn-cv.svg" height="40" alt="Télécharger mon CV (PDF)"></a>&nbsp;<a href="https://bilal-jellaoui.github.io/"><img src="assets/btn-portfolio.svg" height="40" alt="Portfolio"></a>&nbsp;<a href="https://www.linkedin.com/in/bilal-jellaoui"><img src="assets/btn-linkedin.svg" height="40" alt="LinkedIn"></a>&nbsp;<a href="mailto:bilaljellaoui@gmail.com"><img src="assets/btn-email.svg" height="40" alt="Email"></a>

</div>

## À propos

Je construis des systèmes de données **de bout en bout** : préparation des données, modèles de Machine Learning et de NLP, puis intégration dans une application (API REST Flask) ou dans un pipeline temps réel (Kafka).

Je cherche un **stage de PFE de 6 mois à partir de février 2027**, dans l'un de ces domaines :

- **Data Science, Data Analytics & BI** : nettoyage, exploration, segmentation client (RFM, K-means), indicateurs et tableaux de bord.
- **Machine Learning & Deep Learning** : classification, XGBoost, CNN, détection de fraude, modèles servis par API.
- **NLP & IA générative** : DistilBERT, Llama 3.3 via Groq, détection de crise, mémoire de conversation.
- **Big Data & Data Engineering** : Kafka, Kafka Streams, Hadoop, HBase, Hive, pipelines temps réel.

## Compétences

<picture>
  <source media="(max-width: 600px)" srcset="assets/skills-m.svg">
  <img src="assets/skills.svg" width="100%" alt="Langages : Python, Java, C, C++, SQL, Shell. Machine et Deep Learning : scikit-learn, XGBoost, TensorFlow, Keras, PyTorch. NLP et IA générative : Hugging Face, DistilBERT, spaCy, Llama 3.3, Groq API. Data et visualisation : pandas, NumPy, Matplotlib, Seaborn, Power BI, Jupyter. Big Data et streaming : Kafka, Kafka Streams, Hadoop, HDFS, YARN, HBase, Hive. Backend et API : Spring Boot, Flask, API REST, SQLite. DevOps et outils : Docker, Git, GitHub Actions, Maven, JUnit 5, JMeter, Linux, IntelliJ IDEA, VS Code.">
</picture>

## Projets à la une

### ⭐ SoukLine · détecter une panne web en temps réel

<a href="https://github.com/Bilal-Jellaoui/streaming-logs-kafka">
<picture>
  <source media="(max-width: 600px)" srcset="assets/soukline-flow-m.svg">
  <img src="assets/soukline-flow.svg" width="100%" alt="Architecture de SoukLine : site Spring Boot, access.log Tomcat, collecteur Java, Kafka à 3 brokers, deux moteurs de calcul indépendants (Kafka Streams et Java concurrent), alerte 5xx.">
</picture>
</a>

- **Problème.** Quand un site tombe, les erreurs HTTP 5xx explosent dans les logs, mais personne ne les voit à temps.
- **Solution.** Un pipeline temps réel : logs Tomcat → collecteur Java → Kafka (3 brokers) → deux moteurs de calcul indépendants → tableau de bord et alerte.
- **Mon rôle.** Chef d'équipe (6 membres). Parser de logs (regex, normalisation des URL) et **Moteur A** en Kafka Streams (fenêtres de 5 s, temps d'événement lu dans le log). Le Moteur B, écrit à la main en Java (`ExecutorService`, `CyclicBarrier`), sert de point de comparaison.
- **Résultat.** Les deux moteurs donnent les mêmes totaux. Une panne simulée sur `/checkout` fait monter les erreurs 5xx à 25 % et déclenche l'alerte en quelques secondes.
- **Qualité.** Maven multi-modules, Pull Requests relues, tests JUnit, intégration continue GitHub Actions.

<p align="center">
<img src="assets/soukline-alerte.png" width="760" alt="Tableau de bord SoukLine : Moteur A et Moteur B affichent les mêmes totaux, alerte déclenchée sur /checkout avec 25 % d'erreurs 5xx">
<br><sub>Le tableau de bord détecte la panne : 10 requêtes sur 10 en erreur sur <code>/checkout</code>, soit 25 % de 5xx pour un seuil de 10 %.</sub>
</p>

[Voir le code](https://github.com/Bilal-Jellaoui/streaming-logs-kafka) · [Documentation détaillée](https://github.com/Bilal-Jellaoui/streaming-logs-kafka#readme)

### Autres projets à la une

<p align="center">
<a href="https://github.com/Bilal-Jellaoui/BMA-Mental-Health-Chatbot"><img src="assets/card-bma.svg" width="400" alt="BMA, chatbot de santé mentale : DistilBERT, Llama 3.3 via Groq, 105 intentions, 12 émotions, F1 supérieur à 90 %."></a>
<a href="https://github.com/Bilal-Jellaoui/fraud-detection-flask-ml"><img src="assets/card-fraude.svg" width="400" alt="Détection de fraude bancaire : XGBoost, ROC-AUC 0,982, F1 0,871, application Flask avec API REST."></a>
<a href="https://github.com/Bilal-Jellaoui/customer-segmentation-rfm"><img src="assets/card-rfm.svg" width="400" alt="Segmentation client RFM : 541 909 transactions, 4 338 clients, AUC 0,911, K-means en 4 segments."></a>
<a href="https://github.com/Bilal-Jellaoui/Classification-Multi-Classes-des-images-en-IA-avec-Python"><img src="assets/card-zoobeco.svg" width="400" alt="ZooBeco : CNN classant 6 espèces d'animaux, application mobile Kivy."></a>
</p>

## Autres travaux du Master

- **[Compression adaptative de signaux physiologiques](https://github.com/Bilal-Jellaoui/adaptive-physiological-signal-compression)**<br>
  Comparaison d'algorithmes de compression sur des signaux multi-capteurs (ECG, EEG, SpO2, respiration) et sélection adaptative de l'algorithme par une approche métaheuristique. Volume ciblé : 1 à 2 Go.<br>
  `Python` `Métaheuristique` `Traitement du signal`
- **[HBase · optimisation des charges et du stockage](https://github.com/Bilal-Jellaoui/HBase-Workload---Storage-Optimization)**<br>
  Analyse des métriques HBase, détection des points chauds (hotspots) et rééquilibrage des ressources. HDFS pour le stockage, Hive pour l'analyse et les rapports. Présentation orale en anglais.<br>
  `HBase` `HDFS` `Hive` `Hadoop`

## Parcours

<picture>
  <source media="(max-width: 600px)" srcset="assets/parcours-m.svg">
  <img src="assets/parcours.svg" width="100%" alt="Formation : Master Big Data, IA et Applications Avancées (2025-2027), Licence Sciences Mathématiques et Informatique (2025), Baccalauréat Sciences Mathématiques A (2021). Langues : arabe langue maternelle, français bon niveau, anglais intermédiaire.">
</picture>

## Contact

Ouvert aux échanges sur la Data Science, l'IA, le Machine Learning et les opportunités de stage.

**CV** [Télécharger (PDF)](https://github.com/Bilal-Jellaoui/Bilal-Jellaoui/raw/main/CV_Bilal_Jellaoui.pdf) · **Email** [bilaljellaoui@gmail.com](mailto:bilaljellaoui@gmail.com) · **LinkedIn** [bilal-jellaoui](https://www.linkedin.com/in/bilal-jellaoui) · **Portfolio** [bilal-jellaoui.github.io](https://bilal-jellaoui.github.io/)

<div align="center"><sub>Kénitra, Maroc · Disponible pour un stage PFE de 6 mois à partir de février 2027</sub></div>
