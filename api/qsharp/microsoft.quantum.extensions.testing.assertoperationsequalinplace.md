---
uid: Microsoft.Quantum.Extensions.Testing.AssertOperationsEqualInPlace
title: Assertoperationsequalinplace-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Extensions.Testing
qsharp.name: AssertOperationsEqualInPlace
qsharp.summary: >-
  > [!WARNING]

  > AssertOperationsEqualInPlace has been deprecated. Please use <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace> instead.

  >

  > Please use @"microsoft.quantum.diagnostics.assertoperationsequalinplace".

  > Note that the order of the arguments to this operation has changed.
ms.openlocfilehash: 64cc1e5c78af100b652ced24f00f3097c35ea5d1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98820237"
---
# <a name="assertoperationsequalinplace-operation"></a><span data-ttu-id="4e0ec-102">Assertoperationsequalinplace-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4e0ec-102">AssertOperationsEqualInPlace operation</span></span>

<span data-ttu-id="4e0ec-103">Namespace: [Microsoft. Quantum. Extensions. testing](xref:Microsoft.Quantum.Extensions.Testing)</span><span class="sxs-lookup"><span data-stu-id="4e0ec-103">Namespace: [Microsoft.Quantum.Extensions.Testing](xref:Microsoft.Quantum.Extensions.Testing)</span></span>

<span data-ttu-id="4e0ec-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="4e0ec-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


> [!WARNING]
> <span data-ttu-id="4e0ec-105">Assertoperationsequalinplace ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="4e0ec-105">AssertOperationsEqualInPlace has been deprecated.</span></span> <span data-ttu-id="4e0ec-106">Verwenden Sie stattdessen <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace>.</span><span class="sxs-lookup"><span data-stu-id="4e0ec-106">Please use <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace> instead.</span></span>
>
> <span data-ttu-id="4e0ec-107">Verwenden Sie @"microsoft.quantum.diagnostics.assertoperationsequalinplace".</span><span class="sxs-lookup"><span data-stu-id="4e0ec-107">Please use @"microsoft.quantum.diagnostics.assertoperationsequalinplace".</span></span>
> <span data-ttu-id="4e0ec-108">Beachten Sie, dass sich die Reihenfolge der Argumente für diesen Vorgang geändert hat.</span><span class="sxs-lookup"><span data-stu-id="4e0ec-108">Note that the order of the arguments to this operation has changed.</span></span>



```qsharp
operation AssertOperationsEqualInPlace (actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj), nQubits : Int) : Unit
```


## <a name="input"></a><span data-ttu-id="4e0ec-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4e0ec-109">Input</span></span>

### <a name="actual--qubit--unit"></a><span data-ttu-id="4e0ec-110">tatsächlicher Wert: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4e0ec-110">actual : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="expected--qubit--unit--is-adj"></a><span data-ttu-id="4e0ec-111">erwartet: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="4e0ec-111">expected : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="nqubits--int"></a><span data-ttu-id="4e0ec-112">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4e0ec-112">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--unit"></a><span data-ttu-id="4e0ec-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4e0ec-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

