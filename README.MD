PLAN FINAL — Ingénieur Systèmes Cloud & IA
Profil cible : Ingénieur systèmes cloud et IA, base Linux, spécialisé Azure puis AWS, expert identité hybride AD/Entra, capable de concevoir, automatiser, sécuriser et déployer des infrastructures et des services IA.

Durée : 24 mois (avec checkpoints à 6, 12, 18, 24 mois).
Rythme : 1h/jour en semaine + 3h le week-end (~8h/semaine), non négociable.
Poste actuel : helpdesk conservé maximum 24 mois — date de sortie affichée.
Outils : LinkedIn Learning (gratuit via ton employeur), GitHub, lab maison (Proxmox), IA comme accélérateur.

Les 3 piliers du plan
Technique : Linux → Cloud → Automatisation → BDD → Identité

IA entrelacée : tuteur → copilote → composant → produit

Preuves : 3 projets phares + certifs + portfolio GitHub

Roadmap globale 24 mois
Phase	Mois	Objectif	Certifs
Fondations	1–3	Linux solide + Ansible	LFCS
Cloud Azure	4–6	Azure + Entra ID	AZ-900, AZ-104
Identité hybride	7	AD ↔ Entra + Samba AD DC	—
Cloud AWS	8–10	AWS + IA cloud	AWS SAA, AI-900
Multi-cloud + IA	11–12	Terraform multi-cloud + plateforme IA	—
Spécialisation	13–18	Sécurité/Identité + IA appliquée	AZ-500 ou SC-300
Ingénieur IA	19–24	Infra pour l’IA	AI-102
Mois 1 — Linux fondamentaux + IA tuteur
Technique

Proxmox (ou VirtualBox) sur ta machine.

2 VM : Debian + Ubuntu Server.

SSH durci (clés, no root, fail2ban).

Commandes de base : fichiers, permissions, users, processus, systemctl, cron.

BDD

Installe MariaDB sur une VM. Crée users, base, dump/restore simple.

IA entrelacée

IA = tuteur. Chaque commande nouvelle → “explique-moi pourquoi”.

Crée ia-notes/README.md : 3 lignes par session (demande / réponse / ce que j’ai compris).

Interdiction : copier-coller sans comprendre.

LinkedIn Learning

“Learning Linux Command Line” — Scott Simpson.

Livrable : repo lab-infra + ia-notes + 2 VM + SSH durci + MariaDB installée.

Mois 2 — Linux avancé + Ansible + BDD + IA relecteur
Technique

LVM, réseau Linux (ip, ss, nftables/ufw), systemd avancé.

Ansible : inventaire, 1er playbook, variables, handlers.

BDD

PostgreSQL sur une VM : users, rôles, base, backup pg_dump, restore.

Documentation dans lab-infra/db/README.md.

IA entrelacée

Fais générer un playbook Ansible par l’IA → relis ligne par ligne, corrige, teste.

Demande : “Qu’est-ce qui est fragile dans ce playbook ?”

Note les erreurs de l’IA dans ia-notes.

LinkedIn Learning

“Linux Foundation Cert Prep: Essential Commands (Ubuntu)” — KodeKloud.

“Ansible Essential Training” — Anthony Sequeira.

Livrable : ansible-lab avec rôle Debian complet + rôle PostgreSQL.

Mois 3 — LFCS + Ansible sérieux + IA examinateur
Technique

Révisions LFCS + examens blancs.

Passage LFCS.

Ansible avancé : rôles, vault, templates Jinja2, idempotence.

Déploie Prometheus + Grafana via Ansible.

BDD

Rôle Ansible postgresql : install + user + base + backup cron.

IA entrelacée

L’IA génère des questions d’examen blanc LFCS.

Elle joue l’examinateur : “Explique-moi LVM comme si j’avais 12 ans.”

Elle critique ta doc dans lab-infra.

LinkedIn Learning

“LFCS Exam Prep: Managing Security” — KodeKloud.

Livrable : LFCS validée + stack monitoring automatisée + rôle Ansible PostgreSQL.

Mois 4 — Azure AZ-900 + AZ-104 début + IA copilote
Technique

Azure fundamentals : IAM, VNet, VM, stockage, coûts.

AZ-900 passée.

Début AZ-104 : VNet, VM, storage, RBAC.

BDD

Azure Database for PostgreSQL (managée) : firewall, backup auto, restauration.

IA entrelacée

GitHub Copilot pour générer du Terraform Azure simple → relis, corrige.

IA t’explique IAM Azure vs IAM AWS.

LinkedIn Learning

“Microsoft Azure Fundamentals (AZ-900) Cert Prep” — Microsoft Press (4 cours).

“Microsoft Azure Administrator Associate (AZ-104) Cert Prep” — Microsoft Press.

Livrable : 1 VM Azure + VNet + repo terraform-lab + Azure PostgreSQL.

Mois 5 — AZ-104 + Entra ID + IA identité
Technique

AZ-104 complet : compute, réseau, stockage, identité, gouvernance.

Passage AZ-104.

Entra ID : users, groupes, MFA, conditional access, SSO.

BDD

Azure SQL notions + comparaison avec PostgreSQL managé.

IA entrelacée

IA t’explique Kerberos, LDAP, SAML, OAuth avec schémas.

Elle génère des scénarios d’incident Entra ID à résoudre.

Livrable : AZ-104 validée + lab Entra ID (users, MFA, CA).

Mois 6 — Projet phare #1 + IA intégrée
Technique

Infra Azure complète : Terraform + Ansible + monitoring + sauvegarde + doc.

Sécurité : TLS, Key Vault, secrets, hardening.

BDD

App + Azure Database for PostgreSQL + sauvegarde testée + TLS.

IA entrelacée

Ajoute un service IA minimal : chatbot RAG sur ta doc (Ollama ou Azure OpenAI).

IA teste ta doc : “Un débutant peut-il suivre ce README ?”

Livrable : repo projet-phare-1 = infra Azure + Entra + BDD + service IA + doc complète.

Mois 7 — AD hybride + Samba AD DC
Technique

Samba AD DC sur Debian.

AD on-prem ↔ Entra ID Connect.

Linux joint à AD : realmd, sssd, Kerberos, LDAP.

BDD

Intégration BDD + auth AD (notions).

IA entrelacée

IA explique les flux d’authentification hybrides (schémas).

Génère des scripts PowerShell de diagnostic AD → relis, teste.

Ajoute un assistant IA interne qui répond sur tes procédures AD.

LinkedIn Learning

Cours sur Samba AD, Entra ID Connect (recherche ciblée).

Livrable : projet-phare-2 = infra hybride AD/Entra + assistant IA doc.

Mois 8–10 — AWS SAA + IA cloud
Technique

AWS SAA : EC2, VPC, S3, IAM, RDS, Lambda, CloudWatch.

Passage AWS SAA (fin mois 10).

AI-900 (fin mois 10, 1 semaine).

BDD

AWS RDS (MySQL/PostgreSQL) : multi-AZ, snapshots, restauration.

IA entrelacée

IA compare Azure vs AWS service par service (tableau dans ton repo).

Fais générer du Terraform multi-provider par l’IA → corrige.

Déploie un LLM local sur AWS (EC2 GPU spot ou SageMaker) — pour comprendre.

LinkedIn Learning

“AWS Certified Solutions Architect – Associate (SAA-C03) Cert Prep”.

“Microsoft Azure AI Fundamentals (AI-900) Cert Prep”.

Livrable : AWS SAA + AI-900 + infra AWS minimale + LLM local AWS.

Mois 11 — Terraform multi-cloud + IA orchestrateur
Technique

Terraform multi-provider (Azure + AWS), modules, remote state (S3 + DynamoDB).

GitHub Actions : CI/CD pour Terraform.

BDD

Provisionner BDD Azure et AWS par Terraform.

IA entrelacée

Déploie la même app sur Azure et AWS via Terraform.

Workflow GitHub Actions qui utilise l’IA pour reviewer le code Terraform (commentaire auto sur PR).

Livrable : multi-cloud-app = app identique Azure + AWS, déployée par code.

Mois 12 — Projet phare #3 + IA comme produit
Technique

Plateforme IA complète :

Infra Azure + AWS (Terraform)

LLM local ou Azure OpenAI

RAG sur ta doc

Monitoring, sécurité, sauvegarde

CI/CD GitHub Actions

BDD

pgvector (PostgreSQL vectoriel) ou Pinecone/Qdrant pour le RAG.

Redis pour cache/sessions.

IA entrelacée

IA t’aide à écrire ton CV et préparer tes entretiens.

Tu documentes ton parcours dans un article GitHub.

Livrable : projet-phare-3 + portfolio complet + CV orienté ingénieur cloud/IA.

Mois 13–18 — Spécialisation
Technique

Approfondis ton axe : Sécurité (AZ-500) ou Identité (SC-300).

Kubernetes (CKA) en bonus si tu veux pousser DevOps.

BDD

Tuning avancé PostgreSQL, réplication, haute dispo.

NoSQL : Redis, MongoDB notions.

IA entrelacée

AIOps : détection d’anomalies avec Prometheus + modèles simples.

Log analysis : ELK + parsing IA.

Chatbot interne basé sur ta doc (RAG).

Certifs

AZ-500 (sécurité Azure) ou SC-300 (identité).

CKA ou CCNP en bonus.

Livrable : 4ᵉ projet phare (sécurité ou IAOps) + candidatures admin N3 / ingénieur junior.

Mois 19–24 — Ingénieur IA
Technique

Infra pour l’IA : GPU cloud, déploiement LLM, MLOps.

Multi-cloud avancé.

BDD

Bases vectorielles à l’échelle (pgvector, Qdrant).

Data pipelines simples.

IA entrelacée

AI-102 (Azure AI Engineer) — la vraie certif IA.

Spécialisation : AIOps ou infra pour LLM.

Certifs

AI-102.

Livrable : portfolio final + poste ingénieur cloud/IA ou ta société qui tourne.

Certifications — ordre cible
Mois	Certif
3	LFCS
4	AZ-900
5	AZ-104
10	AWS SAA + AI-900
13–18	AZ-500 ou SC-300
19–24	AI-102
Bonus	CKA ou CCNP
Bases de données — fil rouge
Mois	BDD
1	MariaDB (rappel)
2	PostgreSQL + Ansible
4–6	Azure Database for PostgreSQL
8–10	AWS RDS
12	pgvector + Redis
13–18	Tuning, réplication, NoSQL
19–24	Bases vectorielles à l’échelle
Règle : tu n’es pas DBA. Tu es ingénieur cloud qui administre une BDD.

Windows/AD — barre horizontale
Mois 1–6 : 1h/semaine max pour garder le contact.

Mois 7 : module complet (Samba AD DC + AD hybride + Entra Connect).

Après : maintenu via projets, jamais spécialité.

Atout différenciant : Linux ↔ AD (realmd/sssd/kerberos) — rare et payant.

IA — fil rouge
Phase	Rôle de l’IA
Mois 1–3	Tuteur (explique, tu comprends)
Mois 4–6	Copilote (génère, tu relis)
Mois 7–9	Composant (tu déploies des services IA)
Mois 10–12	Produit (tu livres une infra pour l’IA)
Mois 13–18	AIOps + RAG interne
Mois 19–24	Infra LLM + AI-102
Règle d’or : l’IA est ton accélérateur, pas ton pilier. Elle vient après ta base Linux/Cloud. Tu l’utilises pour comprendre, pas pour éviter de comprendre.

Règles anti-dispersion
80/20 : 80 % spécialité, 20 % curiosité (réseau, K8s, PHP, etc.).

Règle du fini : pas de nouveau sujet tant que le livrable du mois n’est pas sur GitHub, documenté.

1 certif à la fois. Jamais deux en parallèle.

Créneau fixe : 1h/jour + 3h week-end. Comme un rendez-vous client.

Date de sortie helpdesk : max 24 mois. Affichée.

IA : chaque usage documenté dans ia-notes. Si tu ne comprends pas, tu ne valides pas.

Checkpoints
Échéance	Objectif
Fin mois 3	LFCS ✅ + Ansible opérationnel + lab documenté + PostgreSQL
Fin mois 6	AZ-104 ✅ + projet phare #1 (Azure + Entra + BDD + IA)
Fin mois 10	AWS SAA ✅ + AI-900 ✅
Fin mois 12	Projet phare #3 (plateforme IA multi-cloud) + portfolio
Fin mois 18	AZ-500 ou SC-300 ✅ + 4ᵉ projet + candidatures
Fin mois 24	AI-102 ✅ + poste ingénieur cloud/IA ou société qui tourne


## Semaine par Semaine 



