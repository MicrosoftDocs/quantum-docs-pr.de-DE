---
uid: Microsoft.Quantum.Canon.ApplyToTail
title: Applydetail-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTail
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 72b55ec7161d5f6af5e4cb512c648078516c3b4e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704634"
---
# <a name="applytotail-operation"></a><span data-ttu-id="d51c0-102">Applydetail-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d51c0-102">ApplyToTail operation</span></span>

<span data-ttu-id="d51c0-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d51c0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d51c0-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d51c0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d51c0-105">Wendet einen Vorgang auf das letzte Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="d51c0-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTail<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="d51c0-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d51c0-106">Description</span></span>

<span data-ttu-id="d51c0-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="d51c0-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="d51c0-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d51c0-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="d51c0-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d51c0-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="d51c0-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d51c0-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="d51c0-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="d51c0-111">targets : 'T[]</span></span>

<span data-ttu-id="d51c0-112">Ein Array von Zielen, auf das der letzte angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="d51c0-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d51c0-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d51c0-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d51c0-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="d51c0-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d51c0-115">GIF</span><span class="sxs-lookup"><span data-stu-id="d51c0-115">'T</span></span>

<span data-ttu-id="d51c0-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d51c0-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="d51c0-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d51c0-117">See Also</span></span>

- [<span data-ttu-id="d51c0-118">Microsoft. Quantum. Canon. applyumtaila</span><span class="sxs-lookup"><span data-stu-id="d51c0-118">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="d51c0-119">Microsoft. Quantum. Canon. Apply| tailc</span><span class="sxs-lookup"><span data-stu-id="d51c0-119">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)
- [<span data-ttu-id="d51c0-120">Microsoft. Quantum. Canon. applyumtailca</span><span class="sxs-lookup"><span data-stu-id="d51c0-120">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)