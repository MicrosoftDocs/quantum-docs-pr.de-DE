---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBECA
title: Reversetdopbeca-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBECA
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: da21b09110400ad4ee862f662d45e166a49e7bd8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222200"
---
# <a name="reversedopbeca-function"></a><span data-ttu-id="aa0a1-102">Reversetdopbeca-Funktion</span><span class="sxs-lookup"><span data-stu-id="aa0a1-102">ReversedOpBECA function</span></span>

<span data-ttu-id="aa0a1-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="aa0a1-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="aa0a1-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="aa0a1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="aa0a1-105">Gibt bei einem Vorgang, der eine Big-Endian-Eingabe annimmt, einen neuen Vorgang zurück, der eine Little-Endian-Eingabe annimmt.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBECA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj + Ctl)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="aa0a1-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aa0a1-106">Input</span></span>

### <a name="op--bigendian--unit--is-adj--ctl"></a><span data-ttu-id="aa0a1-107">OP: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="aa0a1-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="aa0a1-108">Der Vorgang, dessen Eingabe umgekehrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="aa0a1-109">Ausgabe: die [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="aa0a1-110">Ein neuer Vorgang, der seine Eingabe als Little-in-der-Register-Registrierung akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa0a1-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="aa0a1-111">See Also</span></span>

- [<span data-ttu-id="aa0a1-112">Microsoft. Quantum. Arithmetik. applyreversegdopbeca</span><span class="sxs-lookup"><span data-stu-id="aa0a1-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)
- [<span data-ttu-id="aa0a1-113">Microsoft. Quantum. Arithmetik. revereindopbe</span><span class="sxs-lookup"><span data-stu-id="aa0a1-113">Microsoft.Quantum.Arithmetic.ReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [<span data-ttu-id="aa0a1-114">Microsoft. Quantum. Arithmetik. revereindopbea</span><span class="sxs-lookup"><span data-stu-id="aa0a1-114">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="aa0a1-115">Microsoft. Quantum. Arithmetik. revereindopbec</span><span class="sxs-lookup"><span data-stu-id="aa0a1-115">Microsoft.Quantum.Arithmetic.ReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)