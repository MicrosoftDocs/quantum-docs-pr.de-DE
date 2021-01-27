---
uid: Microsoft.Quantum.AmplitudeAmplification.TargetStateReflectionOracle
title: Targetstatuereflectionoracle-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: TargetStateReflectionOracle
qsharp.summary: >-
  Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.

  The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.
ms.openlocfilehash: 4169ccf3e210e27f779311553b845ea04f2c7dc6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843906"
---
# <a name="targetstatereflectionoracle-function"></a><span data-ttu-id="3e4ec-102">Targetstatuereflectionoracle-Funktion</span><span class="sxs-lookup"><span data-stu-id="3e4ec-102">TargetStateReflectionOracle function</span></span>

<span data-ttu-id="3e4ec-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="3e4ec-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="3e4ec-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3e4ec-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3e4ec-105">Erstellt eine `ReflectionOracle` über den Zielzustand, der durch das Flag-Qubit eindeutig gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="3e4ec-105">Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.</span></span>

<span data-ttu-id="3e4ec-106">Der Ziel Status verfügt über ein einzelnes Qubit, das auf 1 festgelegt ist, und alle anderen 0: $ \ket {1} _F $.</span><span class="sxs-lookup"><span data-stu-id="3e4ec-106">The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.</span></span>

```qsharp
function TargetStateReflectionOracle (idxFlagQubit : Int) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="input"></a><span data-ttu-id="3e4ec-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e4ec-107">Input</span></span>

### <a name="idxflagqubit--int"></a><span data-ttu-id="3e4ec-108">idxflagqubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3e4ec-108">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3e4ec-109">Index zum Markieren von Qubit-$f $ of Oracle.</span><span class="sxs-lookup"><span data-stu-id="3e4ec-109">Index to flag qubit $f$ of oracle.</span></span>



## <a name="output--reflectionoracle"></a><span data-ttu-id="3e4ec-110">Ausgabe: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="3e4ec-110">Output : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="3e4ec-111">Ein `ReflectionOracle` , der den durch $ \ket _F $ markierten Zustand wieder gibt {1} .</span><span class="sxs-lookup"><span data-stu-id="3e4ec-111">A `ReflectionOracle` that reflects about the state marked by $\ket{1}_f$.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e4ec-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3e4ec-112">See Also</span></span>

- [<span data-ttu-id="3e4ec-113">Microsoft. Quantum. Canon. reflectionoracle</span><span class="sxs-lookup"><span data-stu-id="3e4ec-113">Microsoft.Quantum.Canon.ReflectionOracle</span></span>](xref:Microsoft.Quantum.Canon.ReflectionOracle)