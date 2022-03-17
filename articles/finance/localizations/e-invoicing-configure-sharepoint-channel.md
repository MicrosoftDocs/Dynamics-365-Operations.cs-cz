---
title: Konfigurace kanálu SharePoint
description: Toto téma vysvětluje, jak nakonfigurovat kanál Microsoft SharePoint pro zpracování příchozích elektronických faktur.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ea3e14ed00b0661d3923c1839135378a8a550499
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371574"
---
# <a name="configure-a-sharepoint-channel"></a>Konfigurace kanálu SharePoint

[!include [banner](../includes/banner.md)]

Jako předpoklad pro konfiguraci kanálu Microsoft SharePoint za účelem zpracování příchozích dokumentů proveďte kroky popsané v tématu [Konfigurace připojení SharePoint](e-invoicing-create-sharepoint-connection.md).

Poté můžete kanál SharePoint použít k importu elektronických faktur dodavatelů ze souborů, které jsou uloženy ve vašich složkách SharePoint.

1. Na svém webu SharePoint vytvořte následující složky:

    - **Hlavní složka** – Složka, ze které bude služba zpracovávat soubory.
    - **Archivní složka** – Složka, do které budou uloženy zpracované soubory.
    - **Chybová složka** – Složka, do které systém přesune soubory, pokud se zpracování nezdaří.

2. Ve službě Regulatory Configuration Service (RCS) vyberte vámi vytvořenou funkci elektronické fakturace. Ujistěte se, že jste vybrali verzi se stavem **Koncept**.
3. Na kartě **Nastavení** vyberte možnost **Přidat**.
4. V rozevíracím dialogovém okně **Vytvořit nastavení funkce** ve skupině polí **Nové** vyberte možnost **Vlastní nastavení**.
5. Ve skupině polí **Typ nastavení** vyberte možnost **Datový kanál**.
6. V poli **Vyberte datový kanál** zvolte **Složka SharePoint**.
7. Vyberte **Vytvořit**.
8. Vyberte řádek, které jste vytvořili dříve, a poté vyberte možnost **Upravit**.
9. Na kartě **Datový kanál** v části **Parametry** nastavte následující povinná pole.

    | Pole                 | Popis |
    |-----------------------|-------------|
    | Datový kanál          | Zadejte jedinečný název pro identifikaci datového kanálu. Název může mít maximálně 10 znaků. Název bude odkazován v pravidlech použitelnosti a v připojených aplikacích během komunikačního procesu. |
    | Adresa SharePointu    | Zadejte adresu URL SharePoint. Zadejte například `<domain>.sharepoint.com`. |
    | ID aplikace        | Zadejte název tajného kódu trezoru klíčů Azure, který obsahuje ID uživatelského účtu SharePoint. Tento tajný kód musí být vytvořen v trezoru klíčů a nastaven v prostředí vaší služby. Hodnota je **ID aplikace (klienta)** z části [Konfigurace připojení SharePoint](e-invoicing-create-sharepoint-connection.md). |
    | Tajný kód aplikace    | Zadejte název tajného kódu trezoru klíčů Azure, který obsahuje heslo uživatelského účtu SharePoint. Hodnota je **Tajný kód registrace aplikace** z části [Konfigurace připojení SharePoint](e-invoicing-create-sharepoint-connection.md). |
    | Název webu             | Zadejte název webu SharePoint. |
    | Název knihovny dokumentů | Zadejte název knihovny dokumentů SharePoint. |
    | Časový limit               | Zadejte maximální časový limit v milisekundách (ms), po který má systém čekat na odpověď. Výchozí hodnota je 10 000 ms (10 sekund). |
    | Hlavní složka           | Zadejte zdroj importu souborů nebo složku, ze které má služba zpracovávat soubory. |
    | Složka archivu        | Zadejte složku, do které se mají ukládat zpracované soubory. |
    | Složka chyb          | Zadejte složku, do které má systém přesunout soubory, pokud se zpracování nezdaří. |
    | Maximální velikost souboru         | Zadejte maximální velikost jednoho zpracovávaného souboru v bajtech. Výchozí hodnota je 20 000 000 bajtů. |
    | Maximální počet souborů      | Zadejte maximální počet zpracovaných souborů v rámci jedné akce. Pokud nechcete omezovat počet souborů, nastavte hodnotu na **0** (nula). |
    | Filtr souborů           | Zadejte řetězec, který bude filtrovat podle názvu souboru. Toto pole je volitelné. Jednoduchá maska jako například **\*něco\* .ext** je podporována; zde každá hvězdička (\*) představuje nula nebo více výskytů jakéhokoli znaku. Například zadejte **\*.pdf** a tak konfigurujte kanál ke čtení souborů PDF. |
    | Vlastní název souboru      | Zadejte vlastní název souboru od klienta. |

10. Na kartě **Pravidla použitelnosti** zkontrolujte a aktualizujte kritéria podle potřeby. Hodnota pole **Kanál** se musí rovnat hodnotě, kterou jste zadali do pole **Datový kanál** v předchozím kroku.
11. Zvolte **Uložit** a zavřete stránku.
