---
uid: Microsoft.Quantum.Synthesis.MCMTMask
title: Mcmtmask-benutzerdefinierter Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: MCMTMask
qsharp.summary: >-
  A type to represent a multiple-controlled multiple-target Toffoli gate.

  The first integer is a bit mask for control lines.  Bit indexes which are set correspond to control line indexes.

  The second integer is a bit mask for target lines.  Bit indexes which are set correspond to target line indexes.

  The bit indexes of both integers must be disjoint.
ms.openlocfilehash: 3c2debbb1f2019c7188dcb00f8ac09154fd4fd4f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203015"
---
# <a name="mcmtmask-user-defined-type"></a>Mcmtmask-benutzerdefinierter Typ

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Ein Typ, der ein mehrfach kontrolliertes multitarget-"deffoli"-Gate darstellt.

Die erste ganze Zahl ist eine Bitmaske für Steuer Zeilen.  Bitindizes, die festgelegt werden, entsprechen Steuer Zeilen Indizes.

Die zweite Ganzzahl ist eine Bitmaske für die Ziellinien.  Bitindizes, die festgelegt werden, entsprechen Ziel Zeilen Indizes.

Die bitindizes beider Ganzzahlen müssen zusammen hanglos sein.

```qsharp

newtype MCMTMask = (ControlMask : Int, TargetMask : Int);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="controlmask--int"></a>Controlmask: [int](xref:microsoft.quantum.lang-ref.int)


### <a name="targetmask--int"></a>Targetmask: [int](xref:microsoft.quantum.lang-ref.int)

