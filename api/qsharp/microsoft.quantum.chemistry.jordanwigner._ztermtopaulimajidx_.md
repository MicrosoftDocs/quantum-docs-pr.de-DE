---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ZTermToPauliMajIdx_
title: _Ztermtopaulimajidx_ -Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ZTermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a Z term to an expression 'GeneratorIndex[]' in terms of Paulis.
ms.openlocfilehash: 56de7b7b425b7d7c5830c15d7119fc1d0291d061
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839079"
---
# <a name="_ztermtopaulimajidx_-function"></a>_Ztermtopaulimajidx_ -Funktion

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Konvertiert einen generatorindex, der einen Z-Begriff beschreibt, in den Ausdruck ' generatorindex [] ' in Bezug auf Paulis.

```qsharp
function _ZTermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex
```


## <a name="input"></a>Eingabe

### <a name="term--generatorindex"></a>Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` , der einen Z-Begriff darstellt.



## <a name="output--optimizedbetermindex"></a>Ausgabe: [optimizedbetermindex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)

' Generatorindex [] ' ausgedrückt: Z-Begriff als Pauli-Begriffe.