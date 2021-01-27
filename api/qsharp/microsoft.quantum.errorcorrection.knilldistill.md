---
uid: Microsoft.Quantum.ErrorCorrection.KnillDistill
title: Knilldinoch-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: KnillDistill
qsharp.summary: Implements the Knill magic state distillation algorithm.
ms.openlocfilehash: 4eff99eebb1e271d240513f827c6e93973ef79a6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853117"
---
# <a name="knilldistill-operation"></a>Knilldinoch-Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementiert den Knill Magic State-Destillations Algorithmus.

```qsharp
operation KnillDistill (roughMagic : Qubit[]) : Bool
```


## <a name="description"></a>Beschreibung

Bei 15 ungefähren Kopien eines Magic State $ $ \begin{align} \cos\bruchteil {\pi} {8} \ket {0} + \sin \bruchteil {\pi} {8} \ket {1} \end{align} ergibt $ $ eine Kopie einer höheren Qualität.

## <a name="input"></a>Eingabe

### <a name="roughmagic--qubit"></a>roughmagic: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Register von 15 Qubits, das ungefähre Kopien eines magischen Zustands enthält. Die folgende Anwendung dieses Destillations Verfahrens `roughMagic[0]` enthält eine Kopie der höheren Qualität, und der Rest des Registers wird auf den Status $ \ket{00\cdots 0} $ zurückgesetzt.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

Wenn `true` , dann wird die Prozedur erfolgreich ausgeführt, und die Kopie der höheren Qualität sollte akzeptiert werden. Gibt an, `false` dass die Prozedur fehlgeschlagen ist und der Status des Registers als nicht definiert angesehen werden soll.

## <a name="remarks"></a>Bemerkungen

Wir folgen dem Algorithmus von "Knill".
Allerdings ist die aktuelle Implementierung von weitem nicht optimal, da zu viele Qubits verwendet werden.
Die magischen Zustände werden in diese Routine eingefügt. in diesem Fall gibt es bessere Protokolle.

## <a name="references"></a>References

- [Knill](https://arxiv.org/abs/quant-ph/0402171)