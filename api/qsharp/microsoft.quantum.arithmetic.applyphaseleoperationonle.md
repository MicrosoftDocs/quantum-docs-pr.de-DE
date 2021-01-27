---
uid: Microsoft.Quantum.Arithmetic.ApplyPhaseLEOperationOnLE
title: Applyphaseleoperationonle-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyPhaseLEOperationOnLE
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.littleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.phaselittleendian>.
ms.openlocfilehash: d94fdb55e051e76dd518eff14b80d1a24516bf8a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843676"
---
# <a name="applyphaseleoperationonle-operation"></a><span data-ttu-id="39b09-102">Applyphaseleoperationonle-Vorgang</span><span class="sxs-lookup"><span data-stu-id="39b09-102">ApplyPhaseLEOperationOnLE operation</span></span>

<span data-ttu-id="39b09-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="39b09-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="39b09-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="39b09-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="39b09-105">Wendet einen Vorgang an, <xref:microsoft.quantum.arithmetic.littleendian> der ein Register als Eingabe für ein Ziel Register des Typs annimmt <xref:microsoft.quantum.arithmetic.phaselittleendian> .</span><span class="sxs-lookup"><span data-stu-id="39b09-105">Applies an operation that takes a <xref:microsoft.quantum.arithmetic.littleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.phaselittleendian>.</span></span>

```qsharp
operation ApplyPhaseLEOperationOnLE (op : (Microsoft.Quantum.Arithmetic.PhaseLittleEndian => Unit), target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="39b09-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39b09-106">Input</span></span>

### <a name="op--phaselittleendian--unit"></a><span data-ttu-id="39b09-107">OP: [phaselittleerdian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="39b09-107">op : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="39b09-108">Der anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="39b09-108">The operation to be applied.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="39b09-109">Ziel: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="39b09-109">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="39b09-110">Das Register, auf das der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="39b09-110">The register to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="39b09-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="39b09-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="39b09-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39b09-112">Remarks</span></span>

<span data-ttu-id="39b09-113">Das Register wird `PhaseLittleEndian` durch die Verwendung von transformiert <xref:microsoft.quantum.canon.qftle> und dann nach der Anwendung von an seine ursprüngliche Darstellung zurückgegeben `op` .</span><span class="sxs-lookup"><span data-stu-id="39b09-113">The register is transformed to `PhaseLittleEndian` by the use of <xref:microsoft.quantum.canon.qftle> and is then returned to its original representation after application of `op`.</span></span>

## <a name="see-also"></a><span data-ttu-id="39b09-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="39b09-114">See Also</span></span>

- [<span data-ttu-id="39b09-115">Microsoft. Quantum. Canon. applyphaseleoperationonlea</span><span class="sxs-lookup"><span data-stu-id="39b09-115">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [<span data-ttu-id="39b09-116">Microsoft. Quantum. Canon. applyphaseleoperationonlea</span><span class="sxs-lookup"><span data-stu-id="39b09-116">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [<span data-ttu-id="39b09-117">Microsoft. Quantum. Canon. applyphaseleoperationonleca</span><span class="sxs-lookup"><span data-stu-id="39b09-117">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLECA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLECA)