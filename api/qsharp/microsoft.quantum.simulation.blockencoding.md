---
uid: Microsoft.Quantum.Simulation.BlockEncoding
title: Blockencoding-benutzerdefinierter Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncoding
qsharp.summary: >-
  Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.

  That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$. That is,

  $$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.
ms.openlocfilehash: 75fdbf13cf07d906982d4a611d1d25b3e29db2cd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225430"
---
# <a name="blockencoding-user-defined-type"></a><span data-ttu-id="b95b2-102">Blockencoding-benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="b95b2-102">BlockEncoding user defined type</span></span>

<span data-ttu-id="b95b2-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="b95b2-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="b95b2-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b95b2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b95b2-105">Stellt eine einheitliche dar, bei der ein beliebiger Operator von Interesse im oberen linken Block codiert wird.</span><span class="sxs-lookup"><span data-stu-id="b95b2-105">Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.</span></span>

<span data-ttu-id="b95b2-106">Das heißt, ein `BlockEncoding` ist ein einheitlicher $U $, bei dem ein beliebiger Operator $H $ of Interest, der für das System Register agiert, `s` in dem Block oben links codiert wird, der dem hilfstatus $ \ket {0} _A $ entspricht.</span><span class="sxs-lookup"><span data-stu-id="b95b2-106">That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$.</span></span> <span data-ttu-id="b95b2-107">Dies bedeutet:</span><span class="sxs-lookup"><span data-stu-id="b95b2-107">That is,</span></span>

<span data-ttu-id="b95b2-108">$ $ \begin{align} (\bra {0} _A \otimes I_s) U (\ket {0} _A \otimes I_s) = H \end{align} $ $.</span><span class="sxs-lookup"><span data-stu-id="b95b2-108">$$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.</span></span>

```qsharp

newtype BlockEncoding = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```

