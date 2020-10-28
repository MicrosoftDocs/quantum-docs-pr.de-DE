---
uid: Microsoft.Quantum.ErrorCorrection.BitFlipRecoveryFn
title: Bitfliprecoveryfn-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: BitFlipRecoveryFn
qsharp.summary: Function for recovery Pauli operations for given syndrome measurement by table lookup for the ⟦3, 1, 1⟧ bit flip code.
ms.openlocfilehash: dad90475b2506187282825e143b11adc5120f453
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702551"
---
# <a name="bitfliprecoveryfn-function"></a>Bitfliprecoveryfn-Funktion

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


Funktion für Wiederherstellungs-Pauli-Vorgänge für die angegebene prozessormessung durch Tabellen Suche für den ⟦ 3, 1, 1 ⟧ Bit-Flip-Code.

```qsharp
function BitFlipRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a>Ausgabe: [Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Funktion des Typs `RecoveryFn` , die eine Messungs Messung annimmt `Result[]` und die Vorgänge zurückgibt, durch die `Pauli[]` der erkannte Fehler korrigiert wird.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. errorcorrection. wiederherstellungfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)