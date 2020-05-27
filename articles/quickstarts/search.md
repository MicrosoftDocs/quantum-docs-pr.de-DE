---
title: 'Ausführen des Grover-Suchalgorithmus in Q#: Quantum Development Kit'
description: Erstellen eines Q#-Projekts, das den Grover-Algorithmus veranschaulicht, einen der kanonischen Quantenalgorithmen.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: 9562e1937a2cac49d682cc0524d8fb29e276d95c
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426807"
---
# <a name="tutorial-implement-grovers-search-algorithm-in-q"></a><span data-ttu-id="8aaf0-103">Tutorial: Implementierung des Grover-Suchalgorithmus in Q\#</span><span class="sxs-lookup"><span data-stu-id="8aaf0-103">Tutorial: Implement Grover's search algorithm in Q\#</span></span>

<span data-ttu-id="8aaf0-104">In diesem Tutorial erfahren Sie, wie Sie eine Grover-Suchabfrage erstellen und ausführen, um die Suche in unstrukturierten Daten zu beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-104">In this tutorial, you can learn how to build and run Grover search to speed up the search of unstructured data.</span></span>  <span data-ttu-id="8aaf0-105">Bei der Grover-Suche handelt es sich um einen der beliebtesten Quantencomputingalgorithmen. Diese relativ kleine Q#-Implementierung vermittelt Ihnen einen Eindruck davon, welche Vorteile die Programmierung von Quantenlösungen mit einer allgemeinen Q#-Quantenprogrammiersprache zum Ausdrücken von Quantenalgorithmen bietet.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-105">Grover's search is one of the most popular quantum computing algorithms, and this relatively small Q# implementation gives you a sense of some of the advantages of programming quantum solutions with a high-level Q# quantum programming language to express quantum algorithms.</span></span>  <span data-ttu-id="8aaf0-106">Die Simulationsausgabe am Ende der Anleitung zeigt, dass die Suche nach einer bestimmten Zeichenfolge in einer Liste unsortierter Einträge nur einen Bruchteil der Zeit dauert, die für die Durchsuchung der gesamten Liste auf einem klassischen Computer benötigt würde.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-106">At the end of the guide, you will see the simulation output demonstrates successfully finding a specific string among a list of unordered entries in a fraction of the time it would take to search the whole list on a classical computer.</span></span>

<span data-ttu-id="8aaf0-107">Der Grover-Algorithmus durchsucht eine Liste unstrukturierter Daten nach bestimmten Elementen.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-107">Grover's algorithm searches a list of unstructured data for specific items.</span></span> <span data-ttu-id="8aaf0-108">Er kann beispielsweise diese Frage beantworten: Ist diese Karte, die aus einem Kartenstapel gezogen wurde, ein Herz As?</span><span class="sxs-lookup"><span data-stu-id="8aaf0-108">For example, it can answer the question: Is this card drawn from a pack of cards an ace of hearts?</span></span> <span data-ttu-id="8aaf0-109">Die Bezeichnung des spezifischen Elements wird als _markierte Eingabe_ bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-109">The labeling of the specific item is called _marked input_.</span></span>

<span data-ttu-id="8aaf0-110">Bei Verwendung des Grover-Suchalgorithmus besteht Sicherheit, dass ein Quantencomputer diese Suche in weniger Schritten ausführt als die Anzahl der Elemente in der durchsuchten Liste – das kann kein klassischer Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-110">Using Grover's search algorithm, a quantum computer is guaranteed to run this search in fewer steps than the number of items in the list that you're searching — something no classical algorithm can do.</span></span> <span data-ttu-id="8aaf0-111">Die höhere Geschwindigkeit ist im Fall des Kartenstapels vernachlässigbar. In Listen, die Millionen oder Milliarden Elemente enthalten, wird sie aber wichtig.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-111">The increased speed in the case of a pack of cards is negligible; however, in lists containing millions or billions of items, it becomes significant.</span></span>

<span data-ttu-id="8aaf0-112">Sie können den Grover-Suchalgorithmus mit wenigen Codezeilen erstellen.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-112">You can build Grover's search algorithm with just a few lines of code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8aaf0-113">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="8aaf0-113">Prerequisites</span></span>

- <span data-ttu-id="8aaf0-114">Das Microsoft [Quantum Development Kit][install].</span><span class="sxs-lookup"><span data-stu-id="8aaf0-114">The Microsoft [Quantum Development Kit][install].</span></span>

## <a name="what-does-grovers-search-algorithm-do"></a><span data-ttu-id="8aaf0-115">Was macht der Grover-Suchalgorithmus?</span><span class="sxs-lookup"><span data-stu-id="8aaf0-115">What does Grover's search algorithm do?</span></span>

<span data-ttu-id="8aaf0-116">Der Grover-Algorithmus fragt, ob ein Element in einer Liste dasjenige ist, nach dem wir suchen.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-116">Grover's algorithm asks whether an item in a list is the one we are searching for.</span></span> <span data-ttu-id="8aaf0-117">Dazu erstellt er eine Quantenüberlagerung der Indizes der Liste mit jedem Koeffizienten (jeder Wahrscheinlichkeitsamplitude), wodurch die Wahrscheinlichkeit dargestellt wird, dass ein bestimmter Index der gesuchte ist.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-117">It does this by constructing a quantum superposition of the indexes of the list with each coefficient, or probability amplitude, representing the probability of that specific index being the one you are looking for.</span></span>

<span data-ttu-id="8aaf0-118">Im Kern des Algorithmus befinden sich zwei Schritte, die den Koeffizienten des gesuchten Index inkrementell verstärken, bis die Wahrscheinlichkeitsamplitude des betreffenden Koeffizienten sich eins annähert.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-118">At the heart of the algorithm are two steps that incrementally boost the coefficient of the index that we are looking for, until the probability amplitude of that coefficient approaches one.</span></span>

<span data-ttu-id="8aaf0-119">Die Anzahl der inkrementellen Verstärkungen ist kleiner als die Anzahl der Elemente in der Liste.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-119">The number of incremental boosts is fewer than the number of items in the list.</span></span> <span data-ttu-id="8aaf0-120">Das ist der Grund, warum der Grover-Suchalgorithmus die Suche in weniger Schritten als jeder klassische Algorithmus durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-120">This is why Grover's search algorithm performs the search in fewer steps than any classical algorithm.</span></span>

![Funktionsdiagramm des Grover-Suchalgorithmus](~/media/grover.png)

## <a name="write-the-code"></a><span data-ttu-id="8aaf0-122">Schreiben des Codes</span><span class="sxs-lookup"><span data-stu-id="8aaf0-122">Write the code</span></span>

1. <span data-ttu-id="8aaf0-123">[Erstellen Sie ein neues Q#-Projekt](xref:microsoft.quantum.howto.createproject) mit dem Namen `Grover` unter Verwendung des Quantum Development Kit in der Entwicklungsumgebung Ihrer Wahl.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-123">Using the Quantum Development Kit, [create a new Q# project](xref:microsoft.quantum.howto.createproject) called `Grover`, in your development environment of choice.</span></span>

1. <span data-ttu-id="8aaf0-124">Fügen Sie den folgenden Code der `Program.qs`-Datei in Ihrem neuen Projekt hinzu:</span><span class="sxs-lookup"><span data-stu-id="8aaf0-124">Add the following code to the `Program.qs` file in your new project:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-41":::

1. <span data-ttu-id="8aaf0-125">Um die Liste zu definieren, die wir durchsuchen, erstellen Sie eine neue Datei `Reflections.qs`, und fügen Sie den folgenden Code ein:</span><span class="sxs-lookup"><span data-stu-id="8aaf0-125">To define the list that we're searching, create a new file `Reflections.qs`, and paste in the following code:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    <span data-ttu-id="8aaf0-126">Die `ReflectAboutMarked`-Operation definiert die markierte Eingabe, nach der Sie suchen: die Zeichenfolge aus abwechselnden Nullen und Einsen.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-126">The `ReflectAboutMarked` operation defines the marked input that you are searching for: the string of alternating zeros and ones.</span></span> <span data-ttu-id="8aaf0-127">In diesem Beispiel wird die markierte Eingabe hartcodiert. Sie kann erweitert werden, um nach verschiedenen Eingaben zu suchen, oder generalisiert, um nach beliebigen Eingaben zu suchen.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-127">This sample hard-codes the marked input, and can be extended to search for different inputs or generalized for any input.</span></span>

1. <span data-ttu-id="8aaf0-128">Führen Sie als Nächstes Ihr neues Q#-Programm aus, um das von `ReflectAboutMarked` markierte Element zu finden.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-128">Next, run your new Q# program to find the item marked by `ReflectAboutMarked`.</span></span>

### <a name="q-command-line-applications-with-visual-studio-or-visual-studio-code"></a><span data-ttu-id="8aaf0-129">Q#-Befehlszeilenanwendungen mit Visual Studio oder Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="8aaf0-129">Q# command line applications with Visual Studio or Visual Studio Code</span></span>

<span data-ttu-id="8aaf0-130">Die ausführbare Datei führt den Vorgang oder die Funktion, der bzw. die mit dem Attribut `@EntryPoint()` markiert ist, abhängig von der Projektkonfiguration und den Befehlszeilenoptionen für einen Simulator oder eine Ressourcenschätzung aus.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-130">The executable will run the operation or function marked with the `@EntryPoint()` attribute on a simulator or resource estimator, depending on the project configuration and command-line options.</span></span>

<span data-ttu-id="8aaf0-131">Drücken Sie in Visual Studio einfach STRG+F5, um das Skript auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-131">In Visual Studio, simply press Ctrl + F5 to execute the script.</span></span>

<span data-ttu-id="8aaf0-132">Erstellen Sie in VS Code erstmalig die Datei `Program.qs`, indem Sie Folgendes im Terminal eingeben:</span><span class="sxs-lookup"><span data-stu-id="8aaf0-132">In VS Code, build the `Program.qs` the first time by typing the below in the terminal:</span></span>

```Command line
dotnet build
```

<span data-ttu-id="8aaf0-133">Bei nachfolgenden Ausführungen muss diese Datei nicht erneut erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-133">For subsequent runs, there is no need to build it again.</span></span> <span data-ttu-id="8aaf0-134">Geben Sie für die Ausführung den folgenden Befehl ein, und drücken Sie die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="8aaf0-134">To run it, type the following command and press enter:</span></span>

```Command line
dotnet run --no-build
```

<span data-ttu-id="8aaf0-135">Im Terminal sollte die folgende Meldung angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="8aaf0-135">You should see the following message displayed in the terminal:</span></span>

```
operations.qs:
This operation applies Grover's algorithm to search all possible inputs to an operation to find a particular marked state.
Usage:
operations.qs [options] [command]

--n-qubits <n-qubits> (REQUIRED)
-s, --simulator <simulator>         The name of the simulator to use.
--version                           Show version information
-?, -h, --help                      Show help and usage information
Commands:
```

<span data-ttu-id="8aaf0-136">Das liegt daran, dass Sie die Anzahl der zu verwendenden Qubits nicht angegeben haben. Vom Terminal werden daher die für die ausführbare Datei verfügbaren Befehle ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-136">This is because you didn't specify the number of qubits you wanted to use, so the terminal tells you the commands available for the executable.</span></span> <span data-ttu-id="8aaf0-137">Wenn Sie 5 Qubits verwenden möchten, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="8aaf0-137">If we want to use 5 qubits we should type:</span></span>

```Command line
dotnet run --n-qubits 5
```

<span data-ttu-id="8aaf0-138">Nach dem Drücken der EINGABETASTE sollte die folgende Ausgabe angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="8aaf0-138">Pressing enter you should see the following output:</span></span>

```
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
[Zero,One,Zero,One,Zero]
```

## <a name="next-steps"></a><span data-ttu-id="8aaf0-139">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="8aaf0-139">Next steps</span></span>

<span data-ttu-id="8aaf0-140">Wenn Ihnen dieses Tutorial gefallen hat, sehen Sie sich einige der unten aufgeführten Ressourcen an, um mehr darüber zu erfahren, wie Sie Q# verwenden können, um eigene Quantenanwendungen zu schreiben:</span><span class="sxs-lookup"><span data-stu-id="8aaf0-140">If you enjoyed this tutorial, check out some of the resources below to learn more about how you can use Q# to write your own quantum applications:</span></span>

- [<span data-ttu-id="8aaf0-141">Zurück zum Leitfaden mit den ersten Schritte mit dem QDK</span><span class="sxs-lookup"><span data-stu-id="8aaf0-141">Back to the Getting Started with QDK guide</span></span>](xref:microsoft.quantum.welcome)
- <span data-ttu-id="8aaf0-142">Ausprobieren eines [Beispiels](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search) für einen allgemeineren Grover-Suchalgorithmus</span><span class="sxs-lookup"><span data-stu-id="8aaf0-142">Try a more general Grover's search algorithm [sample](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search)</span></span>
- [<span data-ttu-id="8aaf0-143">Weitere Informationen zur Grover-Suche mit den Quanten-Katas</span><span class="sxs-lookup"><span data-stu-id="8aaf0-143">Learn more about Grover's search with the Quantum Katas</span></span>](xref:microsoft.quantum.overview.katas)
- <span data-ttu-id="8aaf0-144">Informieren Sie sich ausführlicher über die [Amplitudenverstärkung][amplitude-amplification], die Quantencomputingtechnik hinter dem Suchalgorithmus von Grover.</span><span class="sxs-lookup"><span data-stu-id="8aaf0-144">Read more about [Amplitude amplification][amplitude-amplification], the quantum computing technique behind Grover's search algorithm</span></span>
- [<span data-ttu-id="8aaf0-145">Quantencomputingkonzepte</span><span class="sxs-lookup"><span data-stu-id="8aaf0-145">Quantum computing concepts</span></span>](xref:microsoft.quantum.concepts.intro)
- [<span data-ttu-id="8aaf0-146">Quantum Development Kit-Beispiele</span><span class="sxs-lookup"><span data-stu-id="8aaf0-146">Quantum Development Kit Samples</span></span>](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
[amplitude-amplification]: xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification
