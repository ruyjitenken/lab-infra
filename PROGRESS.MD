# Progression

## Semaine 1 (Mois 1)
- [x] VM debian-lab-01 créée (Proxmox 192.168.1.10, IP .133)
- [x] SSH actif
- [x] Accès WireGuard distant
- [x] Renommage delalily → debian-lab-01
- [x] sudo installé, terry dans groupe sudo
- [x] fwupd-refresh disable + mask + reset-failed
- [ ] Jour 2 : sécurisation SSH (clés, root off, fail2ban)

## Décisions prises
- Spécialité : Linux + Cloud/Automatisation (Azure d'abord, AWS mois 8-10)
- Windows/AD : barre horizontale, module complet mois 7
- BDD : PostgreSQL priorité, MySQL acquis, pgvector mois 12
- IA : accélérateur, pas pilier

## Semaine 1 (suite)
- [x] Clé SSH ed25519 générée (PC perso)
- [x] Clé publique copiée sur debian-lab-01
- [x] PasswordAuthentication no
- [x] PermitRootLogin no
- [x] fail2ban installé et actif

- [x] Clé SSH ed25519 (PC perso = raspberrypi)
- [x] /etc/ssh/sshd_config.d/01-custom.conf : PermitRootLogin no, PasswordAuthentication no, AllowUsers terry
- [x] fail2ban actif
- [x] Test : root refusé (publickey), terry accepté par clé

## Semaine 1 (fin)
- [x] Système à jour (apt full-upgrade)
- [x] LVM : VG delalily-vg avec /, /var, /tmp, /home, swap (hérité de l'install Debian)
- [x] /home/terry en 700, umask 022, terry dans sudo
- Note : VG nommée delalily-vg (cosmétique, à renommer plus tard si besoin)

- [x] VM2 : ubuntu-lab-02 (192.168.1.15) — user terry + sudo + clé SSH
- [x] lary = user install (groupes par défaut), non utilisé pour Ansible
- [x] Ansible ping OK vers ubuntu-lab-02
- [x] Cause timeout : sudo-rs (Ubuntu 25.10+) ≠ prompt Ansible
- [x] Fix : ansible_become_exe=/usr/bin/sudo.ws dans inventory.ini
- [x] Playbook premier.yml : curl, cron, fichier test
- [x] 1ère exécution : changed=1
- [X] 2ᵉ exécution : changed=0 (idempotence à confirmer)
- [x] Fix sudo-rs : ansible_become_exe=/usr/bin/sudo.ws
