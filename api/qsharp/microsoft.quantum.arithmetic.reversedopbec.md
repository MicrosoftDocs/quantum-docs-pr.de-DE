---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBEC
title: Reversetdopbec-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBEC
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 5e9aa6e6dfef74bca004170cf2b1cd91aa13f0b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706314"
---
# <a name="reversedopbec-function"></a><span data-ttu-id="92e5f-102">Reversetdopbec-Funktion</span><span class="sxs-lookup"><span data-stu-id="92e5f-102">ReversedOpBEC function</span></span>

<span data-ttu-id="92e5f-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="92e5f-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="92e5f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="92e5f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="92e5f-105">Gibt bei einem Vorgang, der eine Big-Endian-Eingabe annimmt, einen neuen Vorgang zurück, der eine Little-Endian-Eingabe annimmt.</span><span class="sxs-lookup"><span data-stu-id="92e5f-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBEC (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="92e5f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="92e5f-106">Input</span></span>

### <a name="op--bigendian--unit-ctl"></a><span data-ttu-id="92e5f-107">OP: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="92e5f-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="92e5f-108">Der Vorgang, dessen Eingabe umgekehrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="92e5f-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit-ctl"></a><span data-ttu-id="92e5f-109">Ausgabe: [littleddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="92e5f-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="92e5f-110">Ein neuer Vorgang, der seine Eingabe als Little-in-der-Register-Registrierung akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="92e5f-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="92e5f-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="92e5f-111">See Also</span></span>

- [<span data-ttu-id="92e5f-112">Microsoft. Quantum. Arithmetik. applyrevertendopbec</span><span class="sxs-lookup"><span data-stu-id="92e5f-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [<span data-ttu-id="92e5f-113">Microsoft. Quantum. Arithmetik. revereindopbe</span><span class="sxs-lookup"><span data-stu-id="92e5f-113">Microsoft.Quantum.Arithmetic.ReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [<span data-ttu-id="92e5f-114">Microsoft. Quantum. Arithmetik. revereindopbea</span><span class="sxs-lookup"><span data-stu-id="92e5f-114">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="92e5f-115">Microsoft. Quantum. Arithmetik. revereindopbeca</span><span class="sxs-lookup"><span data-stu-id="92e5f-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)