---
uid: Microsoft.Quantum.Synthesis.DecompositionState
title: Benutzerdefinierter Typ "decompositionstate"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecompositionState
qsharp.summary: State during decomposition based on variable indexes
ms.openlocfilehash: 0547c04828a80b4f696cc17e13c8cc57d0379f96
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725215"
---
# <a name="decompositionstate-user-defined-type"></a>Benutzerdefinierter Typ "decompositionstate"

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paketen [](https://nuget.org/packages/)


Zustand während der Zerlegung basierend auf Variablen Indizes

```qsharp

newtype DecompositionState = (Perm : Int[], Lfunctions : (BigInt, Int)[], Rfunctions : (BigInt, Int)[]);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="perm--int"></a>Perm: [int](xref:microsoft.quantum.lang-ref.int)[]


### <a name="lfunctions--bigintint"></a>Lfunctions: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []


### <a name="rfunctions--bigintint"></a>Rfunctions: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []



## <a name="description"></a>BESCHREIBUNG

Der-Zustand enthält die aktuelle permutations und die derzeit generierten Funktionen für gesteuerte Gates auf der linken Seite und kontrollierte Gates auf der rechten Seite.