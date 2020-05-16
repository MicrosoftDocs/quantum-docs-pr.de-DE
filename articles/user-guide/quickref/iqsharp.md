---
title: IQ#-Magic-Befehle
description: 'Kurz Referenzseite für IQ # Magic-Befehle mit Q # jupyter Notebooks'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
uid: microsoft.quantum.guide.quickref.iqsharp
ms.openlocfilehash: 0cd1a2289132e2760a21fd9d4f4083696353e271
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431018"
---
# <a name="iq-magic-commands"></a><span data-ttu-id="5b793-103">IQ#-Magic-Befehle</span><span class="sxs-lookup"><span data-stu-id="5b793-103">IQ# Magic Commands</span></span>

### <a name="general"></a><span data-ttu-id="5b793-104">Allgemein</span><span class="sxs-lookup"><span data-stu-id="5b793-104">General</span></span>

- <span data-ttu-id="5b793-105">`%config`: Legt Konfigurationseinstellungen fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="5b793-105">`%config`: Sets or gets configuration preferences.</span></span>
- <span data-ttu-id="5b793-106">`%estimate`: Führt eine bestimmte Funktion oder einen Vorgang auf dem quantumschlag-Zielcomputer aus.</span><span class="sxs-lookup"><span data-stu-id="5b793-106">`%estimate`: Runs a given function or operation on the QuantumSimulator target machine.</span></span>
- <span data-ttu-id="5b793-107">`%lsmagic`: Gibt eine Liste aller zurzeit verfügbaren Magic-Befehle zurück.</span><span class="sxs-lookup"><span data-stu-id="5b793-107">`%lsmagic`: Returns a list of all currently available magic commands.</span></span>
- <span data-ttu-id="5b793-108">`%package`: Bietet die Möglichkeit, ein nuget-Paket zu laden.</span><span class="sxs-lookup"><span data-stu-id="5b793-108">`%package`: Provides the ability to load a Nuget package.</span></span>
- <span data-ttu-id="5b793-109">`%performance`: Meldet die aktuellen Leistungsmetriken für diesen Kernel.</span><span class="sxs-lookup"><span data-stu-id="5b793-109">`%performance`: Reports current performance metrics for this kernel.</span></span>
- <span data-ttu-id="5b793-110">`%simulate`: Führt eine bestimmte Funktion oder einen Vorgang auf dem quantumschlag-Zielcomputer aus.</span><span class="sxs-lookup"><span data-stu-id="5b793-110">`%simulate`: Runs a given function or operation on the QuantumSimulator target machine.</span></span>
- <span data-ttu-id="5b793-111">`%toffoli`: Führt eine angegebene Funktion oder einen Vorgang auf dem Bereitstellungs Zielcomputer für den Dienst des Dienst-Simulators aus.</span><span class="sxs-lookup"><span data-stu-id="5b793-111">`%toffoli`: Runs a given function or operation on the ToffoliSimulator simulator target machine.</span></span>
- <span data-ttu-id="5b793-112">`%who`: Stellt Aktionen bereit, die sich auf den aktuellen Arbeitsbereich beziehen.</span><span class="sxs-lookup"><span data-stu-id="5b793-112">`%who`: Provides actions related to the current workspace.</span></span>
- <span data-ttu-id="5b793-113">`%workspace`: Gibt eine Liste aller Vorgänge und Funktionen zurück, die in der aktuellen Sitzung definiert sind, entweder interaktiv oder aus dem aktuellen Arbeitsbereich geladen.</span><span class="sxs-lookup"><span data-stu-id="5b793-113">`%workspace`: Returns a list of all operations and functions defined in the current session, either interactively or loaded from the current workspace.</span></span>

### <a name="chemistry"></a><span data-ttu-id="5b793-114">Chemi</span><span class="sxs-lookup"><span data-stu-id="5b793-114">Chemistry</span></span>

- <span data-ttu-id="5b793-115">`%chemistry.broombridge`: Lädt und gibt die Darstellung der broombridge-elektronischen Strukturprobleme aus einer bestimmten YAML-Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="5b793-115">`%chemistry.broombridge`: Loads and returns Broombridge electronic structure problem representation from a given .yaml file.</span></span>
- <span data-ttu-id="5b793-116">`%chemistry.encode`: Codiert ein Fermion-hamiltonan in ein Format, das von Q # verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="5b793-116">`%chemistry.encode`: Encodes a fermion Hamiltonian to a format consumable by Q#.</span></span>
- <span data-ttu-id="5b793-117">`%chemistry.fh.add_terms`: Fügt einem Fermion-hamiltonan Bedingungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="5b793-117">`%chemistry.fh.add_terms`: Adds terms to a fermion Hamiltonian.</span></span>
- <span data-ttu-id="5b793-118">`%chemistry.fh.load`: Lädt den Fermion-hamiltonan für ein elektronisches Strukturproblem.</span><span class="sxs-lookup"><span data-stu-id="5b793-118">`%chemistry.fh.load`: Loads the fermion Hamiltonian for an electronic structure problem.</span></span> <span data-ttu-id="5b793-119">Das Problem wird aus einer Datei geladen oder als Argument übergeben.</span><span class="sxs-lookup"><span data-stu-id="5b793-119">The problem is loaded from a file or passed as an argument.</span></span>
- <span data-ttu-id="5b793-120">`%chemistry.inputstate.load`: Lädt das Problem der elektronischen broombridge-Struktur und gibt den ausgewählten Eingabe Status zurück.</span><span class="sxs-lookup"><span data-stu-id="5b793-120">`%chemistry.inputstate.load`: Loads Broombridge electronic structure problem and returns selected input state.</span></span>

### <a name="from-microsoftquantumkatas-package"></a><span data-ttu-id="5b793-121">Aus dem Paket "Microsoft. Quantum. Katas"</span><span class="sxs-lookup"><span data-stu-id="5b793-121">From Microsoft.Quantum.Katas package</span></span>

- <span data-ttu-id="5b793-122">`%kata`: Führt einen einzelnen Test aus und meldet, ob der Test erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="5b793-122">`%kata`: Executes a single test, and reports whether the test passed successfully.</span></span>
- <span data-ttu-id="5b793-123">`%check_kata`: Überprüft die Verweis Implementierung für den Test einer einzelnen Kata.</span><span class="sxs-lookup"><span data-stu-id="5b793-123">`%check_kata`: Checks the reference implementation for a single kata's test.</span></span>
    <span data-ttu-id="5b793-124">Insbesondere ersetzt Sie die Verweis Implementierung für eine einzelne Aufgabe in der Zelle und meldet, ob der Test erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="5b793-124">Specifically, it substitutes the reference implementation for a single task into the cell, and reports whether the test passed successfully.</span></span>
