---
title: Einführung in das Quantum Machine Learning-Paket | Microsoft-Dokumentation
description: Einführung in das Quantum Machine Learning-Paket
author: QuantumWriter
ms.author: alexeib@microsoft.com
ms.date: 12/5/2019
ms.topic: article
uid: microsoft.quantum.machine-learning.concepts.intro
ms.openlocfilehash: 7f22d5d3212890abc764f88693937b534466170f
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2020
ms.locfileid: "77907850"
---
# <a name="introduction-to-the-quantum-machine-learning-library"></a>Einführung in die Quantum Machine Learning-Bibliothek

Die Quantum Machine Learning-Bibliothek ist eine API, die in Q# geschrieben ist. Hiermit können Sie Machine Learning-Hybridexperimente durchführen, bei denen das Quantencomputing und das klassische Computing genutzt wird. Mit der Bibliothek haben Sie folgende Möglichkeiten:

- Laden Ihrer eigenen Daten für die Klassifizierung mit Quantensimulatoren

- Verwenden von Beispielen und Tutorials als Einführung in Quantum Machine Learning

Die zu erwartende Leistung ist im Vergleich zu aktuellen klassischen Machine Learning-Frameworks eher niedrig. (Bedenken Sie, dass alle Vorgänge zusätzlich zur Simulation eines Quantengeräts ausgeführt werden, für die bereits ein hoher Rechenaufwand anfällt.)

Diese Dokumentation soll die folgenden Zwecke erfüllen:

- Kurze Einführung in Machine Learning-Tools (in Q\# geschrieben) für Machine Learning-Hybridvorgänge mit Quantencomputing und klassischem Computing
- Einführung in Machine Learning-Konzepte mit dem Schwerpunkt auf deren Realisierung in Klassifizierern für Quantenschaltungen (auch als sequenzielle Klassifizierer für Quantencomputing bezeichnet)
- Bereitstellung von Tutorials zu den Grundlagen für den Einstieg in die Nutzung der Bibliothekstools
- Beschreibung der Trainings- und Validierungsmethoden für diese Klassifizierer und deren Übersetzung in spezifische Q\#-Vorgänge der Bibliothek

Das in dieser Bibliothek implementierte Modell basiert auf dem Trainingsschema für Quantencomputing und klassisches Computing aus dem Artikel zu [Quantenklassifizierern für Schaltungen](https://arxiv.org/abs/1804.00633).
