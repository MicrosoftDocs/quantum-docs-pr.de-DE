---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCode
title: Steanäcode-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCode
qsharp.summary: Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: b981c82acfa82cd58d82666703d4bb95ac5df280
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200474"
---
# <a name="steanecode-function"></a>Steanäcode-Funktion

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt einen CSS-Wert zurück, der den ⟦ 7, 1, 3 ⟧ Steane-Code Encoder und den Decoder mit der direkten Messung darstellt.

```qsharp
function SteaneCode () : Microsoft.Quantum.ErrorCorrection.CSS
```


## <a name="output--css"></a>Ausgabe: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)

Ein Objekt vom Typ CSS, das alle relevanten Daten sammelt, um die Codierung und Fehlerkorrektur für den ⟦ 7, 1, 3 ⟧ Steane-Code auszuführen.

## <a name="remarks"></a>Bemerkungen

Diesen Code finden Sie im folgenden Artikel:

- A. Steane, "mehrfache Partikel Störungen und Quantum-Fehlerkorrektur", proc. Stammt. Soc. Lond. A452 (1996) PP. 2551; https://arxiv.org/abs/quant-ph/9601029.