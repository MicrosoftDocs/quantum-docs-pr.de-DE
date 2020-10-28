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
# <a name="bitfliprecoveryfn-function"></a><span data-ttu-id="65948-102">Bitfliprecoveryfn-Funktion</span><span class="sxs-lookup"><span data-stu-id="65948-102">BitFlipRecoveryFn function</span></span>

<span data-ttu-id="65948-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="65948-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="65948-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="65948-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="65948-105">Funktion für Wiederherstellungs-Pauli-Vorgänge für die angegebene prozessormessung durch Tabellen Suche für den ⟦ 3, 1, 1 ⟧ Bit-Flip-Code.</span><span class="sxs-lookup"><span data-stu-id="65948-105">Function for recovery Pauli operations for given syndrome measurement by table lookup for the ⟦3, 1, 1⟧ bit flip code.</span></span>

```qsharp
function BitFlipRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a><span data-ttu-id="65948-106">Ausgabe: [Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="65948-106">Output : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="65948-107">Funktion des Typs `RecoveryFn` , die eine Messungs Messung annimmt `Result[]` und die Vorgänge zurückgibt, durch die `Pauli[]` der erkannte Fehler korrigiert wird.</span><span class="sxs-lookup"><span data-stu-id="65948-107">Function of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operations that corrects the detected error.</span></span>

## <a name="see-also"></a><span data-ttu-id="65948-108">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="65948-108">See Also</span></span>

- [<span data-ttu-id="65948-109">Microsoft. Quantum. errorcorrection. wiederherstellungfn</span><span class="sxs-lookup"><span data-stu-id="65948-109">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)