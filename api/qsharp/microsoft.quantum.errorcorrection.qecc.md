---
uid: Microsoft.Quantum.ErrorCorrection.QECC
title: Benutzerdefinierter qecc-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: QECC
qsharp.summary: Represents an error-correcting code as defined by its encoder, decoder, and syndrome measurement procedure.
ms.openlocfilehash: 4fab7e25f6ccf9f9af2744e0ebe40418d9681309
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853076"
---
# <a name="qecc-user-defined-type"></a>Benutzerdefinierter qecc-Typ

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Stellt einen Fehler Behebungs Code dar, wie er durch den Encoder, Decoder und die Mess Prozedur Messung definiert wurde.

```qsharp

newtype QECC = (Microsoft.Quantum.ErrorCorrection.EncodeOp, Microsoft.Quantum.ErrorCorrection.DecodeOp, Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp);
```

