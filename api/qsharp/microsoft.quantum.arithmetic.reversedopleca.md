---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLECA
title: Reversetdopleca-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLECA
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: c058243db2b4cee3a72e025b084b4f98f7020a6b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222064"
---
# <a name="reversedopleca-function"></a><span data-ttu-id="1bb24-102">Reversetdopleca-Funktion</span><span class="sxs-lookup"><span data-stu-id="1bb24-102">ReversedOpLECA function</span></span>

<span data-ttu-id="1bb24-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="1bb24-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="1bb24-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1bb24-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1bb24-105">Gibt bei einem Vorgang, der eine Little-Endian-Eingabe annimmt, einen neuen Vorgang zurück, der eine Big-Endian-Eingabe annimmt.</span><span class="sxs-lookup"><span data-stu-id="1bb24-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLECA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="1bb24-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1bb24-106">Input</span></span>

### <a name="op--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="1bb24-107">OP: [littleandian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="1bb24-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="1bb24-108">Der Vorgang, dessen Eingabe umgekehrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1bb24-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit--is-adj--ctl"></a><span data-ttu-id="1bb24-109">Ausgabe: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="1bb24-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="1bb24-110">Ein neuer Vorgang, der seine Eingabe als Big-tedian-Register akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="1bb24-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="1bb24-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1bb24-111">See Also</span></span>

- [<span data-ttu-id="1bb24-112">Microsoft. Quantum. Arithmetik. applyreversegdopleca</span><span class="sxs-lookup"><span data-stu-id="1bb24-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)
- [<span data-ttu-id="1bb24-113">Microsoft. Quantum. Arithmetik. reverldople</span><span class="sxs-lookup"><span data-stu-id="1bb24-113">Microsoft.Quantum.Arithmetic.ReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [<span data-ttu-id="1bb24-114">Microsoft. Quantum. Arithmetik. revereindoplea</span><span class="sxs-lookup"><span data-stu-id="1bb24-114">Microsoft.Quantum.Arithmetic.ReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [<span data-ttu-id="1bb24-115">Microsoft. Quantum. Arithmetik. revereindoplec</span><span class="sxs-lookup"><span data-stu-id="1bb24-115">Microsoft.Quantum.Arithmetic.ReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)