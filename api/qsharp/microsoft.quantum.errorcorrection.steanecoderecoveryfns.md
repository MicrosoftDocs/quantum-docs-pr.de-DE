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
# <a name="steanecoderecoveryfns-function"></a><span data-ttu-id="0da0e-102">Steanecoderecoveryf-Funktion</span><span class="sxs-lookup"><span data-stu-id="0da0e-102">SteaneCodeRecoveryFns function</span></span>

<span data-ttu-id="0da0e-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="0da0e-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="0da0e-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0da0e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0da0e-105">Decoder für kombinierte X-und Z-Teile der stabilistabilisgruppe des ⟦ 7, 1, 3 ⟧ Steane Quantum-Codes.</span><span class="sxs-lookup"><span data-stu-id="0da0e-105">Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
function SteaneCodeRecoveryFns () : (Microsoft.Quantum.ErrorCorrection.RecoveryFn, Microsoft.Quantum.ErrorCorrection.RecoveryFn)
```


## <a name="output--recoveryfnrecoveryfn"></a><span data-ttu-id="0da0e-106">Ausgabe: ([wiederherstellerfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))</span><span class="sxs-lookup"><span data-stu-id="0da0e-106">Output : ([RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))</span></span>

<span data-ttu-id="0da0e-107">Ein Tupel von Funktionen vom Typ `RecoveryFn` , das eine Messungs Messung annimmt `Result[]` und die Vorgänge zurückgibt, durch die `Pauli[]` der erkannte Fehler korrigiert wird.</span><span class="sxs-lookup"><span data-stu-id="0da0e-107">Tuple of functions of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operations that corrects the detected error.</span></span>

## <a name="see-also"></a><span data-ttu-id="0da0e-108">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0da0e-108">See Also</span></span>

- [<span data-ttu-id="0da0e-109">Microsoft. Quantum. errorcorrection. steanecoderecoveryx</span><span class="sxs-lookup"><span data-stu-id="0da0e-109">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [<span data-ttu-id="0da0e-110">Microsoft. Quantum. errorcorrection. steanecoderecoveryz</span><span class="sxs-lookup"><span data-stu-id="0da0e-110">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ)