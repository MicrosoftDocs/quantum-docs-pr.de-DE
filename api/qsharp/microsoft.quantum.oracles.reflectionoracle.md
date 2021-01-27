---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Benutzerdefinierter reflectionoracle-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 1ef07126596b70d2c5574430656009116c34d2bc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854491"
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