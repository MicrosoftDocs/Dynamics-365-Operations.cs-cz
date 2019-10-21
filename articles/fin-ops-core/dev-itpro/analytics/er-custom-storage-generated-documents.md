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
ms.openlocfilehash: a1c41cd4440eaf70f720bfd64884e6ef4662f87a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181466"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a>Určení umístění vlastního úložiště pro vygenerované dokumenty

[!include[banner](../includes/banner.md)]

Aplikační programovací rozhraní (API) rozhraní elektronického výkaznictví umožňuje rozšířit seznam umístění úložišť pro dokumenty, které generují ER formáty. Toto téma obsahuje přehled hlavních úkolů, které musíte dokončit, abyste mohli přidat vlastní umístění úložiště.

## <a name="prerequisites"></a>Předpoklady

Je nutné nasadit topologii, která podporuje průběžné sestavování. (Další informace naleznete v tématu [Nasazení topologií podporujících průběžné sestavování a automatizaci testování](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Pro tuto topologii musíte mít přístup do topologie pro jednu z následujících rolí:

- Návrhář elektronického výkaznictví
- Funkční konzultant elektronického výkaznictví
- Správce systému

Také musí mít přístup k vývojovému prostředí pro tuto topologii.

## <a name="create-or-import-an-er-format-configuration"></a>Vytvoření nebo import konfigurace formátu elektronického výkaznictví

V aktuální topologii [vytvořte nový formát elektronického výkaznictví](tasks/er-format-configuration-2016-11.md) ke generování dokumentů, pro které chcete přidat vlastní umístění úložiště. Alternativně [importujte stávající formát elektronického výkaznictví do této topologie](general-electronic-reporting-manage-configuration-lifecycle.md).

![Stránka návrháře formátu](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> Formát elektronického výkaznictví, který vytvoříte nebo importujete, musí obsahovat alespoň jednu z následujících prvků formátu:
>
> - Soubor
> - Složka
> - Sloučení
> - Příloha

## <a name="create-a-new-document-type"></a>Vytvoření nového typu dokumentu

Chcete-li určit, jak jsou směrovány dokumenty, které generují formát elektronického výkaznictví, musíte nakonfigurovat [umístění elektronického výkaznictví](electronic-reporting-destinations.md). V každém cílovém umístění elektronického výkaznictví, které je nakonfigurováno pro ukládání generovaných dokumentů jako souborů, musíte zadat typ dokumentu v rámci architektury správy dokumentů. Různé typy dokumentů mohou být použity pro směrování dokumentů, které různé formáty elektronického výkaznictví generují.

1. Přidejte nový [typ dokumentu](../../fin-and-ops/organization-administration/configure-document-management.md) pro formát elektronického výkaznictví, který jste předtím vytvořili, nebo importovali. Na následujícím obrázku je typ dokumentu **FileX**.
2. Chcete-li tento typ dokumentu odlišit od jiných typů dokumentů, zahrňte do jeho názvu konkrétní klíčové slovo. Například v následujícím příkladu je název **složka (LOCAL)**.
3. V poli **Třída** určete **Připojit soubor**.
4. V poli **Skupina** určete **Soubor**.

![Stránka typu dokumentu](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> Typy dokumentů jsou specifické pro společnost. Chcete-li použít formát elektronického výkaznictví s nakonfigurovaným umístěním ve více společnostech, musíte v každé společnosti nakonfigurovat samostatný typ dokumentu.

## <a name="review-source-code"></a>Kontrola zdrojového kódu

Zkontrolujte kód metody **insertFile()** třídy **ERDocuManagement**. Všimněte si, že událost **AttachingFile()** je vyvolána během připojování generovaného souboru k záznamu.

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

Je vyvolána událost **AttachingFile()**, když jsou zpracována následující umístění elektronického výkaznictví:

- **Archiv** – Při použití tohoto umístění je v tabulce ERFormatMappingRunJobTable vytvořen nový záznam pro formát elektronického výkaznictví, který je spuštěn. Pole **Archivované** v tomto záznamu je nastaveno na **False**. Je-li formát elektronického výkaznictví spuštěn úspěšně, generovaný dokument je připojen k tomuto záznamu a je vyvolána událost **AttachingFile()**. Typ dokumentu, který je vybrán v tomto umístění elektronického výkaznictví, určuje umístění úložiště pro připojený soubor (Microsoft Azure Storage nebo složka Microsoft SharePoint).
- **Archiv úloh** – Při použití tohoto umístění je v tabulce ERFormatMappingRunJobTable vytvořen nový záznam pro formulář elektronického výkaznictví, který je spuštěn. Pole **Archivované** v tomto záznamu je nastaveno na **True**. Je-li formát elektronického výkaznictví spuštěn úspěšně, generovaný dokument je připojen k tomuto záznamu a je vyvolána událost **AttachingFile()**. Typ dokumentu, který je nakonfigurován v parametrech elektronického výkaznictví, určuje umístění úložiště pro připojený soubor (Azure Storage nebo složka Microsoft SharePoint).

![Stránka parametrů elektronického výkaznictví](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a>Konfigurace umístění elektronického výkaznictví

1. Nakonfigurujte archivovaný cíl pro jeden z dříve uvedených prvků (soubor, složka, sloučení nebo příloha) formátu ER, který jste vytvořili nebo naimportovali. Pokyny jsou uvedeny v části [Konfigurace cílů ER](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).
2. Použijte typ dokumentu, který jste přidali dříve pro nakonfigurované umístění. (Například v tomto tématu je typ dokumentu **FileX**.)

![Dialogové okno nastavení cíle](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a>Úprava zdrojového kódu

1. Přidejte novou třídu do vašeho projektu Microsoft Visual Studio a napište kód, který se přihlásí k odběru k události **AttachingFile()**, která byla uvedena výše. (Další informace o použitém vzorci rozšiřitelnost naleznete v tématu [Odpověď pomocí EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Například v nové třídě napište kód, který provede následující akce:

    1. Uložte generované soubory do složky místního systému souborů serveru, který spouští službu Aplikační objektový server (AOS).
    2. Tyto generované soubory ukládejte pouze tehdy, když se používá nový typ dokumentu (například **FileX**, který má klíčové slovo "(LOCAL)" ve svém názvu), zatímco soubor je připojen k záznamu v protokolu úlohy provedení elektronického výkaznictví.

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

2. Znovu sestavte svůj projekt.

## <a name="run-the-er-format-that-you-created-or-imported"></a>Spuštění formátu elektronického výkaznictví, který jste vytvořili, nebo importovali

1. Spusťte formát elektronického výkaznictví, který jste vytvořili, nebo importovali.
2. Přejděte do nabídky **Správa organizace \> Elektronická sestava \> Úlohy elektronických sestav**. Najděte záznam, který byl vytvořen pro tuto úlohu spuštění a který má k sobě připojený generovaný soubor.
3. Prozkoumejte složku **C:\\0** pro vyhledání stejného vygenerovaného souboru.

## <a name="additional-resources"></a>Další zdroje

- [Místa určení elektronického výkaznictví](electronic-reporting-destinations.md)
- [Domovská stránka pro rozšiřitelnost](../extensibility/extensibility-home-page.md)
