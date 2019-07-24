---
title: Příprava metadat aplikace k použití v RCS
description: Kroky v tomto tématu vysvětlují, jak může uživatel vytvořit novou konfiguraci elektronického výkaznictví, která obsahuje metadata aplikace Finance and Operations pro navrhování konfigurací mapování modelu elektronického výkaznictví v Regulatory configuration service (RCS).
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1bd2298240fa789762a350e90888201c5a7ce45
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726976"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a>Příprava metadat aplikace k použití v RCS
[!include [task guide banner](../../includes/task-guide-banner.md)]

Následující kroky vysvětlují, jak může uživatel v roli správce systému nebo vývojáře elektronického výkaznictví vytvořit novou konfiguraci elektronického výkaznictví, která obsahuje metadata aplikace Microsoft Dynamics 365 for Finance and Operations pro navrhování konfigurací mapování modelu elektronického výkaznictví v Regulatory configuration service (RCS). Tato konfigurace se použije pro návrh ukázkové konfigurace mapování modelu elektronického výkaznictví pro přístup k transakcím zahraničního obchodu. V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. Tyto kroky lze provést v libovolné společnosti. K provedení těchto kroků musíte v RCS nejprve dokončit jednotlivé kroky v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="prerequisites"></a>Předpoklady
1.  Přejděte na **Správa organizace** > **Pracovní prostory** > **Elektronické výkaznictví**. 
2.  Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md). 
3.  Klikněte na **Konfigurace metadat**. 
4.  Předpokládejme, že se použije RCS pro návrh řešení elektronického výkaznictví pro aplikace Finance and Operations, které budou použity k vygenerování elektronických dokumentů, které obsahují informace z cizí obchodní domény. Pro určení mapování mezi datovým modelem elektronického výkaznictví a zdroji požadovaných dat, musíme mít v RCS přístup k metadatům aplikace pro Finance and Operations. Proto v rámci řešení elektronického výkaznictví nakonfigurujeme novou konfiguraci metadat elektronického výkaznictví, která obsahuje všechna metadata aktuálně požadovaná k vygenerování sestav elektronického výkaznictví pro vybranou obchodní doménu. 

## <a name="add-metadata-configuration"></a>Přidání konfigurace metadat 
1.  Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno. 
2.  Do pole **Název** zadejte 'Metadata zahraničního obchodu'. 
3.  Klepněte na možnost **Vytvořit konfiguraci**. 
4.  Klikněte na možnost **Návrhář**. 
5.  Klikněte na tlačítko **Přidat**. 
  
> [!NOTE]
> Můžete vybrat všechna metadata pro celou aplikaci, nebo pro vybrané modely nebo moduly. V tomto případě je třeba mít na paměti, že následující metadata budou automaticky přidána: tabulky záznamů, výčty a rozšířené datové typy. Pokud jsou požadovány další typy metadat, musí být přidány ručně. 
 
Máme některá metadata související s transakcemi zahraničního obchodu pomocí ruční volby položek metadat. 
  
6.  Klikněte na možnost **Přidat datový zdroj**. 
7.  Klikněte na **Záznamy tabulky**. 
8.  Použijte rychlý filtr k filtrování na poli **Název** s hodnotou Intrastat. 
9.  Vyberte záznam tabulky **Intrastat**. 
10. Klikněte na tlačítko **OK**.
  
Přidali jsme informace o metadatech do tabulky záznamů Intrastat. 
  
11. Ve stromovém zobrazení rozbalte **Intrastat záznamů tabulky**\>**Vztahy**. 
12. Ve stromové struktuře vyberte **Intrastat záznamů tabulky**\>**Vztahy\IntrastatCommodity (záznamy tabulky EcoResCategory)**.   
13. Klikněte na **Přidat metadata**. 
  
> [!NOTE]
> Metadata o požadovaných vztazích pro vybranou tabulku záznamů je nutné přidat ručně. 
  
16. Klikněte na možnost **Přidat datový zdroj**. 
17. Klikněte na **Výčet**. 
18. Použijte rychlý filtr k filtrování na poli **Název** s hodnotou IntrastatDirection. 
19. Vyberte záznam **Výčet IntrastatDirection**. 
20. Klikněte na tlačítko **OK**. 
21. Klikněte na možnost **Uložit**.  
22. Zavřete stránku. 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a>Dokončení návrhu konceptu konfigurace metadat
1.  Klikněte na položku **Změnit stav**. 
2.  Klikněte na **Dokončit**. 
3.  Klikněte na tlačítko **OK**. 
4.  Vyberte dokončenou verzi **1**. 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a>Exportujte dokončenou verzi konfigurace metadat z aplikace do souboru XML
1.  Klikněte na **Exchange**. 
2.  Klikněte na **Exportovat jako soubor XML**. 
3.  Klikněte na tlačítko **OK**. 
    
Vytvořená konfigurace metadat elektronického výkaznictví byla uložena jako soubor XML, který lze importovat do RCS a použít jako zdroj informací o metadatech pro obchodní doménu zahraničního obchodu v aplikaci Finance and Operations. Na základě těchto informací můžeme určit mapování mezi metadaty aplikací a datovým modelem elektronického výkaznictví.
