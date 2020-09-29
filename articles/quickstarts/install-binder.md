---
title: Entwickeln mit Q# und Binder
description: Hier erfahren Sie, wie Sie mithilfe von Binder eine Anwendung vom Typ Q# erstellen.
author: bradben
ms.author: v-benbra
ms.date: 9/03/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.binder
no-loc:
- Q#
- $$v
ms.openlocfilehash: f993a1145dd8c01045d4cc7cfd0c98efd574ea78
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90836534"
---
# <a name="develop-with-no-locq-and-binder"></a><span data-ttu-id="85272-103">Entwickeln mit Q# und Binder</span><span class="sxs-lookup"><span data-stu-id="85272-103">Develop with Q# and Binder</span></span>

<span data-ttu-id="85272-104">Sie können Binder verwenden, um Ihre Jupyter Notebook-Instanzen online auszuführen und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="85272-104">You can use Binder to run and share your Jupyter Notebooks online.</span></span>

## <a name="use-binder-with-the-microsoft-qdk-samples"></a><span data-ttu-id="85272-105">Verwenden von Binder mit den Microsoft QDK-Beispielen</span><span class="sxs-lookup"><span data-stu-id="85272-105">Use Binder with the Microsoft QDK samples</span></span>

<span data-ttu-id="85272-106">So konfigurieren Sie Binder automatisch für die Verwendung der Microsoft QDK-Beispiele:</span><span class="sxs-lookup"><span data-stu-id="85272-106">To configure Binder automatically to use the Microsoft QDK samples:</span></span>

1. <span data-ttu-id="85272-107">Öffnen Sie einen Browser, und führen Sie https://aka.ms/try-qsharp aus.</span><span class="sxs-lookup"><span data-stu-id="85272-107">Open a browser and run https://aka.ms/try-qsharp.</span></span>
1. <span data-ttu-id="85272-108">Klicken Sie auf der Landing Page für **Quantum Development Kit-Beispiele** auf **Q#-Notebook**, um zu erfahren, wie Sie IQ# zum Schreiben eigener Quantenanwendungsnotebooks verwenden können.</span><span class="sxs-lookup"><span data-stu-id="85272-108">On the **Quantum Development Kit Samples** landing page, click **Q# notebook** to learn how to use IQ# to write your own quantum application notebooks.</span></span>

![Landing Page für das QDK](~/media/binder-install.png)

## <a name="use-binder-with-your-own-notebooks-and-repository"></a><span data-ttu-id="85272-110">Verwenden von Binder mit eigenen Notebooks und eigenem Repository</span><span class="sxs-lookup"><span data-stu-id="85272-110">Use Binder with your own notebooks and repository</span></span>

<span data-ttu-id="85272-111">Wenn Sie bereits über Notebooks in einem GitHub-Repository verfügen, können Sie Binder für die Verwendung des Repositorys konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="85272-111">If you already have notebooks in a GitHub repository, you can configure Binder to work with your repo:</span></span>

1. <span data-ttu-id="85272-112">Stellen Sie sicher, dass sich im Repositorystamm eine Datei namens *Dockerfile* befindet.</span><span class="sxs-lookup"><span data-stu-id="85272-112">Ensure that there is a file named *Dockerfile* in the root of your repository.</span></span> <span data-ttu-id="85272-113">Die Datei muss mindestens die folgenden Zeilen enthalten:</span><span class="sxs-lookup"><span data-stu-id="85272-113">The file must contain at least the following lines:</span></span>

    ```bash
    FROM mcr.microsoft.com/quantum/iqsharp-base:0.12.20082513
    
    USER root
    COPY . ${HOME}
    RUN chown -R ${USER} ${HOME}
    
    USER ${USER}
    ```

    > [!NOTE]
    > <span data-ttu-id="85272-114">Sie können die aktuelle Version von IQ# in den [Versionshinweisen](xref:microsoft.quantum.relnotes) überprüfen.</span><span class="sxs-lookup"><span data-stu-id="85272-114">You can verify the most current version of IQ# in the [Release Notes](xref:microsoft.quantum.relnotes).</span></span>

    <span data-ttu-id="85272-115">Weitere Informationen zum Erstellen eines Dockerfile finden Sie in der [Referenz zu Dockerfile](https://docs.docker.com/engine/reference/builder/).</span><span class="sxs-lookup"><span data-stu-id="85272-115">For more information about creating a Dockerfile, see the [Dockerfile reference](https://docs.docker.com/engine/reference/builder/).</span></span>

2. <span data-ttu-id="85272-116">Öffnen Sie in einem Browser [mybinder.org](https://mybinder.org).</span><span class="sxs-lookup"><span data-stu-id="85272-116">Open a browser to [mybinder.org](https://mybinder.org).</span></span>
3. <span data-ttu-id="85272-117">Geben Sie den Repositorynamen als **GitHub-URL** (z. B. *MyName/MyRepo*) ein, und klicken Sie auf **Start**.</span><span class="sxs-lookup"><span data-stu-id="85272-117">Enter your repository name as the **GitHub URL** (for example *MyName/MyRepo*), and click **launch**.</span></span>

![MyBinder-Formular](~/media/mybinder.png)
    
## <a name="next-steps"></a><span data-ttu-id="85272-119">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="85272-119">Next steps</span></span>

<span data-ttu-id="85272-120">Nach dem Einrichten Ihrer Binder-Umgebung können Sie nun [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="85272-120">Now that you have set up your Binder environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>