---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.ExpandedCoefficients
title: Expandebug-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: ExpandedCoefficients
qsharp.summary: Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.
ms.openlocfilehash: b953fb8f5737956e8597cd90a7d6bfc0bafce4e3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835623"
---
# <a name="expandedcoefficients-function"></a><span data-ttu-id="25776-102">Expandebug-Funktion</span><span class="sxs-lookup"><span data-stu-id="25776-102">ExpandedCoefficients function</span></span>

<span data-ttu-id="25776-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="25776-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="25776-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="25776-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="25776-105">Erweitert die kompakte Darstellung der Jordan-Wigner Koeffizienten, um eine eins-zu-Eins-Zuordnung zwischen diesen und den Pauli-Begriffen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="25776-105">Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.</span></span>

```qsharp
function ExpandedCoefficients (coeff : Double[], termType : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="25776-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="25776-106">Input</span></span>

### <a name="coeff--double"></a><span data-ttu-id="25776-107">coeff: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="25776-107">coeff : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="25776-108">Ein Array von Koeffizienten, das aus der Jordan-Wigner hamiltonan-Datenstruktur gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="25776-108">An array of coefficients, as read from the Jordan-Wigner Hamiltonian data structure.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="25776-109">Termtype: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="25776-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="25776-110">Der Typ des Jordan-Wigner Begriffs.</span><span class="sxs-lookup"><span data-stu-id="25776-110">The type of the Jordan-Wigner term.</span></span>



## <a name="output--double"></a><span data-ttu-id="25776-111">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="25776-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="25776-112">Erweiterte Arrays von Koeffizienten, 1 pro Pauli-Begriff.</span><span class="sxs-lookup"><span data-stu-id="25776-112">Expanded arrays of coefficients, one per Pauli term.</span></span>