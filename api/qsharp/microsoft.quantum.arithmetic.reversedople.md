---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLE
title: Reverldople-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLE
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: 91b98663028b8a1d54c546e70d8bfe603d71d041
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222251"
---
# <a name="reversedople-function"></a><span data-ttu-id="2b5fa-102">Reverldople-Funktion</span><span class="sxs-lookup"><span data-stu-id="2b5fa-102">ReversedOpLE function</span></span>

<span data-ttu-id="2b5fa-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="2b5fa-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="2b5fa-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2b5fa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2b5fa-105">Gibt bei einem Vorgang, der eine Little-Endian-Eingabe annimmt, einen neuen Vorgang zurück, der eine Big-Endian-Eingabe annimmt.</span><span class="sxs-lookup"><span data-stu-id="2b5fa-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLE (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)
```


## <a name="input"></a><span data-ttu-id="2b5fa-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2b5fa-106">Input</span></span>

### <a name="op--littleendian--unit"></a><span data-ttu-id="2b5fa-107">OP: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2b5fa-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="2b5fa-108">Der Vorgang, dessen Eingabe umgekehrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b5fa-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit"></a><span data-ttu-id="2b5fa-109">Ausgabe: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2b5fa-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="2b5fa-110">Ein neuer Vorgang, der seine Eingabe als Big-tedian-Register akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="2b5fa-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b5fa-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2b5fa-111">See Also</span></span>

- [<span data-ttu-id="2b5fa-112">Microsoft. Quantum. Arithmetik. applyreverldople</span><span class="sxs-lookup"><span data-stu-id="2b5fa-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="2b5fa-113">Microsoft. Quantum. Arithmetik. revereindoplea</span><span class="sxs-lookup"><span data-stu-id="2b5fa-113">Microsoft.Quantum.Arithmetic.ReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [<span data-ttu-id="2b5fa-114">Microsoft. Quantum. Arithmetik. revereindoplec</span><span class="sxs-lookup"><span data-stu-id="2b5fa-114">Microsoft.Quantum.Arithmetic.ReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)
- [<span data-ttu-id="2b5fa-115">Microsoft. Quantum. Arithmetik. reversegdopleca</span><span class="sxs-lookup"><span data-stu-id="2b5fa-115">Microsoft.Quantum.Arithmetic.ReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)