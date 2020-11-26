---
uid: Microsoft.Quantum.Canon.GrayCode
title: Graycode-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: b15586c57180b00064721afc990436320824cba2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206883"
---
# <a name="graycode-function"></a><span data-ttu-id="d995e-102">Graycode-Funktion</span><span class="sxs-lookup"><span data-stu-id="d995e-102">GrayCode function</span></span>

<span data-ttu-id="d995e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d995e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d995e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d995e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d995e-105">Erstellt graue Codesequenzen.</span><span class="sxs-lookup"><span data-stu-id="d995e-105">Creates Gray code sequences</span></span>

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="d995e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d995e-106">Input</span></span>

### <a name="n--int"></a><span data-ttu-id="d995e-107">n: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d995e-107">n : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d995e-108">Anzahl von Bits</span><span class="sxs-lookup"><span data-stu-id="d995e-108">Number of bits</span></span>



## <a name="output--intint"></a><span data-ttu-id="d995e-109">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="d995e-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="d995e-110">Array von Tupeln.</span><span class="sxs-lookup"><span data-stu-id="d995e-110">Array of tuples.</span></span> <span data-ttu-id="d995e-111">Der erste Wert im Tupel ist der Wert in grau Punkt Sequenz zweiter Wert in Tupel ist Position, um den aktuellen Wert zu ändern, um den nächsten Wert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d995e-111">First value in tuple is value in GrayCode sequence Second value in tuple is position to change in current value to get next one.</span></span>