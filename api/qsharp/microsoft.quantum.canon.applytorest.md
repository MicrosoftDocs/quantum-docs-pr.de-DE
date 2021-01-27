---
uid: Microsoft.Quantum.Canon.ApplyToRest
title: Applytor-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRest
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: f18536a056935220feedc4ea50531c5def61d650
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850510"
---
# <a name="applytorest-operation"></a><span data-ttu-id="6dede-102">Applytor-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6dede-102">ApplyToRest operation</span></span>

<span data-ttu-id="6dede-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6dede-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6dede-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6dede-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6dede-105">Wendet einen Vorgang auf alle außer auf das erste Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="6dede-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRest<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="6dede-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6dede-106">Description</span></span>

<span data-ttu-id="6dede-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="6dede-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="6dede-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6dede-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="6dede-109">OP: 't [] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6dede-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="6dede-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6dede-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="6dede-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="6dede-111">targets : 'T[]</span></span>

<span data-ttu-id="6dede-112">Ein Array von Zielen, von denen alle außer der ersten übernommen werden `op` .</span><span class="sxs-lookup"><span data-stu-id="6dede-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6dede-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6dede-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6dede-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="6dede-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6dede-115">GIF</span><span class="sxs-lookup"><span data-stu-id="6dede-115">'T</span></span>

<span data-ttu-id="6dede-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6dede-116">The input type of the operation to be applied.</span></span>

## <a name="example"></a><span data-ttu-id="6dede-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6dede-117">Example</span></span>

<span data-ttu-id="6dede-118">Die folgenden Q #-Code Ausschnitte sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="6dede-118">The following Q# snippets are equivalent:</span></span>

```qsharp
ApplyToRest(ApplyCNOTChain, register);
ApplyCNOTChain(Rest(register));
```

## <a name="see-also"></a><span data-ttu-id="6dede-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6dede-119">See Also</span></span>

- [<span data-ttu-id="6dede-120">Microsoft. Quantum. Canon. applytoriesta</span><span class="sxs-lookup"><span data-stu-id="6dede-120">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="6dede-121">Microsoft. Quantum. Canon. applytor</span><span class="sxs-lookup"><span data-stu-id="6dede-121">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="6dede-122">Microsoft. Quantum. Canon. applytor estca</span><span class="sxs-lookup"><span data-stu-id="6dede-122">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)