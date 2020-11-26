---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLEA
title: Reversetdoplea-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLEA
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: 71b6b87a44f541e5379d8de8a3562febbfa49e1d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222166"
---
# <a name="reversedoplea-function"></a><span data-ttu-id="67130-102">Reversetdoplea-Funktion</span><span class="sxs-lookup"><span data-stu-id="67130-102">ReversedOpLEA function</span></span>

<span data-ttu-id="67130-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="67130-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="67130-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="67130-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="67130-105">Gibt bei einem Vorgang, der eine Little-Endian-Eingabe annimmt, einen neuen Vorgang zurück, der eine Big-Endian-Eingabe annimmt.</span><span class="sxs-lookup"><span data-stu-id="67130-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLEA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="67130-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="67130-106">Input</span></span>

### <a name="op--littleendian--unit--is-adj"></a><span data-ttu-id="67130-107">OP: [littleandian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="67130-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="67130-108">Der Vorgang, dessen Eingabe umgekehrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="67130-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit--is-adj"></a><span data-ttu-id="67130-109">Ausgabe: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="67130-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="67130-110">Ein neuer Vorgang, der seine Eingabe als Big-tedian-Register akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="67130-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="67130-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="67130-111">See Also</span></span>

- [<span data-ttu-id="67130-112">Microsoft. Quantum. Arithmetik. applyrevereldoplea</span><span class="sxs-lookup"><span data-stu-id="67130-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="67130-113">Microsoft. Quantum. Arithmetik. reverldople</span><span class="sxs-lookup"><span data-stu-id="67130-113">Microsoft.Quantum.Arithmetic.ReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [<span data-ttu-id="67130-114">Microsoft. Quantum. Arithmetik. revereindoplec</span><span class="sxs-lookup"><span data-stu-id="67130-114">Microsoft.Quantum.Arithmetic.ReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)
- [<span data-ttu-id="67130-115">Microsoft. Quantum. Arithmetik. reversegdopleca</span><span class="sxs-lookup"><span data-stu-id="67130-115">Microsoft.Quantum.Arithmetic.ReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)