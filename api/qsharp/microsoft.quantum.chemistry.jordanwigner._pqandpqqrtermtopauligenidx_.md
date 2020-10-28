---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQandPQQRTermToPauliGenIdx_
title: _Pqandpqqrtermtopauligenidx_ -Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQandPQQRTermToPauliGenIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ or PQQR term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 44a6d6b63d2f6bc8b628603e78931570d1ec22eb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703355"
---
# <a name="_pqandpqqrtermtopauligenidx_-function"></a>_Pqandpqqrtermtopauligenidx_ -Funktion

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paketen [](https://nuget.org/packages/)


Konvertiert einen generatorindex, der einen PQ-oder pqqr-Begriff beschreibt, in einen Ausdruck "generatorindex []" im Hinblick auf "Paulis".

```qsharp
function _PQandPQQRTermToPauliGenIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a>Eingabe

### <a name="term--generatorindex"></a>Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` , der einen PQ-oder pqqr-Begriff darstellt.



## <a name="output--generatorindex"></a>Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]

"Generatorindex []" ausgedrückt den pq-oder pqqr-Begriff als Pauli-Begriffe.