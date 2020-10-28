---
uid: Microsoft.Quantum.Arithmetic.ApplyLEOperationOnPhaseLEA
title: Applyleoperationonphaselea-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyLEOperationOnPhaseLEA
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.
ms.openlocfilehash: 572c66b201b6d2c816017230527c70c1b3c83371
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707615"
---
# <a name="applyleoperationonphaselea-operation"></a><span data-ttu-id="5e129-102">Applyleoperationonphaselea-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5e129-102">ApplyLEOperationOnPhaseLEA operation</span></span>

<span data-ttu-id="5e129-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5e129-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5e129-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5e129-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5e129-105">Wendet einen Vorgang an, <xref:microsoft.quantum.arithmetic.phaselittleendian> der ein Register als Eingabe für ein Ziel Register des Typs annimmt <xref:microsoft.quantum.arithmetic.littleendian> .</span><span class="sxs-lookup"><span data-stu-id="5e129-105">Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.</span></span>

```qsharp
operation ApplyLEOperationOnPhaseLEA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj), target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="5e129-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5e129-106">Input</span></span>

### <a name="op--littleendian--unit-adj"></a><span data-ttu-id="5e129-107">OP: [littleandian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="5e129-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="5e129-108">Der anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="5e129-108">The operation to be applied.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="5e129-109">Ziel: [phaselittleenddian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5e129-109">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="5e129-110">Das Register, auf das der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5e129-110">The register to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5e129-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5e129-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5e129-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5e129-112">Remarks</span></span>

<span data-ttu-id="5e129-113">Das Register wird `LittleEndian` durch die Verwendung von transformiert <xref:microsoft.quantum.canon.qftle> und dann nach der Anwendung von an seine ursprüngliche Darstellung zurückgegeben `op` .</span><span class="sxs-lookup"><span data-stu-id="5e129-113">The register is transformed to `LittleEndian` by the use of <xref:microsoft.quantum.canon.qftle> and is then returned to its original representation after application of `op`.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e129-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5e129-114">See Also</span></span>

- [<span data-ttu-id="5e129-115">Microsoft. Quantum. Canon. applyleoperationonphasele</span><span class="sxs-lookup"><span data-stu-id="5e129-115">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLE</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLE)
- [<span data-ttu-id="5e129-116">Microsoft. Quantum. Canon. applyleoperationonphaselec</span><span class="sxs-lookup"><span data-stu-id="5e129-116">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEC</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEC)
- [<span data-ttu-id="5e129-117">Microsoft. Quantum. Canon. applyleoperationonphaseleca</span><span class="sxs-lookup"><span data-stu-id="5e129-117">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLECA</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLECA)