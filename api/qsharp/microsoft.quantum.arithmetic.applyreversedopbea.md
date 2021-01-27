---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA
title: Applyrevereindopbea-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBEA
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: 1759764947cdbd84a1db945296d441a13f13767e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843588"
---
# <a name="applyreversedopbea-operation"></a><span data-ttu-id="5875b-102">Applyrevereindopbea-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5875b-102">ApplyReversedOpBEA operation</span></span>

<span data-ttu-id="5875b-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5875b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5875b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5875b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5875b-105">Wendet einen Vorgang an, der eine Big-Endian-Eingabe an eine Register Codierung einer Ganzzahl ohne Vorzeichen unter Verwendung des Little-Endian-Formats nimmt.</span><span class="sxs-lookup"><span data-stu-id="5875b-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBEA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="5875b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5875b-106">Input</span></span>

### <a name="op--bigendian--unit--is-adj"></a><span data-ttu-id="5875b-107">OP: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="5875b-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="5875b-108">Der Vorgang, der auf ein Big-in-Register-Register angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5875b-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="5875b-109">Register: [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5875b-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="5875b-110">Ein zu transformierende Little--zu-Ende-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="5875b-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5875b-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5875b-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="5875b-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5875b-112">See Also</span></span>

- [<span data-ttu-id="5875b-113">Microsoft. Quantum. Arithmetik. applyrevereldopbe</span><span class="sxs-lookup"><span data-stu-id="5875b-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="5875b-114">Microsoft. Quantum. Arithmetik. applyrevertendopbec</span><span class="sxs-lookup"><span data-stu-id="5875b-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [<span data-ttu-id="5875b-115">Microsoft. Quantum. Arithmetik. applyreversegdopbeca</span><span class="sxs-lookup"><span data-stu-id="5875b-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)