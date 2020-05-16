---
title: IQ#-Magic-Befehle
description: 'Kurz Referenzseite für IQ # Magic-Befehle mit Q # jupyter Notebooks'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
uid: microsoft.quantum.guide.quickref.iqsharp
ms.openlocfilehash: 0cd1a2289132e2760a21fd9d4f4083696353e271
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431018"
---
# <a name="iq-magic-commands"></a>IQ#-Magic-Befehle

### <a name="general"></a>Allgemein

- `%config`: Legt Konfigurationseinstellungen fest oder ruft Sie ab.
- `%estimate`: Führt eine bestimmte Funktion oder einen Vorgang auf dem quantumschlag-Zielcomputer aus.
- `%lsmagic`: Gibt eine Liste aller zurzeit verfügbaren Magic-Befehle zurück.
- `%package`: Bietet die Möglichkeit, ein nuget-Paket zu laden.
- `%performance`: Meldet die aktuellen Leistungsmetriken für diesen Kernel.
- `%simulate`: Führt eine bestimmte Funktion oder einen Vorgang auf dem quantumschlag-Zielcomputer aus.
- `%toffoli`: Führt eine angegebene Funktion oder einen Vorgang auf dem Bereitstellungs Zielcomputer für den Dienst des Dienst-Simulators aus.
- `%who`: Stellt Aktionen bereit, die sich auf den aktuellen Arbeitsbereich beziehen.
- `%workspace`: Gibt eine Liste aller Vorgänge und Funktionen zurück, die in der aktuellen Sitzung definiert sind, entweder interaktiv oder aus dem aktuellen Arbeitsbereich geladen.

### <a name="chemistry"></a>Chemi

- `%chemistry.broombridge`: Lädt und gibt die Darstellung der broombridge-elektronischen Strukturprobleme aus einer bestimmten YAML-Datei zurück.
- `%chemistry.encode`: Codiert ein Fermion-hamiltonan in ein Format, das von Q # verwendet werden können.
- `%chemistry.fh.add_terms`: Fügt einem Fermion-hamiltonan Bedingungen hinzu.
- `%chemistry.fh.load`: Lädt den Fermion-hamiltonan für ein elektronisches Strukturproblem. Das Problem wird aus einer Datei geladen oder als Argument übergeben.
- `%chemistry.inputstate.load`: Lädt das Problem der elektronischen broombridge-Struktur und gibt den ausgewählten Eingabe Status zurück.

### <a name="from-microsoftquantumkatas-package"></a>Aus dem Paket "Microsoft. Quantum. Katas"

- `%kata`: Führt einen einzelnen Test aus und meldet, ob der Test erfolgreich abgeschlossen wurde.
- `%check_kata`: Überprüft die Verweis Implementierung für den Test einer einzelnen Kata.
    Insbesondere ersetzt Sie die Verweis Implementierung für eine einzelne Aufgabe in der Zelle und meldet, ob der Test erfolgreich ausgeführt wurde.
