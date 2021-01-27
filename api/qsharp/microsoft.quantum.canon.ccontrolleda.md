---
uid: Microsoft.Quantum.Canon.CControlledA
title: Ccontrolleda-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 823d80182621691f4fa6f42246b3d671f3adfc3a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840990"
---
# <a name="ccontrolleda-function"></a><span data-ttu-id="15f12-102">Ccontrolleda-Funktion</span><span class="sxs-lookup"><span data-stu-id="15f12-102">CControlledA function</span></span>

<span data-ttu-id="15f12-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="15f12-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="15f12-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="15f12-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="15f12-105">Gibt bei einem Vorgang op einen neuen Vorgang zurück, der das OP anwendet, wenn ein klassisches Steuerelement "true" ist.</span><span class="sxs-lookup"><span data-stu-id="15f12-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="15f12-106">Gibt an `false` , dass nichts passiert.</span><span class="sxs-lookup"><span data-stu-id="15f12-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="15f12-107">Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="15f12-107">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
function CControlledA<'T> (op : ('T => Unit is Adj)) : ((Bool, 'T) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="15f12-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="15f12-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="15f12-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="15f12-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="15f12-110">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="15f12-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit--is-adj"></a><span data-ttu-id="15f12-111">Ausgabe: ([bool](xref:microsoft.quantum.lang-ref.bool), 't) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="15f12-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="15f12-112">Ein neuer Vorgang, bei dem es sich um einen op-Vorgang handelt, wenn das klassische Steuerelement</span><span class="sxs-lookup"><span data-stu-id="15f12-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="15f12-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="15f12-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="15f12-114">GIF</span><span class="sxs-lookup"><span data-stu-id="15f12-114">'T</span></span>

<span data-ttu-id="15f12-115">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="15f12-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="15f12-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="15f12-116">See Also</span></span>

- [<span data-ttu-id="15f12-117">Microsoft. Quantum. Canon. ckontrollierten</span><span class="sxs-lookup"><span data-stu-id="15f12-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)