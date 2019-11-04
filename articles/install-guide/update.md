---
title: Erfahren Sie, wie Sie die Microsoft Quantum Development Kit (QDK) aktualisieren.
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: fc430a77f88878437e662c5b54507f70f3c6e020
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2019
ms.locfileid: "73185850"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Aktualisieren des Microsoft Quantum Development Kit (QDK)

Erfahren Sie, wie Sie die Microsoft Quantum Development Kit (QDK) auf die neueste Version aktualisieren.

In diesem Artikel wird davon ausgegangen, dass Sie das QDK bereits installiert haben. Wenn Sie zum ersten Mal installieren, finden Sie weitere Informationen im [Installationshandbuch](xref:microsoft.quantum.install).

Die Aktualisierungs Schritte hängen von Ihrer Entwicklungsumgebung ab. Wählen Sie Ihre Umgebung aus den folgenden Abschnitten aus.

## <a name="python"></a>Python

1. Aktualisieren des `iqsharp` Kernel

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Überprüfen der `iqsharp` Version

    ```bash
    dotnet iqsharp --version
    ```

    Die folgende Ausgabe wird angezeigt.

    ```bash
    iqsharp: 0.9.1909.3002
    Jupyter Core: 1.1.18837.0
    ```

1. Aktualisieren des `qsharp` Pakets

    ```bash
    pip install qsharp --upgrade
    ```

1. Überprüfen der `qsharp` Version

    ```bash
    pip show qsharp
    ```

    Die folgende Ausgabe wird angezeigt.

    ```bash
    Name: qsharp
    Version: 0.9.1909.3002
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

1. Sie können jetzt die aktualisierte QDK-Version verwenden, um Ihre vorhandenen Quantum-Programme auszuführen.

## <a name="jupyter-notebooks"></a>Jupyter Notebooks

1. Aktualisieren des `iqsharp` Kernel

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Überprüfen der `iqsharp` Version

    ```bash
    dotnet iqsharp --version
    ```

    Die folgende Ausgabe wird angezeigt.

    ```bash
    iqsharp: 0.9.1909.3002
    Jupyter Core: 1.1.18837.0
    ```

1. Sie können jetzt ein vorhandenes jupyter Notebook öffnen und es mit dem aktualisierten QDK ausführen.

## <a name="c-on-windows-using-visual-studio"></a>C#unter Windows mit Visual Studio

1. Aktualisieren der f # Visual Studio-Erweiterung

    - Visual Studio fordert Sie auf, Aktualisierungen der [Erweiterung von Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) zu akzeptieren.
    - Akzeptieren des Updates

    > [!NOTE]
    > Die Projektvorlagen werden mit der Erweiterung aktualisiert. Die aktualisierten Vorlagen gelten nur für neu erstellte Projekte. Der Code für die vorhandenen Projekte wird nicht aktualisiert, wenn die Erweiterung aktualisiert wird.

1. Aktualisieren der QDK-Pakete

    - Öffnen einer vorhandenen Anwendung
    - Wählen Sie **Abhängigkeiten** in der Projektmappen-Explorer
    - Wählen Sie **nuget-Pakete verwalten** .
    - Aktualisieren Sie die **Microsoft. Quantum** -Pakete auf die neueste Version.

1. Sie können nun Ihre Anwendung mit dem neuesten QDK ausführen.

## <a name="c-using-vs-code"></a>C#mit vs Code

1. Aktualisieren der Quantum-vs Code Erweiterung

    - Neustart vs Code
    - Navigieren Sie zur Registerkarte **Erweiterungen** .
    - Wählen Sie die **Microsoft Quantum Development Kit für Visual Studio Code Erweiterung aus** .
    - Erweiterung erneut laden

1. Aktualisieren Sie die Quantum-Projektvorlagen:

   - Gehe zu **Ansicht** -> **Befehls Palette**
   - Auswählen von " **Q #: Install Project Templates** "

1. Öffnen Sie eine vorhandene Anwendung in vs Code

   - Bearbeiten Sie die CSPROJ-Datei, um die neuen Paketversionen hinzuzufügen.

    ```xml
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Standard" Version="0.9.1909.3002" />
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.9.1909.3002" />
    </ItemGroup>
    ```

    Wenn Sie andere `Microsoft.Quantum` Pakete verwenden, aktualisieren Sie diese ebenfalls.

1. Sie können Ihre Anwendung jetzt mit dem aktualisierten QDK ausführen.

## <a name="c-using-the-dotnet-command-line-tool"></a>C#mit dem Befehlszeilen Tool "`dotnet`"

1. Aktualisieren der Quantum-Projektvorlagen für .net

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. Aktualisieren und Ausführen einer vorhandenen Anwendung

    - Aktualisieren der QDK-Paketversionen in der Anwendung

        ```bash
        dotnet add package Microsoft.Quantum.Development.Kit
        dotnet add package Microsoft.Quantum.Standard
        ```

        Wenn Ihre Anwendung andere `Microsoft.Quantum` Pakete verwendet, aktualisieren Sie diese ebenfalls.

    - Ausführen der Anwendung

        ```bash
        dotnet run
        ```

    - Ihre Anwendung wird mit den neuen Paketversionen ausgeführt.

## <a name="whats-next"></a>Wie geht es weiter?

Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung aktualisiert haben, können Sie weiterhin ihre Quantum-Programme entwickeln und ausführen. Wenn Sie noch kein Programm geschrieben haben, können Sie mit [Ihrem ersten Quantum-Programm](xref:microsoft.quantum.write-program)beginnen.
