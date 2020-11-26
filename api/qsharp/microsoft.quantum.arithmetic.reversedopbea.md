---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBEA
title: Reversetdopbea-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBEA
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 69fd4401e6862a3a6afaa51fb5b8a3592768bb42
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222302"
---
# <a name="reversedopbea-function"></a><span data-ttu-id="8f0cc-102">Reversetdopbea-Funktion</span><span class="sxs-lookup"><span data-stu-id="8f0cc-102">ReversedOpBEA function</span></span>

<span data-ttu-id="8f0cc-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="8f0cc-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="8f0cc-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8f0cc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8f0cc-105">Gibt bei einem Vorgang, der eine Big-Endian-Eingabe annimmt, einen neuen Vorgang zurück, der eine Little-Endian-Eingabe annimmt.</span><span class="sxs-lookup"><span data-stu-id="8f0cc-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBEA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="8f0cc-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8f0cc-106">Input</span></span>

### <a name="op--bigendian--unit--is-adj"></a><span data-ttu-id="8f0cc-107">OP: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="8f0cc-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="8f0cc-108">Der Vorgang, dessen Eingabe umgekehrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f0cc-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit--is-adj"></a><span data-ttu-id="8f0cc-109">Ausgabe: die [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist "adj".</span><span class="sxs-lookup"><span data-stu-id="8f0cc-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="8f0cc-110">Ein neuer Vorgang, der seine Eingabe als Little-in-der-Register-Registrierung akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="8f0cc-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f0cc-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8f0cc-111">See Also</span></span>

- [<span data-ttu-id="8f0cc-112">Microsoft. Quantum. Arithmetik. applyrevereldopbea</span><span class="sxs-lookup"><span data-stu-id="8f0cc-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="8f0cc-113">Microsoft. Quantum. Arithmetik. revereindopbe</span><span class="sxs-lookup"><span data-stu-id="8f0cc-113">Microsoft.Quantum.Arithmetic.ReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [<span data-ttu-id="8f0cc-114">Microsoft. Quantum. Arithmetik. revereindopbec</span><span class="sxs-lookup"><span data-stu-id="8f0cc-114">Microsoft.Quantum.Arithmetic.ReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [<span data-ttu-id="8f0cc-115">Microsoft. Quantum. Arithmetik. revereindopbeca</span><span class="sxs-lookup"><span data-stu-id="8f0cc-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)