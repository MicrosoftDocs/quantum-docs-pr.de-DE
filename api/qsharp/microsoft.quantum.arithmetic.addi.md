---
uid: Microsoft.Quantum.Arithmetic.AddI
title: ADDI-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddI
qsharp.summary: Automatically chooses between addition with carry and without, depending on the register size of `ys`.
ms.openlocfilehash: 7ee2b9099ea65b95647422dadc1efe4bf043d147
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707655"
---
# <a name="addi-operation"></a><span data-ttu-id="7568c-102">ADDI-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7568c-102">AddI operation</span></span>

<span data-ttu-id="7568c-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="7568c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="7568c-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7568c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7568c-105">Wählt in Abhängigkeit von der Register Größe von automatisch zwischen Addition und ohne ausführen und ohne aus `ys` .</span><span class="sxs-lookup"><span data-stu-id="7568c-105">Automatically chooses between addition with carry and without, depending on the register size of `ys`.</span></span>

```qsharp
operation AddI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="7568c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7568c-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="7568c-107">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7568c-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7568c-108">$n $-Bit-Addend.</span><span class="sxs-lookup"><span data-stu-id="7568c-108">$n$-bit addend.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="7568c-109">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7568c-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7568c-110">Addend mit mindestens $n $ Qubits.</span><span class="sxs-lookup"><span data-stu-id="7568c-110">Addend with at least $n$ qubits.</span></span> <span data-ttu-id="7568c-111">Enthält das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="7568c-111">Will hold the result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7568c-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7568c-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

