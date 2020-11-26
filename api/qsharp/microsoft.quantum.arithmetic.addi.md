---
uid: Microsoft.Quantum.Arithmetic.AddI
title: ADDI-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddI
qsharp.summary: Automatically chooses between addition with carry and without, depending on the register size of `ys`.
ms.openlocfilehash: 9a90d15defd57cf2836a6fda5b52ddaa816fd55e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191022"
---
# <a name="addi-operation"></a><span data-ttu-id="0545f-102">ADDI-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0545f-102">AddI operation</span></span>

<span data-ttu-id="0545f-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0545f-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0545f-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="0545f-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="0545f-105">Wählt in Abhängigkeit von der Register Größe von automatisch zwischen Addition und ohne ausführen und ohne aus `ys` .</span><span class="sxs-lookup"><span data-stu-id="0545f-105">Automatically chooses between addition with carry and without, depending on the register size of `ys`.</span></span>

```qsharp
operation AddI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="0545f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0545f-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="0545f-107">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0545f-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0545f-108">$n $-Bit-Addend.</span><span class="sxs-lookup"><span data-stu-id="0545f-108">$n$-bit addend.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="0545f-109">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0545f-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0545f-110">Addend mit mindestens $n $ Qubits.</span><span class="sxs-lookup"><span data-stu-id="0545f-110">Addend with at least $n$ qubits.</span></span> <span data-ttu-id="0545f-111">Enthält das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="0545f-111">Will hold the result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0545f-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0545f-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

