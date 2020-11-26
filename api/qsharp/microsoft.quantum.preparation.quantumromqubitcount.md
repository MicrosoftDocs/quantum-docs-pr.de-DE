---
uid: Microsoft.Quantum.Preparation.QuantumROMQubitCount
title: Quantenromqubitcount-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROMQubitCount
qsharp.summary: >-
  > [!WARNING]

  > QuantumROMQubitCount has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements> instead.


  Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.
ms.openlocfilehash: 0ec1e042b9f675505f73bfcdcc6706d0bc0367df
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210402"
---
# <a name="quantumromqubitcount-function"></a><span data-ttu-id="73a2a-102">Quantenromqubitcount-Funktion</span><span class="sxs-lookup"><span data-stu-id="73a2a-102">QuantumROMQubitCount function</span></span>

<span data-ttu-id="73a2a-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="73a2a-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="73a2a-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="73a2a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="73a2a-105">Quantum romqubitcount ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="73a2a-105">QuantumROMQubitCount has been deprecated.</span></span> <span data-ttu-id="73a2a-106">Verwenden Sie stattdessen <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements>.</span><span class="sxs-lookup"><span data-stu-id="73a2a-106">Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements> instead.</span></span>

<span data-ttu-id="73a2a-107">Gibt die Gesamtanzahl der Qubits zurück, die dem von zurückgegebenen Vorgang zugeordnet werden müssen `QuantumROM` .</span><span class="sxs-lookup"><span data-stu-id="73a2a-107">Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.</span></span>

```qsharp
function QuantumROMQubitCount (targetError : Double, nCoeffs : Int) : (Int, (Int, Int))
```


## <a name="input"></a><span data-ttu-id="73a2a-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="73a2a-108">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="73a2a-109">targeterror: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="73a2a-109">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="73a2a-110">Der Ziel Fehler $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="73a2a-110">The target error $\epsilon$.</span></span>


### <a name="ncoeffs--int"></a><span data-ttu-id="73a2a-111">ncoeffs: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="73a2a-111">nCoeffs : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="73a2a-112">Anzahl der in angegebenen Koeffizienten `QuantumROM` .</span><span class="sxs-lookup"><span data-stu-id="73a2a-112">Number of coefficients specified in `QuantumROM`.</span></span>



## <a name="output--intintint"></a><span data-ttu-id="73a2a-113">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int), ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)))</span><span class="sxs-lookup"><span data-stu-id="73a2a-113">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int)))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="73a2a-114">Erster Parameter</span><span class="sxs-lookup"><span data-stu-id="73a2a-114">First parameter</span></span>

<span data-ttu-id="73a2a-115">Ein Tupel `(x,(y,z))` , bei dem `x = y + z` die Gesamtzahl der zugeordneten Qubits ist, `y` die Anzahl der Qubits für das `LittleEndian` Register und `z` die Anzahl der Garbage Qubits.</span><span class="sxs-lookup"><span data-stu-id="73a2a-115">A tuple `(x,(y,z))` where `x = y + z` is the total number of qubits allocated, `y` is the number of qubits for the `LittleEndian` register, and `z` is the Number of garbage qubits.</span></span>