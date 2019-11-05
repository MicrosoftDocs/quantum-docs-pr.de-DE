---
title: 'Ausführen des Grover-Suchalgorithmus in Q#: Quantum Development Kit'
description: Erstellen eines Q#-Projekts, das den Grover-Algorithmus veranschaulicht, einen der kanonischen Quantenalgorithmen.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: 75028a1dc29abe5fbea2e789d896563f3d6331c9
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2019
ms.locfileid: "73443935"
---
# <a name="quickstart-implement-grovers-search-algorithm-in-q"></a><span data-ttu-id="fcbd3-103">Schnellstart: Implementierung des Grover-Suchalgorithmus in Q#</span><span class="sxs-lookup"><span data-stu-id="fcbd3-103">Quickstart: Implement Grover's search algorithm in Q#</span></span>

<span data-ttu-id="fcbd3-104">In dieser Schnellstartanleitung erfahren Sie, wie Sie eine Grover-Suchabfrage erstellen und ausführen, um die Suche in unstrukturierten Daten zu beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-104">In this Quickstart, you can learn how to build and run Grover search to speed up the search of unstructured data.</span></span>  <span data-ttu-id="fcbd3-105">Bei der Grover-Suche handelt es sich um einen der beliebtesten Quantencomputingalgorithmen. Diese relativ kleine Q#-Implementierung vermittelt Ihnen einen Eindruck davon, welche Vorteile die Programmierung von Quantenlösungen mit einer allgemeinen Q#-Quantenprogrammiersprache zum Ausdrücken von Quantenalgorithmen bietet.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-105">Grover's search is one of the most popular quantum computing algorithms, and this relatively small Q# implementation gives you a sense of some of the advantages of programming quantum solutions with a high-level Q# quantum programming language to express quantum algorithms.</span></span>  <span data-ttu-id="fcbd3-106">Die Simulationsausgabe am Ende der Anleitung zeigt, dass die Suche nach einer bestimmten Zeichenfolge in einer Liste unsortierter Einträge nur einen Bruchteil der Zeit dauert, die für die Durchsuchung der gesamten Liste auf einem klassischen Computer benötigt würde.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-106">At the end of the guide, you will see the simulation output demonstrates successfully finding a specific string among a list of onordered entries in a fraction of the time it would take to search the whole list on a classical computer.</span></span>

<span data-ttu-id="fcbd3-107">Der Grover-Algorithmus durchsucht eine Liste unstrukturierter Daten nach bestimmten Elementen.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-107">Grover's algorithm searches a list of unstructured data for specific items.</span></span> <span data-ttu-id="fcbd3-108">Er kann beispielsweise diese Frage beantworten: Ist diese Karte, die aus einem Kartenstapel gezogen wurde, ein Herz As?</span><span class="sxs-lookup"><span data-stu-id="fcbd3-108">For example, it can answer the question: Is this card drawn from a pack of cards an ace of hearts?</span></span> <span data-ttu-id="fcbd3-109">Die Bezeichnung des spezifischen Elements wird als _markierte Eingabe_ bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-109">The labeling of the specific item is called _marked input_.</span></span>

<span data-ttu-id="fcbd3-110">Bei Verwendung des Grover-Suchalgorithmus besteht Sicherheit, dass ein Quantencomputer diese Suche in weniger Schritten ausführt als die Anzahl der Elemente in der durchsuchten Liste – das kann kein klassischer Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-110">Using Grover's search algorithm, a quantum computer is guaranteed to run this search in fewer steps than the number of items in the list that you're searching — something no classical algorithm can do.</span></span> <span data-ttu-id="fcbd3-111">Die höhere Geschwindigkeit ist im Fall des Kartenstapels vernachlässigbar. In Listen, die Millionen oder Milliarden Elemente enthalten, wird sie aber wichtig.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-111">The increased speed in the case of a pack of cards is negligible; however, in lists containing millions or billions of items, it becomes significant.</span></span>

<span data-ttu-id="fcbd3-112">Sie können den Grover-Suchalgorithmus mit wenigen Codezeilen erstellen.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-112">You can build Grover's search algorithm with just a few lines of code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fcbd3-113">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="fcbd3-113">Prerequisites</span></span>

- <span data-ttu-id="fcbd3-114">Das Microsoft [Quantum Development Kit][install].</span><span class="sxs-lookup"><span data-stu-id="fcbd3-114">The Microsoft [Quantum Development Kit][install].</span></span>

## <a name="what-does-grovers-search-algorithm-do"></a><span data-ttu-id="fcbd3-115">Was macht der Grover-Suchalgorithmus?</span><span class="sxs-lookup"><span data-stu-id="fcbd3-115">What does Grover's search algorithm do?</span></span>

<span data-ttu-id="fcbd3-116">Der Grover-Algorithmus fragt, ob ein Element in einer Liste dasjenige ist, nach dem wir suchen.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-116">Grover's algorithm asks whether an item in a list is the one we are searching for.</span></span> <span data-ttu-id="fcbd3-117">Dazu erstellt er eine Quantenüberlagerung der Indizes der Liste mit jedem Koeffizienten (jeder Wahrscheinlichkeitsamplitude), wodurch die Wahrscheinlichkeit dargestellt wird, dass ein bestimmter Index der gesuchte ist.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-117">It does this by constructing a quantum superposition of the indexes of the list with each coefficient, or probability amplitude, representing the probability of that specific index being the one you are looking for.</span></span>

<span data-ttu-id="fcbd3-118">Im Kern des Algorithmus befinden sich zwei Schritte, die den Koeffizienten des gesuchten Index inkrementell verstärken, bis die Wahrscheinlichkeitsamplitude des betreffenden Koeffizienten sich eins annähert.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-118">At the heart of the algorithm are two steps that incrementally boost the coefficient of the index that we are looking for, until the probability amplitude of that coefficient approaches one.</span></span>

<span data-ttu-id="fcbd3-119">Die Anzahl der inkrementellen Verstärkungen ist kleiner als die Anzahl der Elemente in der Liste.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-119">The number of incremental boosts is fewer than the number of items in the list.</span></span> <span data-ttu-id="fcbd3-120">Das ist der Grund, warum der Grover-Suchalgorithmus die Suche in weniger Schritten als jeder klassische Algorithmus durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-120">This is why Grover's search algorithm performs the search in fewer steps than any classical algorithm.</span></span>

![Funktionsdiagramm des Grover-Suchalgorithmus](~/media/grover.png)

## <a name="write-the-code"></a><span data-ttu-id="fcbd3-122">Schreiben des Codes</span><span class="sxs-lookup"><span data-stu-id="fcbd3-122">Write the code</span></span>

1. <span data-ttu-id="fcbd3-123">[Erstellen Sie ein neues Q#-Projekt](xref:microsoft.quantum.howto.createproject) mit dem Namen `Grover` unter Verwendung des Quantum Development Kit in der Entwicklungsumgebung Ihrer Wahl.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-123">Using the Quantum Development Kit, [create a new Q# project](xref:microsoft.quantum.howto.createproject) called `Grover`, in your development environment of choice.</span></span>

1. <span data-ttu-id="fcbd3-124">Fügen Sie den folgenden Code der `Operations.qs`-Datei in Ihrem neuen Projekt hinzu:</span><span class="sxs-lookup"><span data-stu-id="fcbd3-124">Add the following code to the `Operations.qs` file in your new project:</span></span>

    [!code-qsharp[](~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs?highlight=5,27)]

1. <span data-ttu-id="fcbd3-125">Um die Liste zu definieren, die wir durchsuchen, erstellen Sie eine neue Datei `Reflections.qs`, und fügen Sie den folgenden Code ein:</span><span class="sxs-lookup"><span data-stu-id="fcbd3-125">To define the list that we're searching, create a new file `Reflections.qs`, and paste in the following code:</span></span>

    [!code-qsharp[](~/quantum/samples/algorithms/simple-grover/Reflections.qs)]

    <span data-ttu-id="fcbd3-126">Die `ReflectAboutMarked`-Operation definiert die markierte Eingabe, nach der Sie suchen: die Zeichenfolge aus abwechselnden Nullen und Einsen.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-126">The `ReflectAboutMarked` operation defines the marked input that you are searching for: the string of alternating zeros and ones.</span></span> <span data-ttu-id="fcbd3-127">In diesem Beispiel wird die markierte Eingabe hartcodiert. Sie kann erweitert werden, um nach verschiedenen Eingaben zu suchen, oder generalisiert, um nach beliebigen Eingaben zu suchen.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-127">This sample hard-codes the marked input, and can be extended to search for different inputs or generalized for any input.</span></span>

1. <span data-ttu-id="fcbd3-128">Führen Sie als Nächstes Ihr neues Q#-Programm aus, um das von `ReflectAboutMarked` markierte Element zu finden.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-128">Next, run your new Q# program to find the item marked by `ReflectAboutMarked`.</span></span>

    ### <a name="python-with-visual-studio-code-or-the-command-linetabtabid-python"></a>[<span data-ttu-id="fcbd3-129">Python mit Visual Studio Code oder Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="fcbd3-129">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)

    <span data-ttu-id="fcbd3-130">Um Ihr neues Q#-Programm aus Python auszuführen, speichern Sie den folgenden Code als `host.py`:</span><span class="sxs-lookup"><span data-stu-id="fcbd3-130">To run your new Q# program from Python, save the following code as `host.py`:</span></span>

    [!code-python[](~/quantum/samples/algorithms/simple-grover/host.py)]

    <span data-ttu-id="fcbd3-131">Anschließend können Sie Ihr Python-Hostprogramm an der Befehlszeile ausführen:</span><span class="sxs-lookup"><span data-stu-id="fcbd3-131">You can then run your Python host program from the command line:</span></span>

    ```bash
    $ python host.py
    Preparing Q# environment...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    [0, 1, 0, 1, 0]
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-linetabtabid-csharp"></a>[<span data-ttu-id="fcbd3-132">C# mit Visual Studio Code oder Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="fcbd3-132">C# with Visual Studio Code or the Command Line</span></span>](#tab/tabid-csharp)

    <span data-ttu-id="fcbd3-133">Um Ihr neues Q#-Programm aus C# auszuführen, ändern Sie `Driver.cs`, so dass es den folgenden C#-Code beinhaltet:</span><span class="sxs-lookup"><span data-stu-id="fcbd3-133">To run your new Q# program from C#, modify `Driver.cs` to include the following C# code:</span></span>

    [!code-csharp[](~/quantum/samples/algorithms/simple-grover/Host.cs)]

    <span data-ttu-id="fcbd3-134">Anschließend können Sie Ihr C#-Hostprogramm an der Befehlszeile ausführen:</span><span class="sxs-lookup"><span data-stu-id="fcbd3-134">You can then run your C# host program from the command line:</span></span>

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```

    ### <a name="c-with-visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="fcbd3-135">C# mit Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="fcbd3-135">C# with Visual Studio 2019</span></span>](#tab/tabid-vs2019)

    <span data-ttu-id="fcbd3-136">Ändern Sie zum Ausführen Ihres neuen Q#-Programms aus C# in Visual Studio `Driver.cs`, sodass der folgende C#-Code enthalten ist:</span><span class="sxs-lookup"><span data-stu-id="fcbd3-136">To run your new Q# program from C# in Visual Studio, modify `Driver.cs` to include the following C# code:</span></span>

    [!code-csharp[](~/quantum/samples/algorithms/simple-grover/Host.cs)]

    <span data-ttu-id="fcbd3-137">Drücken Sie dann F5. Das Programm wird gestartet, und ein neues Fenster mit den folgenden Ergebnissen wird angezeigt:</span><span class="sxs-lookup"><span data-stu-id="fcbd3-137">Then press F5, the program will start execution and a new windows will pop-up with the following results:</span></span> 

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```
    ***

    <span data-ttu-id="fcbd3-138">Die `ReflectAboutMarked`-Operation wird nur viermal aufgerufen, Ihr Q#-Programm war aber imstande, die Eingabe "01010" unter $2^{5} = 32$ möglichen Eingaben zu finden!</span><span class="sxs-lookup"><span data-stu-id="fcbd3-138">The `ReflectAboutMarked` operation is called only four times, but your Q# program was able to find the "01010" input amongst $2^{5} = 32$ possible inputs!</span></span>

## <a name="next-steps"></a><span data-ttu-id="fcbd3-139">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="fcbd3-139">Next steps</span></span>

<span data-ttu-id="fcbd3-140">Wenn Ihnen dieser Schnellstart gefallen hat, sehen Sie sich einige der unten aufgeführten Ressourcen an, um mehr darüber zu erfahren, wie Sie Q# verwenden können, um eigene Quantenanwendungen zu schreiben:</span><span class="sxs-lookup"><span data-stu-id="fcbd3-140">If you enjoyed this quickstart, check out some of the resources below to learn more about how you can use Q# to write your own quantum applications:</span></span>

- [<span data-ttu-id="fcbd3-141">Zurück zum Leitfaden mit den ersten Schritte mit dem QDK</span><span class="sxs-lookup"><span data-stu-id="fcbd3-141">Back to the Getting Started with QDK guide</span></span>](xref:microsoft.quantum.welcome)
- <span data-ttu-id="fcbd3-142">Ausprobieren eines [Beispiels](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search) für einen allgemeineren Grover-Suchalgorithmus</span><span class="sxs-lookup"><span data-stu-id="fcbd3-142">Try a more general Grover's search algorithm [sample](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search)</span></span>
- [<span data-ttu-id="fcbd3-143">Weitere Informationen zur Grover-Suche mit den Quanten-Katas</span><span class="sxs-lookup"><span data-stu-id="fcbd3-143">Learn more about Grover's search with the Quantum Katas</span></span>](xref:microsoft.quantum.overview.katas)
- <span data-ttu-id="fcbd3-144">Informieren Sie sich ausführlicher über die [Amplitudenverstärkung](xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification), die Quantencomputingtechnik hinter dem Suchalgorithmus von Grover.</span><span class="sxs-lookup"><span data-stu-id="fcbd3-144">Read more about [Amplitude amplification](xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification), the quantum computing technique behind Grover's search algorithm</span></span>
- [<span data-ttu-id="fcbd3-145">Quantencomputingkonzepte</span><span class="sxs-lookup"><span data-stu-id="fcbd3-145">Quantum computing concepts</span></span>](xref:microsoft.quantum.concepts.intro)
- [<span data-ttu-id="fcbd3-146">Quantum Development Kit-Beispiele</span><span class="sxs-lookup"><span data-stu-id="fcbd3-146">Quantum Development Kit Samples</span></span>](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
