---
uid: Microsoft.Quantum.Arithmetic.ApplyPhaseLEOperationOnLE
title: Applyphaseleoperationonle-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyPhaseLEOperationOnLE
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.littleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.phaselittleendian>.
ms.openlocfilehash: dacc52766cf72d2bd562b76fc4939f962133e9a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707562"
---
# <a name="applyphaseleoperationonle-operation"></a><span data-ttu-id="871db-102">Applyphaseleoperationonle-Vorgang</span><span class="sxs-lookup"><span data-stu-id="871db-102">ApplyPhaseLEOperationOnLE operation</span></span>

<span data-ttu-id="871db-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="871db-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="871db-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="871db-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="871db-105">Wendet einen Vorgang an, <xref:microsoft.quantum.arithmetic.littleendian> der ein Register als Eingabe für ein Ziel Register des Typs annimmt <xref:microsoft.quantum.arithmetic.phaselittleendian> .</span><span class="sxs-lookup"><span data-stu-id="871db-105">Applies an operation that takes a <xref:microsoft.quantum.arithmetic.littleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.phaselittleendian>.</span></span>

```qsharp
operation ApplyPhaseLEOperationOnLE (op : (Microsoft.Quantum.Arithmetic.PhaseLittleEndian => Unit), target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="871db-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="871db-106">Input</span></span>

### <a name="op--phaselittleendian--unit"></a><span data-ttu-id="871db-107">OP: [phaselittleerdian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="871db-107">op : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="871db-108">Der anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="871db-108">The operation to be applied.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="871db-109">Ziel: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="871db-109">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="871db-110">Das Register, auf das der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="871db-110">The register to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="871db-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="871db-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="871db-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="871db-112">Remarks</span></span>

<span data-ttu-id="871db-113">Das Register wird `PhaseLittleEndian` durch die Verwendung von transformiert <xref:microsoft.quantum.canon.qftle> und dann nach der Anwendung von an seine ursprüngliche Darstellung zurückgegeben `op` .</span><span class="sxs-lookup"><span data-stu-id="871db-113">The register is transformed to `PhaseLittleEndian` by the use of <xref:microsoft.quantum.canon.qftle> and is then returned to its original representation after application of `op`.</span></span>

## <a name="see-also"></a><span data-ttu-id="871db-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="871db-114">See Also</span></span>

- [<span data-ttu-id="871db-115">Microsoft. Quantum. Canon. applyphaseleoperationonlea</span><span class="sxs-lookup"><span data-stu-id="871db-115">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [<span data-ttu-id="871db-116">Microsoft. Quantum. Canon. applyphaseleoperationonlea</span><span class="sxs-lookup"><span data-stu-id="871db-116">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [<span data-ttu-id="871db-117">Microsoft. Quantum. Canon. applyphaseleoperationonleca</span><span class="sxs-lookup"><span data-stu-id="871db-117">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLECA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLECA)