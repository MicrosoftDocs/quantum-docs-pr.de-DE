---
title: Microsoft Quantum-Numerics-Bibliothek-Installation und Validierung
description: Erfahren Sie, wie Sie die Microsoft Quantum-Numerics-Bibliothek zu Ihrer Installation von Visual Studio 2019 oder höher hinzufügen.
author: thomashaener
ms.author: thhaner
ms.date: 05/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.installation
ms.openlocfilehash: cb0d00a509b3986b605dd7f15f9bccc0661bb894
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906337"
---
# <a name="numerics-library-installation-and-validation"></a>Installation und Validierung der Numerics-Bibliothek

Das Quantum Development Kit bietet Unterstützung für die Numerics-Funktionalität durch das [`Microsoft.Quantum.Numerics`](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) nuget-Paket.

**Visual Studio > = 2019:** Wenn Sie Visual Studio 2019 oder höher verwenden, können Sie das Numerics-Paket mit dem nuget-Paket-Manager hinzufügen.
Wählen Sie hierzu "nuget-Pakete verwalten..." aus. aus dem Menü Element "Projekt" in Visual Studio.

Suchen Sie auf der Registerkarte Durchsuchen nach dem Paketnamen "Microsoft. Quantum. Numerics".

> [!NOTE]
> Stellen Sie sicher, dass Sie "incluelease einschließen" aktivieren.

Dadurch werden die Pakete aufgelistet, die zum Herunterladen zur Verfügung stehen.
Wenn Sie mit dem Mauszeiger auf "Microsoft. Quantum. Numerics" zeigen, wird rechts neben der Versionsnummer ein nach unten zeigender Pfeil angezeigt.
Klicken Sie auf den Pfeil, um das Numerics-Paket zu installieren.

Weitere Informationen finden Sie im Leitfaden für die [Benutzeroberfläche des Paket-Managers](https://docs.microsoft.com/nuget/tools/package-manager-ui).

Alternativ können Sie die Numerics-Bibliothek mithilfe der Paket-Manager-Konsole über die Befehlszeilenschnittstelle dem Projekt hinzufügen.

![Verwenden der Paket-Manager-Konsole über die Befehlszeile](../../media/vs2017-nuget-console-menu.png)

Führen Sie in der Paket-Manager-Konsole Folgendes aus:

```
Install-Package Microsoft.Quantum.Numerics
```

Weitere Informationen finden Sie im Handbuch für die [Paket-Manager-Konsole](https://docs.microsoft.com/nuget/tools/package-manager-console).

**Befehlszeile oder Visual Studio Code:** Mithilfe der Befehlszeile eigenständig oder innerhalb Visual Studio Code können Sie den `dotnet`-Befehl verwenden, um dem Projekt einen nuget-Paket Verweis hinzuzufügen:

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```


## <a name="verifying-your-installation"></a>Überprüfen der Installation

Wie das restliche Quantum Development Kit enthält die Numerics-Bibliothek Beispiele, mit deren Hilfe Sie so schnell wie möglich loslegen können.
Zum Testen Ihrer Installation mithilfe dieser Beispiele Klonen Sie das [hauptbeispielrepository](https://github.com/Microsoft/Quantum) , und führen Sie dann eines der Beispiele aus.

So führen Sie das [`CustomModAdd`](https://github.com/microsoft/Quantum/tree/master/samples/numerics/CustomModAdd) Beispiel aus:

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/numerics/CustomModAdd
dotnet run
```
