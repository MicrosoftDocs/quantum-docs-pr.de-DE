---
uid: Microsoft.Quantum.MachineLearning.ApproximateInputEncoder
title: Näheratinput Encoder-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApproximateInputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.
ms.openlocfilehash: 67ef7a47a2e036f0953d946b4ace0e6673b173bd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706887"
---
# <a name="approximateinputencoder-function"></a><span data-ttu-id="eaba2-102">Näheratinput Encoder-Funktion</span><span class="sxs-lookup"><span data-stu-id="eaba2-102">ApproximateInputEncoder function</span></span>

<span data-ttu-id="eaba2-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="eaba2-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="eaba2-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="eaba2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="eaba2-105">Gibt anhand eines Satzes von Koeffizienten und einer Toleranz einen Zustands Vorbereitungs Vorgang zurück, der jeden Koeffizienten als die entsprechende Amplitude eines Berechnungsbasis Zustands bis zur angegebenen Toleranz vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="eaba2-105">Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.</span></span>

```qsharp
function ApproximateInputEncoder (tolerance : Double, coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a><span data-ttu-id="eaba2-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="eaba2-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="eaba2-107">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="eaba2-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="eaba2-108">Die Näherungs Toleranz, die beim Codieren der angegebenen Koeffizienten in einen Eingabe Zustand verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eaba2-108">The approximation tolerance to be used in encoding the given coefficients into an input state.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="eaba2-109">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="eaba2-109">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="eaba2-110">Die Koeffizienten, die in einen Eingabe Zustand codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eaba2-110">The coefficients to be encoded into an input state.</span></span>



## <a name="output--stategenerator"></a><span data-ttu-id="eaba2-111">Ausgabe: [stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="eaba2-111">Output : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="eaba2-112">Ein Zustands Vorbereitungs Vorgang, bei dem die angegebenen Koeffizienten als Eingabe Zustand für ein bestimmtes Register vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="eaba2-112">A state preparation operation that prepares the given coefficients as an input state on a given register.</span></span>