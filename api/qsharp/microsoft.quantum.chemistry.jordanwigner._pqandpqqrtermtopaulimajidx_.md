---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQandPQQRTermToPauliMajIdx_
title: _Pqandpqqrtermtopaulimajidx_ -Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQandPQQRTermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ or PQQR term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 1a04f5f3b66e0dccb650b2d451a086a380b9810a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225005"
---
# <a name="_pqandpqqrtermtopaulimajidx_-function"></a>_Pqandpqqrtermtopaulimajidx_ -Funktion

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Konvertiert einen generatorindex, der einen PQ-oder pqqr-Begriff beschreibt, in einen Ausdruck "generatorindex []" im Hinblick auf "Paulis".

```qsharp
function _PQandPQQRTermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex
```


## <a name="input"></a>Eingabe

### <a name="term--generatorindex"></a>Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` , der einen PQ-oder pqqr-Begriff darstellt.



## <a name="output--optimizedbetermindex"></a>Ausgabe: [optimizedbetermindex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)

"Generatorindex []" ausgedrückt den pq-oder pqqr-Begriff als Pauli-Begriffe.