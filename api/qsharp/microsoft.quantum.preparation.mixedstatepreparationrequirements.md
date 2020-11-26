---
uid: Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
title: Benutzerdefinierter mixedstatepreparationrequirements-Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: MixedStatePreparationRequirements
qsharp.summary: Represents the number of qubits required in order to prepare a given mixed state.
ms.openlocfilehash: 3ea4757f6aa5125418b1e81db9f32e7b668eb359
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228694"
---
# <a name="mixedstatepreparationrequirements-user-defined-type"></a>Benutzerdefinierter mixedstatepreparationrequirements-Typ

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Stellt die Anzahl der erforderlichen Qubits zum Vorbereiten eines gegebenen gemischten Zustands dar.

```qsharp

newtype MixedStatePreparationRequirements = (NTotalQubits : Int, (NIndexQubits : Int, NGarbageQubits : Int));
```



## <a name="named-items"></a>Benannte Elemente

### <a name="ntotalqubits--int"></a>Ntotalqubits: [int](xref:microsoft.quantum.lang-ref.int)


### <a name="nindexqubits--int"></a>Nindexqubits: [int](xref:microsoft.quantum.lang-ref.int)


### <a name="ngarbagequbits--int"></a>Ngarbagequbits: [int](xref:microsoft.quantum.lang-ref.int)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. purifedmixedstate](xref:Microsoft.Quantum.PurifiedMixedState)