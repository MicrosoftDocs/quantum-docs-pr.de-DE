---
uid: Microsoft.Quantum.MachineLearning.ApproximateInputEncoder
title: Näheratinput Encoder-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApproximateInputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.
ms.openlocfilehash: 035c353c34362aa3486a7df9e7bb1bc95a6f63be
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856177"
---
# <a name="approximateinputencoder-function"></a><span data-ttu-id="e6e61-102">Näheratinput Encoder-Funktion</span><span class="sxs-lookup"><span data-stu-id="e6e61-102">ApproximateInputEncoder function</span></span>

<span data-ttu-id="e6e61-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="e6e61-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="e6e61-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="e6e61-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="e6e61-105">Gibt anhand eines Satzes von Koeffizienten und einer Toleranz einen Zustands Vorbereitungs Vorgang zurück, der jeden Koeffizienten als die entsprechende Amplitude eines Berechnungsbasis Zustands bis zur angegebenen Toleranz vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="e6e61-105">Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.</span></span>

```qsharp
function ApproximateInputEncoder (tolerance : Double, coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a><span data-ttu-id="e6e61-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e6e61-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="e6e61-107">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e6e61-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e6e61-108">Die Näherungs Toleranz, die beim Codieren der angegebenen Koeffizienten in einen Eingabe Zustand verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6e61-108">The approximation tolerance to be used in encoding the given coefficients into an input state.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="e6e61-109">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="e6e61-109">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="e6e61-110">Die Koeffizienten, die in einen Eingabe Zustand codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e6e61-110">The coefficients to be encoded into an input state.</span></span>



## <a name="output--stategenerator"></a><span data-ttu-id="e6e61-111">Ausgabe: [stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="e6e61-111">Output : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="e6e61-112">Ein Zustands Vorbereitungs Vorgang, bei dem die angegebenen Koeffizienten als Eingabe Zustand für ein bestimmtes Register vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="e6e61-112">A state preparation operation that prepares the given coefficients as an input state on a given register.</span></span>