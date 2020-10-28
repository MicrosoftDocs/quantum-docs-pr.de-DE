---
uid: Microsoft.Quantum.Chemistry.HTerm
title: Benutzerdefinierter hterm-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTerm
qsharp.summary: Format of data passed from C# to Q# to represent a term of the Hamiltonian. The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 7a18db539e55e4c1086b3d83725e3d4ba87f0117
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703566"
---
# <a name="hterm-user-defined-type"></a>Benutzerdefinierter hterm-Typ

Namespace: [Microsoft. Quantum. Chemistry](xref:Microsoft.Quantum.Chemistry)

Paketen [](https://nuget.org/packages/)


Das Format der Daten, die von c# an Q # übergeben werden, um einen Begriff von "hamiltonan" darzustellen.
Die Bedeutung der dargestellten Daten wird durch den Algorithmus bestimmt, der Sie empfängt.

```qsharp

newtype HTerm = (Int[], Double[]);
```

