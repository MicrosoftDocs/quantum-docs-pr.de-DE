---
uid: Microsoft.Quantum.MachineLearning.InputEncoder
title: Inputencoder-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.
ms.openlocfilehash: 771cf01866498f4662864939e6946526c2b5827a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701375"
---
# <a name="inputencoder-function"></a><span data-ttu-id="06f4c-102">Inputencoder-Funktion</span><span class="sxs-lookup"><span data-stu-id="06f4c-102">InputEncoder function</span></span>

<span data-ttu-id="06f4c-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="06f4c-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="06f4c-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="06f4c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="06f4c-105">Gibt bei einem Satz von Koeffizienten und einer Toleranz einen Zustands Vorbereitungs Vorgang zurück, bei dem jeder Koeffizient als die entsprechende Amplitude eines Berechnungsbasis Zustands vorbereitet wird.</span><span class="sxs-lookup"><span data-stu-id="06f4c-105">Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.</span></span>

```qsharp
function InputEncoder (coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a><span data-ttu-id="06f4c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="06f4c-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="06f4c-107">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="06f4c-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="06f4c-108">Die Koeffizienten, die in einen Eingabe Zustand codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="06f4c-108">The coefficients to be encoded into an input state.</span></span>



## <a name="output--stategenerator"></a><span data-ttu-id="06f4c-109">Ausgabe: [stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="06f4c-109">Output : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="06f4c-110">Ein Zustands Vorbereitungs Vorgang, bei dem die angegebenen Koeffizienten als Eingabe Zustand für ein bestimmtes Register vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="06f4c-110">A state preparation operation that prepares the given coefficients as an input state on a given register.</span></span>