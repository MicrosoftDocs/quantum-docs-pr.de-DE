---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedGeneratorSystem
title: Jwoptimizedgeneratorsystem-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.
ms.openlocfilehash: 8e4c06b9447a2e5838cced876febee03d1af5315
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701814"
---
# <a name="jwoptimizedgeneratorsystem-function"></a><span data-ttu-id="2abda-102">Jwoptimizedgeneratorsystem-Funktion</span><span class="sxs-lookup"><span data-stu-id="2abda-102">JWOptimizedGeneratorSystem function</span></span>

<span data-ttu-id="2abda-103">Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="2abda-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="2abda-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2abda-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2abda-105">Konvertiert eine von beschriebene hamiltona `JWOptimizedHTerms` in eine, `GeneratorSystem` die in Bezug auf die `GeneratorIndex` in dieser Datei definierte Konvention ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="2abda-105">Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.</span></span>

```qsharp
function JWOptimizedGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="2abda-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2abda-106">Input</span></span>

### <a name="data--jwoptimizedhterms"></a><span data-ttu-id="2abda-107">Daten: [jwoptimizedhterms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span><span class="sxs-lookup"><span data-stu-id="2abda-107">data : [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span></span>

<span data-ttu-id="2abda-108">Beschreibung von hamiltonan im `JWOptimizedHTerms` Format.</span><span class="sxs-lookup"><span data-stu-id="2abda-108">Description of Hamiltonian in `JWOptimizedHTerms` format.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="2abda-109">Ausgabe: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="2abda-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="2abda-110">Darstellung von hamiltonan als `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="2abda-110">Representation of Hamiltonian as `GeneratorSystem`.</span></span>