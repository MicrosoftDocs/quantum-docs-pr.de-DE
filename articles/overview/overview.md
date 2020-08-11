---
title: Einführung in Quantencomputing
description: Es wird beschrieben, was Quantencomputing ist, was Quantencomputer leisten können und wie Sie das Quantencomputing erlernen können.
author: bradben
ms.author: bradben
ms.date: 05/05/2020
ms.topic: overview
uid: microsoft.quantum.overview.introduction
no-loc:
- Q#
- $$v
ms.openlocfilehash: 59cb595ac207d6e84358fc6ba742e0e0019c76f9
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87866977"
---
# <a name="introduction-to-quantum-computing-and-the-quantum-development-kit"></a>Einführung in Quantencomputing und in das Quantum Development Kit

Beim Microsoft Quantum Development Kit (QDK) handelt es sich um eine Reihe von Open-Source-Tools, die Entwicklern dabei helfen sollen, sich mit Quantenalgorithmen vertraut zu machen und Quantenprogramme zu schreiben. Quantencomputing verspricht, einige der größten Herausforderungen unseres Planeten in Bereichen wie Umweltschutz, Landwirtschaft, Gesundheitswesen, Energie, Klima und Materialwissenschaft sowie in anderen, bislang noch unbekannten Bereichen zu lösen.  

Bei einigen dieser Probleme stoßen selbst unsere leistungsstärksten Computer an ihre Grenzen. Die Quantentechnologie steht noch ziemlich am Anfang ihrer Entwicklung und hat das Potenzial, unser Verständnis von Computing fundamental zu verändern.

## <a name="what-is-quantum-computing"></a>Was ist Quantencomputing?

Im modernen Sprachgebrauch bedeutet „Quant“ die kleinstmögliche diskrete Einheit einer beliebigen physischen Eigenschaft und bezieht sich in der Regel auf Eigenschaften atomarer oder subatomarer Teilchen. Quantencomputer verwenden echte Quantenteilchen, künstliche Atome oder kollektive Eigenschaften von Quantenteilchen als Verarbeitungseinheiten und sind groß, komplex und teuer.

Sie machen sich das einzigartige Verhalten der Quantenphysik zunutze und übertragen es auf das Computing, wodurch herkömmliche Programmiermethoden um neue Konzepte erweitert und Phänomene der Quantenphysik wie Superposition, Verschränkung und Quanteninterferenz genutzt werden können.

## <a name="what-can-a-quantum-computer-do"></a>Was kann ein Quantencomputer?

Ein Quantencomputer ist kein Supercomputer, der alle Aufgaben schneller bewältigt. Es gibt jedoch einige Bereiche, für die Quantencomputer besonders gut geeignet sind:

- [Quantensimulation](xref:microsoft.quantum.overview.introduction#quantum-simulation)
- [Kryptografie](xref:microsoft.quantum.overview.introduction#cryptography-and-shors-algorithm)
- [Suche](xref:microsoft.quantum.overview.introduction#search-and-grovers-algorithm)
- [Optimierung](xref:microsoft.quantum.overview.introduction#quantum-inspired-computing-and-optimization)
- [Maschinelles Lernen](xref:microsoft.quantum.overview.introduction#quantum-machine-learning)

## <a name="quantum-simulation"></a>Quantensimulation

Da die Berechnungen von Quantencomputern auf Quantenphänomenen basieren, eignen sie sich gut für die Modellierung anderer Quantensysteme. Fotosynthese, Supraleitfähigkeit und komplexe molekulare Gebilde sind Beispiele für Aspekte der Quantenmechanik, die von Quantenprogrammen simuliert werden können.

## <a name="cryptography-and-shors-algorithm"></a>Kryptografie und Shor-Algorithmus

1994 zeigte Peter Shor, dass es mit einem skalierbaren Quantencomputer möglich ist, gängige Verschlüsselungstechniken wie etwa den RSA-Algorithmus zu knacken. Die klassische Kryptografie basiert auf der Schwierigkeit von Problemen, etwa bei der Primfaktorzerlegung oder bei diskreten Logarithmen. Viele dieser Probleme lassen sich jedoch mit Quantencomputern effizienter lösen.

## <a name="search-and-grovers-algorithm"></a>Suche und Grover-Algorithmus

1996 entwickelte Lov Grover einen Quantenalgorithmus, der Suchvorgänge für unstrukturierte Daten drastisch beschleunigte. Hierzu wird die Suche mit weniger Schritten ausgeführt, als dies bei einem klassischen Algorithmus möglich wäre.

## <a name="quantum-inspired-computing-and-optimization"></a>Von Quanten inspiriertes Computing und Optimierung

Von Quanten inspirierte Algorithmen machen sich Quantenprinzipien zunutze, um eine höhere Geschwindigkeit und Genauigkeit zu erreichen, werden aber auf klassischen Computersystemen implementiert. Dieser Ansatz ermöglicht es Entwicklern, schon heute von der Leistungsfähigkeit neuer Quantentechniken zu profitieren, ohne auf Quantenhardware warten zu müssen, da sich die entsprechende Branche noch im Aufbau befindet.

Optimierung ist die Suche nach der besten Lösung für ein Problem unter Berücksichtigung des gewünschten Ergebnisses und der geltenden Einschränkungen. Wichtige Entscheidungen in Industrie und Wissenschaft werden immer auf der Grundlage von Faktoren wie Kosten, Qualität oder Produktionszeit getroffen. Mit von Quanten inspirierten Optimierungsalgorithmen, die auf aktuellen klassischen Computern ausgeführt werden, können Lösungen gefunden werden, die bislang nicht möglich waren. Anwendungsbeispiele wären etwa die Verkehrsflussoptimierung zur Vermeidung von Staus sowie die Gatezuweisung im Luftverkehr, die Paketzustellung, die Auftragsplanung und vieles mehr. Durchbrüche in der Materialwissenschaft führen zu neuen Energieformen, zu Akkus mit höherer Kapazität sowie zu leichteren und länger haltbaren Materialien.

> [!NOTE]
> Informieren Sie sich ausführlicher darüber, wie das von Quanten inspirierte Computing von Microsoft in der [Materialwissenschaft](https://cloudblogs.microsoft.com/quantum/2020/01/21/oti-lumionics-accelerating-materials-design-microsoft-azure-quantum/), beim [Risikomanagement](https://cloudblogs.microsoft.com/quantum/2019/05/22/microsoft-quantum-collaborates-with-willis-towers-watson-to-transform-risk-management-solutions/) und in der [Medizin](https://blogs.microsoft.com/blog/2018/05/18/microsoft-quantum-helps-case-western-reserve-university-advance-mri-research/) genutzt wird.

## <a name="quantum-machine-learning"></a>Quantenbasiertes maschinelles Lernen

Maschinelles Lernen auf klassischen Computern revolutioniert die Welt der Wissenschaft und die Geschäftswelt. Der hohe Rechenaufwand für das Trainieren der Modelle behindert jedoch die Entwicklung und die Anwendungsmöglichkeiten auf diesem Gebiet. Beim quantenbasierten maschinellen Lernen geht es um die Entwicklung und Implementierung von Quantensoftware zur Beschleunigung des maschinellen Lernens (verglichen mit klassischen Computern).

Das Quantum Development Kit enthält die [Quantum Machine Learning-Bibliothek](xref:microsoft.quantum.machine-learning.concepts.intro), mit der Sie Machine Learning-Hybridexperimente durchführen können, bei denen sowohl Quantencomputing als auch klassisches Computing genutzt wird. Die Bibliothek enthält Beispiele und Tutorials und stellt die erforderlichen Tools bereit, um einen neuen Hybridalgorithmus mit einer Kombination aus Quantencomputing und klassischem Computing – den Quantenklassifizierer für Schaltungen – zu implementieren, um Probleme im Zusammenhang mit der überwachten Klassifizierung zu lösen.

## <a name="no-locq-and-the-microsoft-quantum-development-kit-qdk"></a>Q# und das Microsoft Quantum Development Kit (QDK)

Q# ist die Open-Source-Programmiersprache von Microsoft für die Entwicklung und Ausführung von Quantenalgorithmen. Sie ist im [QDK](https://docs.microsoft.com/quantum/) enthalten. Dabei handelt es sich um ein umfassendes Entwicklungskit für Q#, das mit Standardtools und -sprachen verwendet werden kann, um Quantenanwendungen zu entwickeln, die Sie in verschiedenen Umgebungen ausführen können – unter anderem im integrierten Quantensimulator für den vollständigen Zustand.

Es gibt Erweiterungen für Visual Studio und VS Code sowie Pakete für Python und Jupyter Notebook.

Das QDK enthält eine Standardbibliothek sowie spezielle Bibliotheken für Chemie, maschinelles Lernen und numerische Werte.

Die Dokumentation beinhaltet einen Leitfaden, Tutorials und Beispielcode für Q#, um einen schnellen Einstieg zu ermöglichen, aber auch umfassende Artikel, die Ihnen dabei helfen, sich ausführlicher mit den Konzepten des Quantencomputings auseinanderzusetzen.  

## <a name="microsoft-quantum-hardware-partners"></a>Microsoft-Partner für Quantenhardware

Microsoft arbeitet mit Unternehmen im Bereich der Quantenhardware zusammen, um Entwicklern Cloudzugriff auf Quantenhardware zu ermöglichen. Mithilfe der [Azure Quantum-Plattform](https://azure.microsoft.com/services/quantum/) und der Sprache Q# können sich Entwickler mit Quantenalgorithmen beschäftigen und ihre Quantenprogramme auf verschiedenen Arten von Quantenhardware ausführen.

[IonQ](https://ionq.com/news/november-4-2019-microsoft-partnership) und [Honeywell](https://www.honeywell.com/en-us/newsroom/news/2019/11/the-future-of-quantum-computing) arbeiten jeweils mit **Ionenfallen-basierten** Prozessoren, bei denen einzelne, in einem elektrischen Feld gefangene Ionen genutzt werden. [QCI](https://quantumcircuits.com/news-and-publications/quantum-circuits-partners-with-microsoft-on-azure-quantum) arbeitet dagegen mit supraleitenden Schaltkreisen.

## <a name="next-steps"></a>Nächste Schritte

[Grundlegendes zu Quantencomputing](xref:microsoft.quantum.overview.understanding)
[Erste Schritte mit dem Quantum Development Kit](xref:microsoft.quantum.welcome)