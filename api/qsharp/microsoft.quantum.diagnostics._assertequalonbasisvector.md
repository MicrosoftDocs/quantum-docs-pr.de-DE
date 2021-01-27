---
uid: Microsoft.Quantum.Diagnostics._assertEqualOnBasisVector
title: _assertEqualOnBasisVector Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _assertEqualOnBasisVector
qsharp.summary: Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same. The basis state is described by `basis` parameter. See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.
ms.openlocfilehash: 041fecfa27ae5bd17fa8fdc89ce964f985f6124b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853578"
---
# <a name="_assertequalonbasisvector-operation"></a><span data-ttu-id="eb71a-102">_assertEqualOnBasisVector Vorgang</span><span class="sxs-lookup"><span data-stu-id="eb71a-102">_assertEqualOnBasisVector operation</span></span>

<span data-ttu-id="eb71a-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="eb71a-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="eb71a-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="eb71a-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="eb71a-105">Überprüft, ob das Ergebnis der Anwendung von zwei Vorgängen `givenU` und `expectedU` des Basis Zustands gleich ist.</span><span class="sxs-lookup"><span data-stu-id="eb71a-105">Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same.</span></span> <span data-ttu-id="eb71a-106">Der Basisstatus wird durch den- `basis` Parameter beschrieben.</span><span class="sxs-lookup"><span data-stu-id="eb71a-106">The basis state is described by `basis` parameter.</span></span>
<span data-ttu-id="eb71a-107"><xref:microsoft.quantum.extensions.fliptobasis>Weitere Informationen zu dieser Beschreibung finden Sie unter function.</span><span class="sxs-lookup"><span data-stu-id="eb71a-107">See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.</span></span>

```qsharp
operation _assertEqualOnBasisVector (basis : Int[], givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="eb71a-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="eb71a-108">Input</span></span>

### <a name="basis--int"></a><span data-ttu-id="eb71a-109">Basis: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="eb71a-109">basis : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="eb71a-110">Der durch eine Single-Qubit-Basis-ID angegebene Status-ID (0 <= ID <= 3) für jeden $n $ Qubits.</span><span class="sxs-lookup"><span data-stu-id="eb71a-110">Basis state specified by a single-qubit basis state ID (0 <= id <= 3) for each of $n$ qubits.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="eb71a-111">givenu: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eb71a-111">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="eb71a-112">Der Vorgang auf $n $ Qubits, der geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb71a-112">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit--is-adj"></a><span data-ttu-id="eb71a-113">expectedu: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="eb71a-113">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="eb71a-114">Verweis Vorgang auf $n $ Qubits, mit dem givenu verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb71a-114">Reference operation on $n$ qubits that givenU is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="eb71a-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eb71a-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

