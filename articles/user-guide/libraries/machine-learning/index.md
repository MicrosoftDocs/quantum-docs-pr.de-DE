---
title: Einführung in das Quantum Machine Learning-Paket | Microsoft-Dokumentation
description: Einführung in das Quantum Machine Learning-Paket
author: QuantumWriter
ms.author: alexeib@microsoft.com
ms.date: 12/5/2019
ms.topic: article
uid: microsoft.quantum.machine-learning.concepts.intro
ms.openlocfilehash: 7f22d5d3212890abc764f88693937b534466170f
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85273664"
---
# <a name="introduction-to-the-quantum-machine-learning-library"></a><span data-ttu-id="5c612-103">Einführung in die Quantum Machine Learning-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5c612-103">Introduction to the Quantum Machine Learning Library</span></span>

<span data-ttu-id="5c612-104">Die Quantum Machine Learning-Bibliothek ist eine API, die in Q# geschrieben ist. Hiermit können Sie Machine Learning-Hybridexperimente durchführen, bei denen das Quantencomputing und das klassische Computing genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="5c612-104">The Quantum Machine Learning Library is an API, written in Q#, that gives you the ability to run hybrid quantum/classical machine learning experiments.</span></span> <span data-ttu-id="5c612-105">Mit der Bibliothek haben Sie folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="5c612-105">The library gives you the ability to:</span></span>

- <span data-ttu-id="5c612-106">Laden Ihrer eigenen Daten für die Klassifizierung mit Quantensimulatoren</span><span class="sxs-lookup"><span data-stu-id="5c612-106">Load your own data to classify with quantum simulators</span></span>

- <span data-ttu-id="5c612-107">Verwenden von Beispielen und Tutorials als Einführung in Quantum Machine Learning</span><span class="sxs-lookup"><span data-stu-id="5c612-107">Use samples and tutorials to get introduced to the field of quantum machine learning</span></span>

<span data-ttu-id="5c612-108">Die zu erwartende Leistung ist im Vergleich zu aktuellen klassischen Machine Learning-Frameworks eher niedrig. (Bedenken Sie, dass alle Vorgänge zusätzlich zur Simulation eines Quantengeräts ausgeführt werden, für die bereits ein hoher Rechenaufwand anfällt.)</span><span class="sxs-lookup"><span data-stu-id="5c612-108">You can expect low performance compared to current classical machine learning frameworks (remember that everything is running on top of the simulation of a quantum device that is already computationally expensive).</span></span>

<span data-ttu-id="5c612-109">Diese Dokumentation soll die folgenden Zwecke erfüllen:</span><span class="sxs-lookup"><span data-stu-id="5c612-109">The purpose of this documentation is:</span></span>

- <span data-ttu-id="5c612-110">Kurze Einführung in Machine Learning-Tools (in Q\# geschrieben) für Machine Learning-Hybridvorgänge mit Quantencomputing und klassischem Computing</span><span class="sxs-lookup"><span data-stu-id="5c612-110">A concise introduction to machine learning tools (written in Q\#) for hybrid quantum/classical learning.</span></span>
- <span data-ttu-id="5c612-111">Einführung in Machine Learning-Konzepte mit dem Schwerpunkt auf deren Realisierung in Klassifizierern für Quantenschaltungen (auch als sequenzielle Klassifizierer für Quantencomputing bezeichnet)</span><span class="sxs-lookup"><span data-stu-id="5c612-111">Introduce machine learning concepts and specifically their realization in quantum circuit centric classifiers (also known as quantum sequential classifiers).</span></span>
- <span data-ttu-id="5c612-112">Bereitstellung von Tutorials zu den Grundlagen für den Einstieg in die Nutzung der Bibliothekstools</span><span class="sxs-lookup"><span data-stu-id="5c612-112">Provide a set of tutorials on the basics to start using the tools provided by the library.</span></span>
- <span data-ttu-id="5c612-113">Beschreibung der Trainings- und Validierungsmethoden für diese Klassifizierer und deren Übersetzung in spezifische Q\#-Vorgänge der Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5c612-113">Discuss the training and validation methods for such classifiers and how they translate into specific Q\# operations provided by the library.</span></span>

<span data-ttu-id="5c612-114">Das in dieser Bibliothek implementierte Modell basiert auf dem Trainingsschema für Quantencomputing und klassisches Computing aus dem Artikel zu [Quantenklassifizierern für Schaltungen](https://arxiv.org/abs/1804.00633).</span><span class="sxs-lookup"><span data-stu-id="5c612-114">The model implemented in this library is based on the quantum-classical training scheme presented in [Circuit-centric quantum classifiers](https://arxiv.org/abs/1804.00633)</span></span>
