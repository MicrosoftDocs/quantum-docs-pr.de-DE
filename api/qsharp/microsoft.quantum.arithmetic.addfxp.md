---
uid: Microsoft.Quantum.Arithmetic.AddFxP
title: Addfxp-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddFxP
qsharp.summary: Adds two fixed-point numbers stored in quantum registers.
ms.openlocfilehash: 60b7cad3d0bd8800e67830ca921f8e2d705b8f39
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843871"
---
# <a name="addfxp-operation"></a><span data-ttu-id="77e2f-102">Addfxp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="77e2f-102">AddFxP operation</span></span>

<span data-ttu-id="77e2f-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="77e2f-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="77e2f-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="77e2f-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="77e2f-105">Addiert zwei in quantenregistern gespeicherte Fixed-Point-Nummern.</span><span class="sxs-lookup"><span data-stu-id="77e2f-105">Adds two fixed-point numbers stored in quantum registers.</span></span>

```qsharp
operation AddFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="77e2f-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77e2f-106">Description</span></span>

<span data-ttu-id="77e2f-107">Bei Angabe von zwei fixpointregistern in den Zuständen $ \ket{f_1} $ und $ \ket{f_2} $ wird der Vorgang "$ \ket{f_1} \ket{f_2} \mapsto \ket{f_1} \ket{f_1 + f_2} $" durchführt.</span><span class="sxs-lookup"><span data-stu-id="77e2f-107">Given two fixed-point registers respectively in states $\ket{f_1}$ and $\ket{f_2}$, performs the operation $\ket{f_1} \ket{f_2} \mapsto \ket{f_1} \ket{f_1 + f_2}$.</span></span>

## <a name="input"></a><span data-ttu-id="77e2f-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="77e2f-108">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="77e2f-109">Fp1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="77e2f-109">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="77e2f-110">Erste festpunktzahl</span><span class="sxs-lookup"><span data-stu-id="77e2f-110">First fixed-point number</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="77e2f-111">FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="77e2f-111">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="77e2f-112">Die zweite festpunktzahl wird aktualisiert und enthält nun die Summe der beiden Eingaben.</span><span class="sxs-lookup"><span data-stu-id="77e2f-112">Second fixed-point number, will be updated to contain the sum of the two inputs.</span></span>



## <a name="output--unit"></a><span data-ttu-id="77e2f-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="77e2f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="77e2f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77e2f-114">Remarks</span></span>

<span data-ttu-id="77e2f-115">Die aktuelle-Implementierung erfordert, dass die zwei fest Komma Zahlen die gleiche Punktposition aufweisen, die vom unbedeutenden Bit gezählt wird, d. h. $n _I $ und $p, dass _I $ gleich sein muss.</span><span class="sxs-lookup"><span data-stu-id="77e2f-115">The current implementation requires the two fixed-point numbers to have the same point position counting from the least-significant bit, i.e., $n_i$ and $p_i$ must be equal.</span></span>