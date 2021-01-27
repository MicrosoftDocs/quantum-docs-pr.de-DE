---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: Menrementoperators-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: 204ae621b77559a894f0bce14e494824d58e4ad6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835396"
---
# <a name="measurementoperators-function"></a><span data-ttu-id="5b3d3-102">Menrementoperators-Funktion</span><span class="sxs-lookup"><span data-stu-id="5b3d3-102">MeasurementOperators function</span></span>

<span data-ttu-id="5b3d3-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="5b3d3-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="5b3d3-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="5b3d3-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="5b3d3-105">Berechnet alle Mess Operatoren, die erforderlich sind, um die Erwartung eines Jordan-Wigner Begriffs zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-105">Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.</span></span>

```qsharp
function MeasurementOperators (nQubits : Int, indices : Int[], termType : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="5b3d3-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5b3d3-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="5b3d3-107">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5b3d3-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5b3d3-108">Die Anzahl der zum Simulieren des molekularen Systems erforderlichen Qubits.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-108">The number of qubits required to simulate the molecular system.</span></span>


### <a name="indices--int"></a><span data-ttu-id="5b3d3-109">Indizes: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5b3d3-109">indices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="5b3d3-110">Ein Array, das die Indizes des Qubit-Felds enthält, auf den jeder Pauli-Operator angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-110">An array containing the indices of the qubit each Pauli operator is applied to.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="5b3d3-111">Termtype: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5b3d3-111">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5b3d3-112">Der Typ des Jordan-Wigner Begriffs.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-112">The type of the Jordan-Wigner term.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="5b3d3-113">Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="5b3d3-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="5b3d3-114">Ein Array von Mess Operatoren (jedes ist ein Array von Pauli).</span><span class="sxs-lookup"><span data-stu-id="5b3d3-114">An array of measurement operators (each being an array of Pauli).</span></span>