---
title: I Q# Magic-Befehle
description: Kurz Referenzseite für I Q# Magic-Befehle mit Q# jupyter Notebooks
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
uid: microsoft.quantum.guide.quickref.iqsharp
no-loc:
- Q#
- $$v
ms.openlocfilehash: 1d2d092588e1a5c69d12e5d50377e3e26412c094
ms.sourcegitcommit: 75c4edc7c410cc63dc8352e2a5bef44b433ed188
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/25/2020
ms.locfileid: "88863693"
---
# <a name="ino-locq-magic-commands"></a>I Q# Magic-Befehle

### <a name="general"></a>Allgemein

- [`%config`](xref:microsoft.quantum.iqsharp.magic-ref.config): Ermöglicht das Festlegen oder Abfragen von Konfigurationsoptionen.
- [`%estimate`](xref:microsoft.quantum.iqsharp.magic-ref.estimate): Führt eine bestimmte Funktion oder einen Vorgang auf dem resourcesestimator-Zielcomputer aus.
- [`%lsmagic`](xref:microsoft.quantum.iqsharp.magic-ref.lsmagic): Gibt eine Liste aller zurzeit verfügbaren Magic-Befehle zurück.
- [`%lsopen`](xref:microsoft.quantum.iqsharp.magic-ref.lsopen): Listet die aktuell geöffneten Namespaces und ihre Aliase auf.
- [`%package`](xref:microsoft.quantum.iqsharp.magic-ref.package): Bietet die Möglichkeit, ein nuget-Paket zu laden.
- [`%performance`](xref:microsoft.quantum.iqsharp.magic-ref.performance): Meldet die aktuellen Leistungsmetriken für diesen Kernel.
- [`%project`](xref:microsoft.quantum.iqsharp.magic-ref.project): Bietet die Möglichkeit zum Anzeigen oder Hinzufügen von Q# Projekt verweisen. 
- [`%simulate`](xref:microsoft.quantum.iqsharp.magic-ref.simulate): Führt eine bestimmte Funktion oder einen Vorgang auf dem quantumschlag-Zielcomputer aus.
- [`%toffoli`](xref:microsoft.quantum.iqsharp.magic-ref.toffoli): Führt eine bestimmte Funktion oder einen Vorgang auf dem Zielcomputer "tffolisimulator" aus.
- [`%who`](xref:microsoft.quantum.iqsharp.magic-ref.who): Listet die Q# Vorgänge auf, die in der aktuellen Sitzung verfügbar sind.
- [`%workspace`](xref:microsoft.quantum.iqsharp.magic-ref.workspace): Stellt Aktionen bereit, die sich auf den aktuellen Arbeitsbereich beziehen.

### <a name="azure-quantum-integration"></a>Azure-Quantum-Integration

- [`%azure.connect`](xref:microsoft.quantum.iqsharp.magic-ref.azure.connect): Stellt eine Verbindung mit einem Azure Quantum Workspace her oder zeigt den aktuellen Verbindungsstatus an.
- [`%azure.execute`](xref:microsoft.quantum.iqsharp.magic-ref.azure.execute): Führt einen Auftrag in einem Azure Quantum-Arbeitsbereich aus.
- [`%azure.jobs`](xref:microsoft.quantum.iqsharp.magic-ref.azure.jobs): Hiermit wird eine Liste der Aufträge im aktuellen Azure Quantum-Arbeitsbereich angezeigt.
- [`%azure.output`](xref:microsoft.quantum.iqsharp.magic-ref.azure.output): Zeigt die Ergebnisse für einen Auftrag im aktuellen Azure Quantum-Arbeitsbereich an.
- [`%azure.status`](xref:microsoft.quantum.iqsharp.magic-ref.azure.status): Zeigt den Status eines Auftrags im aktuellen Azure Quantum-Arbeitsbereich an.
- [`%azure.submit`](xref:microsoft.quantum.iqsharp.magic-ref.azure.submit): Übermittelt einen Auftrag an einen Azure Quantum-Arbeitsbereich.
- [`%azure.target`](xref:microsoft.quantum.iqsharp.magic-ref.azure.target): Legt das aktive Ausführungs Ziel für die Q# Auftrags Übermittlung in einem Azure Quantum-Arbeitsbereich fest oder zeigt es an.

### <a name="chemistry-from-microsoftquantumchemistry-package"></a>Chemie (aus dem Microsoft. Quantum. Chemistry-Paket)

- [`%chemistry.broombridge`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.broombridge): Lädt und gibt die Darstellung der broombridge-elektronischen Strukturprobleme aus einer bestimmten YAML-Datei zurück.
- [`%chemistry.encode`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.encode): Codiert ein Fermion-hamiltonan in ein Format, das von verwendet werden können Q# .
- [`%chemistry.fh.add_terms`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.add_terms): Fügt einem Fermion-hamiltonan Bedingungen hinzu.
- [`%chemistry.fh.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.load): Lädt den Fermion-hamiltonan für ein elektronisches Strukturproblem. Das Problem wird aus einer Datei geladen oder als Argument übergeben.
- [`%chemistry.inputstate.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.inputstate.load): Lädt das Problem der elektronischen broombridge-Struktur und gibt den ausgewählten Eingabe Status zurück.

### <a name="katas-from-microsoftquantumkatas-package"></a>Katas (aus dem Microsoft. Quantum. Katas-Paket)

- [`%kata`](xref:microsoft.quantum.iqsharp.magic-ref.kata): Führt einen einzelnen Test aus und meldet, ob der Test erfolgreich abgeschlossen wurde.
- [`%check_kata`](xref:microsoft.quantum.iqsharp.magic-ref.check_kata): Überprüft die Verweis Implementierung für den Test einer einzelnen Kata.
    Insbesondere ersetzt Sie die Verweis Implementierung für eine einzelne Aufgabe in der Zelle und meldet, ob der Test erfolgreich ausgeführt wurde.
