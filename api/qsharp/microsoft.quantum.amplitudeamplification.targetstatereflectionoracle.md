---
uid: Microsoft.Quantum.AmplitudeAmplification.TargetStateReflectionOracle
title: Targetstatuereflectionoracle-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: TargetStateReflectionOracle
qsharp.summary: >-
  Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.

  The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.
ms.openlocfilehash: 65ad316a6ac986ebd0dc28b25859026a60aa3239
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191107"
---
# <a name="targetstatereflectionoracle-function"></a><span data-ttu-id="605f3-102">Targetstatuereflectionoracle-Funktion</span><span class="sxs-lookup"><span data-stu-id="605f3-102">TargetStateReflectionOracle function</span></span>

<span data-ttu-id="605f3-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="605f3-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="605f3-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="605f3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="605f3-105">Erstellt eine `ReflectionOracle` über den Zielzustand, der durch das Flag-Qubit eindeutig gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="605f3-105">Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.</span></span>

<span data-ttu-id="605f3-106">Der Ziel Status verfügt über ein einzelnes Qubit, das auf 1 festgelegt ist, und alle anderen 0: $ \ket {1} _F $.</span><span class="sxs-lookup"><span data-stu-id="605f3-106">The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.</span></span>

```qsharp
function TargetStateReflectionOracle (idxFlagQubit : Int) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="input"></a><span data-ttu-id="605f3-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="605f3-107">Input</span></span>

### <a name="idxflagqubit--int"></a><span data-ttu-id="605f3-108">idxflagqubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="605f3-108">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="605f3-109">Index zum Markieren von Qubit-$f $ of Oracle.</span><span class="sxs-lookup"><span data-stu-id="605f3-109">Index to flag qubit $f$ of oracle.</span></span>



## <a name="output--reflectionoracle"></a><span data-ttu-id="605f3-110">Ausgabe: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="605f3-110">Output : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="605f3-111">Ein `ReflectionOracle` , der den durch $ \ket _F $ markierten Zustand wieder gibt {1} .</span><span class="sxs-lookup"><span data-stu-id="605f3-111">A `ReflectionOracle` that reflects about the state marked by $\ket{1}_f$.</span></span>

## <a name="see-also"></a><span data-ttu-id="605f3-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="605f3-112">See Also</span></span>

- [<span data-ttu-id="605f3-113">Microsoft. Quantum. Canon. reflectionoracle</span><span class="sxs-lookup"><span data-stu-id="605f3-113">Microsoft.Quantum.Canon.ReflectionOracle</span></span>](xref:Microsoft.Quantum.Canon.ReflectionOracle)