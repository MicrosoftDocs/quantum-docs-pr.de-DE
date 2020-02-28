---
title: Vollständiger Zustands Simulator
description: 'Erfahren Sie, wie Sie Ihre Q #-Programme auf dem Microsoft Quantum Development Kit vollständigen Status Simulator ausführen.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 12/7/2017
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: f73abbc4366b003e4b22366ed83ca9c897737307
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906116"
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

## <a name="seed"></a>Seed

Der `QuantumSimulator` verwendet einen Zufallszahlengenerator, um die Quantum-Zufälligkeit zu simulieren. Zu Testzwecken ist es manchmal sinnvoll, deterministische Ergebnisse zu haben. Dies kann erreicht werden, indem ein Ausgangswert für den Zufallszahlengenerator im Konstruktor der `QuantumSimulator`über den Parameter "`randomNumberGeneratorSeed`" bereitgestellt wird:

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="threads"></a>Threads

Der `QuantumSimulator` verwendet [OpenMP](http://www.openmp.org/) , um die erforderliche lineare Algebra zu parallelisieren. OpenMP verwendet standardmäßig alle verfügbaren Hardwarethreads, weshalb Programme mit wenigen Qubits häufig langsam ausgeführt werden, stellt die Koordination die tatsächliche Arbeit in den Schatten. Dies kann korrigiert werden, indem die Umgebungsvariable `OMP_NUM_THREADS` auf eine kleine Zahl festgelegt wird. Als grobe Faustregel gilt, dass 1 Thread für etwa 4 Qubits genügt und dann für jeden weiteren Qubit ein weiterer Thread benötigt wird. Dies hängt jedoch stark von Ihrem Algorithmus ab.

