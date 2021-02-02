---
title: Entwickeln mit Q# und Python
description: Hier erfahren Sie, wie Sie mithilfe von Python eine Anwendung vom Typ Q# erstellen.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: quickstart
uid: microsoft.quantum.install.python
no-loc:
- Q#
- $$v
ms.openlocfilehash: 1ec40b6f1b7a8d9144860e3b8cfd554eb51bae81
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844270"
---
# <a name="develop-with-q-and-python"></a>Entwickeln mit Q# und Python

Installieren Sie das QDK, um Python-Hostprogramme zum Aufrufen von Q#-Vorgängen zu entwickeln.

## <a name="install-the-qsharp-python-package"></a>Installieren des `qsharp`-Python-Pakets

### <a name="install-using-conda-recommended"></a>[Installation mithilfe von Conda (empfohlen)](#tab/tabid-conda)

1. Installieren Sie [Miniconda](https://docs.conda.io/en/latest/miniconda.html) oder [Anaconda](https://www.anaconda.com/products/individual#Downloads). **Hinweis:** Eine 64-Bit-Installation ist erforderlich.

1. Öffnen Sie eine Anaconda-Eingabeaufforderung.

   - Wenn Sie PowerShell oder pwsh verwenden möchten: Öffnen Sie eine Shell, führen Sie `conda init powershell`aus, schließen Sie die Shell, und öffnen Sie sie erneut.

1. Erstellen und aktivieren Sie eine neue Conda-Umgebung namens `qsharp-env` mit den erforderlichen Paketen (einschließlich Jupyter Notebook und IQ#). Führen Sie dazu die folgenden Befehle aus:

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. Führen Sie `python -c "import qsharp"` über das gleiche Terminal aus, um die Installation zu überprüfen und den lokalen Paketcache mit allen erforderlichen QDK-Komponenten aufzufüllen.

### <a name="install-using-net-cli-and-pip-advanced"></a>[Installieren mit der .NET-CLI und PIP (erweitert)](#tab/tabid-dotnetcli)

1. Voraussetzungen:

    - [Python](https://www.python.org/downloads/) 3.6 oder höher
    - Der [PIP](https://pip.pypa.io/en/stable/installing)-Python-Paket-Manager
    - [.NET Core SDK 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. Installieren Sie das `qsharp`-Paket. Hierbei handelt es sich um ein Python-Paket, das die Interoperabilität zwischen Q# und Python ermöglicht.

    ```
    pip install qsharp
    ```

1. Installieren Sie IQ#. Dies ist ein von Jupyter und Python verwendeter Kernel, der die Kernfunktionen zum Kompilieren und Ausführen von Q#-Vorgängen bereitstellt.

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > Wenn Sie während des Schritts `dotnet iqsharp install` einen Fehler erhalten, sollten Sie ein neues Terminalfenster öffnen und den Vorgang dann wiederholen.
    > Falls der Vorgang immer noch nicht erfolgreich ist, sollten Sie mit dem installierten Tool `dotnet-iqsharp` (unter Windows `dotnet-iqsharp.exe`) Folgendes ausführen:
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > Ersetzen Sie hierbei `/path/to/dotnet-iqsharp` durch den absoluten Pfad zum Tool `dotnet-iqsharp` in Ihrem Dateisystem.
    > Normalerweise finden Sie dies unter `.dotnet/tools` in Ihrem Benutzerprofilordner.
    
**_

Das ist alles! Sie verfügen nun sowohl über das `qsharp`-Python-Paket als auch über den IQ#-Kernel für Jupyter, der die Kernfunktionen für das Kompilieren und Ausführen von Q#-Vorgängen in Python bereitstellt und die Verwendung von Q#-Jupyter Notebook-Instanzen ermöglicht.

## <a name="choose-your-ide"></a>Auswählen Ihrer IDE

Q# mit Python kann zwar in einer beliebigen IDE verwendet werden, wir empfehlen jedoch Visual Studio Code (VS Code) als IDE für Ihre Q#- und Python-Anwendungen. Mit der QDK-Erweiterung für Visual Studio Code erhalten Sie Zugriff auf umfangreichere Funktionen wie Warnungen, Syntaxhervorhebung, Projektvorlagen usw.

Wenn Sie VS Code verwenden möchten, gehen Sie wie folgt vor:

- Führen Sie die Installation von [VS Code](https://code.visualstudio.com/download) durch (Windows, Linux und Mac).
- Installieren Sie die [QDK-Erweiterung für VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

Wenn Sie einen anderen Editor verwenden möchten, sind Sie nach Ausführung der obigen Anweisungen dafür bereit.

## <a name="write-your-first-q-program"></a>Schreiben Ihres ersten Q#-Programms

Nun können Sie Ihre Installation des `qsharp`-Python-Pakets überprüfen, indem Sie ein einfaches Q#-Programm schreiben und ausführen.

1. Erstellen Sie einen minimalen Q#-Vorgang, indem Sie eine Datei mit dem Namen `Operation.qs` erstellen und ihr den folgenden Code hinzufügen:

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="3-14":::

1. Erstellen Sie im gleichen Ordner wie `Operation.qs` ein Python-Programm namens `host.py`, um den Q#-Vorgang `SampleQuantumRandomNumberGenerator()` zu simulieren:

    ```python
    import qsharp
    from Qrng import SampleQuantumRandomNumberGenerator

    print(SampleQuantumRandomNumberGenerator.simulate())
    ```

1. Führen Sie das Programm in der Umgebung aus, die Sie während der Installation erstellt haben (d. h. in der Conda- oder Python-Umgebung, in der Sie `qsharp` installiert haben):

    ```
    python host.py
    ```

1. Das Ergebnis des von Ihnen aufgerufenen Vorgangs sollte angezeigt werden. Da in diesem Fall ein zufälliges Ergebnis durch den Vorgang generiert wird, wird entweder `0` oder `1` auf dem Bildschirm angezeigt. Wenn Sie das Programm wiederholt ausführen, sollte jedes Ergebnis ungefähr die Hälfte der Zeit angezeigt werden.

> [!NOTE]
> _ Beim Python-Code handelt es sich nur um ein normales Python-Programm. Sie können eine beliebige Python-Umgebung verwenden, einschließlich Python-basierter Jupyter Notebook-Instanzen, um das Python-Programm zu schreiben und Q#-Vorgänge aufzurufen. Das Python-Programm kann Q#-Vorgänge aus allen QS-Dateien importieren, die sich im gleichen Ordner befinden wie der Python-Code.

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung getestet haben, können Sie dieses Tutorial durchführen, um [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) zu schreiben und auszuführen.
