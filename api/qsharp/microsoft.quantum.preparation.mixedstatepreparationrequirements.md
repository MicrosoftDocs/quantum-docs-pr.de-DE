---
uid: Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
title: Benutzerdefinierter mixedstatepreparationrequirements-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: MixedStatePreparationRequirements
qsharp.summary: Represents the number of qubits required in order to prepare a given mixed state.
ms.openlocfilehash: df57b7b43fc84f7ddf68392f6a2b7013225da730
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856931"
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