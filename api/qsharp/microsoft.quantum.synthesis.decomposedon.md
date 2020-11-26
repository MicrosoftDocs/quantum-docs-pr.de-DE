---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: Debug-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: 79f952e7bc7ba9f5337cf5e7a625e0d270a2e17a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203228"
---
# <a name="decomposedon-function"></a>Debug-Funktion

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Zerlegt eine permutations für eine Variable.

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a>BESCHREIBUNG

Bei Angabe einer permutations $ \pi $ ( `perm` ) und eines Index $i $ ( `index` ), diese Methode gibt drei Permutationen $ ((\ pi_l, \ pi_r), \pi ') $ so zurück, dass die Bilder von $ \ pi_l $ und $ \ pi_r $ Bits in ihren Elementen bei anderen Indizes als $i $ und Bilder von $ \pi ' $ do not Change Bit $i $ in ihren Elementen nicht ändern.

## <a name="input"></a>Eingabe

### <a name="perm--int"></a>Perm: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="index--int"></a>Index: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--intintint"></a>Ausgabe: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])

