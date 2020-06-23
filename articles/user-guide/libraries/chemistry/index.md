---
title: Einführung in die Quantum Chemistry Library (Quantenchemiebibliothek)
description: Es wird beschrieben, was die Microsoft-Quantenchemiebibliothek ist und wie sie genutzt wird, um auf Quantencomputern elektronische Strukturprobleme zu simulieren.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.intro
ms.openlocfilehash: 4268eafa5e53c0a026d179503ac6db88652a8f90
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85273427"
---
# <a name="introduction-to-the-quantum-chemistry-library"></a>Einführung in die Quantum Chemistry Library (Quantenchemiebibliothek)

Die Simulation physischer Systeme spielt beim Quantencomputing seit Langem eine zentrale Rolle.  Der Grund hierfür ist die weit verbreitete Ansicht, dass Quantendynamiken auf Quantencomputern nicht simuliert werden können. Das bedeutet, dass die Komplexität der Simulation des Systems exponentiell mit der Größe des betreffenden Quantensystems steigt.  Das Simulieren von Problemen in der Chemie und der Materialwissenschaft bleibt vielleicht einer der interessantesten Anwendungsbereiche des Quantencomputings und würde das Testen chemischer Reaktionsmechanismen ermöglichen, die bisher nicht gemessen oder simuliert werden konnten.  Außerdem könnten korrelierte elektronische Materialien wie Hochtemperatursupraleiter simuliert werden. Die Liste der Anwendungsbereiche ist lang.

Der Zweck dieser Dokumentation ist es, eine kurze Einführung in die Simulation elektronischer Strukturprobleme auf Quantencomputern bereitzustellen, um dem Leser die Rolle der vielen Aspekte der Hamilton-Simulationsbibliothek näher zu bringen.  Wir beginnen mit einer kurzen Einführung in die Quantenmechanik und erläutern dann, wie elektronische Systeme darin modelliert werden.  Anschließend wird erläutert, wie diese Quantendynamiken mithilfe eines Quantencomputers emuliert werden können.  Danach werden zwei Methoden vorgestellt, die zum Kompilieren der Quantendynamiken in Sequenzen von elementaren Gates verwendet werden: Trotter-Suzuki-Dekompositionen und Qubits.
