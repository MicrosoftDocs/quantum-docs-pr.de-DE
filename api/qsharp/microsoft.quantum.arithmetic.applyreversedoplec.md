---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC
title: Applyrevereindoplec-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLEC
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: 75b6c0f09c0699b50d9ac1b0274e8074520fc241
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202650"
---
# <a name="applyreversedoplec-operation"></a><span data-ttu-id="3c86d-102">Applyrevereindoplec-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3c86d-102">ApplyReversedOpLEC operation</span></span>

<span data-ttu-id="3c86d-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="3c86d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="3c86d-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3c86d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3c86d-105">Wendet einen Vorgang an, der eine Little-Endian-Eingabe an eine Register Codierung einer Ganzzahl ohne Vorzeichen unter Verwendung des Big-Endian-Formats nimmt.</span><span class="sxs-lookup"><span data-stu-id="3c86d-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLEC (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="3c86d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3c86d-106">Input</span></span>

### <a name="op--littleendian--unit--is-ctl"></a><span data-ttu-id="3c86d-107">OP: [littleandian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="3c86d-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="3c86d-108">Der Vorgang, der für ein Little-in-Register-Register fungiert.</span><span class="sxs-lookup"><span data-stu-id="3c86d-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="3c86d-109">registrieren: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="3c86d-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="3c86d-110">Ein Big-tedian-Register, das transformiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c86d-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3c86d-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3c86d-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="3c86d-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3c86d-112">See Also</span></span>

- [<span data-ttu-id="3c86d-113">Microsoft. Quantum. Arithmetik. applyreverldople</span><span class="sxs-lookup"><span data-stu-id="3c86d-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="3c86d-114">Microsoft. Quantum. Arithmetik. applyrevereldoplea</span><span class="sxs-lookup"><span data-stu-id="3c86d-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="3c86d-115">Microsoft. Quantum. Arithmetik. applyreversegdopleca</span><span class="sxs-lookup"><span data-stu-id="3c86d-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)