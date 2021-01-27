---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC
title: Applyrevereindopbec-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBEC
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: 7d118d1b04c37a80e61dfab2ee2265b3596b5877
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843553"
---
# <a name="applyreversedopbec-operation"></a><span data-ttu-id="95c12-102">Applyrevereindopbec-Vorgang</span><span class="sxs-lookup"><span data-stu-id="95c12-102">ApplyReversedOpBEC operation</span></span>

<span data-ttu-id="95c12-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="95c12-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="95c12-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="95c12-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="95c12-105">Wendet einen Vorgang an, der eine Big-Endian-Eingabe an eine Register Codierung einer Ganzzahl ohne Vorzeichen unter Verwendung des Little-Endian-Formats nimmt.</span><span class="sxs-lookup"><span data-stu-id="95c12-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBEC (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="95c12-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="95c12-106">Input</span></span>

### <a name="op--bigendian--unit--is-ctl"></a><span data-ttu-id="95c12-107">OP: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="95c12-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="95c12-108">Der Vorgang, der auf ein Big-in-Register-Register angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="95c12-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="95c12-109">Register: [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="95c12-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="95c12-110">Ein zu transformierende Little--zu-Ende-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="95c12-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="95c12-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="95c12-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="95c12-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="95c12-112">See Also</span></span>

- [<span data-ttu-id="95c12-113">Microsoft. Quantum. Arithmetik. applyrevereldopbe</span><span class="sxs-lookup"><span data-stu-id="95c12-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="95c12-114">Microsoft. Quantum. Arithmetik. applyrevereldopbea</span><span class="sxs-lookup"><span data-stu-id="95c12-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="95c12-115">Microsoft. Quantum. Arithmetik. applyreversegdopbeca</span><span class="sxs-lookup"><span data-stu-id="95c12-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)