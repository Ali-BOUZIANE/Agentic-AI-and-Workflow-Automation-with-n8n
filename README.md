# 🤖 Automatisation Intelligente : Agent d'IA pour la Gestion Doctorale avec n8n

## 📌 Présentation du Projet
Ce projet met en œuvre un **système d'IA agentique** autonome conçu pour orchestrer la communication et la logistique d'une **Journée Doctorale**. Contrairement aux systèmes traditionnels basés sur des règles rigides, cet agent est capable d'agir de manière proactive et indépendante pour atteindre des objectifs complexes sans supervision humaine constante.

---

## 🎯 Problématique & Solution
* **Le Défi** : La gestion manuelle de centaines d'e-mails personnalisés et la mise à jour des plannings constituent une source majeure d'erreurs et de perte de temps.
* **La Solution** : Un agent intelligent qui comprend le statut de chaque doctorant (1ère année vs années suivantes) et adapte dynamiquement le message et les consignes (poster vs présentation orale).

---

## 🧠 Architecture : Le Cadre ReAct
L'agent utilise le pattern **ReAct (Reasoning/Action)** pour naviguer dans son environnement :

1.  **Raisonnement** : L'IA analyse le contexte et planifie les étapes nécessaires.
2.  **Action** : L'agent interagit avec son environnement via des outils (APIs).
3.  **Observation** : Il collecte des informations sur l'état du système pour ajuster ses décisions futures.

---

## 🛠️ Technologies Utilisées
* **Orchestrateur** : **n8n** pour la gestion visuelle des workflows agentiques.
* **Modèle de Langage (LLM)** : **Google Gemini 1.5 Flash/Pro**, choisi pour sa fenêtre de contexte étendue et ses capacités de *Tool Calling*.
* **Mémoire** : *Window Buffer Memory* pour maintenir le contexte des interactions.
* **Outils (Tools)** : Intégration directe avec **Google Sheets API** (source de vérité) et **Gmail API** (envoi des communications).

---

## ⚙️ Workflow Technique
Le workflow n8n permet à l'agent de disposer d'une autonomie décisionnelle complète :

* **Extraction de données** : L'agent consulte le fichier Google Sheets pour obtenir la liste des doctorants et le planning.
* **Grounding (Précision)** : Utilisation du Sheets comme unique source de vérité pour éviter les hallucinations.
* **Exécution** : Génération et envoi automatique d'e-mails HTML personnalisés via Gmail.
* **Traçabilité** : Mise à jour automatique du statut "Doctorant informé" dans le fichier source après chaque action réussie.

---

## ✅ Résultats obtenus
* **Personnalisation Intelligente** : Adaptation du contenu de l'e-mail selon le niveau de recherche du destinataire.
* **Automatisation de bout en bout** : Gestion fluide du flux d'invitation à la contribution sans intervention manuelle.
* **Suivi en Temps Réel** : Tableau de bord Google Sheets mis à jour dynamiquement par l'IA.

---

**Réalisé par : Ali BOUZIANE** *Ingénieur en Génie Informatique | IA, Big Data & Cybersécurité*
