---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQandPQQRTermToPauliMajIdx_
title: _Pqandpqqrtermtopaulimajidx_ -Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQandPQQRTermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ or PQQR term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 68a9aec7768269e2d5f295d5ea3cbb136ea1ef2c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851496"
---
# <a name="_pqandpqqrtermtopaulimajidx_-function"></a><span data-ttu-id="4f0ee-102">_Pqandpqqrtermtopaulimajidx_ -Funktion</span><span class="sxs-lookup"><span data-stu-id="4f0ee-102">_PQandPQQRTermToPauliMajIdx_ function</span></span>

<span data-ttu-id="4f0ee-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="4f0ee-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="4f0ee-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="4f0ee-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="4f0ee-105">Konvertiert einen generatorindex, der einen PQ-oder pqqr-Begriff beschreibt, in einen Ausdruck "generatorindex []" im Hinblick auf "Paulis".</span><span class="sxs-lookup"><span data-stu-id="4f0ee-105">Converts a GeneratorIndex describing a PQ or PQQR term to an expression 'GeneratorIndex[]' in terms of Paulis</span></span>

```qsharp
function _PQandPQQRTermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex
```


## <a name="input"></a><span data-ttu-id="4f0ee-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4f0ee-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="4f0ee-107">Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="4f0ee-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="4f0ee-108">`GeneratorIndex` , der einen PQ-oder pqqr-Begriff darstellt.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-108">`GeneratorIndex` representing a PQ or PQQR term.</span></span>



## <a name="output--optimizedbetermindex"></a><span data-ttu-id="4f0ee-109">Ausgabe: [optimizedbetermindex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span><span class="sxs-lookup"><span data-stu-id="4f0ee-109">Output : [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span></span>

<span data-ttu-id="4f0ee-110">"Generatorindex []" ausgedrückt den pq-oder pqqr-Begriff als Pauli-Begriffe.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-110">'GeneratorIndex[]' expressing PQ or PQQR term as Pauli terms.</span></span>