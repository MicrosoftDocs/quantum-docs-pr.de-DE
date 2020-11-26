---
uid: Microsoft.Quantum.Simulation.QuantumWalkByQubitization
title: Quantenwalkbyqubitisierung-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: QuantumWalkByQubitization
qsharp.summary: Converts a block-encoding reflection into a quantum walk.
ms.openlocfilehash: ccef1bbf400e01800053777d0010acb7addaef53
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192484"
---
# <a name="quantumwalkbyqubitization-function"></a>Quantenwalkbyqubitisierung-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Konvertiert eine Block Codierungs Reflektion in einen Quantum Walk.

```qsharp
function QuantumWalkByQubitization (blockEncoding : Microsoft.Quantum.Simulation.BlockEncodingReflection) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="description"></a>BESCHREIBUNG

Wenn ein `BlockEncodingReflection` von einem einheitlichen $U $ repräsentiert wird, der einen Operator $H $ of Interest codiert, konvertiert ihn in einen Quantum Walk $W $, der das Spektrum von $ \pm e ^ {\pm i\sin ^ {-1} (H)} $ enthält.

## <a name="input"></a>Eingabe

### <a name="blockencoding--blockencodingreflection"></a>blockencoding: [blockencodingreflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)

Ein `BlockEncodingReflection` einheitlicher $U $, der in einen Quantum Walk konvertiert werden soll.



## <a name="output--qubitqubit--unit--is-adj--ctl"></a>Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein Quantum Walk $W $, das sich zusammen in Registern verhält `a` und `s` $H $ codiert und das Spektrum von $ \pm e ^ {\pm i\sin ^ {-1} (H)} $ enthält.

## <a name="references"></a>Referenzen

- Hamiltona Simulation by qubitisierung Guang Hao Low, ISAL. Chuang https://arxiv.org/abs/1610.06546

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Simulation. blockencoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Microsoft. Quantum. Simulation. blockencodingreflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)