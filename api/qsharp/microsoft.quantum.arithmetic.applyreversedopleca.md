---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA
title: Applyreverledopleca-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLECA
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: d0d444afcc1fa760f3035101e82cf8043c6541c5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843498"
---
# <a name="applyreversedopleca-operation"></a><span data-ttu-id="5edcf-102">Applyreverledopleca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5edcf-102">ApplyReversedOpLECA operation</span></span>

<span data-ttu-id="5edcf-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5edcf-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5edcf-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5edcf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5edcf-105">Wendet einen Vorgang an, der eine Little-Endian-Eingabe an eine Register Codierung einer Ganzzahl ohne Vorzeichen unter Verwendung des Big-Endian-Formats nimmt.</span><span class="sxs-lookup"><span data-stu-id="5edcf-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLECA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl + Adj), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="5edcf-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5edcf-106">Input</span></span>

### <a name="op--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="5edcf-107">OP: [littleandian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="5edcf-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="5edcf-108">Der Vorgang, der für ein Little-in-Register-Register fungiert.</span><span class="sxs-lookup"><span data-stu-id="5edcf-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="5edcf-109">registrieren: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="5edcf-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="5edcf-110">Ein Big-tedian-Register, das transformiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5edcf-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5edcf-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5edcf-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="5edcf-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5edcf-112">See Also</span></span>

- [<span data-ttu-id="5edcf-113">Microsoft. Quantum. Arithmetik. applyreverldople</span><span class="sxs-lookup"><span data-stu-id="5edcf-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="5edcf-114">Microsoft. Quantum. Arithmetik. applyrevereldoplea</span><span class="sxs-lookup"><span data-stu-id="5edcf-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="5edcf-115">Microsoft. Quantum. Arithmetik. applyrevereldoplec</span><span class="sxs-lookup"><span data-stu-id="5edcf-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)