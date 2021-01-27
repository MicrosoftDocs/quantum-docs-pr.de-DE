---
uid: Microsoft.Quantum.MachineLearning.InputEncoder
title: Inputencoder-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.
ms.openlocfilehash: ed70d9f24af06f8918083307c98a5f6c4671f1c3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852940"
---
# <a name="inputencoder-function"></a><span data-ttu-id="2c8b9-102">Inputencoder-Funktion</span><span class="sxs-lookup"><span data-stu-id="2c8b9-102">InputEncoder function</span></span>

<span data-ttu-id="2c8b9-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="2c8b9-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="2c8b9-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="2c8b9-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="2c8b9-105">Gibt bei einem Satz von Koeffizienten und einer Toleranz einen Zustands Vorbereitungs Vorgang zurück, bei dem jeder Koeffizient als die entsprechende Amplitude eines Berechnungsbasis Zustands vorbereitet wird.</span><span class="sxs-lookup"><span data-stu-id="2c8b9-105">Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.</span></span>

```qsharp
function InputEncoder (coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a><span data-ttu-id="2c8b9-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2c8b9-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="2c8b9-107">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="2c8b9-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="2c8b9-108">Die Koeffizienten, die in einen Eingabe Zustand codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2c8b9-108">The coefficients to be encoded into an input state.</span></span>



## <a name="output--stategenerator"></a><span data-ttu-id="2c8b9-109">Ausgabe: [stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="2c8b9-109">Output : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="2c8b9-110">Ein Zustands Vorbereitungs Vorgang, bei dem die angegebenen Koeffizienten als Eingabe Zustand für ein bestimmtes Register vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="2c8b9-110">A state preparation operation that prepares the given coefficients as an input state on a given register.</span></span>