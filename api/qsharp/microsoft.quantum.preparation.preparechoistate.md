---
uid: Microsoft.Quantum.Preparation.PrepareChoiState
title: Preparechoistate-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiState
qsharp.summary: Prepares the Choi–Jamiłkowski state for a given operation onto given reference and target registers.
ms.openlocfilehash: 8b2917a7d9414539f2f7c821c4115fc4b21d0373
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723998"
---
# <a name="preparechoistate-operation"></a>Preparechoistate-Vorgang

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paketen [](https://nuget.org/packages/)


Bereitet den Status "Choi – jamiłkowski" für einen bestimmten Vorgang auf angegebene Verweis-und Ziel Register vor.

```qsharp
operation PrepareChoiState (op : (Qubit[] => Unit), reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="op--qubit--unit"></a>OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Der Vorgang $ \lambda $, dessen Metadaten– jamiłkowski State $J (\lambda)/2 ^ N $ vorbereitet werden soll, wobei $N $ die Anzahl der Qubits ist, die von verwendet werden `op` .


### <a name="reference--qubit"></a>Verweis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Register von Qubits, beginnend mit dem Status $ \ket{00\cdots 0} $, der als Verweis für die Aktion von verwendet werden soll `op` .


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Register von Qubits, das anfänglich im $ \ket{00\cdots 0} $-Zustand `op` ist, in dem Sie angewendet werden sollen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Der Bundesstaat Choi – jamiłkowski $J (\lambda) $ eines Quantum-Prozesses ist als $ $ \begin{align} J (\lambda) \mathrel{: =} (\boldone \otimes \lambda) (| \boldone\rangle \! \rangle\langle \! \langle\boldone |), \end{align} $ $ WHERE $ | X\rangle \! \rangle $ ist die *Vektorisierung* einer Matrix $X $ in der spaltenstapel Konvention. Das Erlernen einer klassischen Beschreibung dieses Zustands enthält vollständige Informationen zu den Auswirkungen von $ \lambda $, die auf beliebige Eingabe Zustände reagieren, und bildet die Grundlage der *Quantum-Prozess Tomographie* .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Preparation. preparechoistatuea](xref:Microsoft.Quantum.Preparation.PrepareChoiStateA)
- [Microsoft. Quantum. Preparation. preparechoistatus EC](xref:Microsoft.Quantum.Preparation.PrepareChoiStateC)
- [Microsoft. Quantum. Preparation. preparechoistatueca](xref:Microsoft.Quantum.Preparation.PrepareChoiStateCA)