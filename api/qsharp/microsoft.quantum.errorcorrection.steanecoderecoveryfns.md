---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns
title: Steanecoderecoveryf-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryFns
qsharp.summary: Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 7395996e75c5a1c0c5d13f76d9ec76acae5683c7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200406"
---
# <a name="steanecoderecoveryfns-function"></a>Steanecoderecoveryf-Funktion

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Decoder für kombinierte X-und Z-Teile der stabilistabilisgruppe des ⟦ 7, 1, 3 ⟧ Steane Quantum-Codes.

```qsharp
function SteaneCodeRecoveryFns () : (Microsoft.Quantum.ErrorCorrection.RecoveryFn, Microsoft.Quantum.ErrorCorrection.RecoveryFn)
```


## <a name="output--recoveryfnrecoveryfn"></a>Ausgabe: ([wiederherstellerfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))

Ein Tupel von Funktionen vom Typ `RecoveryFn` , das eine Messungs Messung annimmt `Result[]` und die Vorgänge zurückgibt, durch die `Pauli[]` der erkannte Fehler korrigiert wird.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. errorcorrection. steanecoderecoveryx](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [Microsoft. Quantum. errorcorrection. steanecoderecoveryz](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ)