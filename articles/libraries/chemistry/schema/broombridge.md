---
title: Broombridge-Quantum-Chemie Schema
description: Übersicht über das broombridge-Quantum-Chemie Schema, das verwendet wird, um reale Chemie Probleme mit dem Microsoft Quantum Development Kit zu modellieren.
author: martinro
ms.author: martinro@microsoft.com
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.broombridge
ms.openlocfilehash: a746b63055bb1b2c1168b89993a7459ca9597f86
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907816"
---
# <a name="broombridge-quantum-chemistry-schema"></a>Broombridge-Quantum-Chemie Schema # 

Leistungsstarke Rechen Software, wie z. b. [nwchem](http://www.nwchem-sw.org/) , bietet die Möglichkeit, eine große Bandbreite an realen Chemie-Problemen zu modellieren. Wir verwenden ein [YAML](https://en.wikipedia.org/wiki/YAML)-basiertes Schema, das als **broombridge**bezeichnet wird, um mit der Microsoft Quantum Chemistry-Bibliothek auf die Molekular Modelle von nwchem zuzugreifen. Der Name wurde als Verweis auf ein [Wahrzeichen](https://en.wikipedia.org/wiki/Broom_Bridge) ausgewählt, das in manchen Kreisen als Geburtsort von hamiltonane gefeiert wird. 

[Nwchem](https://github.com/nwchemgit/nwchem) ist ein Open Source-Projekt, das unter der Lizenz für die Lizenz für Bildungseinrichtungen (License Community License, ECL) 2,0 lizenziert ist. Broombridge ist ein Open-Source-Schema, das [hier](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) angegeben wird und eine [Definition](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/broombridge-0.1.schema.json) enthält, nach der [RFC 2119](https://tools.ietf.org/html/rfc2119) und das Validierungs Steuerelement [Skript](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/validator.py) gemäß der mit-Lizenz lizenziert sind. 

Als YAML-basiert ist broombridge eine strukturierte, lesbare und menschlich bearbeitbare Methode zur Darstellung elektronischer Strukturprobleme. Insbesondere können die folgenden Daten dargestellt werden: 
- Fermionische hamiltonane können mit einem-und zwei-Elektronen-inteden dargestellt werden. 
- Die Zustände "Ground" und "aufgeregt" können mithilfe von Erstellungs Sequenzen dargestellt
- Obere und untere Grenzen der Energie Stufen können angegeben werden.

Das Datenformat kann aus nwchem mühelos generiert werden: Es gibt eine Vielzahl von Methoden, die von einer vollständigen nwchem-Installation bis hin zum Ausführen von Grafikkarten, wie z. b. den [hier](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests) bereitgestellten und Ausgabe broombridge, als Teil des Testlaufs, über ein docker-Image von nwchem reichen, das auch zum Generieren von broombridge aus dem Zum Schluss wird eine visuelle Methode zum schnellen Einstieg in die Rechen Chemie ohne die Installation von Chemie Software über die [EMSL-Pfeile](https://arrows.emsl.pnnl.gov/api/qsharp_chem) -Schnittstelle für nwchem bereitgestellt. 

Auf hoher Ebene kann das Zusammenwirken zwischen nwchem und dem Microsoft Quantum Development Kit wie folgt visualisiert werden: ![Chemie-Stapel](~/media/broombridge.png) das blaue schattierte Feld das broombridge-Schema darstellt, stellen die verschiedenen grauen schattierten Felder andere interne Daten Darstellungen dar, die zur Darstellung und Verarbeitung von Quantum-Algorithmen für die computingressource basierend auf realen Chemie-Problemen ausgewählt wurden. 

[Hier](https://github.com/microsoft/Quantum/tree/master/Chemistry/IntegralData/YAML)werden mehrere mithilfe des broombridge-Schemas definierte chemische Darstellungen bereitgestellt.
