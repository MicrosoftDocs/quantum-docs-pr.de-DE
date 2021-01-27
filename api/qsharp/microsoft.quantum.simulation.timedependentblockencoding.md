---
uid: Microsoft.Quantum.Simulation.TimeDependentBlockEncoding
title: Timedependentblockencoding (benutzerdefinierter Typ)
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentBlockEncoding
qsharp.summary: >-
  Represents a `BlockEncoding` that is controlled by a clock register.

  That is, a `TimeDependentBlockEncoding` is a unitary $U$ controlled by a state $\ket{k}_d$ in clock register `d` such that an arbitrary operator $H_k$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$. That is,

  $$ \begin{align} (\bra{0}\_a\otimes I_{ds})U(\ket{0}\_a\otimes I_{ds}) = \sum_{k}\ket{k}\bra{k}\_d\otimes H_k. \end{align} $$.
ms.openlocfilehash: e2b191a4fc44f99c88f25da9b1ee6460d936740b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814262"
---
# <a name="timedependentblockencoding-user-defined-type"></a><span data-ttu-id="28d4e-102">Timedependentblockencoding (benutzerdefinierter Typ)</span><span class="sxs-lookup"><span data-stu-id="28d4e-102">TimeDependentBlockEncoding user defined type</span></span>

<span data-ttu-id="28d4e-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="28d4e-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="28d4e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="28d4e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="28d4e-105">Stellt eine dar `BlockEncoding` , die von einem Uhren Register gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="28d4e-105">Represents a `BlockEncoding` that is controlled by a clock register.</span></span>

<span data-ttu-id="28d4e-106">Das heißt, ein `TimeDependentBlockEncoding` ist ein einheitlicher $U $, der durch den Status $ \ket{k} _D $ in der Uhr registriert wird `d` , sodass ein beliebiger Operator $H _K $ of Interest, der für das System Register `s` gilt, in dem Block oben links codiert wird, der dem hilfstatus $ \ket {0} _A $ entspricht.</span><span class="sxs-lookup"><span data-stu-id="28d4e-106">That is, a `TimeDependentBlockEncoding` is a unitary $U$ controlled by a state $\ket{k}_d$ in clock register `d` such that an arbitrary operator $H_k$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$.</span></span> <span data-ttu-id="28d4e-107">Dies bedeutet:</span><span class="sxs-lookup"><span data-stu-id="28d4e-107">That is,</span></span>

<span data-ttu-id="28d4e-108">$ $ \begin{align} (\bra {0} \_ a\otimes I_ {DS}) U (\ket {0} \_ a\otimes I_ {DS}) = \ sum_ {k} \ket{k}\bra{k} \_ d\otimes H_k.</span><span class="sxs-lookup"><span data-stu-id="28d4e-108">$$ \begin{align} (\bra{0}\_a\otimes I_{ds})U(\ket{0}\_a\otimes I_{ds}) = \sum_{k}\ket{k}\bra{k}\_d\otimes H_k.</span></span>
<span data-ttu-id="28d4e-109">\end{align} $ $.</span><span class="sxs-lookup"><span data-stu-id="28d4e-109">\end{align} $$.</span></span>

```qsharp

newtype TimeDependentBlockEncoding = (((Qubit[], Qubit[], Qubit[]) => Unit is Adj + Ctl));
```

