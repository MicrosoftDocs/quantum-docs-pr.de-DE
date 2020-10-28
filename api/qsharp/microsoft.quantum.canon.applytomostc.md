---
uid: Microsoft.Quantum.Canon.ApplyToMostC
title: Applytomostc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostC
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: a5927f6b296dd50afec8979c8e8ac22979b8a082
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704743"
---
# <a name="applytomostc-operation"></a><span data-ttu-id="01e52-102">Applytomostc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="01e52-102">ApplyToMostC operation</span></span>

<span data-ttu-id="01e52-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="01e52-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="01e52-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="01e52-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="01e52-105">Wendet einen Vorgang auf alle bis auf das letzte Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="01e52-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="01e52-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01e52-106">Description</span></span>

<span data-ttu-id="01e52-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="01e52-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="01e52-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="01e52-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="01e52-109">OP: 't [] => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="01e52-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="01e52-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="01e52-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="01e52-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="01e52-111">targets : 'T[]</span></span>

<span data-ttu-id="01e52-112">Ein Array von Zielen, von denen alle außer der letzten angewendet werden `op` .</span><span class="sxs-lookup"><span data-stu-id="01e52-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="01e52-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="01e52-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="01e52-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="01e52-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="01e52-115">GIF</span><span class="sxs-lookup"><span data-stu-id="01e52-115">'T</span></span>

<span data-ttu-id="01e52-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="01e52-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="01e52-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="01e52-117">See Also</span></span>

- [<span data-ttu-id="01e52-118">Microsoft. Quantum. Canon. applytomost</span><span class="sxs-lookup"><span data-stu-id="01e52-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="01e52-119">Microsoft. Quantum. Canon. applytomosta</span><span class="sxs-lookup"><span data-stu-id="01e52-119">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="01e52-120">Microsoft. Quantum. Canon. applytomostca</span><span class="sxs-lookup"><span data-stu-id="01e52-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)