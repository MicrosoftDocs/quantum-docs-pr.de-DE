---
uid: Microsoft.Quantum.Canon.GrayCode
title: Graycode-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: fc673ae21a952788b5beb74c1bad94ee9fe54480
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704167"
---
# <a name="graycode-function"></a><span data-ttu-id="99dcc-102">Graycode-Funktion</span><span class="sxs-lookup"><span data-stu-id="99dcc-102">GrayCode function</span></span>

<span data-ttu-id="99dcc-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="99dcc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="99dcc-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="99dcc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="99dcc-105">Erstellt graue Codesequenzen.</span><span class="sxs-lookup"><span data-stu-id="99dcc-105">Creates Gray code sequences</span></span>

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="99dcc-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="99dcc-106">Input</span></span>

### <a name="n--int"></a><span data-ttu-id="99dcc-107">n: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="99dcc-107">n : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="99dcc-108">Anzahl von Bits</span><span class="sxs-lookup"><span data-stu-id="99dcc-108">Number of bits</span></span>



## <a name="output--intint"></a><span data-ttu-id="99dcc-109">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="99dcc-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="99dcc-110">Array von Tupeln.</span><span class="sxs-lookup"><span data-stu-id="99dcc-110">Array of tuples.</span></span> <span data-ttu-id="99dcc-111">Der erste Wert im Tupel ist der Wert in grau Punkt Sequenz zweiter Wert in Tupel ist Position, um den aktuellen Wert zu ändern, um den nächsten Wert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="99dcc-111">First value in tuple is value in GrayCode sequence Second value in tuple is position to change in current value to get next one.</span></span>