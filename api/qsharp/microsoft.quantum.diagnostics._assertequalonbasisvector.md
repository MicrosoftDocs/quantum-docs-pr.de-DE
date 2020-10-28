---
uid: Microsoft.Quantum.Diagnostics._assertEqualOnBasisVector
title: _assertEqualOnBasisVector Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _assertEqualOnBasisVector
qsharp.summary: Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same. The basis state is described by `basis` parameter. See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.
ms.openlocfilehash: 01b6d5aede102e47df86ea70d071d81eba1ade6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702833"
---
# <a name="_assertequalonbasisvector-operation"></a><span data-ttu-id="36b1d-102">_assertEqualOnBasisVector Vorgang</span><span class="sxs-lookup"><span data-stu-id="36b1d-102">_assertEqualOnBasisVector operation</span></span>

<span data-ttu-id="36b1d-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="36b1d-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="36b1d-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="36b1d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="36b1d-105">Überprüft, ob das Ergebnis der Anwendung von zwei Vorgängen `givenU` und `expectedU` des Basis Zustands gleich ist.</span><span class="sxs-lookup"><span data-stu-id="36b1d-105">Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same.</span></span> <span data-ttu-id="36b1d-106">Der Basisstatus wird durch den- `basis` Parameter beschrieben.</span><span class="sxs-lookup"><span data-stu-id="36b1d-106">The basis state is described by `basis` parameter.</span></span>
<span data-ttu-id="36b1d-107"><xref:microsoft.quantum.extensions.fliptobasis>Weitere Informationen zu dieser Beschreibung finden Sie unter function.</span><span class="sxs-lookup"><span data-stu-id="36b1d-107">See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.</span></span>

```qsharp
operation _assertEqualOnBasisVector (basis : Int[], givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="36b1d-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="36b1d-108">Input</span></span>

### <a name="basis--int"></a><span data-ttu-id="36b1d-109">Basis: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="36b1d-109">basis : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="36b1d-110">Der durch eine Single-Qubit-Basis-ID angegebene Status-ID (0 <= ID <= 3) für jeden $n $ Qubits.</span><span class="sxs-lookup"><span data-stu-id="36b1d-110">Basis state specified by a single-qubit basis state ID (0 <= id <= 3) for each of $n$ qubits.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="36b1d-111">givenu: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="36b1d-111">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="36b1d-112">Der Vorgang auf $n $ Qubits, der geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="36b1d-112">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit-adj"></a><span data-ttu-id="36b1d-113">expectedu: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="36b1d-113">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="36b1d-114">Verweis Vorgang auf $n $ Qubits, mit dem givenu verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="36b1d-114">Reference operation on $n$ qubits that givenU is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="36b1d-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="36b1d-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

