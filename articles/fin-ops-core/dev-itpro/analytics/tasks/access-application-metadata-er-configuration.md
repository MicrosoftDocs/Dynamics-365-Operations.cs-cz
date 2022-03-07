---
title: Přístup k metadatům aplikace pomocí konfigurace elektronického výkaznictví
description: Kroky v tomto tématu popisují, jak může uživatel služby Regulatory Configuration Service navrhnout nové mapování modelu elektronického výkaznictví pomocí metadat.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58697148ecf83f4962bd64a221945b6d911e11a6
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093298"
---
# <a name="access-application-metadata-by-using-er-configuration"></a>Přístup k metadatům aplikace pomocí konfigurace elektronického výkaznictví

[!include [banner](../../includes/banner.md)]

Následující kroky vysvětlují, jak může uživatel služby Regulatory Configuration Service s rolí Správce systému nebo Návrhář elektronického výkaznictví navrhnout nové mapování modelu elektronického výkaznictví (ER) pro pomocí metadat aplikace. K metadatům aplikace se přistupuje pomocí konfigurace metadat ER, která obsahuje ukázkovou sadu metadat pro přístup k transakcím zahraničního obchodu. Provedení těchto kroků vyžaduje, abyste nejprve dokončili kroky v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md). Pak proveďte kroky uvedené v tématu [Příprava použití metadat aplikace v RCS](prepare-application-metadata-rcs.md).

## <a name="prerequisites"></a>Předpoklady
1. Přejděte na **Všechny pracovní prostory** > **Elektronické výkaznictví**. 
2. Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md). 

## <a name="import-metadata-configuration"></a>Import konfigurace metadat 
1. Klikněte na **Konfigurace metadat**. 
2. Importujte konfiguraci metadat ER obsahující metadata, která jsou nakonfigurována pro generování elektronických dokumentů pro zahraniční obchod. Konfigurace metadat ER byla exportována jako soubor XML, zatímco byly dokončeny kroky v proceduře [Příprava metadat aplikace k použití v RCS](prepare-application-metadata-rcs.md). 
3. Klikněte na **Exchange**. 
4. Klikněte na **Načíst ze souboru XML**. 
5. Klikněte na **Procházet** a vyberte soubor 'Foreign trade metadata.xml'. 
6. Klikněte na tlačítko **OK**. 
7. Zavřete stránku. 

## <a name="create-data-model-configuration"></a>Vytvoření konfigurace datového modelu
1. Klikněte na **Konfigurace výkaznictví**. 
2. Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno. 
3. Do pole **Název** zadejte 'Model zahraničního obchodu'. 
4. Klepněte na možnost **Vytvořit konfiguraci**. 
5. Klikněte na možnost **Návrhář**. 
6. Kliknutím na možnost **Nový** otevřete dialogové okno. 
7. Do pole **Název** zadejte Kořen. 
8. Klikněte na tlačítko **Přidat**. 
9. Kliknutím na možnost **Nový** otevřete dialogové okno. 
10.    Do pole **Název** zadejte Transakce. 
11.    V poli **Typ položky** vyberte **Seznam záznamů**. 
12.    Klikněte na tlačítko **Přidat**. 
13.    Kliknutím na možnost **Nový** otevřete dialogové okno. 
14.    Do pole **Název** zadejte ID záznamu komodity. 
15.    V poli **Typ položky** vyberte **Řetězec**. 
16.    Klikněte na tlačítko **Přidat**. 
17.    Kliknutím na možnost **Nový** otevřete dialogové okno. 
18.    Do pole **Název** zadejte Fakturovaná částka. 
19.    V poli **Typ položky** vyberte **Reálný**. 
20.    Klikněte na tlačítko **Přidat**. 
21.    Kliknutím na možnost **Nový** otevřete dialogové okno. 
22.    Do pole **Název** zadejte Datum. 
23.    V poli **Typ položky** vyberte **Datum**. 
24.    Klikněte na tlačítko **Přidat**. 
25.    Klikněte na **Kořenový odkaz**. 
26.    Klikněte na tlačítko **OK**. 
27.    Klikněte na možnost **Uložit**. 
28.    Zavřete stránku. 
29.    Klikněte na položku **Změnit stav**. 
30.    Klikněte na **Dokončit**. 
31.    Klikněte na tlačítko **OK**. 

## <a name="create-model-mapping-configuration"></a>Vytvoření konfigurace mapování modelu 
1. Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno. 
2. V poli **Nový** zadejte Mapování modelu založené na datovém modelu Model zahraničního obchodu. 
3. Do pole **Název** zadejte 'Mapování zahraničního obchodu'. 
4. Klepněte na možnost **Vytvořit konfiguraci**. 
5. Rozbalte oddíl **Předpoklady**. 
6. Klikněte na možnost **Upravit**. 
7. Klepněte na možnost **Nový**. 
8. Označte na seznamu vybraný řádek. 
9. V poli **Typ komponenty předpokladu** vyberte **Konfigurace**. 
10.    Vyberte konfiguraci **Metadata zahraničního obchodu**. 
11.    Klikněte na možnost **Uložit**. 
12.    Přidali jsme odkaz na verzi 1 konfigurace'Metadata zahraničního obchodu'. Metadata aplikace z této konfigurace budou nabízena, dokud nebude toto mapování modelu navrženo. 
13.    Zavřete stránku. 
14.    Klikněte na možnost **Návrhář**. 
15.    Klikněte na možnost **Návrhář**. 
16.    Ve stromovém zobrazení vyberte možnost **Dynamics 365 for Operations\Table records**. 
17.    Klikněte na možnost **Přidat kořen**. 
18.    Do pole **Název** zadejte Intrastat. 
19.    Vyberte záznamy tabulky **Intrastat**. 
20.    Klikněte na tlačítko **OK**. 

> [!NOTE]
> Byly nabídnuty pouze dvě tabulky, protože do sady metadat, která je právě používána, byly přidány pouze dvě tabulky. 

21.    Klikněte na **Vazba**. 
22.    Ve stromu rozbalte **Intrastat**. 
23.    Ve stromovém zobrazení vyberte **Intrastat\AmountMST**. 
24.    Ve stromovém zobrazení rozbalte **Transakce = Intrastat**. 
25.    Ve stromovém zobrazení vyberte možnost **Transaction = Intrastat\Invoiced amount**. 
26.    Klikněte na **Vazba**. 
27.    Ve stromovém zobrazení vyberte **Intrastat\TransDate**. 
28.    Ve stromovém zobrazení vyberte **Transakce = Intrastat\Date**. 
29.    Klikněte na **Vazba**. 
30.    Ve stromovém zobrazení rozbalte **Intrastat\>Relations**. 
31.    Ve stromovém zobrazení rozbalte **Intrastat\>Relations\IntrastatCommodity**. 
32.    Ve stromovém zobrazení vyberte **Intrastat\>Relations\IntrastatCommodity\Code**. 
33.    Ve stromovém zobrazení vyberte **Transaction = Intrastat\Commodity code**. 
34.    Klikněte na **Vazba**. 
35.    Klikněte na tlačítko **Ověřit**. 

> [!NOTE]
> Úspěšně jsme provedli vázání prvků datového modelu s položkami datových zdrojů, které jsou popsány pomocí podrobností metadat aplikace z odkazované konfigurace metadat ER. 
36.    Klikněte na možnost **Uložit**. 
37.    Zavřete stránku. 
38.    Zavřete stránku. 
39.    V případě potřeby můžete rozšířit stávající sadu metadat a poté exportovat novou dokončenou verzi konfigurace metadat ER. Poté ji můžete importovat do RCS a aktualizovat předpoklady konfigurace mapování konfigurovaných modelů odkazující na novou verzi importované konfigurace metadat. 

> [!NOTE]
> Tento způsob získání informací o metadatech aplikace je jediný dostupný pro lokálně nasazené aplikace (v případě místních obchodních dat (LBD) nebo místně se používá model nasazení).
        
