---
title: Quantensimulatoren und Q#-Programme
description: Hier werden die Quantensimulatoren beschrieben, die als Zielcomputer für Q#-Programme verfügbar sind.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 6/17/2020
ms.topic: article
uid: microsoft.quantum.machines
no-loc:
- Q#
- $$v
ms.openlocfilehash: 77401ca3642b89d708f338f852dc60bf7346b87b
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868303"
---
# <a name="quantum-simulators"></a>Quantensimulatoren

Bei Quantensimulatoren handelt es sich um Softwareprogramme, die auf klassischen Computern ausgeführt werden und als *Zielcomputer* für ein Q#-Programm fungieren. Sie ermöglichen das Ausführen und Testen von Quantenprogrammen in einer Umgebung, die die Reaktion von Qubits auf verschiedene Operationen vorhersagt. In diesem Artikel erfahren Sie, welche Quantensimulatoren im Quantum Development Kit (QDK) enthalten sind. Darüber hinaus enthält er Informationen zu den verschiedenen Verfahren, mit denen Sie ein Q#-Programm an die Quantensimulatoren übergeben können – etwa über die Befehlszeile oder mit Treibercode, der in einer klassischen Sprache geschrieben ist.  



## <a name="the-quantum-development-kit-qdk-quantum-simulators"></a>Quantensimulatoren im Quantum Development Kit (QDK)

Der Quantensimulator ist für das Bereitstellen der Implementierungen von Quantenprimitiven für einen Algorithmus zuständig. Dies gilt auch für primitive Vorgänge, z. B. `H`, `CNOT` und `Measure`, sowie für die Verwaltung und Nachverfolgung von Qubits. Das QDK enthält verschiedene Klassen von Quantensimulatoren, die für unterschiedliche Ausführungsmodelle desselben Quantenalgorithmus stehen. 


Mit jeder Art von Quantensimulator können unterschiedliche Implementierungen dieser Primitive bereitgestellt werden. Mit dem [Simulator für den vollständigen Zustand](xref:microsoft.quantum.machines.full-state-simulator) wird der Quantenalgorithmus beispielsweise ausgeführt, indem der [Quantenzustandsvektor](xref:microsoft.quantum.glossary#quantum-state) vollständig simuliert wird, während der tatsächliche Quantenzustand beim [Ablaufverfolgungssimulator für Quantencomputer](xref:microsoft.quantum.machines.qc-trace-simulator.intro) nicht berücksichtigt wird. Stattdessen wird hiermit die Nutzung von Gates, Qubits und anderen Ressourcen für den Algorithmus nachverfolgt.

### <a name="quantum-machine-classes"></a>Quantencomputerklassen

Für die Zukunft ist für das QDK die Definition weiterer Quantencomputerklassen geplant, um andere Arten von Simulationen und die Ausführung auf Quantenhardware zu unterstützen. Indem der Algorithmus konstant gehalten wird, während die zugrunde liegende Computerimplementierung variiert, wird das Testen und Debuggen eines simulierten Algorithmus vereinfacht. Anschließend können Sie beim Ausführen auf echter Hardware sicher sein, dass sich der Algorithmus nicht geändert hat.

Das QDK enthält mehrere Quantencomputerklassen, die allesamt im Namespace `Microsoft.Quantum.Simulation.Simulators` definiert sind.

|Simulator |Klasse|Beschreibung|
|-----|------|---|
|[Simulator für den vollständigen Zustand](xref:microsoft.quantum.machines.full-state-simulator)| `QuantumSimulator` | Dient zum Ausführen und Debuggen von Quantenalgorithmen und ist auf ca. 30 Qubits begrenzt. |
|[Einfache Ressourcenschätzung](xref:microsoft.quantum.machines.resources-estimator)| `ResourcesEstimator` | Dient zum Durchführen einer Analyse auf oberster Ebene für die Ressourcen, die zum Ausführen eines Quantenalgorithmus benötigt werden, und unterstützt Tausende von Qubits.|
|[Auf der Ablaufverfolgung basierende Ressourcenschätzung](xref:microsoft.quantum.machines.qc-trace-simulator.intro)|  `QCTraceSimulator` |Dient zum Ausführen einer erweiterten Analyse des Ressourcenverbrauchs für das gesamte Aufrufdiagramm des Algorithmus und unterstützt Tausende von Qubits.|
|[Toffoli-Simulator](xref:microsoft.quantum.machines.toffoli-simulator)| `ToffoliSimulator` |Dient zum Simulieren von Quantenalgorithmen, die auf die Quantenoperationen `X`, `CNOT` und mehrfach gesteuertes `X` beschränkt sind, und unterstützt Millionen von Qubits. |

## <a name="invoking-the-quantum-simulator"></a>Aufrufen des Quantensimulators

Unter [Möglichkeiten zum Ausführen eines Q#-Programms](xref:microsoft.quantum.guide.host-programs) sind drei Möglichkeiten zum Übergeben des Q#-Codes an den Quantensimulator beschrieben: 

* Verwenden der Befehlszeile
* Verwenden eines Python-Hostprogramms
* Verwenden eines C#-Hostprogramms

Quantencomputer sind Instanzen normaler .NET-Klassen. Sie werden also genauso wie .NET-Klassen erstellt, indem ihr Konstruktor aufgerufen wird. Die Vorgehensweise hängt hierbei jeweils davon ab, wie Sie das Q#-Programm ausführen.

## <a name="next-steps"></a>Nächste Schritte

* Ausführliche Informationen zum Aufrufen von Zielcomputern für Q#-Programme in unterschiedlichen Umgebungen finden Sie unter [Möglichkeiten zum Ausführen eines Q#-Programms](xref:microsoft.quantum.guide.host-programs).
