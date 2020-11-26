---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLEC
title: Reversetdoplec-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLEC
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: 8c91391691b23786df02ae2a35264b578dccad41
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222081"
---
# <a name="reversedoplec-function"></a><span data-ttu-id="53488-102">Reversetdoplec-Funktion</span><span class="sxs-lookup"><span data-stu-id="53488-102">ReversedOpLEC function</span></span>

<span data-ttu-id="53488-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="53488-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="53488-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="53488-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="53488-105">Gibt bei einem Vorgang, der eine Little-Endian-Eingabe annimmt, einen neuen Vorgang zurück, der eine Big-Endian-Eingabe annimmt.</span><span class="sxs-lookup"><span data-stu-id="53488-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLEC (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="53488-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53488-106">Input</span></span>

### <a name="op--littleendian--unit--is-ctl"></a><span data-ttu-id="53488-107">OP: [littleandian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="53488-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="53488-108">Der Vorgang, dessen Eingabe umgekehrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="53488-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit--is-ctl"></a><span data-ttu-id="53488-109">Ausgabe: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="53488-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="53488-110">Ein neuer Vorgang, der seine Eingabe als Big-tedian-Register akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="53488-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="53488-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="53488-111">See Also</span></span>

- [<span data-ttu-id="53488-112">Microsoft. Quantum. Arithmetik. applyrevereldoplec</span><span class="sxs-lookup"><span data-stu-id="53488-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)
- [<span data-ttu-id="53488-113">Microsoft. Quantum. Arithmetik. reverldople</span><span class="sxs-lookup"><span data-stu-id="53488-113">Microsoft.Quantum.Arithmetic.ReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [<span data-ttu-id="53488-114">Microsoft. Quantum. Arithmetik. revereindoplea</span><span class="sxs-lookup"><span data-stu-id="53488-114">Microsoft.Quantum.Arithmetic.ReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [<span data-ttu-id="53488-115">Microsoft. Quantum. Arithmetik. reversegdopleca</span><span class="sxs-lookup"><span data-stu-id="53488-115">Microsoft.Quantum.Arithmetic.ReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)