---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingByLCU
title: Applyblockencodingbylcu-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingByLCU
qsharp.summary: Implementation of `BlockEncodingByLCU`.
ms.openlocfilehash: a9a9e3bbd598453719f49f78392f3a92c9401b36
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852826"
---
# <a name="applyblockencodingbylcu-operation"></a><span data-ttu-id="4cb58-102">Applyblockencodingbylcu-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4cb58-102">ApplyBlockEncodingByLCU operation</span></span>

<span data-ttu-id="4cb58-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="4cb58-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="4cb58-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4cb58-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4cb58-105">Implementierung von `BlockEncodingByLCU`.</span><span class="sxs-lookup"><span data-stu-id="4cb58-105">Implementation of `BlockEncodingByLCU`.</span></span>

```qsharp
operation ApplyBlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl), auxiliary : 'T, system : 'S) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="4cb58-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4cb58-106">Input</span></span>

### <a name="statepreparation--t--unit--is-adj--ctl"></a><span data-ttu-id="4cb58-107">statepreparation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="4cb58-107">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="selector--ts--unit--is-adj--ctl"></a><span data-ttu-id="4cb58-108">Selektor: ('t, es) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="4cb58-108">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="auxiliary--t"></a><span data-ttu-id="4cb58-109">Zusatz: 't</span><span class="sxs-lookup"><span data-stu-id="4cb58-109">auxiliary : 'T</span></span>




### <a name="system--s"></a><span data-ttu-id="4cb58-110">System:</span><span class="sxs-lookup"><span data-stu-id="4cb58-110">system : 'S</span></span>





## <a name="output--unit"></a><span data-ttu-id="4cb58-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4cb58-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4cb58-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="4cb58-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4cb58-113">GIF</span><span class="sxs-lookup"><span data-stu-id="4cb58-113">'T</span></span>


### <a name="s"></a><span data-ttu-id="4cb58-114">Spaniens</span><span class="sxs-lookup"><span data-stu-id="4cb58-114">'S</span></span>

