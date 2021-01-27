---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: Isnotzero-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: 9384e5dafd4b5b7d44cb348c9537ebc2c621466d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839598"
---
# <a name="isnotzero-function"></a><span data-ttu-id="f5685-102">Isnotzero-Funktion</span><span class="sxs-lookup"><span data-stu-id="f5685-102">IsNotZero function</span></span>

<span data-ttu-id="f5685-103">Namespace: [Microsoft. Quantum. Chemistry](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="f5685-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="f5685-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="f5685-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="f5685-105">Überprüft, ob eine `Double` Zahl nicht ungefähr 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="f5685-105">Checks whether a `Double` number is not approximately zero.</span></span>

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="f5685-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f5685-106">Input</span></span>

### <a name="number--double"></a><span data-ttu-id="f5685-107">Zahl: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f5685-107">number : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f5685-108">Zu überprüfende Zahl</span><span class="sxs-lookup"><span data-stu-id="f5685-108">Number to be checked</span></span>



## <a name="output--bool"></a><span data-ttu-id="f5685-109">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f5685-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f5685-110">Gibt true zurück, wenn `number` einen absoluten Wert hat, der größer als ist `1e-15` .</span><span class="sxs-lookup"><span data-stu-id="f5685-110">Returns true if `number` has an absolute value greater than `1e-15`.</span></span>