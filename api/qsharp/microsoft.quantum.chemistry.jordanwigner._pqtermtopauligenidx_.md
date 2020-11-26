---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQTermToPauliGenIdx_
title: _Pqtermtopauligenidx_ -Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQTermToPauliGenIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 7f1794f9e46323ccf722407fb7ae82f73ed76e40
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96215434"
---
# <a name="_pqtermtopauligenidx_-function"></a><span data-ttu-id="16a57-102">_Pqtermtopauligenidx_ -Funktion</span><span class="sxs-lookup"><span data-stu-id="16a57-102">_PQTermToPauliGenIdx_ function</span></span>

<span data-ttu-id="16a57-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="16a57-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="16a57-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="16a57-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="16a57-105">Konvertiert einen generatorindex, der einen PQ-Begriff beschreibt, in einen Ausdruck "generatorindex []" im Hinblick auf "Paulis".</span><span class="sxs-lookup"><span data-stu-id="16a57-105">Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis</span></span>

```qsharp
function _PQTermToPauliGenIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a><span data-ttu-id="16a57-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="16a57-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="16a57-107">Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="16a57-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="16a57-108">`GeneratorIndex` , der einen PQ-Begriff darstellt.</span><span class="sxs-lookup"><span data-stu-id="16a57-108">`GeneratorIndex` representing a PQ term.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="16a57-109">Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span><span class="sxs-lookup"><span data-stu-id="16a57-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span></span>

<span data-ttu-id="16a57-110">' Generatorindex [] ' ausgedrückt den pq-Begriff als Pauli-Begriffe.</span><span class="sxs-lookup"><span data-stu-id="16a57-110">'GeneratorIndex[]' expressing PQ term as Pauli terms.</span></span>