---
uid: Microsoft.Quantum.Chemistry.HTermToGenIdx
title: Htermabgenidx-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermToGenIdx
qsharp.summary: Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.
ms.openlocfilehash: 46745632e2f6bafad0d7359141522b84f48c039d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839614"
---
# <a name="htermtogenidx-function"></a>Htermabgenidx-Funktion

Namespace: [Microsoft. Quantum. Chemistry](xref:Microsoft.Quantum.Chemistry)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Konvertiert einen hamiltona-Begriff im `HTerm` Datenformat in einen generatorindex.

```qsharp
function HTermToGenIdx (term : Microsoft.Quantum.Chemistry.HTerm, termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>Eingabe

### <a name="term--hterm"></a>Begriff: [hterm](xref:Microsoft.Quantum.Chemistry.HTerm)

Eingabedaten im- `HTerm` Format.


### <a name="termtype--int"></a>Termtype: [int](xref:microsoft.quantum.lang-ref.int)[]

Zusätzliche Informationen, die generatorindex hinzugefügt werden.



## <a name="output--generatorindex"></a>Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Ein generatorindex, der einen von dargestellten hamiltona-Begriff darstellt `term` , sowie zusätzliche Informationen, die von hinzugefügt werden `termType` .