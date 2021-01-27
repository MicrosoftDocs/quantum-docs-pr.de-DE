---
title: Mitwirken von Beispielen an das Microsoft QDK
description: Erfahren Sie, wie Sie Beispielcode zum Microsoft Quantum Development Kit (QDK) beitragen.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: contributor-guide
uid: microsoft.quantum.contributing.samples
no-loc:
- Q#
- $$v
ms.openlocfilehash: 0c940a4cf228c694a899988f469158b1bb6e2425
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847584"
---
# <a name="contributing-samples-to-the-quantum-development-kit"></a><span data-ttu-id="ba434-103">Mitwirken von Beispielen für das Quantum Development Kit</span><span class="sxs-lookup"><span data-stu-id="ba434-103">Contributing Samples to the Quantum Development Kit</span></span>

<span data-ttu-id="ba434-104">Wenn Sie an dem [beispielrepository](https://github.com/Microsoft/Quantum)Code mitwirken möchten, vielen Dank, dass Sie die Quantum Development Community besser platzieren!</span><span class="sxs-lookup"><span data-stu-id="ba434-104">If you're interested in contributing code to the [samples repository](https://github.com/Microsoft/Quantum), thank you for making the quantum development community a better place!</span></span>

## <a name="the-quantum-development-kit-samples-repository"></a><span data-ttu-id="ba434-105">Das Quantum Development Kit-beispielrepository</span><span class="sxs-lookup"><span data-stu-id="ba434-105">The Quantum Development Kit Samples Repository</span></span>

<span data-ttu-id="ba434-106">Um Ihnen bei der Vorbereitung Ihres Beitrags zu helfen, so weit wie möglich zu helfen, ist es hilfreich, sich einen kurzen Blick darauf zu verschaffen, wie das beispielrepository angelegt wird:</span><span class="sxs-lookup"><span data-stu-id="ba434-106">To help you prepare your contribution to help out as much as possible, it's helpful to take a quick look at how the samples repository is laid out:</span></span>

```plaintext
microsoft/Quantum
📁 samples/
  📁 algorithms/
    📁 chsh-game/
      📝 CHSHGame.csproj
      📝 Game.qs
      📝 Host.cs
      📝 host.py
      📝 README.md
     ⋮
  📁 arithmetic/
  📁 characterization/
  📁 chemistry/
   ⋮
```

<span data-ttu-id="ba434-107">Das heißt, die Beispiele im [Microsoft/quantum-Repository](https://github.com/microsoft/Quantum) werden nach Themenbereich in verschiedene Ordner aufgeteilt `algorithms/` , z. b `arithmetic/` ., oder `characterization/` .</span><span class="sxs-lookup"><span data-stu-id="ba434-107">That is, the samples in the [microsoft/Quantum repository](https://github.com/microsoft/Quantum) are broken down by subject area into different folders such as `algorithms/`, `arithmetic/`, or `characterization/`.</span></span>
<span data-ttu-id="ba434-108">Innerhalb des Ordners für jeden Themenbereich besteht jedes Beispiel aus einem einzelnen Ordner, der alle Elemente sammelt, die ein Benutzer zum Durchsuchen und verwenden dieses Beispiels benötigt.</span><span class="sxs-lookup"><span data-stu-id="ba434-108">Within the folder for each subject area, each sample consists of a single folder that collects everything a user will need to explore and make use of that sample.</span></span>

## <a name="how-samples-are-structured"></a><span data-ttu-id="ba434-109">Strukturieren von Beispielen</span><span class="sxs-lookup"><span data-stu-id="ba434-109">How Samples are Structured</span></span>

<span data-ttu-id="ba434-110">Sehen wir uns die Dateien an, aus denen sich die einzelnen Ordner bilden, betrachten wir das [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/main/samples/algorithms/chsh-game) Beispiel.</span><span class="sxs-lookup"><span data-stu-id="ba434-110">Looking at the files that make up each folder, let's dive into the [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/main/samples/algorithms/chsh-game) sample.</span></span>

| <span data-ttu-id="ba434-111">Datei</span><span class="sxs-lookup"><span data-stu-id="ba434-111">File</span></span>              | <span data-ttu-id="ba434-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba434-112">Description</span></span>                                                |
|-------------------|------------------------------------------------------------|
| `CHSHGame.csproj` | <span data-ttu-id="ba434-113">Q# Das Projekt, mit dem das Beispiel mit dem .net Core SDK erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ba434-113">Q# project used to build the sample with the .NET Core SDK</span></span> |
| `Game.qs`         | <span data-ttu-id="ba434-114">Q# Vorgänge und Funktionen für das Beispiel</span><span class="sxs-lookup"><span data-stu-id="ba434-114">Q# operations and functions for the sample</span></span>                 |
| `Host.cs`         | <span data-ttu-id="ba434-115">Zum Ausführen des Beispiels verwendetes c#-Host Programm</span><span class="sxs-lookup"><span data-stu-id="ba434-115">C# host program used to run the sample</span></span>                     |
| `host.py`         | <span data-ttu-id="ba434-116">Zum Ausführen des Beispiels verwendetes python-Host Programm</span><span class="sxs-lookup"><span data-stu-id="ba434-116">Python host program used to run the sample</span></span>                 |
| `README.md`       | <span data-ttu-id="ba434-117">Dokumentation zur Funktionsweise des Beispiels und zur Verwendung</span><span class="sxs-lookup"><span data-stu-id="ba434-117">Documentation on what the sample does and how to use it</span></span>    |

<span data-ttu-id="ba434-118">Nicht alle Samples verfügen über genau denselben Satz von Dateien (z. b. können einige Beispiele nur c#-Code enthalten, andere verfügen möglicherweise nicht über einen python-Host, oder einige Beispiele erfordern möglicherweise, dass die Datendateien für die Daten ordnungsgemäß funktionieren).</span><span class="sxs-lookup"><span data-stu-id="ba434-118">Not all samples will have the exact same set of files (e.g.: some samples may be C#-only, others may not have a Python host, or some samples may require auxillary data files to work).</span></span>

## <a name="anatomy-of-a-helpful-readme-file"></a><span data-ttu-id="ba434-119">Anatomie einer hilfreichen Infodatei</span><span class="sxs-lookup"><span data-stu-id="ba434-119">Anatomy of a Helpful README File</span></span>

<span data-ttu-id="ba434-120">Eine besonders wichtige Datei ist allerdings die `README.md` Datei, die die Benutzer für den Einstieg in Ihr Beispiel benötigen.</span><span class="sxs-lookup"><span data-stu-id="ba434-120">One especially important file, though, is the `README.md` file, as that's what users need to get started with your sample!</span></span>

<span data-ttu-id="ba434-121">Jede `README.md` sollte mit einigen Metadaten beginnen, die Ihnen helfen, ihren Beitrag zu docs.Microsoft.com/Samples finden.</span><span class="sxs-lookup"><span data-stu-id="ba434-121">Each `README.md` should start with some metadata that helps docs.microsoft.com/samples find your contribution.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="ba434-122">Sehen Sie sich an, wie das Beispiel für das CHSH-Spiel</span><span class="sxs-lookup"><span data-stu-id="ba434-122">See how the chsh-game sample is rendered</span></span>](https://docs.microsoft.com/samples/microsoft/quantum/validating-quantum-mechanics/)

<span data-ttu-id="ba434-123">Diese Metadaten werden als [YAML-Header](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) bereitgestellt, der angibt, welche Sprachen Ihr Beispiel abdeckt (in der Regel, `qsharp` `csharp` und `python` ) und welche Produkte in Ihrem Beispiel behandelt werden (in der Regel nur `qdk` ).</span><span class="sxs-lookup"><span data-stu-id="ba434-123">This metadata is provided as a [YAML header](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) that indicates what languages your sample covers (typically, this will be `qsharp`, `csharp`, and `python`), and what products your sample covers (typically, just `qdk`).</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="1-11":::

> [!IMPORTANT]
> <span data-ttu-id="ba434-124">Der `page_type: sample` Schlüssel im-Header ist erforderlich, damit das Beispiel unter docs.Microsoft.com/Samples angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ba434-124">The `page_type: sample` key in the header is required for your sample to appear at docs.microsoft.com/samples.</span></span>
> <span data-ttu-id="ba434-125">Ebenso sind der `product` -Schlüssel und der- `language` Schlüssel wichtig, um Benutzern zu helfen, das Beispiel zu finden und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ba434-125">Similarly, the `product` and `language` keys are critical for helping users to find and run your sample.</span></span>

<span data-ttu-id="ba434-126">Danach ist es hilfreich, eine kurze Einführung zu erhalten, in der das neue Beispiel angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="ba434-126">After that, it's helpful to give a short intro that says what your new sample does:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="13-21":::

<span data-ttu-id="ba434-127">Benutzer Ihres Beispiels können auch wissen, was Sie benötigen, um es auszuführen (z. b. benötigen Benutzer nur das Quantum Development Kit selbst oder benötigen zusätzliche Software, wie z. b. node.js?):</span><span class="sxs-lookup"><span data-stu-id="ba434-127">Users of your sample will also appreciate knowing what they need to run it (e.g.: do users just need the Quantum Development Kit itself, or do they need additional software such as node.js?):</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="23-25":::

<span data-ttu-id="ba434-128">Damit können Sie die Benutzer darüber informieren, wie das Beispiel ausgeführt werden soll:</span><span class="sxs-lookup"><span data-stu-id="ba434-128">With all that in place, you can tell users how to run your sample:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="27-50":::

<span data-ttu-id="ba434-129">Schließlich ist es hilfreich, Benutzern mitzuteilen, was jede Datei in Ihrem Beispiel tut und wo Sie weitere Informationen erhalten können:</span><span class="sxs-lookup"><span data-stu-id="ba434-129">Finally, it's helpful to tell users what each file in your sample does, and where they can go for more information:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="52-61":::

> [!WARNING]
> <span data-ttu-id="ba434-130">Stellen Sie sicher, dass Sie hier absolute URLs verwenden, da das Beispiel unter einer anderen URL angezeigt wird, wenn es unter docs.Microsoft.com/Samples gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="ba434-130">Make sure to use absolute URLs here, since your sample will appear at a different URL when rendered at docs.microsoft.com/samples!</span></span>
