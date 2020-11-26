---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.ExpandedCoefficients
title: Expandebug-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: ExpandedCoefficients
qsharp.summary: Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.
ms.openlocfilehash: 92d7deb7010791e7de3d22ad4616b20110d5e84e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214380"
---
# <a name="expandedcoefficients-function"></a><span data-ttu-id="229fa-102">Expandebug-Funktion</span><span class="sxs-lookup"><span data-stu-id="229fa-102">ExpandedCoefficients function</span></span>

<span data-ttu-id="229fa-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="229fa-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="229fa-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="229fa-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="229fa-105">Erweitert die kompakte Darstellung der Jordan-Wigner Koeffizienten, um eine eins-zu-Eins-Zuordnung zwischen diesen und den Pauli-Begriffen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="229fa-105">Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.</span></span>

```qsharp
function ExpandedCoefficients (coeff : Double[], termType : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="229fa-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="229fa-106">Input</span></span>

### <a name="coeff--double"></a><span data-ttu-id="229fa-107">coeff: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="229fa-107">coeff : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="229fa-108">Ein Array von Koeffizienten, das aus der Jordan-Wigner hamiltonan-Datenstruktur gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="229fa-108">An array of coefficients, as read from the Jordan-Wigner Hamiltonian data structure.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="229fa-109">Termtype: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="229fa-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="229fa-110">Der Typ des Jordan-Wigner Begriffs.</span><span class="sxs-lookup"><span data-stu-id="229fa-110">The type of the Jordan-Wigner term.</span></span>



## <a name="output--double"></a><span data-ttu-id="229fa-111">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="229fa-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="229fa-112">Erweiterte Arrays von Koeffizienten, 1 pro Pauli-Begriff.</span><span class="sxs-lookup"><span data-stu-id="229fa-112">Expanded arrays of coefficients, one per Pauli term.</span></span>