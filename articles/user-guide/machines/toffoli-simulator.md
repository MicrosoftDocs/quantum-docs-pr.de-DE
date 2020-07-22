---
title: Quantum-zu-ffoli-Simulator-Quantum Development Kit
description: Erfahren Sie mehr über den Microsoft QDK-Simulator für den Einsatz von Microsoft QDK, einen speziellen Zweck-Quantum-Simulator, der mit Millionen von Qubits verwendet werden kann
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 6/25/2020
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
ms.openlocfilehash: a6ceee592e628215511ec83475d9e25bf54674f7
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86870616"
---
# <a name="quantum-development-kit-qdk-toffoli-simulator"></a>Quantum Development Kit (QDK)-Simulator (QDK)

Der simulatorqdk-Simulator ist ein Zweck gesteuerter Simulator mit eingeschränktem Bereich und unterstützt nur `X` , `CNOT` und mehr gesteuerte `X` Quantum-Vorgänge. Alle klassischen Logik und Berechnungen sind verfügbar.

Während der ""-und "deffoli"-Simulator mehr Funktionen als der [vollständige Zustands Simulator](xref:microsoft.quantum.machines.full-state-simulator)bietet, hat dies den Vorteil, dass viel mehr Qubits simuliert werden kann. Der-Simulator kann mit Millionen von Qubits verwendet werden, während der vollständige Zustands Simulator auf ungefähr 30 Qubits beschränkt ist. Dies ist beispielsweise bei Oracles nützlich, die Boolesche Funktionen auswerten. Sie können mit dem begrenzten Satz unterstützter Algorithmen implementiert und auf einer großen Anzahl von Qubits getestet werden.

## <a name="invoking-the-toffoli-simulator"></a>Aufrufen des-Simulators "tyffoli"

Der-Simulator wird über die-Klasse verfügbar gemacht `ToffoliSimulator` . Weitere Informationen finden Sie unter [Möglichkeiten zum Ausführen eines Q #-Programms](xref:microsoft.quantum.guide.host-programs).

### <a name="invoking-the-toffoli-simulator-from-c"></a>Aufrufen des-Simulators von C #

Wie bei anderen Ziel Computern erstellen Sie zunächst eine Instanz der `ToffoliSimulator` -Klasse und übergeben Sie dann als ersten Parameter der-Methode eines Vorgangs `Run` .

Beachten Sie, dass die-Klasse im Gegensatz zur- `QuantumSimulator` Klasse `ToffoliSimulator` die <xref:System.IDisposable> -Schnittstelle nicht implementiert, sodass Sie Sie nicht in eine-Anweisung einschließen müssen `using` .

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

### <a name="invoking-the-toffoli-simulator-from-python"></a>Aufrufen des atffoli-Simulators aus python

Verwenden Sie die [toffoli_simulate ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) -Methode aus der Python-Bibliothek mit dem importierten Q #-Vorgang:

```python
qubit_result = myOperation.toffoli_simulate()
```

### <a name="invoking-the-toffoli-simulator-from-the-command-line"></a>Aufrufen des-Simulators von der Befehlszeile aus

Wenn Sie ein Q #-Programm über die Befehlszeile ausführen, verwenden Sie den Parameter **--Simulator** (oder **-s** ), um den Bereitstellungs Zielcomputer für den ""-Simulator anzugeben. Der folgende Befehl führt ein Programm mit der Ressourcenschätzung aus: 

```dotnetcli
dotnet run -s ToffoliSimulator
```

### <a name="invoking-the-toffoli-simulator-from-juptyer-notebooks"></a>Aufrufen des-Simulators von juptyer Notebooks

Verwenden [Sie den](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) Befehl "IQ # Magic", um den Q #-Vorgang auszuführen.

```
%toffoli myOperation
```

## <a name="supported-operations"></a>Unterstützte Vorgänge

Der Schalter "-Schalter" unterstützt Folgendes:

* Drehungen und exponentialweise, z. b. `R` und `Exp` , wenn der resultierende Vorgang `X` oder die Identitätsmatrix ist.
* Messungen und [Assert](xref:microsoft.quantum.diagnostics.assertmeasurement) -Vorgänge, aber nur in der Pauli- `Z` Basis. Beachten Sie, dass die Wahrscheinlichkeit eines Messvorgangs immer entweder **0** oder **1**ist. Es gibt keine Zufälligkeit im-Simulator von "".
* `DumpMachine`-und- `DumpRegister` Funktionen.
Beide Funktionen geben den aktuellen `Z` Status jedes Qubit aus, ein Qubit pro Zeile.

## <a name="specifying-the-number-of-qubits"></a>Angeben der Anzahl von Qubits

Standardmäßig ordnet eine- `ToffoliSimulator` Instanz Speicherplatz für 65.536 Qubits zu.
Wenn für Ihren Algorithmus mehr Qubits erforderlich sind, können Sie die Qubit-Anzahl angeben, indem Sie dem Konstruktor einen Wert für den Parameter bereitstellen `qubitCount` .
Für jedes zusätzliche Qubit ist nur ein Byte Arbeitsspeicher erforderlich, sodass die Anzahl der benötigten Qubits nicht signifikant ist.

Beispiel:

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```

## <a name="see-also"></a>Weitere Informationen

- [Quantum-Ressourcenschätzung](xref:microsoft.quantum.machines.resources-estimator)
- [Quantum-Ablauf Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [Quantum-vollständiger Zustands Simulator](xref:microsoft.quantum.machines.full-state-simulator) 