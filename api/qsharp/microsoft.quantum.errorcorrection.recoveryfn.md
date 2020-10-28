---
uid: Microsoft.Quantum.ErrorCorrection.RecoveryFn
title: Benutzerdefinierter Typ "wiederherstellungsfn"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoveryFn
qsharp.summary: Type for function that maps an error syndrome to a sequence of `Pauli[]` operations that correct the detected error.
ms.openlocfilehash: 6f4db7312fadbd8ca4c6b8533f78c2c5a886f30e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702420"
---
# <a name="recoveryfn-user-defined-type"></a>Benutzerdefinierter Typ "wiederherstellungsfn"

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


Der Typ für die Funktion, die einer Sequenz von `Pauli[]` Vorgängen, die den erkannten Fehler beheben, ein Fehler-Syndrom zuordnet.

```qsharp

newtype RecoveryFn = ((Microsoft.Quantum.ErrorCorrection.Syndrome -> Pauli[]));
```

