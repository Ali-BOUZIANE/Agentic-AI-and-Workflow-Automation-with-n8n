# 🤖 Automatisation Intelligente : Agent d'IA pour la Gestion Doctorale avec n8n

## 📌 Présentation du Projet
[cite_start]Ce projet met en œuvre un **système d'IA agentique** autonome conçu pour orchestrer la communication et la logistique d'une **Journée Doctorale**[cite: 1, 14]. [cite_start]Contrairement aux systèmes traditionnels basés sur des règles rigides, cet agent est capable d'agir de manière proactive et indépendante pour atteindre des objectifs complexes sans supervision humaine constante[cite: 4, 6].



---

## 🎯 Problématique & Solution
* [cite_start]**Le Défi** : La gestion manuelle de centaines d'e-mails personnalisés et la mise à jour des plannings constituent une source majeure d'erreurs et de perte de temps[cite: 15].
* [cite_start]**La Solution** : Un agent intelligent qui comprend le statut de chaque doctorant (1ère année vs années suivantes) et adapte dynamiquement le message et les consignes (poster vs présentation orale)[cite: 8, 16].

---

## 🧠 Architecture : Le Cadre ReAct
[cite_start]L'agent utilise le pattern **ReAct (Reasoning/Action)** pour naviguer dans son environnement[cite: 9, 10]:



1.  [cite_start]**Raisonnement** : L'IA analyse le contexte et planifie les étapes nécessaires[cite: 11].
2.  [cite_start]**Action** : L'agent interagit avec son environnement via des outils (APIs)[cite: 12].
3.  [cite_start]**Observation** : Il collecte des informations sur l'état du système pour ajuster ses décisions futures[cite: 13].

---

## 🛠️ Technologies Utilisées
* [cite_start]**Orchestrateur** : [n8n](https://n8n.io/) pour la gestion visuelle des workflows agentiques[cite: 22].
* [cite_start]**Modèle de Langage (LLM)** : Google Gemini 1.5 Flash/Pro, choisi pour sa fenêtre de contexte étendue et ses capacités de *Tool Calling*[cite: 23].
* [cite_start]**Mémoire** : *Window Buffer Memory* pour maintenir le contexte des interactions[cite: 24, 30].
* [cite_start]**Outils (Tools)** : Intégration directe avec **Google Sheets API** (source de vérité) et **Gmail API** (envoi des communications)[cite: 25, 31, 35].

---

## ⚙️ Workflow Technique
[cite_start]Le workflow n8n permet à l'agent de disposer d'une autonomie décisionnelle complète[cite: 18, 27]:



* [cite_start]**Extraction de données** : L'agent consulte le fichier Google Sheets pour obtenir la liste des doctorants et le planning[cite: 31, 33].
* [cite_start]**Grounding (Précision)** : Utilisation du Sheets comme unique source de vérité pour éviter les hallucinations[cite: 19].
* [cite_start]**Exécution** : Génération et envoi automatique d'e-mails HTML personnalisés via Gmail[cite: 35, 38].
* [cite_start]**Traçabilité** : Mise à jour automatique du statut "Doctorant informé" dans le fichier source après chaque action réussie[cite: 20, 36].

---

## ✅ Résultats obtenus
* [cite_start]**Personnalisation Intelligente** : Adaptation du contenu de l'e-mail selon le niveau de recherche du destinataire[cite: 8].
* [cite_start]**Automatisation de bout en bout** : Gestion fluide du flux d'invitation à la contribution sans intervention manuelle[cite: 38].
* [cite_start]**Suivi en Temps Réel** : Tableau de bord Google Sheets mis à jour dynamiquement par l'IA[cite: 20, 32].

---

[cite_start]**Réalisé par : Ali BOUZIANE** [cite: 2]
*Ingénieur en Génie Informatique | IA, Big Data & Cybersécurité*
