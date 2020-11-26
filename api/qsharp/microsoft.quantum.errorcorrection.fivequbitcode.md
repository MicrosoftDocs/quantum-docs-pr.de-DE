---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCode
title: "\"Fvequbitcode\"-Funktion"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCode
qsharp.summary: Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 3b45af29897735905f7fe52340e2a8e425bd8cbe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200882"
---
# <a name="fivequbitcode-function"></a>"Fvequbitcode"-Funktion

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt einen qecc-Wert zurück, der den ⟦ 5, 1, 3 ⟧ Code Encoder und den Decoder mit der direkten Messung darstellt.

```qsharp
function FiveQubitCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a>Ausgabe: [qecc](xref:Microsoft.Quantum.ErrorCorrection.QECC)

Gibt eine Implementierung eines Quantum-Fehlerkorrekturcodes zurück, indem ein-Typ angegeben wird `QECC` .

## <a name="remarks"></a>Bemerkungen

Dieser Code wurde in den folgenden zwei Dokumenten unabhängig voneinander gefunden:

- C. H. Bennett, D. divincenzo, J. A. Smolin und W. K. Wootters, "gemischte Zustands jede Verflechtungen und Quantum-Fehlerkorrektur", "Phys. Rev. A, 54 (1996) PP. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 und
- R. Laflamme, C. Miquel, J. P. Paz und W. H. Zurek, "Perfect Quantum Error Korrektur Code", "Phys. Rev. Lett. 77 (1996) PP. 198-201; https://arxiv.org/abs/quant-ph/9602019