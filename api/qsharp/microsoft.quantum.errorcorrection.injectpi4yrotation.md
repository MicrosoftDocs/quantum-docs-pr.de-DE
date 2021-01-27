---
uid: Microsoft.Quantum.ErrorCorrection.InjectPi4YRotation
title: InjectPi4YRotation-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: InjectPi4YRotation
qsharp.summary: Rotates a single qubit by π/4 about the Y-axis.
ms.openlocfilehash: 249c347c9e9729e719eda69e4e9a21847d9a46eb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98825938"
---
# <a name="injectpi4yrotation-operation"></a><span data-ttu-id="9f57d-102">InjectPi4YRotation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9f57d-102">InjectPi4YRotation operation</span></span>

<span data-ttu-id="9f57d-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="9f57d-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="9f57d-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9f57d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9f57d-105">Dreht ein einzelnes Qubit um die Y-Achse.</span><span class="sxs-lookup"><span data-stu-id="9f57d-105">Rotates a single qubit by π/4 about the Y-axis.</span></span>

```qsharp
operation InjectPi4YRotation (data : Qubit, magic : Qubit) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="9f57d-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f57d-106">Description</span></span>

<span data-ttu-id="9f57d-107">Führt eine Drehung/4-Drehung um durch `Y` .</span><span class="sxs-lookup"><span data-stu-id="9f57d-107">Performs a π/4 rotation about `Y`.</span></span>

<span data-ttu-id="9f57d-108">Die Drehung erfolgt durch die Verwendung eines magischen Zustands. Das heißt, eine Kopie des Zustands $ $ \begin{align} \cos\bruchteil {\pi} {8} \ket {0} + \sin \bruchteil {\pi} {8} \ket {1} .</span><span class="sxs-lookup"><span data-stu-id="9f57d-108">The rotation is performed by consuming a magic state; that is, a copy of the state $$ \begin{align} \cos\frac{\pi}{8} \ket{0} + \sin \frac{\pi}{8} \ket{1}.</span></span>
<span data-ttu-id="9f57d-109">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="9f57d-109">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="9f57d-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9f57d-110">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="9f57d-111">Daten: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9f57d-111">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9f57d-112">Ein Qubit, das um $Y $ um $ \pi/$4 gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f57d-112">A qubit to be rotated about $Y$ by $\pi / 4$.</span></span>


### <a name="magic--qubit"></a><span data-ttu-id="9f57d-113">Magic: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9f57d-113">magic : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9f57d-114">Ein Qubit, das sich anfänglich im Magic-Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="9f57d-114">A qubit initially in the magic state.</span></span> <span data-ttu-id="9f57d-115">Die folgende Anwendung dieses Vorgangs `magic` wird an den Status "$ \ket $" zurückgegeben {0} .</span><span class="sxs-lookup"><span data-stu-id="9f57d-115">Following application of this operation, `magic` is returned to the $\ket{0}$ state.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9f57d-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9f57d-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9f57d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f57d-117">Remarks</span></span>

<span data-ttu-id="9f57d-118">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="9f57d-118">The following are equivalent:</span></span>

```qsharp
Ry(PI() / 4.0, data);
```

<span data-ttu-id="9f57d-119">and</span><span class="sxs-lookup"><span data-stu-id="9f57d-119">and</span></span>

```qsharp
using (magic = Qubit()) {
    Ry(PI() / 4.0, magic);
    InjectPi4YRotation(data, magic);
    Reset(magic);
}
```

<span data-ttu-id="9f57d-120">Dieser Vorgang unterstützt das `Adjoint` Funktor. in diesem Fall wird derselbe magische Zustand verwendet, aber die Auswirkung auf das Daten-Qubit ist eine $-\ pi/4 $ $Y $-Rotation.</span><span class="sxs-lookup"><span data-stu-id="9f57d-120">This operation supports the `Adjoint` functor, in which case the same magic state is consumed, but the effect on the data qubit is a $-\pi/4$ $Y$-rotation.</span></span>