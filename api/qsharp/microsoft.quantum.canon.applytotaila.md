---
uid: Microsoft.Quantum.Canon.ApplyToTailA
title: Applydetaila-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 2cacac14ad6e5003f1a50d9b84c4e0f96950dd7d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207920"
---
# <a name="applytotaila-operation"></a><span data-ttu-id="ef07c-102">Applydetaila-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ef07c-102">ApplyToTailA operation</span></span>

<span data-ttu-id="ef07c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ef07c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ef07c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ef07c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ef07c-105">Wendet einen Vorgang auf das letzte Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="ef07c-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailA<'T> (op : ('T => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="ef07c-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef07c-106">Description</span></span>

<span data-ttu-id="ef07c-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="ef07c-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="ef07c-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef07c-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="ef07c-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="ef07c-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="ef07c-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ef07c-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="ef07c-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="ef07c-111">targets : 'T[]</span></span>

<span data-ttu-id="ef07c-112">Ein Array von Zielen, auf das der letzte angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="ef07c-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ef07c-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ef07c-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ef07c-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ef07c-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ef07c-115">GIF</span><span class="sxs-lookup"><span data-stu-id="ef07c-115">'T</span></span>

<span data-ttu-id="ef07c-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef07c-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef07c-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ef07c-117">See Also</span></span>

- [<span data-ttu-id="ef07c-118">Microsoft. Quantum. Canon. applyumtail</span><span class="sxs-lookup"><span data-stu-id="ef07c-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="ef07c-119">Microsoft. Quantum. Canon. Apply| tailc</span><span class="sxs-lookup"><span data-stu-id="ef07c-119">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)
- [<span data-ttu-id="ef07c-120">Microsoft. Quantum. Canon. applyumtailca</span><span class="sxs-lookup"><span data-stu-id="ef07c-120">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)