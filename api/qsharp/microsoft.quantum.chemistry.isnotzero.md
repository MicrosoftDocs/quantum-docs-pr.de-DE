---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: Isnotzero-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: 3c0f9c6695e8c9ec4a0953d5217c28c512ac7de1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703548"
---
# <a name="isnotzero-function"></a><span data-ttu-id="f135c-102">Isnotzero-Funktion</span><span class="sxs-lookup"><span data-stu-id="f135c-102">IsNotZero function</span></span>

<span data-ttu-id="f135c-103">Namespace: [Microsoft. Quantum. Chemistry](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="f135c-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="f135c-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f135c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f135c-105">Überprüft, ob eine `Double` Zahl nicht ungefähr 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="f135c-105">Checks whether a `Double` number is not approximately zero.</span></span>

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="f135c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f135c-106">Input</span></span>

### <a name="number--double"></a><span data-ttu-id="f135c-107">Zahl: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f135c-107">number : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f135c-108">Zu überprüfende Zahl</span><span class="sxs-lookup"><span data-stu-id="f135c-108">Number to be checked</span></span>



## <a name="output--bool"></a><span data-ttu-id="f135c-109">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f135c-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f135c-110">Gibt true zurück, wenn `number` einen absoluten Wert hat, der größer als ist `1e-15` .</span><span class="sxs-lookup"><span data-stu-id="f135c-110">Returns true if `number` has an absolute value greater than `1e-15`.</span></span>