---
uid: Microsoft.Quantum.Canon.ApplyAndChain
title: Applyandchain-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyAndChain
qsharp.summary: Computes a chain of AND gates
ms.openlocfilehash: c53bca6ecf964f4358b0a7ff1c61d4e8e195cd7d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219361"
---
# <a name="applyandchain-operation"></a>Applyandchain-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Berechnet eine Kette von und Gates

```qsharp
operation ApplyAndChain (auxRegister : Qubit[], ctrlRegister : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="description"></a>BESCHREIBUNG

Die zusätzlichen Qubits zum Berechnen temporärer Ergebnisse müssen explizit angegeben werden.
Die Länge dieses Registers ist `Length(ctrlRegister) - 2` , wenn mindestens zwei Steuerelemente vorhanden sind, andernfalls ist die Länge 0 (null).

## <a name="input"></a>Eingabe

### <a name="auxregister--qubit"></a>"auxregister": [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="ctrlregister--qubit"></a>ctrlregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

