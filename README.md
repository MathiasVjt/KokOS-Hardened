# KokOS Linux Hardened

KokOS (Kompaktes. Offenes. Kinderleichtes. Operating System) ist eine Linux Distribution, welche genau auf die Anforderungen der HTL Wien West angefertigt wurde.

KokOS basiert auf Arch Linux und nutzt KDE als Desktopumgebung, Arch wurde als Basis ausgewählt um einen möglichsten minimalistischen Anfang zu haben ohne auf grundlegende Funktionen zu verzichten. 

# Features

## Active Directory Integration

Rechner auf denen KokOS installiert wurde können mit nur einem Klick der Active Directory Domäne beitreten. Microsoft Accouns können somit zum einloggen benutzt werden, was den Vorteil hat, dass man sich den Account auf dem Rechner mit keinem mehr teilen muss.

## Kontrolle

Lehrer können über das Tool **Veyon** ganz einfach alle PCs überwachen bzw steuern um sicherzustellen, dass SchülerInnen jederzeit arbeiten.

## Sicherheit

KokOS setzt mehrere Maßnahmen um die Sicherheit an den Schulrechnern zu gewährleisten

* KokOS wird standardmäßig mit dem Hardened Kernel ausgeliefert, welcher von Haus aus deutlich erhöhte Sicherheit bietet.
* SchülerInnen können nicht mehr über Grub sich Root Rechte verschaffen wie in der aktuellen Schul-Distro, da Grub nicht mehr zugänglich ist.
* Da wir die Distribution von Grund auf erstellt haben, wurde besonders drauf geachtet nur das zu aktivieren, was auch wirklich notwendig ist, was zu einer kleineren Angriffsfläche führt.

## Anpassbarkeit

NutzerInnen dürfen vorgegebene KDE Design Optionen konfigurieren, was es jedem / jeder SchülerIn ermöglicht, seinen / ihren Desktop so zu konfigurieren wie man möchte.

## Offen

KokOS Linux, das KokOS Repository, wie auch alle KokOS Design Elemente sind nach der GPLv3 Lizenz Open-Source. 

# Grundsätzliches

# Pacman.conf in archiso/airootfs/etc/

Diese pacman.conf wird dann tatsächlich am installierten System verwendet und *nicht* beim kompilieren der ISO. 


# Archiso/packages.x86_64

Neue Pakete können über die Datei *archiso/packages.x86-64* hinzugefügt werden. 
Hier müssen auch alle Treiber hinzugefügt werden die in der ISO verwendet werden. (z.B. xf86-video-intel, nvidia, etc...)


# Build Prozess


Zum kompilieren der fertigen ISO können die Skripts im folgenden Ordner genutzt werden:

<b>installation-scripts</b>

script 30 löscht den Cache und lädt alles noch einmal herunter.

script 40 nutzt den derzeitigen Pacman Cache.

Die ISO findet man dann in:

 ~/KokOS-Iso-Hardened-Out
