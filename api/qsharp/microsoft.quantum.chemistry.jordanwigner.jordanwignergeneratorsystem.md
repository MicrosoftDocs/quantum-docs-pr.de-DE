---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerGeneratorSystem
title: Jordanwignergeneratorsystem-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.
ms.openlocfilehash: a75d46ef0b38fbcef99b7ab22454e1b5a9475b11
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98837777"
---
# <a name="jordanwignergeneratorsystem-function"></a><span data-ttu-id="58fce-102">Jordanwignergeneratorsystem-Funktion</span><span class="sxs-lookup"><span data-stu-id="58fce-102">JordanWignerGeneratorSystem function</span></span>

<span data-ttu-id="58fce-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="58fce-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="58fce-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="58fce-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="58fce-105">Konvertiert eine von beschriebene hamiltona `JWOptimizedHTerms` in eine, `GeneratorSystem` die in Bezug auf die `GeneratorIndex` in dieser Datei definierte Konvention ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="58fce-105">Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.</span></span>

```qsharp
function JordanWignerGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="58fce-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="58fce-106">Input</span></span>

### <a name="data--jwoptimizedhterms"></a><span data-ttu-id="58fce-107">Daten: [jwoptimizedhterms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span><span class="sxs-lookup"><span data-stu-id="58fce-107">data : [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span></span>

<span data-ttu-id="58fce-108">Beschreibung von hamiltonan im `JWOptimizedHTerms` Format.</span><span class="sxs-lookup"><span data-stu-id="58fce-108">Description of Hamiltonian in `JWOptimizedHTerms` format.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="58fce-109">Ausgabe: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="58fce-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="58fce-110">Darstellung von hamiltonan als `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="58fce-110">Representation of Hamiltonian as `GeneratorSystem`.</span></span>