---
uid: Microsoft.Quantum.ErrorCorrection.RecoveryFn
title: Benutzerdefinierter Typ "wiederherstellungsfn"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoveryFn
qsharp.summary: Type for function that maps an error syndrome to a sequence of `Pauli[]` operations that correct the detected error.
ms.openlocfilehash: 7e8afa37e6225239ae7cafa1f48377a97c43297d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98825103"
---
# <a name="recoveryfn-user-defined-type"></a>Benutzerdefinierter Typ "wiederherstellungsfn"

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Der Typ für die Funktion, die einer Sequenz von `Pauli[]` Vorgängen, die den erkannten Fehler beheben, ein Fehler-Syndrom zuordnet.

```qsharp

newtype RecoveryFn = ((Microsoft.Quantum.ErrorCorrection.Syndrome -> Pauli[]));
```

