---
uid: Microsoft.Quantum.Synthesis.MCMTMask
title: Mcmtmask-benutzerdefinierter Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: MCMTMask
qsharp.summary: >-
  A type to represent a multiple-controlled multiple-target Toffoli gate.

  The first integer is a bit mask for control lines.  Bit indexes which are set correspond to control line indexes.

  The second integer is a bit mask for target lines.  Bit indexes which are set correspond to target line indexes.

  The bit indexes of both integers must be disjoint.
ms.openlocfilehash: 50bec0f9aca95afab83491db6b742d1f0323371f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855379"
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

