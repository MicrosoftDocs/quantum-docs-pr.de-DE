---
uid: Microsoft.Quantum.Canon.ApplyToHead
title: Applydehead-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHead
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 4e627b467e9354e774c2ead8b89ddd3ff3a42ef7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841336"
---
# <a name="applytohead-operation"></a><span data-ttu-id="08334-102">Applydehead-Vorgang</span><span class="sxs-lookup"><span data-stu-id="08334-102">ApplyToHead operation</span></span>

<span data-ttu-id="08334-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="08334-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="08334-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="08334-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="08334-105">Wendet einen Vorgang auf das erste Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="08334-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHead<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="08334-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08334-106">Description</span></span>

<span data-ttu-id="08334-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="08334-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="08334-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="08334-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="08334-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="08334-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="08334-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="08334-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="08334-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="08334-111">targets : 'T[]</span></span>

<span data-ttu-id="08334-112">Ein Array von Zielen, von dem die erste angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="08334-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="08334-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="08334-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="08334-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="08334-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="08334-115">GIF</span><span class="sxs-lookup"><span data-stu-id="08334-115">'T</span></span>

<span data-ttu-id="08334-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="08334-116">The input type of the operation to be applied.</span></span>

## <a name="example"></a><span data-ttu-id="08334-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="08334-117">Example</span></span>

<span data-ttu-id="08334-118">Die folgenden Q #-Code Ausschnitte sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="08334-118">The following Q# snippets are equivalent:</span></span>

```qsharp
ApplyToHead(H, register);
H(Head(register));
```

## <a name="see-also"></a><span data-ttu-id="08334-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="08334-119">See Also</span></span>

- [<span data-ttu-id="08334-120">Microsoft. Quantum. Canon. applyumheada</span><span class="sxs-lookup"><span data-stu-id="08334-120">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="08334-121">Microsoft. Quantum. Canon. applyumheadc</span><span class="sxs-lookup"><span data-stu-id="08334-121">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="08334-122">Microsoft. Quantum. Canon. ApplyTo headca</span><span class="sxs-lookup"><span data-stu-id="08334-122">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)