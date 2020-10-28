---
uid: Microsoft.Quantum.Diagnostics.DumpMachine
title: Dumpmachine-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpMachine
qsharp.summary: Dumps the current target machine's status.
ms.openlocfilehash: c85cf6764bdc913a71448c525318f45743bf1df0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702713"
---
# <a name="dumpmachine-function"></a><span data-ttu-id="c8875-102">Dumpmachine-Funktion</span><span class="sxs-lookup"><span data-stu-id="c8875-102">DumpMachine function</span></span>

<span data-ttu-id="c8875-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="c8875-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="c8875-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c8875-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c8875-105">Sichert den Status des aktuellen Ziel Computers.</span><span class="sxs-lookup"><span data-stu-id="c8875-105">Dumps the current target machine's status.</span></span>

```qsharp
function DumpMachine<'T> (location : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="c8875-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c8875-106">Input</span></span>

### <a name="location--t"></a><span data-ttu-id="c8875-107">Speicherort: 't</span><span class="sxs-lookup"><span data-stu-id="c8875-107">location : 'T</span></span>

<span data-ttu-id="c8875-108">Stellt Informationen dazu bereit, wo das Abbild des Computers generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8875-108">Provides information on where to generate the machine's dump.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c8875-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c8875-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="c8875-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="c8875-110">None.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c8875-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="c8875-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c8875-112">GIF</span><span class="sxs-lookup"><span data-stu-id="c8875-112">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="c8875-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c8875-113">Remarks</span></span>

<span data-ttu-id="c8875-114">Diese Methode ermöglicht es Ihnen, Informationen über den aktuellen Status des Ziel Computers in einer Datei oder an einem anderen Speicherort zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c8875-114">This method allows you to dump information about the current status of the target machine into a file or some other location.</span></span>
<span data-ttu-id="c8875-115">Die tatsächlich generierten Informationen und die Semantik von `location` sind für jeden Zielcomputer spezifisch.</span><span class="sxs-lookup"><span data-stu-id="c8875-115">The actual information generated and the semantics of `location` are specific to each target machine.</span></span> <span data-ttu-id="c8875-116">Wenn Sie jedoch ein leeres Tupel als Speicherort ( `()` ) bereitstellen oder einfach nur den-Parameter weglassen, bedeutet dies in `location` der Regel, dass die Ausgabe in der Konsole generiert wird.</span><span class="sxs-lookup"><span data-stu-id="c8875-116">However, providing an empty tuple as a location (`()`) or just omitting the `location` parameter typically means to generate the output to the console.</span></span>

<span data-ttu-id="c8875-117">Für den lokalen vollständigen Zustands Simulator, der als Teil des Quantum Development Kit verteilt wird, erwartet diese Methode eine Zeichenfolge mit dem Pfad zu einer Datei, in der die Wave-Funktion als eindimensionales Array komplexer Zahlen geschrieben wird, wobei jedes Element die Verstärkung der Wahrscheinlichkeit darstellt, den entsprechenden Zustand zu messen.</span><span class="sxs-lookup"><span data-stu-id="c8875-117">For the local full state simulator distributed as part of the Quantum Development Kit, this method  expects a string with the path to a file in which it will write the wave function as a one-dimensional array of complex numbers, in which each element represents the amplitudes of the probability of measuring the corresponding state.</span></span>