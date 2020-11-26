---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBE
title: Reversetdopbe-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBE
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 3c39a90ed4b5df09b90d8b5020d8b824285b50eb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222319"
---
# <a name="reversedopbe-function"></a><span data-ttu-id="5ca8d-102">Reversetdopbe-Funktion</span><span class="sxs-lookup"><span data-stu-id="5ca8d-102">ReversedOpBE function</span></span>

<span data-ttu-id="5ca8d-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5ca8d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5ca8d-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5ca8d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5ca8d-105">Gibt bei einem Vorgang, der eine Big-Endian-Eingabe annimmt, einen neuen Vorgang zurück, der eine Little-Endian-Eingabe annimmt.</span><span class="sxs-lookup"><span data-stu-id="5ca8d-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBE (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)
```


## <a name="input"></a><span data-ttu-id="5ca8d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ca8d-106">Input</span></span>

### <a name="op--bigendian--unit"></a><span data-ttu-id="5ca8d-107">OP: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5ca8d-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5ca8d-108">Der Vorgang, dessen Eingabe umgekehrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ca8d-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit"></a><span data-ttu-id="5ca8d-109">Ausgabe: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5ca8d-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5ca8d-110">Ein neuer Vorgang, der seine Eingabe als Little-in-der-Register-Registrierung akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="5ca8d-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ca8d-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5ca8d-111">See Also</span></span>

- [<span data-ttu-id="5ca8d-112">Microsoft. Quantum. Arithmetik. applyrevereldopbe</span><span class="sxs-lookup"><span data-stu-id="5ca8d-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="5ca8d-113">Microsoft. Quantum. Arithmetik. revereindopbea</span><span class="sxs-lookup"><span data-stu-id="5ca8d-113">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="5ca8d-114">Microsoft. Quantum. Arithmetik. revereindopbec</span><span class="sxs-lookup"><span data-stu-id="5ca8d-114">Microsoft.Quantum.Arithmetic.ReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [<span data-ttu-id="5ca8d-115">Microsoft. Quantum. Arithmetik. revereindopbeca</span><span class="sxs-lookup"><span data-stu-id="5ca8d-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)