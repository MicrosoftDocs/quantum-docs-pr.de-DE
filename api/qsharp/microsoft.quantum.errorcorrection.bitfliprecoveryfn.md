---
uid: Microsoft.Quantum.ErrorCorrection.BitFlipRecoveryFn
title: Bitfliprecoveryfn-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: BitFlipRecoveryFn
qsharp.summary: Function for recovery Pauli operations for given syndrome measurement by table lookup for the ⟦3, 1, 1⟧ bit flip code.
ms.openlocfilehash: f8d102cd54222f61058c655e72c63e86d2f5af03
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201205"
---
# <a name="bitfliprecoveryfn-function"></a><span data-ttu-id="002dc-102">Bitfliprecoveryfn-Funktion</span><span class="sxs-lookup"><span data-stu-id="002dc-102">BitFlipRecoveryFn function</span></span>

<span data-ttu-id="002dc-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="002dc-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="002dc-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="002dc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="002dc-105">Funktion für Wiederherstellungs-Pauli-Vorgänge für die angegebene prozessormessung durch Tabellen Suche für den ⟦ 3, 1, 1 ⟧ Bit-Flip-Code.</span><span class="sxs-lookup"><span data-stu-id="002dc-105">Function for recovery Pauli operations for given syndrome measurement by table lookup for the ⟦3, 1, 1⟧ bit flip code.</span></span>

```qsharp
function BitFlipRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a><span data-ttu-id="002dc-106">Ausgabe: [Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="002dc-106">Output : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="002dc-107">Funktion des Typs `RecoveryFn` , die eine Messungs Messung annimmt `Result[]` und die Vorgänge zurückgibt, durch die `Pauli[]` der erkannte Fehler korrigiert wird.</span><span class="sxs-lookup"><span data-stu-id="002dc-107">Function of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operations that corrects the detected error.</span></span>

## <a name="see-also"></a><span data-ttu-id="002dc-108">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="002dc-108">See Also</span></span>

- [<span data-ttu-id="002dc-109">Microsoft. Quantum. errorcorrection. wiederherstellungfn</span><span class="sxs-lookup"><span data-stu-id="002dc-109">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)