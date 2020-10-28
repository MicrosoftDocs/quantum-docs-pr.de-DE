---
uid: Microsoft.Quantum.ErrorCorrection.InjectPi4YRotation
title: InjectPi4YRotation-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: InjectPi4YRotation
qsharp.summary: Rotates a single qubit by π/4 about the Y-axis.
ms.openlocfilehash: 8558767050c317661dfb490143fa3c8f4ea009e2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702474"
---
# <a name="injectpi4yrotation-operation"></a><span data-ttu-id="f2dbb-102">InjectPi4YRotation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f2dbb-102">InjectPi4YRotation operation</span></span>

<span data-ttu-id="f2dbb-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="f2dbb-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="f2dbb-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f2dbb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f2dbb-105">Dreht ein einzelnes Qubit um die Y-Achse.</span><span class="sxs-lookup"><span data-stu-id="f2dbb-105">Rotates a single qubit by π/4 about the Y-axis.</span></span>

```qsharp
operation InjectPi4YRotation (data : Qubit, magic : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="f2dbb-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2dbb-106">Description</span></span>

<span data-ttu-id="f2dbb-107">Führt eine Drehung/4-Drehung um durch `Y` .</span><span class="sxs-lookup"><span data-stu-id="f2dbb-107">Performs a π/4 rotation about `Y`.</span></span>

<span data-ttu-id="f2dbb-108">Die Drehung erfolgt durch die Verwendung eines magischen Zustands. Das heißt, eine Kopie des Zustands $ $ \begin{align} \cos\bruchteil {\pi} {8} \ket {0} + \sin \bruchteil {\pi} {8} \ket {1} .</span><span class="sxs-lookup"><span data-stu-id="f2dbb-108">The rotation is performed by consuming a magic state; that is, a copy of the state $$ \begin{align} \cos\frac{\pi}{8} \ket{0} + \sin \frac{\pi}{8} \ket{1}.</span></span>
<span data-ttu-id="f2dbb-109">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="f2dbb-109">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="f2dbb-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2dbb-110">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="f2dbb-111">Daten: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f2dbb-111">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f2dbb-112">Ein Qubit, das um $Y $ um $ \pi/$4 gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2dbb-112">A qubit to be rotated about $Y$ by $\pi / 4$.</span></span>


### <a name="magic--qubit"></a><span data-ttu-id="f2dbb-113">Magic: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f2dbb-113">magic : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f2dbb-114">Ein Qubit, das sich anfänglich im Magic-Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="f2dbb-114">A qubit initially in the magic state.</span></span> <span data-ttu-id="f2dbb-115">Die folgende Anwendung dieses Vorgangs `magic` wird an den Status "$ \ket $" zurückgegeben {0} .</span><span class="sxs-lookup"><span data-stu-id="f2dbb-115">Following application of this operation, `magic` is returned to the $\ket{0}$ state.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f2dbb-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f2dbb-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f2dbb-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f2dbb-117">Remarks</span></span>

<span data-ttu-id="f2dbb-118">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="f2dbb-118">The following are equivalent:</span></span>

```qsharp
Ry(PI() / 4.0, data);
```

<span data-ttu-id="f2dbb-119">und</span><span class="sxs-lookup"><span data-stu-id="f2dbb-119">and</span></span>

```qsharp
using (magic = Qubit()) {
    Ry(PI() / 4.0, magic);
    InjectPi4YRotation(data, magic);
    Reset(magic);
}
```

<span data-ttu-id="f2dbb-120">Dieser Vorgang unterstützt das `Adjoint` Funktor. in diesem Fall wird derselbe magische Zustand verwendet, aber die Auswirkung auf das Daten-Qubit ist eine $-\ pi/4 $ $Y $-Rotation.</span><span class="sxs-lookup"><span data-stu-id="f2dbb-120">This operation supports the `Adjoint` functor, in which case the same magic state is consumed, but the effect on the data qubit is a $-\pi/4$ $Y$-rotation.</span></span>