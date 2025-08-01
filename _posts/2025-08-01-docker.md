---
layout: post
title:  "Docker bereinigen"
date:   2025-08-01 10:13:27 +0100
categories: docker
lang: de
tags: docker
---


## 🧹 **Docker Bereinigung – kompakte Übersicht**

### 🔥 Alles ungenutzte entfernen (Container, Images, Netzwerke, Volumes):

```bash
docker system prune -a --volumes -f
```

---

### 🧼 Einzelne Komponenten gezielt bereinigen:

| Zweck                 | Befehl                      |
| --------------------- | --------------------------- |
| Gestoppte Container   | `docker container prune -f` |
| Nicht genutzte Images | `docker image prune -a -f`  |
| Ungenutzte Netzwerke  | `docker network prune -f`   |
| Ungenutzte Volumes    | `docker volume prune -f`    |

---

### 📊 Speicherverbrauch anzeigen:

```bash
docker system df -v
```

---

### 💣 Alles restlos löschen (Vorsicht!):

```bash
systemctl stop docker
rm -rf /var/lib/docker
systemctl start docker
```

> 🔴 **Löscht alles**: Images, Container, Netzwerke, Volumes, Cache, Overlay2 etc.

---

Wenn du willst, kann ich daraus auch ein kleines Bash-Skript bauen (`docker-clean.sh`) mit optionaler Interaktivität.
