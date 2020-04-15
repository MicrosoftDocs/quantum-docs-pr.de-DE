---
title: Quantum Development Kit-Simulator
description: Erfahren Sie mehr über den Microsoft QDK-Simulator für den Einsatz von Microsoft QDK, einen speziellen Zweck-Quantum-Simulator, der mit Millionen von Qubits verwendet werden kann
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 01/16/2019
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
ms.openlocfilehash: 8a29caaa0fa058600a74e7d130e644374cbfa19c
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907017"
---
# <a name="quantum-development-kit-toffoli-simulator"></a>Quantum Development Kit-Simulator

Das Quantum Development Kit bietet einen deffoli-Simulator, bei dem es sich um einen Zweck Simulator handelt, mit dem Quantum-Algorithmen simuliert werden können, die auf x-, CNOT-und multigesteuerte X-Quantum-Vorgänge beschränkt sind (alle klassischen Logik und Berechnungen sind verfügbar).

Während der Vorgang "deffoli" in der Operation wesentlich eingeschränkter ist als der [vollständige Zustands Simulator](xref:microsoft.quantum.machines.full-state-simulator), kann er weitaus mehr Qubits simulieren.
Der-Simulator kann mit Millionen von Qubits verwendet werden, während der vollständige Zustands Simulator im Allgemeinen auf ungefähr 30 beschränkt ist.
Es kann einen begrenzten Satz von Quantum-Algorithmen ausführen und Debuggen, die in Q# auf dem Computer geschrieben wurden. Beispielsweise können Oracles, die Boolesche Funktionen evaluieren, mithilfe dieser Gates implementiert werden. Diese werden daher bei einer großen Anzahl von Qubits mit diesem Simulator getestet.

Dieser Quantum-Simulator wird über die `ToffoliSimulator`-Klasse verfügbar gemacht.
Um den Simulator zu verwenden, erstellen Sie einfach eine Instanz dieser Klasse, und übergeben Sie Sie an die `Run`-Methode des Quantum-Vorgangs, den Sie zusammen mit den restlichen Parametern ausführen möchten:

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

## <a name="other-operations"></a>Andere Vorgänge

Der `ToffoliSimulator` unterstützt Drehungen und exponentiierte Paulis, z. b. `R` und `Exp`, wenn der resultierende Vorgang gleich `X` oder der Identität ist.

Messungen und Assert werden unterstützt, aber nur in der Pauli-`Z` Basis.
Beachten Sie, dass die Wahrscheinlichkeit einer Messung immer entweder 0 oder 1 ist. Es gibt keine Zufälligkeit im-Simulator von "".

`DumpMachine` und `DumpRegister` werden unterstützt.
Beide geben den aktuellen `Z`basierten Status jedes Qubit, ein Qubit pro Zeile, aus.

## <a name="qubitcount"></a>Qubitcount

Standardmäßig wird von der `ToffoliSimulator` Speicherplatz für 65.536 Qubits zugewiesen.
Wenn der Algorithmus mehr als diesen Wert erfordert, können Sie die Anzahl der Qubits ändern, indem Sie einen Wert für den `qubitCount`-Parameter für den Konstruktor bereitstellen.
Jedes zusätzliche Qubit erfordert ein zusätzliches Byte Arbeitsspeicher, sodass die Anzahl der benötigten Qubits nicht signifikant ist.

Beispiel:

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```
