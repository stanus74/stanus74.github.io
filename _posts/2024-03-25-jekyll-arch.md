---
layout: post
title:  "Install Jekyll on Arch Linux"
date:   2024-03-25 19:13:27 +0100
categories: jekyll arch
---
```
# Jekyll Installation und Einrichtung

In diesem Beitrag gehen wir durch die Installation von Jekyll, einem beliebten statischen Seiten-Generator, der in Ruby geschrieben ist. Wir werden auch sehen, wie man Ruby über einen Version-Manager wie rbenv oder RVM installiert. Diese Anleitung ist kompatibel mit macOS und Linux.

## Schritt 1: Installation von Ruby

Da Jekyll in Ruby geschrieben ist, beginnen wir mit der Installation von Ruby. Die Verwendung eines Ruby-Version-Managers wie `rbenv` oder `RVM` wird empfohlen, um verschiedene Ruby-Versionen zu verwalten.

### rbenv

#### Installation auf macOS:

```bash
brew install rbenv
```

#### Installation auf Linux:

```bash
sudo apt update
sudo apt install -y rbenv
sudo apt-get install ruby-build
```

#### Initialisierung von rbenv:

Füge `rbenv init` zu deiner Shell-Startdatei hinzu:

```bash
echo 'eval "$(rbenv init -)"' >> ~/.bashrc
# Für Zsh
echo 'eval "$(rbenv init -)"' >> ~/.zshrc
```

Starte deine Shell neu oder führe die Initialisierung aus:

```bash
eval "$(rbenv init -)"
```

#### Installiere eine Ruby-Version:

```bash
rbenv install 2.7.2
rbenv global 2.7.2
```

### RVM

#### Installation:

```bash
\curl -sSL https://get.rvm.io | bash -s stable
```

#### Ruby installieren:

```bash
rvm install ruby
rvm use ruby --default
```

## Schritt 2: Installation von Jekyll

Mit Ruby installiert, kannst du Jekyll und Bundler installieren.

```bash
gem install jekyll bundler
```

## Schritt 3: Erstellen eines neuen Jekyll-Projekts

Erstelle ein neues Jekyll-Projekt mit:

```bash
jekyll new mein_blog
```

Wechsle in das Projektverzeichnis:

```bash
cd mein_blog
```

## Starte den Jekyll-Server:

Um deinen neu erstellten Jekyll-Blog zu sehen, starte den Jekyll-Server:

```bash
bundle exec jekyll serve
```

Jetzt kannst du deinen Webbrowser öffnen und `http://localhost:4000` besuchen, um deine Jekyll-Seite zu sehen.
```









[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
