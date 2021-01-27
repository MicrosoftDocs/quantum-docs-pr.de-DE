---
uid: Microsoft.Quantum.Arithmetic.AddI
title: ADDI-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddI
qsharp.summary: Automatically chooses between addition with carry and without, depending on the register size of `ys`.
ms.openlocfilehash: a17403652cc2b2712defe52112a3ac599330da9f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843843"
---
# <a name="addi-operation"></a><span data-ttu-id="7b040-102">ADDI-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7b040-102">AddI operation</span></span>

<span data-ttu-id="7b040-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="7b040-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="7b040-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="7b040-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="7b040-105">Wählt in Abhängigkeit von der Register Größe von automatisch zwischen Addition und ohne ausführen und ohne aus `ys` .</span><span class="sxs-lookup"><span data-stu-id="7b040-105">Automatically chooses between addition with carry and without, depending on the register size of `ys`.</span></span>

```qsharp
operation AddI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="7b040-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7b040-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="7b040-107">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7b040-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7b040-108">$n $-Bit-Addend.</span><span class="sxs-lookup"><span data-stu-id="7b040-108">$n$-bit addend.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="7b040-109">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7b040-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7b040-110">Addend mit mindestens $n $ Qubits.</span><span class="sxs-lookup"><span data-stu-id="7b040-110">Addend with at least $n$ qubits.</span></span> <span data-ttu-id="7b040-111">Enthält das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="7b040-111">Will hold the result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7b040-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7b040-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

