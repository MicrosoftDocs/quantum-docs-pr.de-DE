---
uid: Microsoft.Quantum.ErrorCorrection._ExtractLogicalQubitFromSteaneCode
title: _ExtractLogicalQubitFromSteaneCode Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: _ExtractLogicalQubitFromSteaneCode
qsharp.summary: >-
  Syndrome measurement and the inverse of embedding.

  $X$- and $Z$-stabilizers are not treated equally, which is due to the particular choice of the encoding circuit. This asymmetry leads to a different syndrome extraction routine. One could measure the syndrome by measuring multi-qubit Pauli operator directly on the code state, but for the distillation purpose the logical qubit is returned into a single qubit, in course of which the syndrome measurements can be done without further ancillas.
ms.openlocfilehash: fe64343e30a0a3f0d05382e7812d37d5b13133d3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853212"
---
# <a name="_extractlogicalqubitfromsteanecode-operation"></a>_ExtractLogicalQubitFromSteaneCode Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Die Messgeräte Messung und die Umkehrung der Einbettung.

$X $-und $Z $-Stabilizers werden nicht gleichermaßen behandelt, was auf die jeweilige Auswahl der Codierungs Verbindung zurückzuführen ist.
Diese Asymmetrie führt zu einer anderen Extraktions Routine für die Analyse.
Sie können das-Syndrom Messen, indem Sie den multiqubit-Pauli-Operator direkt auf den Code Zustand messen. für den Zweck der Wiederverwendung wird jedoch das logische Qubit an ein einzelnes Qubit zurückgegeben.

```qsharp
operation _ExtractLogicalQubitFromSteaneCode (code : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit, Int, Int)
```


## <a name="input"></a>Eingabe

### <a name="code--logicalregister"></a>Code: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)





## <a name="output--qubitintint"></a>Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))

Das logische Qubit und ein paar von ganzen Zahlen für $X $--Syndrom und $Z $--Syndrom.
Sie stellen den Index des Code-Qubit dar, auf dem ein einzelner $X $-oder $Z $-Error das gemessene Syndrom verursacht hätte.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass dieser Vorgang nicht als gekennzeichnet ist `internal` , da Komponententests direkt von diesem Vorgang abhängig sind. Bei zukünftigen Verbesserungen sollten Komponententests umgestaltet werden, damit Sie nur direkt von öffentlichen callables abhängig sind.

> [!WARNING]
> Diese Routine ist auf eine bestimmte Codierungs Verbindung für den 7-Qubit-Code von Steane zugeschnitten. Wenn die Codierungs Verbindung geändert wird, muss das Ergebnis des-syndrotes möglicherweise anders interpretiert werden.