---
uid: Microsoft.Quantum.Synthesis.Extended
title: Erweiterte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Extended
qsharp.summary: Extends a spectrum by inverted coefficients
ms.openlocfilehash: 1855f3cab98c5fbf08c4505b90423df50cbec95b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855472"
---
# <a name="extended-function"></a><span data-ttu-id="437a7-102">Erweiterte Funktion</span><span class="sxs-lookup"><span data-stu-id="437a7-102">Extended function</span></span>

<span data-ttu-id="437a7-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="437a7-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="437a7-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="437a7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="437a7-105">Erweitert ein Spektrum durch invertierte Koeffizienten</span><span class="sxs-lookup"><span data-stu-id="437a7-105">Extends a spectrum by inverted coefficients</span></span>

```qsharp
function Extended (spectrum : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="437a7-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="437a7-106">Input</span></span>

### <a name="spectrum--int"></a><span data-ttu-id="437a7-107">Spektrum: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="437a7-107">spectrum : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="437a7-108">Spektral Koeffizienten</span><span class="sxs-lookup"><span data-stu-id="437a7-108">Spectral coefficients</span></span>



## <a name="output--int"></a><span data-ttu-id="437a7-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="437a7-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="437a7-110">Koeffizienten gefolgt von umgekehrter Kopie</span><span class="sxs-lookup"><span data-stu-id="437a7-110">Coefficients followed by inverted copy</span></span>

## <a name="example"></a><span data-ttu-id="437a7-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="437a7-111">Example</span></span>

```qsharp
Extended([2, 2, 2, -2]); // [2, 2, 2, -2, -2, -2, -2, 2]
```