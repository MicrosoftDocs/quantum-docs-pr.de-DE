---
uid: Microsoft.Quantum.Simulation.TimeDependentBlockEncoding
title: Timedependentblockencoding (benutzerdefinierter Typ)
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentBlockEncoding
qsharp.summary: >-
  Represents a `BlockEncoding` that is controlled by a clock register.

  That is, a `TimeDependentBlockEncoding` is a unitary $U$ controlled by a state $\ket{k}_d$ in clock register `d` such that an arbitrary operator $H_k$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$. That is,

  $$ \begin{align} (\bra{0}\_a\otimes I_{ds})U(\ket{0}\_a\otimes I_{ds}) = \sum_{k}\ket{k}\bra{k}\_d\otimes H_k. \end{align} $$.
ms.openlocfilehash: 1cb3a3cf1e16b194eebd1574da6f9934fc34e5f7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725761"
---
# <a name="timedependentblockencoding-user-defined-type"></a>Timedependentblockencoding (benutzerdefinierter Typ)

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Stellt eine dar `BlockEncoding` , die von einem Uhren Register gesteuert wird.

Das heißt, ein `TimeDependentBlockEncoding` ist ein einheitlicher $U $, der durch den Status $ \ket{k} _D $ in der Uhr registriert wird `d` , sodass ein beliebiger Operator $H _K $ of Interest, der für das System Register `s` gilt, in dem Block oben links codiert wird, der dem hilfstatus $ \ket {0} _A $ entspricht. Dies bedeutet:

$ $ \begin{align} (\bra {0} \_ a\otimes I_ {DS}) U (\ket {0} \_ a\otimes I_ {DS}) = \ sum_ {k} \ket{k}\bra{k} \_ d\otimes H_k.
\end{align} $ $.

```qsharp

newtype TimeDependentBlockEncoding = (((Qubit[], Qubit[], Qubit[]) => Unit is Adj + Ctl));
```

