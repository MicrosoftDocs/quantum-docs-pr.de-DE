---
title: Aktualisieren des Quantum Development Kit (QDK)
description: Es wird beschrieben, wie Sie Ihre Q#-Projekte und das Microsoft Quantum Development Kit auf die aktuelle Version aktualisieren.
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 457083ea4756d64375834e5a276c2d91031138fe
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2020
ms.locfileid: "85885141"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Aktualisieren des Microsoft Quantum Development Kit (QDK)

Es wird beschrieben, wie Sie das Microsoft Quantum Development Kit (QDK) auf die aktuelle Version aktualisieren.

In diesem Artikel wird vorausgesetzt, dass Sie das QDK bereits installiert haben. Bei der erstmaligen Installation hilft Ihnen das [Installationshandbuch](xref:microsoft.quantum.install) weiter.

Wir empfehlen Ihnen, immer das neueste QDK-Release zu verwenden. Befolgen Sie diesen Aktualisierungsleitfaden, um das Upgrade auf die aktuelle QDK-Version durchzuführen. Der Prozess besteht aus zwei Teilen:
1. Aktualisieren Ihrer vorhandenen Q#-Dateien und -Projekte zur Ausrichtung Ihres Codes auf aktualisierte Syntax
2. Aktualisieren des eigentlichen QDK für die von Ihnen gewählte Entwicklungsumgebung

## <a name="updating-q-projects"></a>Aktualisieren von Q#-Projekten 

Unabhängig davon, ob Sie C# oder Python zum Hosten von Q#-Vorgängen nutzen, können Sie die unten angegebene Anleitung zum Aktualisieren Ihrer Q#-Projekte verwenden.

1. Überprüfen Sie zunächst, ob Sie die neueste Version des [.NET Core SDK 3.1](https://dotnet.microsoft.com/download) nutzen. Führen Sie an der Eingabeaufforderung den folgenden Befehl aus:

    ```dotnetcli
    dotnet --version
    ```

    Überprüfen Sie, ob `3.1.100` oder höher ausgegeben wird. Falls nicht, sollten Sie die [aktuelle Version](https://dotnet.microsoft.com/download) installieren und die Überprüfung dann erneut durchführen. Befolgen Sie anschließend unten die Anleitung je nach Ihrem Setup (Visual Studio, Visual Studio Code oder direkt über die Befehlszeile).

### <a name="update-q-projects-in-visual-studio"></a>Aktualisieren von Q#-Projekten in Visual Studio
 
1. Führen Sie ein Update auf die aktuelle Version von Visual Studio 2019 durch. Eine entsprechende Anleitung finden Sie [hier](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019).
2. Öffnen Sie Ihre Projektmappe in Visual Studio.
3. Wählen Sie im Menü die Option **Erstellen** -> **Projektmappe bereinigen** aus.
4. Aktualisieren Sie in Ihren CSPROJ-Dateien jeweils das Zielframework auf `netcoreapp3.1` (bzw. `netstandard2.1`, falls es sich um ein Bibliotheksprojekt handelt).
    Bearbeiten Sie hierfür Zeilen der folgenden Art:

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    Ausführlichere Informationen zum Angeben von Zielframeworks finden Sie [hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).

5. Legen Sie in allen CSPROJ-Dateien das SDK auf `Microsoft.Quantum.Sdk` fest (wie in der Zeile unten angegeben). Beachten Sie, dass die Versionsnummer der neuesten verfügbaren Version entsprechen sollte. Sie können dies ermitteln, indem Sie in den [Versionshinweisen](https://docs.microsoft.com/quantum/relnotes/) nachsehen.

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
    ```

6. Speichern und schließen Sie alle Dateien in Ihrer Projektmappe.

7. Wählen Sie **Extras** -> **Befehlszeile** -> **Developer-Eingabeaufforderung** aus. Alternativ können Sie auch die Paketverwaltungskonsole in Visual Studio verwenden.

8. Führen Sie für jedes Projekt der Projektmappe den folgenden Befehl aus, um dieses Paket zu **entfernen**:

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   Gehen Sie wie folgt vor, falls für Ihre Projekte noch andere Microsoft.Quantum- oder Microsoft.Azure.Quantum-Pakete (z. B. Microsoft.Quantum.Numerics) genutzt werden: Führen Sie den Befehl **add** für diese Pakete aus, um die genutzte Version zu aktualisieren.

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. Schließen Sie die Eingabeaufforderung, und wählen Sie **Erstellen** -> **Projektmappe erstellen** aus (*nicht* die Option „Projektmappe neu erstellen“).

Sie können nun zu [Aktualisieren Ihrer Visual Studio-QDK-Erweiterung](#update-visual-studio-qdk-extension) springen.


### <a name="update-q-projects-in-visual-studio-code"></a>Aktualisieren von Q#-Projekten in Visual Studio Code

1. Öffnen Sie in Visual Studio Code den Ordner, der das zu aktualisierende Projekt enthält.
2. Wählen Sie **Terminal** -> **Neues Terminal** aus.
3. Befolgen Sie die Anleitung für die Aktualisierung über die Befehlszeile (unten angegeben).

### <a name="update-q-projects-using-the-command-line"></a>Aktualisieren von Q#-Projekten über die Befehlszeile

1. Navigieren Sie zu dem Ordner, der Ihre Hauptprojektdatei enthält.

2. Führen Sie den folgenden Befehl aus:

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. Bestimmen Sie die aktuelle Version des QDK. Informationen hierzu finden Sie in den [Versionshinweisen](https://docs.microsoft.com/quantum/relnotes/). Die Versionsangabe hat in etwa das folgende Format: `0.11.2006.207`.

4. Führen Sie in Ihren `.csproj`-Dateien jeweils die folgenden Schritte aus:

    - Aktualisieren Sie das Zielframework auf `netcoreapp3.1` (bzw. `netstandard2.1`, falls es sich um ein Bibliotheksprojekt handelt). Bearbeiten Sie hierfür Zeilen der folgenden Art:

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        Ausführlichere Informationen zum Angeben von Zielframeworks finden Sie [hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).

    - Ersetzen Sie in der Projektdefinition den Verweis auf das SDK. Stellen Sie sicher, dass die Versionsnummer dem Wert entspricht, den Sie in **Schritt 3** ermittelt haben.

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
        ```

    - Entfernen Sie den Verweis auf das Paket `Microsoft.Quantum.Development.Kit` (falls vorhanden), der im folgenden Eintrag angegeben ist:

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - Aktualisieren Sie die Version aller Microsoft Quantum-Pakete auf die letzte veröffentlichte Version des QDK (in **Schritt 3** ermittelt). Für die Benennung dieser Pakete wird das folgende Muster genutzt:

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        Verweise auf Pakete haben das folgende Format:

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.11.2006.207" />
        ```

    - Speichern Sie die aktualisierte Datei.

    - Stellen Sie die Abhängigkeiten des Projekts wieder her, indem Sie wie folgt vorgehen:

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. Navigieren Sie zurück zum Ordner, der Ihr Hauptprojekt enthält, und führen Sie Folgendes aus:

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

Nachdem Ihre Q#-Projekte nun aktualisiert wurden, sollten Sie die Anleitung unten befolgen, um das eigentliche QDK zu aktualisieren.

## <a name="updating-the-qdk"></a>Aktualisieren des QDK

Der Prozess zur Aktualisierung des QDK variiert je nach Entwicklungssprache und -umgebung.
Wählen Sie unten Ihre Entwicklungsumgebung aus.

* [Python: Aktualisieren des `qsharp`-Pakets](#update-the-qsharp-python-package)
* [Jupyter Notebooks: Aktualisieren des IQ#-Kernels](#update-the-iq-jupyter-kernel)
* [Visual Studio: Aktualisieren der QDK-Erweiterung](#update-visual-studio-qdk-extension)
* [VS Code: Aktualisieren der QDK-Erweiterung](#update-vs-code-qdk-extension)
* [Befehlszeile und C# : Aktualisieren der Projektvorlagen](#c-using-the-dotnet-command-line-tool)


### <a name="update-the-qsharp-python-package"></a>Aktualisieren des `qsharp`-Python-Pakets

Die Aktualisierungsprozedur hängt davon ab, ob Sie ursprünglich mithilfe von Conda oder mithilfe der .NET-CLI und PIP installiert haben.

#### <a name="update-using-conda-recommended"></a>[Aktualisieren mithilfe von Conda (empfohlen)](#tab/tabid-conda)

1. Aktivieren Sie die Conda-Umgebung, in der Sie das `qsharp`-Paket installiert haben, und führen Sie dann den folgenden Befehl aus, um das Paket zu aktualisieren:

    ```
    conda update -c quantum-engineering qsharp
    ```

1. Führen Sie am Speicherort Ihrer `.qs`-Dateien den folgenden Befehl aus:

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

#### <a name="update-using-net-cli-and-pip-advanced"></a>[Aktualisieren mit der .NET-CLI und PIP (erweitert)](#tab/tabid-dotnetcli)

1. Aktualisieren Sie den `iqsharp`-Kernel. 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Überprüfen Sie die `iqsharp`-Version.

    ```dotnetcli
    dotnet iqsharp --version
    ```

    Die folgende Ausgabe wird angezeigt.

    ```
    iqsharp: 0.12.20070124
    Jupyter Core: 1.4.0.0
    ```

    Keine Sorge, wenn Ihre `iqsharp`-Version höher ist. Sie sollte mit dem [aktuellen Release](xref:microsoft.quantum.relnotes) identisch sein.

1. Aktualisieren des `qsharp`-Pakets:

    ```
    pip install qsharp --upgrade
    ```

1. Überprüfen der `qsharp`-Version:

    ```
    pip show qsharp
    ```

    Die folgende Ausgabe wird angezeigt.

    ```
    Name: qsharp
    Version: 0.12.20070124
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

1. Führen Sie am Speicherort Ihrer `.qs`-Dateien den folgenden Befehl aus:

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

***

Sie können jetzt das aktualisierte `qsharp`-Python-Paket verwenden, um Ihre vorhandenen Quantenprogramme auszuführen.

### <a name="update-the-iq-jupyter-kernel"></a>Aktualisieren des IQ#-Jupyter-Kernels

Die Aktualisierungsprozedur hängt davon ab, ob Sie ursprünglich mithilfe von Conda oder mithilfe der .NET-CLI und PIP installiert haben.

#### <a name="update-using-conda-recommended"></a>[Aktualisieren mithilfe von Conda (empfohlen)](#tab/tabid-conda)

1. Aktivieren Sie die Conda-Umgebung, in der Sie das `qsharp`-Paket installiert haben, und führen Sie dann den folgenden Befehl aus, um das Paket zu aktualisieren:

    ```
    conda update -c quantum-engineering qsharp
    ```

1. Führen Sie den folgenden Befehl in einer Zelle in allen Ihren vorhandenen Q#-Jupyter Notebooks aus:

    ```
    %workspace reload
    ```

#### <a name="update-using-net-cli-and-pip-advanced"></a>[Aktualisieren mit der .NET-CLI und PIP (erweitert)](#tab/tabid-dotnetcli)

1. Aktualisieren des `Microsoft.Quantum.IQSharp`-Pakets:

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Überprüfen der `iqsharp`-Version:

    ```dotnetcli
    dotnet iqsharp --version
    ```

    Die Ausgabe sollte in etwa wie folgt aussehen:

    ```
    iqsharp: 0.12.20070124
    Jupyter Core: 1.4.0.0
    ```

    Keine Sorge, wenn Ihre `iqsharp`-Version höher ist. Sie sollte mit dem [aktuellen Release](xref:microsoft.quantum.relnotes) identisch sein.

1. Führen Sie den folgenden Befehl in einer Zelle in allen Ihren vorhandenen Q#-Jupyter Notebooks aus:

    ```
    %workspace reload
    ```

***

Sie können jetzt den aktualisierten IQ#-Kernel verwenden, um Ihre vorhandenen Q#-Jupyter Notebooks auszuführen.

### <a name="update-visual-studio-qdk-extension"></a>Aktualisieren der Visual Studio-QDK-Erweiterung

1. Aktualisieren Sie die Q#-Visual Studio-Erweiterung.

    - In Visual Studio wird eine Aufforderung zum Akzeptieren der Updates für die [Visual Studio-Quantum-Erweiterung](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) angezeigt.
    - Akzeptieren Sie das Update.

    > [!NOTE]
    > Die Projektvorlagen werden mit der Erweiterung aktualisiert. Die aktualisierten Vorlagen gelten nur für neu erstellte Projekte. Der Code für Ihre vorhandenen Projekte wird bei der Aktualisierung der Erweiterung nicht aktualisiert.

### <a name="update-vs-code-qdk-extension"></a>Aktualisieren der VS Code-QDK-Erweiterung

1. Aktualisieren Sie die Quantum-Erweiterung für VS Code.

    - Starten Sie VS Code neu.
    - Navigieren Sie zur Registerkarte **Erweiterungen**.
    - Wählen Sie die Erweiterung **Microsoft Quantum Development Kit for Visual Studio Code** aus.
    - Laden Sie die Erweiterung neu.

2. Aktualisieren Sie die Quantum-Projektvorlagen:

   - Navigieren Sie zu **Ansicht** -> **Befehlspalette**.
   - Wählen Sie **Q#: Install project templates** (Q#: Projektvorlagen installieren) aus.
   - Nach wenigen Sekunden sollte ein Popupfenster mit der Bestätigung angezeigt werden, dass die „Projektvorlagen erfolgreich installiert wurden“.

### <a name="c-using-the-dotnet-command-line-tool"></a>C#: `dotnet`-Befehlszeilentool

1. Aktualisieren Sie die Quantum-Projektvorlagen für .NET.

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```
