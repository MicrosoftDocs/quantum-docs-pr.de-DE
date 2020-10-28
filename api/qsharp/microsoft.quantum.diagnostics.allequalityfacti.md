---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactI
title: Allequalityfakti-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactI
qsharp.summary: Asserts that two arrays of integer values are equal.
ms.openlocfilehash: 9ccd212010ae557de5ca4ab2a38d4724c5c29aa8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702797"
---
# <a name="allequalityfacti-function"></a><span data-ttu-id="753ec-102">Allequalityfakti-Funktion</span><span class="sxs-lookup"><span data-stu-id="753ec-102">AllEqualityFactI function</span></span>

<span data-ttu-id="753ec-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="753ec-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="753ec-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="753ec-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="753ec-105">Bestätigt, dass zwei Arrays von ganzzahligen Werten gleich sind.</span><span class="sxs-lookup"><span data-stu-id="753ec-105">Asserts that two arrays of integer values are equal.</span></span>

```qsharp
function AllEqualityFactI (actual : Int[], expected : Int[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="753ec-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="753ec-106">Input</span></span>

### <a name="actual--int"></a><span data-ttu-id="753ec-107">tatsächlicher Wert: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="753ec-107">actual : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="753ec-108">Das Array, das von einem interessanten Testfall erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="753ec-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--int"></a><span data-ttu-id="753ec-109">erwartet: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="753ec-109">expected : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="753ec-110">Das Array, das von einem interessanten Testfall erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="753ec-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="753ec-111">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="753ec-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="753ec-112">Eine Meldung, die gedruckt werden soll, wenn die Arrays nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="753ec-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="753ec-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="753ec-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

