---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactI
title: Allequalityfakti-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactI
qsharp.summary: Asserts that two arrays of integer values are equal.
ms.openlocfilehash: a7043b9c670f79e270180c583fef56b70c1a3bcb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830890"
---
# <a name="allequalityfacti-function"></a><span data-ttu-id="40e9e-102">Allequalityfakti-Funktion</span><span class="sxs-lookup"><span data-stu-id="40e9e-102">AllEqualityFactI function</span></span>

<span data-ttu-id="40e9e-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="40e9e-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="40e9e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="40e9e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="40e9e-105">Bestätigt, dass zwei Arrays von ganzzahligen Werten gleich sind.</span><span class="sxs-lookup"><span data-stu-id="40e9e-105">Asserts that two arrays of integer values are equal.</span></span>

```qsharp
function AllEqualityFactI (actual : Int[], expected : Int[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="40e9e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="40e9e-106">Input</span></span>

### <a name="actual--int"></a><span data-ttu-id="40e9e-107">tatsächlicher Wert: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="40e9e-107">actual : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="40e9e-108">Das Array, das von einem interessanten Testfall erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="40e9e-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--int"></a><span data-ttu-id="40e9e-109">erwartet: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="40e9e-109">expected : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="40e9e-110">Das Array, das von einem interessanten Testfall erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="40e9e-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="40e9e-111">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="40e9e-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="40e9e-112">Eine Meldung, die gedruckt werden soll, wenn die Arrays nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="40e9e-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="40e9e-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="40e9e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

