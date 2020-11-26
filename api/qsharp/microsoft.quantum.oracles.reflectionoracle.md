---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Benutzerdefinierter reflectionoracle-Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 7bb0626e7cca9ae0b640699ea57f2e114bda2d06
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226654"
---
# <a name="reflectionoracle-user-defined-type"></a>Benutzerdefinierter reflectionoracle-Typ

Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Stellt ein reflektionsinoracle dar.

Ein reflektionsinoracle, $O $, weist Eingaben auf:

- Die Phase $ \phi $, um die der reflektierte Teilbereich gedreht werden soll.
- Das Qubit-Register, für das die angegebene Reflektion durchgeführt werden soll.

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a>Benannte Elemente

### <a name="applyreflection--doublequbit--unit--is-adj--ctl"></a>Applyreflection: ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL



## <a name="remarks"></a>Bemerkungen

Diese Oracle $O = \boldone-(1-e ^ {i \phi}) \ket{\psi}\bra{\psi} $ führt eine partielle Reflektion durch eine Phase $ \phi $ zu einem einzelnen reinen Status $ \ket{\psi} $ aus.