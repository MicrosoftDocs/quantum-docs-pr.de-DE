---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA
title: Applyrevereindopbeca-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBECA
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: 71e99d3390a2e510fd7ed28f3f6d8ed43b3ca7e6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843583"
---
# <a name="applyreversedopbeca-operation"></a><span data-ttu-id="13fdc-102">Applyrevereindopbeca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="13fdc-102">ApplyReversedOpBECA operation</span></span>

<span data-ttu-id="13fdc-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="13fdc-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="13fdc-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="13fdc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="13fdc-105">Wendet einen Vorgang an, der eine Big-Endian-Eingabe an eine Register Codierung einer Ganzzahl ohne Vorzeichen unter Verwendung des Little-Endian-Formats nimmt.</span><span class="sxs-lookup"><span data-stu-id="13fdc-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBECA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl + Adj), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="13fdc-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="13fdc-106">Input</span></span>

### <a name="op--bigendian--unit--is-adj--ctl"></a><span data-ttu-id="13fdc-107">OP: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="13fdc-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="13fdc-108">Der Vorgang, der auf ein Big-in-Register-Register angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="13fdc-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="13fdc-109">Register: [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="13fdc-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="13fdc-110">Ein zu transformierende Little--zu-Ende-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="13fdc-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="13fdc-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="13fdc-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="13fdc-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="13fdc-112">See Also</span></span>

- [<span data-ttu-id="13fdc-113">Microsoft. Quantum. Arithmetik. applyrevereldopbe</span><span class="sxs-lookup"><span data-stu-id="13fdc-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="13fdc-114">Microsoft. Quantum. Arithmetik. applyrevereldopbea</span><span class="sxs-lookup"><span data-stu-id="13fdc-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="13fdc-115">Microsoft. Quantum. Arithmetik. applyrevertendopbec</span><span class="sxs-lookup"><span data-stu-id="13fdc-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)