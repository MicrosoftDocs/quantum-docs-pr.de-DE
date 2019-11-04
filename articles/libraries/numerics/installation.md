---
title: Installation und Validierung der Numerics-Bibliothek | Microsoft-Dokumentation
description: Installation und Validierung der Numerics-Bibliothek
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.installation
ms.openlocfilehash: 8369a6f342ee8e6f56b69bd1f2ce3df40e4093aa
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184626"
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

![](~/media/vs2017-nuget-console-menu.png)

Führen Sie in der Paket-Manager-Konsole Folgendes aus:

```
Install-Package Microsoft.Quantum.Numerics
```

Weitere Informationen finden Sie im Handbuch für die [Paket-Manager-Konsole](https://docs.microsoft.com/nuget/tools/package-manager-console).

**Befehlszeile oder Visual Studio Code:** Mithilfe der Befehlszeile eigenständig oder innerhalb Visual Studio Code können Sie den `dotnet`-Befehl verwenden, um dem Projekt einen nuget-Paket Verweis hinzuzufügen:

```bash
dotnet add package Microsoft.Quantum.Numerics
```


## <a name="verifying-your-installation"></a>Überprüfen der Installation

Wie das restliche Quantum Development Kit enthält die Numerics-Bibliothek Beispiele, mit deren Hilfe Sie so schnell wie möglich loslegen können.
Zum Testen Ihrer Installation mithilfe dieser Beispiele Klonen Sie das [hauptbeispielrepository](https://github.com/Microsoft/Quantum) , und führen Sie dann eines der Beispiele aus.

So führen Sie das [`CustomModAdd`](https://github.com/microsoft/Quantum/tree/master/Numerics/CustomModAdd) Beispiel aus:

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/Numerics/CustomModAdd
dotnet run
```