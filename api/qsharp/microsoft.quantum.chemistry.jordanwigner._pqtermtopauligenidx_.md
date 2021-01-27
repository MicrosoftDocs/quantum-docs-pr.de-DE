---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQTermToPauliGenIdx_
title: _Pqtermtopauligenidx_ -Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQTermToPauliGenIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 046b3b7b78cee7f046607277896100e20c33a32d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839313"
---
# <a name="_pqtermtopauligenidx_-function"></a>_Pqtermtopauligenidx_ -Funktion

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Konvertiert einen generatorindex, der einen PQ-Begriff beschreibt, in einen Ausdruck "generatorindex []" im Hinblick auf "Paulis".

```qsharp
function _PQTermToPauliGenIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a>Eingabe

### <a name="term--generatorindex"></a>Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` , der einen PQ-Begriff darstellt.



## <a name="output--generatorindex"></a>Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]

' Generatorindex [] ' ausgedrückt den pq-Begriff als Pauli-Begriffe.