---
uid: Microsoft.Quantum.Preparation.QuantumROMQubitCount
title: Quantenromqubitcount-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROMQubitCount
qsharp.summary: Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.
ms.openlocfilehash: 988d5efa3e27cf5e9a276ab3ab443c10f88fe1ad
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722933"
---
# <a name="quantumromqubitcount-function"></a><span data-ttu-id="bf2ae-102">Quantenromqubitcount-Funktion</span><span class="sxs-lookup"><span data-stu-id="bf2ae-102">QuantumROMQubitCount function</span></span>

<span data-ttu-id="bf2ae-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="bf2ae-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="bf2ae-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bf2ae-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bf2ae-105">Gibt die Gesamtanzahl der Qubits zurück, die dem von zurückgegebenen Vorgang zugeordnet werden müssen `QuantumROM` .</span><span class="sxs-lookup"><span data-stu-id="bf2ae-105">Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.</span></span>

```qsharp
function QuantumROMQubitCount (targetError : Double, nCoeffs : Int) : (Int, (Int, Int))
```


## <a name="input"></a><span data-ttu-id="bf2ae-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bf2ae-106">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="bf2ae-107">targeterror: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bf2ae-107">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bf2ae-108">Der Ziel Fehler $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="bf2ae-108">The target error $\epsilon$.</span></span>


### <a name="ncoeffs--int"></a><span data-ttu-id="bf2ae-109">ncoeffs: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bf2ae-109">nCoeffs : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bf2ae-110">Anzahl der in angegebenen Koeffizienten `QuantumROM` .</span><span class="sxs-lookup"><span data-stu-id="bf2ae-110">Number of coefficients specified in `QuantumROM`.</span></span>



## <a name="output--intintint"></a><span data-ttu-id="bf2ae-111">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int), ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)))</span><span class="sxs-lookup"><span data-stu-id="bf2ae-111">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int)))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="bf2ae-112">Erster Parameter</span><span class="sxs-lookup"><span data-stu-id="bf2ae-112">First parameter</span></span>

<span data-ttu-id="bf2ae-113">Ein Tupel `(x,(y,z))` , bei dem `x = y + z` die Gesamtzahl der zugeordneten Qubits ist, `y` die Anzahl der Qubits für das `LittleEndian` Register und `z` die Anzahl der Garbage Qubits.</span><span class="sxs-lookup"><span data-stu-id="bf2ae-113">A tuple `(x,(y,z))` where `x = y + z` is the total number of qubits allocated, `y` is the number of qubits for the `LittleEndian` register, and `z` is the Number of garbage qubits.</span></span>