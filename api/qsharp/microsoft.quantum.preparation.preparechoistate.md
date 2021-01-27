---
uid: Microsoft.Quantum.Preparation.PrepareChoiState
title: Preparechoistate-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiState
qsharp.summary: Prepares the Choi–Jamiołkowski state for a given operation onto given reference and target registers.
ms.openlocfilehash: cb34078c09f8c28b5b9bbda1bae6936d13ffcc78
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854405"
---
# <a name="preparechoistate-operation"></a>Preparechoistate-Vorgang

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bereitet den Status "Choi – jamiołkowski" für einen bestimmten Vorgang auf angegebene Verweis-und Ziel Register vor.

```qsharp
operation PrepareChoiState (op : (Qubit[] => Unit), reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="op--qubit--unit"></a>OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Der Vorgang $ \lambda $, dessen Metadaten– jamiołkowski State $J (\lambda)/2 ^ N $ vorbereitet werden soll, wobei $N $ die Anzahl der Qubits ist, die von verwendet werden `op` .


### <a name="reference--qubit"></a>Verweis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Register von Qubits, beginnend mit dem Status $ \ket{00\cdots 0} $, der als Verweis für die Aktion von verwendet werden soll `op` .


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Register von Qubits, das anfänglich im $ \ket{00\cdots 0} $-Zustand `op` ist, in dem Sie angewendet werden sollen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Der Bundesstaat Choi – jamiłkowski $J (\lambda) $ eines Quantum-Prozesses ist als $ $ \begin{align} J (\lambda) \mathrel{: =} (\boldone \otimes \lambda) (| \boldone\rangle \! \rangle\langle \! \langle\boldone |), \end{align} $ $ WHERE $ | X\rangle \! \rangle $ ist die *Vektorisierung* einer Matrix $X $ in der spaltenstapel Konvention. Das Erlernen einer klassischen Beschreibung dieses Zustands enthält vollständige Informationen zu den Auswirkungen von $ \lambda $, die auf beliebige Eingabe Zustände reagieren, und bildet die Grundlage der *Quantum-Prozess Tomographie*.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Preparation. preparechoistatuea](xref:Microsoft.Quantum.Preparation.PrepareChoiStateA)
- [Microsoft. Quantum. Preparation. preparechoistatus EC](xref:Microsoft.Quantum.Preparation.PrepareChoiStateC)
- [Microsoft. Quantum. Preparation. preparechoistatueca](xref:Microsoft.Quantum.Preparation.PrepareChoiStateCA)