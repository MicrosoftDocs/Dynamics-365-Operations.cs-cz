---
title: Určení umístění vlastního úložiště pro vygenerované dokumenty
description: Toto téma vysvětluje, jak rozšířit seznam umístění úložišť pro dokumenty, které generují formáty elektronického výkaznictví.
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: f65118b6a7393ced9d80c30fad7540a7b27da6c7
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569077"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a><span data-ttu-id="75708-103">Určení umístění vlastního úložiště pro vygenerované dokumenty</span><span class="sxs-lookup"><span data-stu-id="75708-103">Specify a custom storage location for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="75708-104">Aplikační programovací rozhraní (API) rozhraní elektronického výkaznictví umožňuje rozšířit seznam umístění úložišť pro dokumenty, které generují ER formáty.</span><span class="sxs-lookup"><span data-stu-id="75708-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="75708-105">Toto téma obsahuje přehled hlavních úkolů, které musíte dokončit, abyste mohli přidat vlastní umístění úložiště.</span><span class="sxs-lookup"><span data-stu-id="75708-105">This topic includes an overview of the main tasks that you must complete to add a custom storage location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="75708-106">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="75708-106">Prerequisites</span></span>

<span data-ttu-id="75708-107">Je nutné nasadit topologii, která podporuje průběžné sestavování.</span><span class="sxs-lookup"><span data-stu-id="75708-107">You must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="75708-108">(Další informace naleznete v tématu [Nasazení topologií podporujících průběžné sestavování a automatizaci testování](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Pro tuto topologii musíte mít přístup do topologie pro jednu z následujících rolí:</span><span class="sxs-lookup"><span data-stu-id="75708-108">(For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="75708-109">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="75708-109">Electronic reporting developer</span></span>
- <span data-ttu-id="75708-110">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="75708-110">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="75708-111">Správce systému</span><span class="sxs-lookup"><span data-stu-id="75708-111">System administrator</span></span>

<span data-ttu-id="75708-112">Také musí mít přístup k vývojovému prostředí pro tuto topologii.</span><span class="sxs-lookup"><span data-stu-id="75708-112">You must also have access to the development environment for this topology.</span></span>

## <a name="create-or-import-an-er-format-configuration"></a><span data-ttu-id="75708-113">Vytvoření nebo import konfigurace formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="75708-113">Create or import an ER format configuration</span></span>

<span data-ttu-id="75708-114">V aktuální topologii [vytvořte nový formát elektronického výkaznictví](tasks/er-format-configuration-2016-11.md) ke generování dokumentů, pro které chcete přidat vlastní umístění úložiště.</span><span class="sxs-lookup"><span data-stu-id="75708-114">In the current topology, [create a new ER format](tasks/er-format-configuration-2016-11.md) to generate documents that you plan to add a custom storage location for.</span></span> <span data-ttu-id="75708-115">Alternativně [importujte stávající formát elektronického výkaznictví do této topologie](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="75708-115">Alternatively, [import an existing ER format into this topology](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![Stránka návrháře formátu](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> <span data-ttu-id="75708-117">Formát elektronického výkaznictví, který vytvoříte nebo importujete, musí obsahovat alespoň jednu z následujících prvků formátu:</span><span class="sxs-lookup"><span data-stu-id="75708-117">The ER format that you create or import must contain at least one of the following format elements:</span></span>
>
> - <span data-ttu-id="75708-118">Soubor</span><span class="sxs-lookup"><span data-stu-id="75708-118">File</span></span>
> - <span data-ttu-id="75708-119">Složka</span><span class="sxs-lookup"><span data-stu-id="75708-119">Folder</span></span>
> - <span data-ttu-id="75708-120">Sloučení</span><span class="sxs-lookup"><span data-stu-id="75708-120">Merger</span></span>
> - <span data-ttu-id="75708-121">Příloha</span><span class="sxs-lookup"><span data-stu-id="75708-121">Attachment</span></span>

## <a name="create-a-new-document-type"></a><span data-ttu-id="75708-122">Vytvoření nového typu dokumentu</span><span class="sxs-lookup"><span data-stu-id="75708-122">Create a new document type</span></span>

<span data-ttu-id="75708-123">Chcete-li určit, jak jsou směrovány dokumenty, které generují formát elektronického výkaznictví, musíte nakonfigurovat [umístění elektronického výkaznictví](electronic-reporting-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="75708-123">To specify how documents that an ER format generates are routed, you must configure [ER destinations](electronic-reporting-destinations.md).</span></span> <span data-ttu-id="75708-124">V každém cílovém umístění elektronického výkaznictví, které je nakonfigurováno pro ukládání generovaných dokumentů jako souborů, musíte zadat typ dokumentu v rámci architektury správy dokumentů.</span><span class="sxs-lookup"><span data-stu-id="75708-124">In each ER destination that is configured to store generated documents as files, you must specify a document type of the Document management framework.</span></span> <span data-ttu-id="75708-125">Různé typy dokumentů mohou být použity pro směrování dokumentů, které různé formáty elektronického výkaznictví generují.</span><span class="sxs-lookup"><span data-stu-id="75708-125">Different document types can be used to route documents that different ER formats generate.</span></span>

1. <span data-ttu-id="75708-126">Přidejte nový [typ dokumentu](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) pro formát elektronického výkaznictví, který jste předtím vytvořili, nebo importovali.</span><span class="sxs-lookup"><span data-stu-id="75708-126">Add a new [document type](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) for the ER format that you created or imported earlier.</span></span> <span data-ttu-id="75708-127">Na následujícím obrázku je typ dokumentu **FileX**.</span><span class="sxs-lookup"><span data-stu-id="75708-127">In the illustration that follows, the document type is **FileX**.</span></span>
2. <span data-ttu-id="75708-128">Chcete-li tento typ dokumentu odlišit od jiných typů dokumentů, zahrňte do jeho názvu konkrétní klíčové slovo.</span><span class="sxs-lookup"><span data-stu-id="75708-128">To differentiate this document type from other document types, include a specific keyword in its name.</span></span> <span data-ttu-id="75708-129">Například v následujícím příkladu je název **složka (LOCAL)**.</span><span class="sxs-lookup"><span data-stu-id="75708-129">For example, in the illustration that follows, the name is **(LOCAL) folder**.</span></span>
3. <span data-ttu-id="75708-130">V poli **Třída** určete **Připojit soubor**.</span><span class="sxs-lookup"><span data-stu-id="75708-130">In the **Class** field, specify **Attach file**.</span></span>
4. <span data-ttu-id="75708-131">V poli **Skupina** určete **Soubor**.</span><span class="sxs-lookup"><span data-stu-id="75708-131">In the **Group** field, specify **File**.</span></span>

![Stránka typu dokumentu](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> <span data-ttu-id="75708-133">Typy dokumentů jsou specifické pro společnost.</span><span class="sxs-lookup"><span data-stu-id="75708-133">Document types are company-specific.</span></span> <span data-ttu-id="75708-134">Chcete-li použít formát elektronického výkaznictví s nakonfigurovaným umístěním ve více společnostech, musíte v každé společnosti nakonfigurovat samostatný typ dokumentu.</span><span class="sxs-lookup"><span data-stu-id="75708-134">To use an ER format with a configured destination in multiple companies, you must configure a separate document type in each company.</span></span>

## <a name="review-source-code"></a><span data-ttu-id="75708-135">Kontrola zdrojového kódu</span><span class="sxs-lookup"><span data-stu-id="75708-135">Review source code</span></span>

<span data-ttu-id="75708-136">Zkontrolujte kód metody **insertFile()** třídy **ERDocuManagement**.</span><span class="sxs-lookup"><span data-stu-id="75708-136">Review the code of the **insertFile()** method of the **ERDocuManagement** class.</span></span> <span data-ttu-id="75708-137">Všimněte si, že událost **AttachingFile()** je vyvolána během připojování generovaného souboru k záznamu.</span><span class="sxs-lookup"><span data-stu-id="75708-137">Notice that the **AttachingFile()** event is raised while the generated file is attached to a record.</span></span>

```
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

<span data-ttu-id="75708-138">Je vyvolána událost **AttachingFile()**, když jsou zpracována následující umístění elektronického výkaznictví:</span><span class="sxs-lookup"><span data-stu-id="75708-138">The **AttachingFile()** event is raised when the following ER destinations are processed:</span></span>

- <span data-ttu-id="75708-139">**Archiv** – Při použití tohoto umístění je v tabulce ERFormatMappingRunJobTable vytvořen nový záznam pro formát elektronického výkaznictví, který je spuštěn.</span><span class="sxs-lookup"><span data-stu-id="75708-139">**Archive** – When this destination is used, a new record for the ER format that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="75708-140">Pole **Archivované** v tomto záznamu je nastaveno na **False**.</span><span class="sxs-lookup"><span data-stu-id="75708-140">The **Archived** field in this record is set to **False**.</span></span> <span data-ttu-id="75708-141">Je-li formát elektronického výkaznictví spuštěn úspěšně, generovaný dokument je připojen k tomuto záznamu a je vyvolána událost **AttachingFile()**.</span><span class="sxs-lookup"><span data-stu-id="75708-141">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="75708-142">Typ dokumentu, který je vybrán v tomto umístění elektronického výkaznictví, určuje umístění úložiště pro připojený soubor (Microsoft Azure Storage nebo složka Microsoft SharePoint).</span><span class="sxs-lookup"><span data-stu-id="75708-142">The document type that is selected in this ER destination determines the storage location for the attached file (Microsoft Azure Storage or a Microsoft SharePoint folder).</span></span>
- <span data-ttu-id="75708-143">**Archiv úloh** – Při použití tohoto umístění je v tabulce ERFormatMappingRunJobTable vytvořen nový záznam pro formulář elektronického výkaznictví, který je spuštěn.</span><span class="sxs-lookup"><span data-stu-id="75708-143">**Job archive** – When this destination is used, a new record for the ER form that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="75708-144">Pole **Archivované** v tomto záznamu je nastaveno na **True**.</span><span class="sxs-lookup"><span data-stu-id="75708-144">The **Archived** field in this record is set to **True**.</span></span> <span data-ttu-id="75708-145">Je-li formát elektronického výkaznictví spuštěn úspěšně, generovaný dokument je připojen k tomuto záznamu a je vyvolána událost **AttachingFile()**.</span><span class="sxs-lookup"><span data-stu-id="75708-145">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="75708-146">Typ dokumentu, který je nakonfigurován v parametrech elektronického výkaznictví, určuje umístění úložiště pro připojený soubor (Azure Storage nebo složka Microsoft SharePoint).</span><span class="sxs-lookup"><span data-stu-id="75708-146">The document type that is configured in the ER parameters determines the storage location for the attached file (Azure Storage or a SharePoint folder).</span></span>

![Stránka parametrů elektronického výkaznictví](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a><span data-ttu-id="75708-148">Konfigurace umístění elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="75708-148">Configure an ER destination</span></span>

1. <span data-ttu-id="75708-149">Nakonfigurujte archivovaný cíl pro jeden z dříve uvedených prvků (soubor, složka, sloučení nebo příloha) formátu ER, který jste vytvořili nebo naimportovali.</span><span class="sxs-lookup"><span data-stu-id="75708-149">Configure the archived destination for one of the previously mentioned elements (file, folder, merger, or attachment) of the ER format that you created or imported.</span></span> <span data-ttu-id="75708-150">Pokyny jsou uvedeny v části [Konfigurace cílů ER](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span><span class="sxs-lookup"><span data-stu-id="75708-150">For guidance, see [ER Configure destinations](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span></span>
2. <span data-ttu-id="75708-151">Použijte typ dokumentu, který jste přidali dříve pro nakonfigurované umístění.</span><span class="sxs-lookup"><span data-stu-id="75708-151">Use the document type that you added earlier for the configured destination.</span></span> <span data-ttu-id="75708-152">(Například v tomto tématu je typ dokumentu **FileX**.)</span><span class="sxs-lookup"><span data-stu-id="75708-152">(For the example in this topic, the document type is **FileX**.)</span></span>

![Dialogové okno nastavení cíle](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a><span data-ttu-id="75708-154">Úprava zdrojového kódu</span><span class="sxs-lookup"><span data-stu-id="75708-154">Modify source code</span></span>

1. <span data-ttu-id="75708-155">Přidejte novou třídu do vašeho projektu Microsoft Visual Studio a napište kód, který se přihlásí k odběru k události **AttachingFile()**, která byla uvedena výše.</span><span class="sxs-lookup"><span data-stu-id="75708-155">Add a new class to your Microsoft Visual Studio project, and write code to subscribe to the **AttachingFile()** event that was mentioned earlier.</span></span> <span data-ttu-id="75708-156">(Další informace o použitém vzorci rozšiřitelnost naleznete v tématu [Odpověď pomocí EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Například v nové třídě napište kód, který provede následující akce:</span><span class="sxs-lookup"><span data-stu-id="75708-156">(For more information about the extensibility pattern that is used, see [Respond by using EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) For example, in the new class, write code that performs the following actions:</span></span>

    1. <span data-ttu-id="75708-157">Uložte generované soubory do složky místního systému souborů serveru, který spouští službu Aplikační objektový server (AOS).</span><span class="sxs-lookup"><span data-stu-id="75708-157">Store generated files in a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    2. <span data-ttu-id="75708-158">Tyto generované soubory ukládejte pouze tehdy, když se používá nový typ dokumentu (například **FileX**, který má klíčové slovo "(LOCAL)" ve svém názvu), zatímco soubor je připojen k záznamu v protokolu úlohy provedení elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="75708-158">Store these generated files only when the new document type (for example, the **FileX** type that has the "(LOCAL)" keyword in its name) is used while a file is attached to the record in the ER execution job log.</span></span>

    ```
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. <span data-ttu-id="75708-159">Znovu sestavte svůj projekt.</span><span class="sxs-lookup"><span data-stu-id="75708-159">Rebuild your project.</span></span>

## <a name="run-the-er-format-that-you-created-or-imported"></a><span data-ttu-id="75708-160">Spuštění formátu elektronického výkaznictví, který jste vytvořili, nebo importovali</span><span class="sxs-lookup"><span data-stu-id="75708-160">Run the ER format that you created or imported</span></span>

1. <span data-ttu-id="75708-161">Spusťte formát elektronického výkaznictví, který jste vytvořili, nebo importovali.</span><span class="sxs-lookup"><span data-stu-id="75708-161">Execute the ER format that you created or imported.</span></span>
2. <span data-ttu-id="75708-162">Přejděte do nabídky **Správa organizace \> Elektronická sestava \> Úlohy elektronických sestav**.</span><span class="sxs-lookup"><span data-stu-id="75708-162">Go to **Organization administration \> Electronic reporting \> Electronic reporting jobs**.</span></span> <span data-ttu-id="75708-163">Najděte záznam, který byl vytvořen pro tuto úlohu spuštění a který má k sobě připojený generovaný soubor.</span><span class="sxs-lookup"><span data-stu-id="75708-163">Find the record that was created for this execution job, and that has the generated file attached to it.</span></span>
3. <span data-ttu-id="75708-164">Prozkoumejte složku **C:\\0** pro vyhledání stejného vygenerovaného souboru.</span><span class="sxs-lookup"><span data-stu-id="75708-164">Explore the local **C:\\0** folder to find same generated file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75708-165">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="75708-165">Additional resources</span></span>

- [<span data-ttu-id="75708-166">Místa určení elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="75708-166">Electronic reporting destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="75708-167">Domovská stránka pro rozšiřitelnost</span><span class="sxs-lookup"><span data-stu-id="75708-167">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
