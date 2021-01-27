---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns
title: Steanecoderecoveryf-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryFns
qsharp.summary: Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 8dc715042f98b90b8cea7e2d6ecb5d02a78d297f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853030"
---
# <a name="steanecoderecoveryfns-function"></a><span data-ttu-id="5e314-102">Steanecoderecoveryf-Funktion</span><span class="sxs-lookup"><span data-stu-id="5e314-102">SteaneCodeRecoveryFns function</span></span>

<span data-ttu-id="5e314-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="5e314-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="5e314-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5e314-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5e314-105">Decoder für kombinierte X-und Z-Teile der stabilistabilisgruppe des ⟦ 7, 1, 3 ⟧ Steane Quantum-Codes.</span><span class="sxs-lookup"><span data-stu-id="5e314-105">Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
function SteaneCodeRecoveryFns () : (Microsoft.Quantum.ErrorCorrection.RecoveryFn, Microsoft.Quantum.ErrorCorrection.RecoveryFn)
```


## <a name="output--recoveryfnrecoveryfn"></a><span data-ttu-id="5e314-106">Ausgabe: ([wiederherstellerfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))</span><span class="sxs-lookup"><span data-stu-id="5e314-106">Output : ([RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))</span></span>

<span data-ttu-id="5e314-107">Ein Tupel von Funktionen vom Typ `RecoveryFn` , das eine Messungs Messung annimmt `Result[]` und die Vorgänge zurückgibt, durch die `Pauli[]` der erkannte Fehler korrigiert wird.</span><span class="sxs-lookup"><span data-stu-id="5e314-107">Tuple of functions of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operations that corrects the detected error.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e314-108">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5e314-108">See Also</span></span>

- [<span data-ttu-id="5e314-109">Microsoft. Quantum. errorcorrection. steanecoderecoveryx</span><span class="sxs-lookup"><span data-stu-id="5e314-109">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [<span data-ttu-id="5e314-110">Microsoft. Quantum. errorcorrection. steanecoderecoveryz</span><span class="sxs-lookup"><span data-stu-id="5e314-110">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ)