---
uid: Microsoft.Quantum.Canon.ApplyToTail
title: Applydetail-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTail
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 077e6dedee68b0bd05a668387b22f8bec87a4041
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850435"
---
# <a name="applytotail-operation"></a><span data-ttu-id="f9b71-102">Applydetail-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f9b71-102">ApplyToTail operation</span></span>

<span data-ttu-id="f9b71-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f9b71-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f9b71-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f9b71-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f9b71-105">Wendet einen Vorgang auf das letzte Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="f9b71-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTail<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="f9b71-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9b71-106">Description</span></span>

<span data-ttu-id="f9b71-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="f9b71-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="f9b71-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f9b71-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="f9b71-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f9b71-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="f9b71-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f9b71-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="f9b71-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="f9b71-111">targets : 'T[]</span></span>

<span data-ttu-id="f9b71-112">Ein Array von Zielen, auf das der letzte angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="f9b71-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f9b71-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f9b71-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f9b71-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f9b71-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f9b71-115">GIF</span><span class="sxs-lookup"><span data-stu-id="f9b71-115">'T</span></span>

<span data-ttu-id="f9b71-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9b71-116">The input type of the operation to be applied.</span></span>

## <a name="example"></a><span data-ttu-id="f9b71-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f9b71-117">Example</span></span>

<span data-ttu-id="f9b71-118">Die folgenden Q #-Code Ausschnitte sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="f9b71-118">The following Q# snippets are equivalent:</span></span>

```qsharp
ApplyToTail(H, register);
H(Tail(register));
```

## <a name="see-also"></a><span data-ttu-id="f9b71-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f9b71-119">See Also</span></span>

- [<span data-ttu-id="f9b71-120">Microsoft. Quantum. Canon. applyumtaila</span><span class="sxs-lookup"><span data-stu-id="f9b71-120">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="f9b71-121">Microsoft. Quantum. Canon. Apply| tailc</span><span class="sxs-lookup"><span data-stu-id="f9b71-121">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)
- [<span data-ttu-id="f9b71-122">Microsoft. Quantum. Canon. applyumtailca</span><span class="sxs-lookup"><span data-stu-id="f9b71-122">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)