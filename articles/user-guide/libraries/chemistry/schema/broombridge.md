---
title: Broombridge-Quantum-Chemie Schema
description: Übersicht über das broombridge-Quantum-Chemie Schema, das verwendet wird, um reale Chemie Probleme mit dem Microsoft Quantum Development Kit zu modellieren.
author: martinro
ms.author: martinro@microsoft.com
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.broombridge
ms.openlocfilehash: 708c4277080c358cb35a49fbf1dde0394d331043
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275078"
---
# <a name="broombridge-quantum-chemistry-schema"></a><span data-ttu-id="74f79-103">Broombridge-Quantum-Chemie Schema</span><span class="sxs-lookup"><span data-stu-id="74f79-103">Broombridge Quantum Chemistry Schema</span></span> # 

<span data-ttu-id="74f79-104">Leistungsfähige Software für die Rechen Software, wie z. b. [nwchem](http://www.nwchem-sw.org/) , bietet Ihnen die Möglichkeit, eine Vielzahl von Problemen in der Praxis zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="74f79-104">Powerful computational chemistry software such as [NWChem](http://www.nwchem-sw.org/) allows you to model a wide range of real-world chemistry problems.</span></span> <span data-ttu-id="74f79-105">Verwenden Sie ein [YAML](https://en.wikipedia.org/wiki/YAML)-basiertes Schema mit dem Namen " **broombridge**", um mit der Microsoft Quantum Chemistry-Bibliothek auf nwchem-Molekulare Modelle zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="74f79-105">In order to access NWChem molecular models with the Microsoft Quantum Chemistry library, you use a [YAML](https://en.wikipedia.org/wiki/YAML)-based schema named **Broombridge**.</span></span> <span data-ttu-id="74f79-106">Der Name wurde als Verweis auf ein [Wahrzeichen](https://en.wikipedia.org/wiki/Broom_Bridge) ausgewählt, das in manchen Kreisen als Geburtsort von hamiltonane gefeiert wird.</span><span class="sxs-lookup"><span data-stu-id="74f79-106">The name was chosen in reference to a [landmark](https://en.wikipedia.org/wiki/Broom_Bridge) which in some circles is celebrated as a birthplace of Hamiltonians.</span></span> 

<span data-ttu-id="74f79-107">[Nwchem](https://github.com/nwchemgit/nwchem) ist ein Open Source-Projekt, das unter der Lizenz für die Lizenz für Bildungseinrichtungen (License Community License, ECL) 2,0 lizenziert ist.</span><span class="sxs-lookup"><span data-stu-id="74f79-107">[NWChem](https://github.com/nwchemgit/nwchem) is an Open Source project licensed under the permissive Educational Community License (ECL) 2.0 license.</span></span> <span data-ttu-id="74f79-108">Das [broombridge-Quantum-Schema](https://docs.microsoft.com/quantum/libraries/chemistry/schema/spec_v_0_2)ist ein Open-Source-Schema, das eine [Definition](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/broombridge-0.1.schema.json) in [RFC 2119](https://tools.ietf.org/html/rfc2119) und ein Validierungs Steuerelement [Skript](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/validator.py) enthält, das unter der mit-Lizenz lizenziert ist.</span><span class="sxs-lookup"><span data-stu-id="74f79-108">The [Broombridge Quantum Chemistry Schema](https://docs.microsoft.com/quantum/libraries/chemistry/schema/spec_v_0_2)) is an Open Source schema that includes a [definition](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/broombridge-0.1.schema.json) following [RFC 2119](https://tools.ietf.org/html/rfc2119) and a [validator script](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/validator.py) licensed under the MIT license.</span></span> 

<span data-ttu-id="74f79-109">Als YAML-basiert ist broombridge eine strukturierte, lesbare und menschlich bearbeitbare Methode zur Darstellung elektronischer Strukturprobleme.</span><span class="sxs-lookup"><span data-stu-id="74f79-109">Being YAML-based, Broombridge is a structured, human-readable and human-editable way of representing electronic structure problems.</span></span> <span data-ttu-id="74f79-110">Insbesondere können die folgenden Daten dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="74f79-110">In particular, the following data can be represented:</span></span>
- <span data-ttu-id="74f79-111">Fermionische hamiltonane können mit einem-und zwei-Elektronen-inteden dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="74f79-111">Fermionic Hamiltonians can be represented using one- and two-electron integrals.</span></span>
- <span data-ttu-id="74f79-112">Die Zustände "Ground" und "aufgeregt" können mithilfe von Erstellungs Sequenzen dargestellt</span><span class="sxs-lookup"><span data-stu-id="74f79-112">Ground and excited states can be presented using creation sequences.</span></span>
- <span data-ttu-id="74f79-113">Obere und untere Grenzen der Energie Stufen können angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="74f79-113">Upper and lower bounds of energy levels can be specified.</span></span>

<span data-ttu-id="74f79-114">Daten können aus nwchem mithilfe verschiedener Methoden generiert werden, z. b. durch die Verwendung einer vollständigen Installation von nwchem zum Ausführen von Grafikkarten (z. b. die in der [nwchem-Bibliothek](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests) bereitgestellten Daten, die broombridge als Teil des Testlaufs ausgeben) oder eines docker-Images von nwchem, das auch zum Generieren von broombridge aus</span><span class="sxs-lookup"><span data-stu-id="74f79-114">Data can be generated from NWChem using various methods, such as using a full installation of NWChem to run chemistry decks (for example the ones provided in the [NWChem library](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests) that output Broombridge as part of the run), or a docker image of NWChem which can also be used to generate Broombridge from chemistry decks.</span></span> <span data-ttu-id="74f79-115">Um schnell mit der Rechen Chemie zu beginnen, ohne jegliche chemische Software installieren zu müssen, können Sie die visuelle Benutzeroberfläche für nwchem verwenden, die von [EMSL-Pfeilen](https://arrows.emsl.pnnl.gov/api/qsharp_chem)bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="74f79-115">To get started with computational chemistry quickly without having to install any chemistry software, you can use the visual interface to NWChem provided by [EMSL Arrows](https://arrows.emsl.pnnl.gov/api/qsharp_chem).</span></span>

<span data-ttu-id="74f79-116">Auf hoher Ebene kann das Zusammenwirken zwischen nwchem und dem Microsoft Quantum Development Kit wie folgt visualisiert werden: ![ ](~/media/broombridge.png) das blaue schattierte Feld stellt das broombridge-Schema dar. die verschiedenen grauen schattierten Felder stellen andere interne Daten Darstellungen dar, die für die Darstellung und Verarbeitung von Quantum-Algorithmen für die computingressource basierend auf realen Chemie Problemen ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="74f79-116">At a high level, the interplay between NWChem and the Microsoft Quantum Development Kit can be visualized as follows: ![Chemistry stack](~/media/broombridge.png) The blue shaded box represents the Broombridge schema, the various grey shaded boxes represent other internal data representations that were chosen to represent and process quantum algorithms for computational chemistry based on real-world chemistry problems.</span></span>

<span data-ttu-id="74f79-117">Der Ordner " [Integral/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) " im Quantum Development Kit-beispielrepository enthält mehrere mithilfe des broombridge-Schemas definierte chemische Darstellungen.</span><span class="sxs-lookup"><span data-stu-id="74f79-117">The [Integral/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) folder in the Quantum Development Kit Samples repository contains multiple chemical representations defined using the Broombridge schema.</span></span>