---
uid: Microsoft.Quantum.Oracles.ReflectionOracleFromDeterministicStateOracle
title: Reflectionoraclefromdeterministicstateoracle-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracleFromDeterministicStateOracle
qsharp.summary: Constructs reflection about a given state from an oracle.
ms.openlocfilehash: c2d37216aebcdc5243d0f1d6ec9db261cc9bd0c8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722178"
---
# <a name="reflectionoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="27594-102">Reflectionoraclefromdeterministicstateoracle-Funktion</span><span class="sxs-lookup"><span data-stu-id="27594-102">ReflectionOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="27594-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="27594-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="27594-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="27594-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="27594-105">Erstellt Reflektion über einen angegebenen Zustand aus einem Oracle.</span><span class="sxs-lookup"><span data-stu-id="27594-105">Constructs reflection about a given state from an oracle.</span></span>

```qsharp
function ReflectionOracleFromDeterministicStateOracle (oracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="description"></a><span data-ttu-id="27594-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27594-106">Description</span></span>

<span data-ttu-id="27594-107">Bei einem durch eine einheitliche Matrix $O $ dargestellten deterministischen Zustands Vorbereitungs-Oracle ist das Ergebnis dieser Funktion ein Oracle, das eine Reflektion auf den Status $ \ket{\psi} $ anwendet, der von Oracle $O $; vorbereitet wurde. Das heißt, der Status $ \ket{\psi} $, sodass $O \ket {0} = \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="27594-107">Given a deterministic state preparation oracle represented by a unitary matrix $O$, the result of this function is an oracle that applies a reflection around the state $\ket{\psi}$ prepared by the oracle $O$; that is, the state $\ket{\psi}$ such that $O\ket{0} = \ket{\psi}$.</span></span>

## <a name="input"></a><span data-ttu-id="27594-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="27594-108">Input</span></span>

### <a name="oracle--deterministicstateoracle"></a><span data-ttu-id="27594-109">Oracle: [deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="27594-109">oracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="27594-110">Ein Oracle, das Kopien des Zustands $ \ket{\psi} $ vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="27594-110">An oracle that prepares copies of the state $\ket{\psi}$.</span></span>



## <a name="output--reflectionoracle"></a><span data-ttu-id="27594-111">Ausgabe: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="27594-111">Output : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="27594-112">Ein Oracle, das den Status $ \ket{\psi} $ widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="27594-112">An oracle that reflects about the state $\ket{\psi}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="27594-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="27594-113">See Also</span></span>

- [<span data-ttu-id="27594-114">Microsoft. Quantum. Oracles. deterministicstateoracle</span><span class="sxs-lookup"><span data-stu-id="27594-114">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="27594-115">Microsoft. Quantum. Oracles. reflectionoracle</span><span class="sxs-lookup"><span data-stu-id="27594-115">Microsoft.Quantum.Oracles.ReflectionOracle</span></span>](xref:Microsoft.Quantum.Oracles.ReflectionOracle)