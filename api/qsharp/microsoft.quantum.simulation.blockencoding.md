---
uid: Microsoft.Quantum.Simulation.BlockEncoding
title: Blockencoding-benutzerdefinierter Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncoding
qsharp.summary: >-
  Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.

  That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$. That is,

  $$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.
ms.openlocfilehash: 1b769c58fd23b4ebc9d779cec3c47d8275822e5a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722695"
---
# <a name="blockencoding-user-defined-type"></a>Blockencoding-benutzerdefinierter Typ

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Stellt eine einheitliche dar, bei der ein beliebiger Operator von Interesse im oberen linken Block codiert wird.

Das heißt, ein `BlockEncoding` ist ein einheitlicher $U $, bei dem ein beliebiger Operator $H $ of Interest, der für das System Register agiert, `s` in dem Block oben links codiert wird, der dem hilfstatus $ \ket {0} _A $ entspricht. Dies bedeutet:

$ $ \begin{align} (\bra {0} _A \otimes I_s) U (\ket {0} _A \otimes I_s) = H \end{align} $ $.

```qsharp

newtype BlockEncoding = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```

