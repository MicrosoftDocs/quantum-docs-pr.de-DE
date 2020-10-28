---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: Debug-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: b033723a50fb85e77c9d4baec1f94231327e9b25
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725216"
---
# <a name="decomposedon-function"></a>Debug-Funktion

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paketen [](https://nuget.org/packages/)


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

