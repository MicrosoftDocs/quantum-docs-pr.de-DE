---
title: Beispiele für Quantenanwendungen im Bereich der Chemie
description: Erkunden Sie die Beispielanwendungen, die in der Microsoft-Quantenchemiebibliothek enthalten sind.
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples
ms.openlocfilehash: 5168fc8592d34a32ba67e5a0c4793aa17599fd35
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2020
ms.locfileid: "77906490"
---
# <a name="quantum-chemistry-examples"></a>Beispiele der Quantenchemie

In Konzepten der Quantenchemie wurden Beispiele für Fermion-Hamiltonoperator manuell konstruiert. Nun werden die Chemiesimulationsalgorithmen, die unter [Simulieren von hamiltonschen Dynamiken](xref:microsoft.quantum.libraries.standard.algorithms) beschrieben werden, mit der [Quantenphasenschätzung](xref:microsoft.quantum.libraries.characterization) in der kanonischen Bibliothek kombiniert. Diese Kombination ermöglicht Schätzungen des Energieniveaus im dargestellten Molekül. Dies ist einer der wichtigsten Anwendungsfälle von Quantenchemie in einem Quantencomputer. 

Anstatt die Regeln zu Hamiltonoperatoren einzeln aufzuführen, arbeiten Sie sich durch Beispiele, die die Durchführung von Quantenchemieexperimenten nach Maß ermöglichen. Sie Beginnen mit Beispielen, in denen ein chemischer Hamiltonoperator geladen wird, der im [Broombridge-Schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) verschlüsselt ist.

Mit Molekülen, die für die Simulation im [Simulator für vollständige Zustände](xref:microsoft.quantum.machines.full-state-simulator) zu groß sind, kann dennoch interessante Wissenschaft durchgeführt werden. Beispielsweise können die Ressourcenkosten zum Durchführen umfassender Chemiesimulationen immer noch mithilfe des [Ablaufverfolgungssimulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro) ausgewertet werden.

Als Nächstes werden einige interessante Anwendungsfälle der Chemiesimulationsbibliothek mithilfe einiger Beispiele veranschaulicht.
