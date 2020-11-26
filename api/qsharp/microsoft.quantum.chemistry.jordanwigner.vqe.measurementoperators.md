---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: Menrementoperators-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: a5ea9a776f522e927f2f4545bd417d35bda83994
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214346"
---
# <a name="measurementoperators-function"></a><span data-ttu-id="22608-102">Menrementoperators-Funktion</span><span class="sxs-lookup"><span data-stu-id="22608-102">MeasurementOperators function</span></span>

<span data-ttu-id="22608-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="22608-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="22608-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="22608-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="22608-105">Berechnet alle Mess Operatoren, die erforderlich sind, um die Erwartung eines Jordan-Wigner Begriffs zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="22608-105">Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.</span></span>

```qsharp
function MeasurementOperators (nQubits : Int, indices : Int[], termType : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="22608-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22608-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="22608-107">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="22608-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="22608-108">Die Anzahl der zum Simulieren des molekularen Systems erforderlichen Qubits.</span><span class="sxs-lookup"><span data-stu-id="22608-108">The number of qubits required to simulate the molecular system.</span></span>


### <a name="indices--int"></a><span data-ttu-id="22608-109">Indizes: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="22608-109">indices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="22608-110">Ein Array, das die Indizes des Qubit-Felds enthält, auf den jeder Pauli-Operator angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="22608-110">An array containing the indices of the qubit each Pauli operator is applied to.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="22608-111">Termtype: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="22608-111">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="22608-112">Der Typ des Jordan-Wigner Begriffs.</span><span class="sxs-lookup"><span data-stu-id="22608-112">The type of the Jordan-Wigner term.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="22608-113">Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="22608-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="22608-114">Ein Array von Mess Operatoren (jedes ist ein Array von Pauli).</span><span class="sxs-lookup"><span data-stu-id="22608-114">An array of measurement operators (each being an array of Pauli).</span></span>