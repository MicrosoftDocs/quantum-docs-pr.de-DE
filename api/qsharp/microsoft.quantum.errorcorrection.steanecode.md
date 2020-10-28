---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCode
title: Steanäcode-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCode
qsharp.summary: Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: ea36320fff1f0c24426e2fcead976ef051d6699f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702414"
---
# <a name="steanecode-function"></a>Steanäcode-Funktion

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


Gibt einen CSS-Wert zurück, der den ⟦ 7, 1, 3 ⟧ Steane-Code Encoder und den Decoder mit der direkten Messung darstellt.

```qsharp
function SteaneCode () : Microsoft.Quantum.ErrorCorrection.CSS
```


## <a name="output--css"></a>Ausgabe: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)

Ein Objekt vom Typ CSS, das alle relevanten Daten sammelt, um die Codierung und Fehlerkorrektur für den ⟦ 7, 1, 3 ⟧ Steane-Code auszuführen.

## <a name="remarks"></a>Hinweise

Diesen Code finden Sie im folgenden Artikel:

- A. Steane, "mehrfache Partikel Störungen und Quantum-Fehlerkorrektur", proc. Stammt. Soc. Lond. A452 (1996) PP. 2551; https://arxiv.org/abs/quant-ph/9601029.