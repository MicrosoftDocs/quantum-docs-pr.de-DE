---
uid: Microsoft.Quantum.Synthesis.MCMTMask
title: Mcmtmask-benutzerdefinierter Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: MCMTMask
qsharp.summary: >-
  A type to represent a multiple-controlled multiple-target Toffoli gate.

  The first integer is a bit mask for control lines.  Bit indexes which are set correspond to control line indexes.

  The second integer is a bit mask for target lines.  Bit indexes which are set correspond to target line indexes.

  The bit indexes of both integers must be disjoint.
ms.openlocfilehash: 0d3ca12d55fa4b5e8332d50939954de29e39b715
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725496"
---
# <a name="mcmtmask-user-defined-type"></a>Mcmtmask-benutzerdefinierter Typ

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paketen [](https://nuget.org/packages/)


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

