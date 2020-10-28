---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns
title: Steanecoderecoveryf-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryFns
qsharp.summary: Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: b1dd1c2e9a71e58bd8a86d1759a8b6af13a49614
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702396"
---
# <a name="steanecoderecoveryfns-function"></a>Steanecoderecoveryf-Funktion

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


Decoder für kombinierte X-und Z-Teile der stabilistabilisgruppe des ⟦ 7, 1, 3 ⟧ Steane Quantum-Codes.

```qsharp
function SteaneCodeRecoveryFns () : (Microsoft.Quantum.ErrorCorrection.RecoveryFn, Microsoft.Quantum.ErrorCorrection.RecoveryFn)
```


## <a name="output--recoveryfnrecoveryfn"></a>Ausgabe: ([wiederherstellerfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))

Ein Tupel von Funktionen vom Typ `RecoveryFn` , das eine Messungs Messung annimmt `Result[]` und die Vorgänge zurückgibt, durch die `Pauli[]` der erkannte Fehler korrigiert wird.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. errorcorrection. steanecoderecoveryx](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [Microsoft. Quantum. errorcorrection. steanecoderecoveryz](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ)