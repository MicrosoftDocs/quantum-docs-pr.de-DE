---
uid: Microsoft.Quantum.Targeting.RequiresCapability
title: Benutzerdefinierter Typ "Requirements scapability"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Targeting
qsharp.name: RequiresCapability
qsharp.summary: Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.
ms.openlocfilehash: 0d9e4eb294b3ce91058c204d5dba37ea29b4ac28
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231006"
---
# <a name="requirescapability-user-defined-type"></a><span data-ttu-id="a6a55-102">Benutzerdefinierter Typ "Requirements scapability"</span><span class="sxs-lookup"><span data-stu-id="a6a55-102">RequiresCapability user defined type</span></span>

<span data-ttu-id="a6a55-103">Namespace: [Microsoft. Quantum. Targeting](xref:Microsoft.Quantum.Targeting)</span><span class="sxs-lookup"><span data-stu-id="a6a55-103">Namespace: [Microsoft.Quantum.Targeting](xref:Microsoft.Quantum.Targeting)</span></span>

<span data-ttu-id="a6a55-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a6a55-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a6a55-105">Vom Compiler erkanntes Attribut, das verwendet wird, um eine Aufruf Bare mit den erforderlichen Lauf Zeitfunktionen zu markieren.</span><span class="sxs-lookup"><span data-stu-id="a6a55-105">Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype RequiresCapability = (Level : String, Reason : String);
```



## <a name="named-items"></a><span data-ttu-id="a6a55-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="a6a55-106">Named Items</span></span>

### <a name="level--string"></a><span data-ttu-id="a6a55-107">Ebene: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="a6a55-107">Level : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="a6a55-108">Der Name der Lauf Zeit Funktionsebene, die für die Aufruf Bare-Funktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a6a55-108">The name of the runtime capability level required by the callable.</span></span>
### <a name="reason--string"></a><span data-ttu-id="a6a55-109">Ursache: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="a6a55-109">Reason : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="a6a55-110">Eine Beschreibung, warum die Aufruf Bare Funktion diese Lauf Zeitfunktion erfordert.</span><span class="sxs-lookup"><span data-stu-id="a6a55-110">A description of why the callable requires this runtime capability.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6a55-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6a55-111">Remarks</span></span>

<span data-ttu-id="a6a55-112">Dieses Attribut wird automatisch aufrufen durch den Compiler hinzugefügt, es sei denn, es ist bereits eine Instanz dieses Attributs für die Aufruf Bare Instanz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a6a55-112">This attribute is automatically added to callables by the compiler, unless an instance of this attribute already exists on the callable.</span></span> <span data-ttu-id="a6a55-113">Es sollte nicht verwendet werden, außer in seltenen Fällen, in denen der Compiler die erforderliche Funktion nicht ordnungsgemäß ableiten kann.</span><span class="sxs-lookup"><span data-stu-id="a6a55-113">It should not be used except in rare cases where the compiler does not infer the required capability correctly.</span></span>

<span data-ttu-id="a6a55-114">Im folgenden finden Sie eine Liste der Funktionsebenen, in der Reihenfolge, in der die Funktionen erhöht werden, oder zum verringern</span><span class="sxs-lookup"><span data-stu-id="a6a55-114">Below is the list of capability level names, in order of increasing capabilities or decreasing restrictions:</span></span>

## `"BasicQuantumFunctionality"`

<span data-ttu-id="a6a55-115">Die Messergebnisse können nicht auf Gleichheit verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="a6a55-115">Measurement results cannot be compared for equality.</span></span>

## `"BasicMeasurementFeedback"`

<span data-ttu-id="a6a55-116">Messergebnisse können nur bei bedingten Ausdrücken der if-Anweisung in-Vorgängen auf Gleichheit verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="a6a55-116">Measurement results can be compared for equality only in if-statement conditional expressions in operations.</span></span> <span data-ttu-id="a6a55-117">Der-Block einer if-Anweisung, die von einem Ergebnis abhängt, kann keine Set-Anweisungen für änderbare Variablen enthalten, die außerhalb des-Blocks deklariert werden, oder Return-Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="a6a55-117">The block of an if-statement that depends on a result cannot contain set statements for mutable variables declared outside the block, or return statements.</span></span>

## `"FullComputation"`

<span data-ttu-id="a6a55-118">Keine Lauf Zeiteinschränkungen.</span><span class="sxs-lookup"><span data-stu-id="a6a55-118">No runtime restrictions.</span></span> <span data-ttu-id="a6a55-119">Alle f #-Programme können ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a6a55-119">Any Q# program can be executed.</span></span>