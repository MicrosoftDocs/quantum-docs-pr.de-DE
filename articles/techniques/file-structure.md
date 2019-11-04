---
title: Einführung in die Quantum-Entwicklungstechniken | Microsoft-Dokumentation
description: Einführung in die Quantum-Entwicklungstechniken
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 702d23293a1c340ddd3d7032d0e05294345469b2
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442559"
---
# <a name="q-program-overview"></a>Q #-Programmübersicht

F # ist eine skalierbare, domänenspezifische Programmiersprache mit mehreren Paradigmen für das Quantum Computing. F # ist eine Quantum-Programmiersprache, mit der Sie beschreiben können, wie Anweisungen auf Quantum-Computern ausgeführt werden. Die Computer, die als Zielgruppe eingesetzt werden können, reichen von Simulatoren bis zur eigentlichen Quantum-Hardware. F # ist skalierbar: Es kann verwendet werden, um einfache Demonstrationsprogramme wie Teleports zu schreiben, die auf wenigen Qubits ausgeführt werden. Sie unterstützt aber auch das Schreiben großer, anspruchsvoller Programme, wie z. b. Simulationen komplexer Moleküle, die große Computer mit Millionen von Qubits erfordern. Auch wenn große physische Computer noch in der Zukunft liegen, ermöglicht Q # es Programmierern, jetzt komplexe Quantum-Algorithmen zu programmieren. Weitere Informationen finden Sie unter Unterstützung für verschiedene Aufgaben, z. b. Debuggen, Profilerstellung, Ressourcenschätzung und bestimmte spezielle Simulationen auf skalierbare Weise. 

Aus technischer Sicht kann ein Quantum-Programm als ein bestimmter Satz klassischer Funktionen angesehen werden, die beim Aufrufen von Quantum-Verbindungen als Nebeneffekte generieren. Eine wichtige Konsequenz dieser Ansicht besteht darin, dass ein in Q # geschriebenes Programm Qubits selbst nicht direkt modelliert, sondern vielmehr beschreibt, wie ein klassischer Steuerungscomputer mit diesen Qubits interagiert.
Entwurfs bedingt definiert f # daher nicht die Quantum-Zustände oder andere Eigenschaften von Quantum-Mechanismen direkt, sondern indirekt durch die Aktion der verschiedenen Unterroutinen, die in der Sprache definiert sind.
Sehen Sie sich beispielsweise den Status $ \ket{+} = \left (\ket{0} + \ket{1}\right)/\sqrt{2}$ an, der im Handbuch für die [Quantum Computing-Konzepte](xref:microsoft.quantum.concepts.intro) erläutert wird.
Um diesen Status in Q # vorzubereiten, verwenden wir die Fakten, die die Qubits im $ \ket{0}$ State initialisiert werden, und die $ \ket{+} = h\ket{0}$, wobei $H $ die Hadamard-Transformation ist:

```qsharp
using (qubit = Qubit()) {
    // At this point, qubit is in the state |0〉.
    H(qubit);
    // We've now applied H, such that our qubit is in H|0〉 = |+〉, as we wanted.
}
```
## <a name="q-tranformations-of-quantum-states"></a>Q #-Tranformationen von Quantum-Zuständen

Wichtig: beim Schreiben des obigen Programms haben wir nicht explizit auf den Bundesstaat in Q # verwiesen, sondern vielmehr beschrieben, wie der Zustand von unserem Programm *transformiert* wurde.
Ähnlich wie ein Grafik-Shader-Programm eine Beschreibung von Transformationen zu jedem Scheitelpunkt sammelt, sammelt ein Quantum-Programm in Q # Transformationen in Quantum-Zuständen.
Dies ermöglicht es uns, unabhängig davon, was ein Quantum-Status *ist* , auch auf jedem Zielcomputer zu sein, der je nach Computer unterschiedliche Interpretationen aufweisen kann. 

Aus der Perspektive eines Q #-Programms ist ein Qubit ein vollständig undurchsichtiger Verweis auf die interne Struktur eines Ziel Computers.
Ein Q #-Programm kann nicht auf den Zustand eines Qubit, seine Darstellung auf einem Zielcomputer oder auch darauf hinweisen, ob es sich um das gleiche Qubit wie jedes andere Qubit handelt, das für das Programm verfügbar ist.
Ein Programm kann z. b. Vorgänge wie `Measure` zum Erlernen von Informationen aus einem Qubit und zum Abrufen von Vorgängen, z. b. `X` und `H`, um auf den Zustand eines Qubit zu reagieren.
Diese Vorgänge haben keine intrinsische Definition innerhalb der Sprache und werden nur durch den Zielcomputer, der zum Ausführen eines bestimmten Q #-Programms verwendet wird, konkretisiert.
Ein Q #-Programm kombiniert diese Vorgänge neu, wie von einem Zielcomputer definiert, um neue Vorgänge auf höherer Ebene zu erstellen, um die Quantum-Berechnung auszudrücken.
Auf diese Weise vereinfacht f # das Ausdrücken der Logik zugrunde liegenden Quantum-und Hybrid-Quantum-Hybrid Algorithmen und ist gleichzeitig in Bezug auf die Struktur eines Ziel Computers oder Simulators allgemein.

## <a name="q-operations-and-functions"></a>F #-Vorgänge und-Funktionen

Konkret besteht ein Q #-Programm aus mindestens einem *Vorgang*, einer oder mehreren *Funktionen*und benutzerdefinierten Typen. Vorgänge werden verwendet, um die Transformationen des Zustands eines Quantum-Computers zu beschreiben, und sind der grundlegendste Baustein von Q #-Programmen. Jeder in Q # definierte Vorgang kann dann eine beliebige Anzahl anderer Vorgänge aufzurufen, einschließlich der integrierten System *internen Vorgänge,* die von einem Zielcomputer implementiert werden.
Bei der Kompilierung wird jeder Vorgang als .NET-Klassentyp dargestellt, der den Ziel Computern bereitgestellt werden kann.

Im Gegensatz zu Vorgängen werden Funktionen verwendet, um rein klassisches Verhalten zu beschreiben, und Sie haben keine Auswirkungen, außer wenn Sie klassische Ausgabewerte berechnen. F # ist eine stark typisierte Sprache und enthält eine Reihe integrierter primitiver Typen sowie Unterstützung für benutzerdefinierte Typen. 

Im weiteren Verlauf dieses Handbuchs erfahren Sie, wie Sie verschiedene sprach Konzepte und-Konstrukte verwenden, um uns bei der Definition komplexer Quantum-Programme über die grundlegenden Bausteine von Vorgängen, Funktionen und Typen zu unterstützen. 

## <a name="structure-of-q-source-files"></a>Struktur von f #-Quelldateien

Eine Q #-Quelldatei besteht minimal aus einer *Namespace Deklaration*, die einen .NET-Namespace angibt, der die Definitionen in der Quelldatei enthält.
Definitionen aus anderen Q #-Quelldateien und-Bibliotheken können mithilfe der `open`-Anweisung eingeschlossen werden.
Beispielsweise werden die meisten Vorgänge, die grundlegende Gates definieren, im <xref:microsoft.quantum.intrinsic>-Namespace definiert.
Um dies für den Code verfügbar zu machen, `open` Sie einfach den Namespace am Anfang jeder Datei:

```qsharp
namespace Example {
    open Microsoft.Quantum.Intrinsic;

    // ...
}
```

Innerhalb eines Namespace kann jede f #-Quelldatei eine beliebige Kombination von *Vorgängen*, *Funktionen*und *benutzerdefinierten Typen*definieren.
Im restlichen Teil dieses Abschnitts werden diese wiederum beschrieben und Beispiele dafür bereitgestellt, wie Sie in der Praxis verwendet werden können, um nützliche Quantum-Programme zu erstellen.
