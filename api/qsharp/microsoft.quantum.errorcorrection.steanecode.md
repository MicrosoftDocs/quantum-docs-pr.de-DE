---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCode
title: Steanäcode-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCode
qsharp.summary: Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: af3f3ef5088b898bd827ebca00fdc7fcb992f2a1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853052"
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