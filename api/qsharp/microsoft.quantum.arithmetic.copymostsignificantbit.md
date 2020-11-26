---
uid: Microsoft.Quantum.Arithmetic.CopyMostSignificantBit
title: Copymustsignifiantbit-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CopyMostSignificantBit
qsharp.summary: Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.
ms.openlocfilehash: 39a2dc2fe33f46c2767def06a44cde07e2f01497
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223288"
---
# <a name="copymostsignificantbit-operation"></a><span data-ttu-id="8b1ed-102">Copymustsignifiantbit-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8b1ed-102">CopyMostSignificantBit operation</span></span>

<span data-ttu-id="8b1ed-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="8b1ed-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="8b1ed-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8b1ed-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8b1ed-105">Kopiert das signifikanteste Bit eines Qubit-Registers, das `from` eine Ganzzahl ohne Vorzeichen in das Qubit darstellt `target` .</span><span class="sxs-lookup"><span data-stu-id="8b1ed-105">Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.</span></span>

```qsharp
operation CopyMostSignificantBit (from : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="8b1ed-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8b1ed-106">Input</span></span>

### <a name="from--littleendian"></a><span data-ttu-id="8b1ed-107">von: [littleddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8b1ed-107">from : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="8b1ed-108">Die Ganzzahl ohne Vorzeichen, von der das höchste Bit kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="8b1ed-108">The unsigned integer from which the highest bit is copied from.</span></span>
<span data-ttu-id="8b1ed-109">die Ganzzahl wird im Little-Endian-Format codiert.</span><span class="sxs-lookup"><span data-stu-id="8b1ed-109">the integer is encoded in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="8b1ed-110">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8b1ed-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="8b1ed-111">Das Qubit, in dem das höchste Bit kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="8b1ed-111">The qubit in which the highest bit is being copied.</span></span> <span data-ttu-id="8b1ed-112">Die Bitcodierung erfolgt auf Berechnungsbasis.</span><span class="sxs-lookup"><span data-stu-id="8b1ed-112">The bit encoding is in computational basis.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8b1ed-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8b1ed-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="8b1ed-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8b1ed-114">See Also</span></span>

- [<span data-ttu-id="8b1ed-115">Microsoft. Quantum. Arithmetik. Little-Dian</span><span class="sxs-lookup"><span data-stu-id="8b1ed-115">Microsoft.Quantum.Arithmetic.LittleEndian</span></span>](xref:Microsoft.Quantum.Arithmetic.LittleEndian)