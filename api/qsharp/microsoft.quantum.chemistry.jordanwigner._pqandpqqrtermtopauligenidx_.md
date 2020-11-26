---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQandPQQRTermToPauliGenIdx_
title: _Pqandpqqrtermtopauligenidx_ -Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQandPQQRTermToPauliGenIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ or PQQR term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 17acd2c09129275af90222e30fd96a7551e18b50
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203534"
---
# <a name="_pqandpqqrtermtopauligenidx_-function"></a><span data-ttu-id="d2347-102">_Pqandpqqrtermtopauligenidx_ -Funktion</span><span class="sxs-lookup"><span data-stu-id="d2347-102">_PQandPQQRTermToPauliGenIdx_ function</span></span>

<span data-ttu-id="d2347-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="d2347-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="d2347-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="d2347-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="d2347-105">Konvertiert einen generatorindex, der einen PQ-oder pqqr-Begriff beschreibt, in einen Ausdruck "generatorindex []" im Hinblick auf "Paulis".</span><span class="sxs-lookup"><span data-stu-id="d2347-105">Converts a GeneratorIndex describing a PQ or PQQR term to an expression 'GeneratorIndex[]' in terms of Paulis</span></span>

```qsharp
function _PQandPQQRTermToPauliGenIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a><span data-ttu-id="d2347-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2347-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="d2347-107">Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="d2347-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="d2347-108">`GeneratorIndex` , der einen PQ-oder pqqr-Begriff darstellt.</span><span class="sxs-lookup"><span data-stu-id="d2347-108">`GeneratorIndex` representing a PQ or PQQR term.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="d2347-109">Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span><span class="sxs-lookup"><span data-stu-id="d2347-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span></span>

<span data-ttu-id="d2347-110">"Generatorindex []" ausgedrückt den pq-oder pqqr-Begriff als Pauli-Begriffe.</span><span class="sxs-lookup"><span data-stu-id="d2347-110">'GeneratorIndex[]' expressing PQ or PQQR term as Pauli terms.</span></span>