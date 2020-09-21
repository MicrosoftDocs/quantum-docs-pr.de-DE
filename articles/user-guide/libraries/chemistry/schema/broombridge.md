---
title: Broombridge-Quantum-Chemie Schema
description: Übersicht über das broombridge-Quantum-Chemie Schema, das verwendet wird, um reale Chemie Probleme mit dem Microsoft Quantum Development Kit zu modellieren.
author: martinro
ms.author: martinro
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.broombridge
no-loc:
- Q#
- $$v
ms.openlocfilehash: e580fd8267cc7ba30533d557eceb486f8c205be6
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835773"
---
# <a name="broombridge-quantum-chemistry-schema"></a>Broombridge-Quantum-Chemie Schema # 

Leistungsfähige Software für die Rechen Software, wie z. b. [nwchem](http://www.nwchem-sw.org/) , bietet Ihnen die Möglichkeit, eine Vielzahl von Problemen in der Praxis zu modellieren. Verwenden Sie ein [YAML](https://en.wikipedia.org/wiki/YAML)-basiertes Schema mit dem Namen " **broombridge**", um mit der Microsoft Quantum Chemistry-Bibliothek auf nwchem-Molekulare Modelle zuzugreifen. Der Name wurde als Verweis auf ein [Wahrzeichen](https://en.wikipedia.org/wiki/Broom_Bridge) ausgewählt, das in manchen Kreisen als Geburtsort von hamiltonane gefeiert wird. 

[Nwchem](https://github.com/nwchemgit/nwchem) ist ein Open Source-Projekt, das unter der Lizenz für die Lizenz für Bildungseinrichtungen (License Community License, ECL) 2,0 lizenziert ist. Das [broombridge-Quantum-Schema](https://docs.microsoft.com/quantum/libraries/chemistry/schema/spec_v_0_2)ist ein Open-Source-Schema, das eine [Definition](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/broombridge-0.1.schema.json) in [RFC 2119](https://tools.ietf.org/html/rfc2119) und ein Validierungs Steuerelement [Skript](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/validator.py) enthält, das unter der mit-Lizenz lizenziert ist. 

Als YAML-basiert ist broombridge eine strukturierte, lesbare und menschlich bearbeitbare Methode zur Darstellung elektronischer Strukturprobleme. Insbesondere können die folgenden Daten dargestellt werden:
- Fermionische hamiltonane können mit einem-und zwei-Elektronen-inteden dargestellt werden.
- Die Zustände "Ground" und "aufgeregt" können mithilfe von Erstellungs Sequenzen dargestellt
- Obere und untere Grenzen der Energie Stufen können angegeben werden.

Daten können aus nwchem mithilfe verschiedener Methoden generiert werden, z. b. durch die Verwendung einer vollständigen Installation von nwchem zum Ausführen von Grafikkarten (z. b. die in der [nwchem-Bibliothek](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests) bereitgestellten Daten, die broombridge als Teil des Testlaufs ausgeben) oder eines docker-Images von nwchem, das auch zum Generieren von broombridge aus Um schnell mit der Rechen Chemie zu beginnen, ohne jegliche chemische Software installieren zu müssen, können Sie die visuelle Benutzeroberfläche für nwchem verwenden, die von [EMSL-Pfeilen](https://arrows.emsl.pnnl.gov/api/qsharp_chem)bereitgestellt wird.

Auf hoher Ebene kann das Zusammenwirken zwischen nwchem und dem Microsoft Quantum Development Kit wie folgt visualisiert werden: ![ ](~/media/broombridge.png) das blaue schattierte Feld stellt das broombridge-Schema dar. die verschiedenen grauen schattierten Felder stellen andere interne Daten Darstellungen dar, die für die Darstellung und Verarbeitung von Quantum-Algorithmen für die computingressource basierend auf realen Chemie Problemen ausgewählt wurden.

Der Ordner " [Integral/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) " im Quantum Development Kit-beispielrepository enthält mehrere mithilfe des broombridge-Schemas definierte chemische Darstellungen.
