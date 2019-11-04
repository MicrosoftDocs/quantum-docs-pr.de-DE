---
title: Quantum Development Kit-vollständiger Status Simulator | Microsoft-Dokumentation
description: Übersicht über den voll Zustands Simulator von Microsoft Quantum Development Kit
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 12/7/2017
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: ab0e65765d27e301a59948d7c02105a523022e68
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184677"
---
# <a name="quantum-development-kit-full-state-simulator"></a>Vollständiger Status Simulator für das Quantum Development Kit

Das Quantum Development Kit bietet einen vollständigen Quantum-Simulator ähnlich dem [Liq $ UI | \rangle $](http://stationq.github.io/Liquid/) von Microsoft Research.
Dieser Simulator kann zum Ausführen und Debuggen von in Q # geschriebenen Quantenalgorithmen auf dem Computer verwendet werden.

Dieser Quantum-Simulator wird über die `QuantumSimulator`-Klasse verfügbar gemacht. Um den Simulator zu verwenden, erstellen Sie einfach eine Instanz dieser Klasse, und übergeben Sie Sie an die `Run`-Methode des Quantum-Vorgangs, den Sie zusammen mit den restlichen Parametern ausführen möchten:

```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

## <a name="idisposable"></a>IDisposable

Die `QuantumSimulator`-Klasse implementiert <xref:System.IDisposable>. Daher sollte die `Dispose`-Methode aufgerufen werden, sobald die Instanz des Simulators nicht mehr verwendet wird. Die beste Möglichkeit hierfür ist das Einschließen des Simulators innerhalb einer `using`-Anweisung, wie im obigen Beispiel gezeigt.

## <a name="seed"></a>säen

Der `QuantumSimulator` verwendet einen Zufallszahlengenerator, um die Quantum-Zufälligkeit zu simulieren. Zu Testzwecken ist es manchmal sinnvoll, deterministische Ergebnisse zu haben. Dies kann erreicht werden, indem ein Ausgangswert für den Zufallszahlengenerator im Konstruktor der `QuantumSimulator`über den Parameter "`randomNumberGeneratorSeed`" bereitgestellt wird:

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="threads"></a>Threads

Der `QuantumSimulator` verwendet [OpenMP](http://www.openmp.org/) , um die erforderliche lineare Algebra zu parallelisieren. Standardmäßig verwendet OpenMP alle verfügbaren Hardwarethreads, was bedeutet, dass Programme mit einer kleinen Anzahl von Qubits häufig langsam ausgeführt werden, da die eigentliche Arbeit durch die erforderliche Koordination in den Mittelpunkt gestellt wird. Dies kann korrigiert werden, indem die Umgebungsvariable `OMP_NUM_THREADS` auf eine kleine Zahl festgelegt wird. Als sehr grobe Faustregel ist 1 Thread für bis zu ungefähr 4 Qubits geeignet, und dann ist ein zusätzlicher Thread pro Qubit gut, obwohl dies stark von Ihrem Algorithmus abhängig ist.

