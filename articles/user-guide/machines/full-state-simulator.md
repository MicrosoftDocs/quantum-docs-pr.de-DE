---
title: Full State Quantum Simulator-Quantum Development Kit
description: Erfahren Sie, wie Sie Ihre Q# Programme auf dem Microsoft Quantum Development Kit vollständigen Status Simulator ausführen.
author: anpaz-msft
ms.author: anpaz
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
no-loc:
- Q#
- $$v
ms.openlocfilehash: 632af681c5818ab7246c0f5849a8b8e716b570cb
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833370"
---
# <a name="quantum-development-kit-qdk-full-state-simulator"></a>Vollständiger Status Simulator für das Quantum Development Kit (QDK)

Das QDK bietet einen vollständigen Status Simulator, der einen Quantum-Computer auf dem lokalen Computer simuliert. Mithilfe des vollständigen Zustands Simulators können Sie in geschriebene Quantum-Algorithmen ausführen und Debuggen Q# , wobei bis zu 30 Qubits verwendet werden. Der vollständige Zustands Simulator ähnelt dem Quantum-Simulator, der in der  [Liq $ UI | \rangle $](http://stationq.github.io/Liquid/) Platform von Microsoft Research verwendet wird.

## <a name="invoking-and-running-the-full-state-simulator"></a>Aufrufen und Ausführen des vollständigen Zustands Simulators

Sie machen den vollständigen Zustands Simulator über die- `QuantumSimulator` Klasse verfügbar. Weitere Informationen finden Sie unter [Möglichkeiten zum Ausführen eines Q# Programms](xref:microsoft.quantum.guide.host-programs).

### <a name="invoking-the-simulator-from-c"></a>Aufrufen des Simulators von C #

Erstellen Sie eine Instanz der `QuantumSimulator` -Klasse, und übergeben Sie Sie dann an die- `Run` Methode eines Quantum-Vorgangs zusammen mit allen weiteren Parametern.
```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

Da die- `QuantumSimulator` Klasse die- <xref:System.IDisposable> Schnittstelle implementiert, muss die-Methode aufgerufen werden, `Dispose` Wenn die Instanz des Simulators nicht mehr benötigt wird. Die beste Möglichkeit hierfür ist das Einschließen der simulatordeklaration und der Vorgänge in einer [using](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/using-statement) -Anweisung, die automatisch die- `Dispose` Methode aufruft.

### <a name="invoking-the-simulator-from-python"></a>Aufrufen des Simulators aus python

Verwenden Sie die Methode " [simulieren ()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) " aus der Q# Python-Bibliothek mit dem importierten Q# Vorgang:

```python
qubit_result = myOperation.simulate()
```

### <a name="invoking-the-simulator-from-the-command-line"></a>Aufrufen des Simulators über die Befehlszeile

Wenn ein Q# Programm von der Befehlszeile aus ausgeführt wird, ist der vollständige Zustands Simulator der Standardziel Computer. Optional können Sie den Parameter **--Simulator** (oder **-s** ) verwenden, um den gewünschten Zielcomputer anzugeben. Beide der folgenden Befehle führen ein Programm mithilfe des vollständigen Zustands Simulators aus. 

```dotnetcli
dotnet run
dotnet run -s QuantumSimulator
```

### <a name="invoking-the-simulator-from-juptyer-notebooks"></a>Aufrufen des Simulators aus juptyer Notebooks

Verwenden Sie den I Q# Magic-Befehl [% simulieren](xref:microsoft.quantum.iqsharp.magic-ref.simulate) , um den Q# Vorgang auszuführen.

```
%simulate myOperation
```
## <a name="seeding-the-simulator"></a>Seeding des Simulators

Standardmäßig verwendet der vollständige Zustands Simulator einen Zufallszahlengenerator, um die Quantum-Zufälligkeit zu simulieren. Zu Testzwecken ist es manchmal sinnvoll, deterministische Ergebnisse zu haben. In einem c#-Programm können Sie dies erreichen, indem Sie über den-Parameter einen Ausgangswert für den Zufallszahlengenerator im `QuantumSimulator` Konstruktor bereitstellen `randomNumberGeneratorSeed` .

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="configuring-threads"></a>Konfigurieren von Threads

Der vollständige Zustands Simulator verwendet [OpenMP](http://www.openmp.org/) , um die erforderliche lineare Algebra zu parallelisieren. Standardmäßig verwendet OpenMP alle verfügbaren Hardwarethreads, was bedeutet, dass Programme mit einer kleinen Anzahl von Qubits häufig langsam ausgeführt werden, da die erforderliche Koordination die eigentliche Arbeit vergrenzt. Sie können dieses Problem beheben, indem Sie die Umgebungsvariable `OMP_NUM_THREADS` auf eine kleine Zahl festlegen. Konfigurieren Sie als Faustregel einen Thread für bis zu vier Qubits und dann einen zusätzlichen Thread pro Qubit. Möglicherweise müssen Sie die Variable abhängig von Ihrem Algorithmus anpassen.

## <a name="see-also"></a>Weitere Informationen

- [Ressourcenschätzung für Quantencomputer](xref:microsoft.quantum.machines.resources-estimator)
- [Toffoli-Simulator für Quantencomputer](xref:microsoft.quantum.machines.toffoli-simulator)
- [Quantum-Ablauf Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)