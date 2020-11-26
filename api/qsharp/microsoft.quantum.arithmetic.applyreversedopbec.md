---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC
title: Applyrevereindopbec-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBEC
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: 3a5fef3bb4549433540b2a7b5e94d3cd2d527639
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202769"
---
# <a name="applyreversedopbec-operation"></a><span data-ttu-id="cefea-102">Applyrevereindopbec-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cefea-102">ApplyReversedOpBEC operation</span></span>

<span data-ttu-id="cefea-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="cefea-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="cefea-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cefea-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cefea-105">Wendet einen Vorgang an, der eine Big-Endian-Eingabe an eine Register Codierung einer Ganzzahl ohne Vorzeichen unter Verwendung des Little-Endian-Formats nimmt.</span><span class="sxs-lookup"><span data-stu-id="cefea-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBEC (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="cefea-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cefea-106">Input</span></span>

### <a name="op--bigendian--unit--is-ctl"></a><span data-ttu-id="cefea-107">OP: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="cefea-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="cefea-108">Der Vorgang, der auf ein Big-in-Register-Register angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="cefea-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="cefea-109">Register: [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="cefea-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="cefea-110">Ein zu transformierende Little--zu-Ende-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="cefea-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cefea-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cefea-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="cefea-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cefea-112">See Also</span></span>

- [<span data-ttu-id="cefea-113">Microsoft. Quantum. Arithmetik. applyrevereldopbe</span><span class="sxs-lookup"><span data-stu-id="cefea-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="cefea-114">Microsoft. Quantum. Arithmetik. applyrevereldopbea</span><span class="sxs-lookup"><span data-stu-id="cefea-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="cefea-115">Microsoft. Quantum. Arithmetik. applyreversegdopbeca</span><span class="sxs-lookup"><span data-stu-id="cefea-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)