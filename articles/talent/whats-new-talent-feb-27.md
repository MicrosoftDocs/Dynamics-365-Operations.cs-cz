---
title: Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (27. února 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b622276000c56a5af1bb258dbc3c6c4a56af4d20
ms.sourcegitcommit: 479b8cda7e411830bf1f579fab3692c980dcf850
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/08/2019
ms.locfileid: "782810"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-27-2019"></a>Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (27. února 2019)

[!include [banner](includes/banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2163

### <a name="add-a-custom-fields-menu-item-to-system-administration"></a>Přidání položky nabídky vlastních polí do správy systému

Navigace k nabídce **Vlastní pole** byla přidána do pracovního prostoru **Správa systému**.

### <a name="hide-the-import-and-create-options-for-new-mobile-applications"></a>Skrytí importu a vytvoření možností pro nové mobilní aplikace

V současné době nelze vytvořit nové mobilní aplikace v aplikaci Talent. Možnost vytvořit nové mobilní rozhraní byla odebrána z nabídky **Mobilní aplikace**.

### <a name="variable-compensation-award-dmf-entity"></a>Odměna variabilní kompenzace (entita DMF)

V této verzi je nyní pro export k dispozici entita **Odměna variabilní kompenzace** Data Management Framework (DMF).

### <a name="uk-addresses-appear-in-the-personnel-management-analytics-page-as-swiss-addresses"></a>Adresy Velké Británie se zobrazují v analytice správy zaměstnanců jako švýcarské adresy

V této verzi se zobrazují adresy podle města. Tato verze opravuje problémy, kde vizualizace špatně představovaly umístění zaměstnance.

### <a name="the-workforce-power-bi-report-shows-an-error-when-a-workers-seniority-date-is-on-leap-day"></a>Sestava zaměstnanců v Power BI zobrazuje chybu, když je datum služebního věku pracovníka v přestupný den

Oprava byla provedena v aplikaci Microsoft Power BI a zohledňuje data služebního věku, které připadají na 29. února.

### <a name="employee-fixed-compensation-employee-variable-awards-employee-variable-plans-enrollments-allow-for-custom-fields"></a>Fixní kompenzace zaměstnanců, variabilní odměny zaměstnanců, a variabilní plány zaměstnanců (registrací) povolují vlastní pole

Nyní lze přidat vlastní pole pro fixní kompenzace zaměstnanců, variabilní odměny zaměstnanců, a variabilní plány zaměstnanců (registrace). Kromě informací, které jsou ve výchozím nastavení k dispozici, můžete nyní sledovat další informace o fixních a variabilních plánech kompenzace zaměstnance. Vlastní pole lze zadat a aktualizovat buď prostřednictvím uživatelského rozhraní, nebo prostřednictvím entit, které jsou k dispozici.

### <a name="other-miscellaneous-bug-fixes"></a>Ostatní různé opravy chyb

Tato verze obsahuje jiné menší opravy chyb.

## <a name="coming-soon"></a>Již brzy

### <a name="advanced-compensation-security-fixed-and-variable"></a>Rozšířené zabezpečení kompenzace (fixní a variabilní)

V mnoha organizacích mohou manažeři kompenzací a zaměstnaneckých výhod mít přístup pouze k určitým záznamům o kompenzacích. Tyto záznamy mohou být pro vedoucí pracovníky nebo regionální zaměstnance. Tato změna umožní oddělení lidských zdrojů spravovat a udržovat plány kompenzace pro různé skupiny zaměstnanců v organizaci. Fixním a variabilním plánům lze přiřadit role zabezpečení, které určí přístup k plánům a údajům zaměstnance souvisejících s těmito plány (jako jsou například informace o mzdě a záznamy o bonusech). Kompenzace pro tyto zaměstnance budou moci zpracovávat pouze role s určeným přístupem.

### <a name="platform-update-24"></a>Aktualizace platformy 24

Další informace o aplikaci Microsoft Dynamics 365 for Finance and Operations v aktualizaci Platform Update 24 (březen 2019) naleznete v části [Funkce Preview v aplikaci Finance and Operations, aktualizace Platform Update 24 (březen 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).

### <a name="make-employee-fixed-compensation-available-for-future-position-assignments"></a>Zpřístupnění fixní kompenzace zaměstnance pro budoucí přiřazení pozice

Je obvyklé, že zaměstnanec je přijat do organizace s budoucím počátečním datem. Tato změna umožňuje definování fixní kompenzace pro zaměstnance s budoucími přiřazeními pozice.

## <a name="known-issues"></a>Známé problémy

### <a name="changes-to-the-core-hr-integration-template-talent-common-data-service-for-apps-to-finance-and-operations"></a>Změny šablony integrace Core HR (Talent Common Data Service for Apps do Finance and Operations)
Šablona pro Core HR byla aktualizována na šablonu rozšířeného dotazu. Ve výchozím nastavení bude proto rozšířený dotaz k dispozici pro projekty vytvořené pomocí této šablony. Všechny výchozí funkce mapování budou navíc viditelné pouze v editoru rozšířených dotazů. (Výchozí funkce mapování se zobrazí v mapování jako FN.)

Další informace o chybách mapování naleznete v tématu [Co je nového a co se změnilo v Dynamics 365 for Talent Core HR (14. prosince 2018)](https://docs.microsoft.com/dynamics365/unified-operations/talent/whats-new-talent-december-14).

Chcete-li použít novou šablonu, vytvořte nový projekt a vyberte novou šablonu integrace aplikace Talent.

Chcete-li aktualizovat svou stávající šablonu, postupujte takto.

1. Aktualizujte následující mapování:

    - **Pracovní pozice na pozice:** Odeberte toto mapování.
    - **Pracovní pozice do přiřazení práce nadřazené pozice:** Odeberte toto mapování.
    - **Pracovní pozice na základní pozici:** Přidejte nové mapování z entity **Pracovní pozice** Common Data Service for Apps na entitu **Základní pozice** Finance and Operations. Přesuňte ji do pozice 7 v číselné řadě.

        [![Mapování Pracovní pozice na základní pozici](./media/CDS-Mapping1.png)](./media/CDS-Mapping1.png)

    - **Pracovní pozice na podrobnosti pozice:** Přidejte nové mapování z entity **Pracovní pozice** Common Data Service for Apps na entitu **Podrobnosti pozice** Finance and Operations. Přesuňte ji do pozice 8 v číselné řadě.

        [![Mapování Pracovní pozice na Podrobnosti pozice](./media/CDS-Mapping2.png)](./media/CDS-Mapping2.png)

    - **Pracovní pozice na trvání pozice:** Přidejte nové mapování z entity **Pracovní pozice** Common Data Service for Apps na entitu **Trvání pozice** Finance and Operations.

        [![Mapování Pracovní pozice na Trvání pozice](./media/CDS-Mapping3.png)](./media/CDS-Mapping3.png)

    - **Pracovní pozice na hierarchie pozice:** Přidejte nové mapování z entity **Pracovní pozice** Common Data Service for Apps na entitu **Hierarchie pozice** Finance and Operations. Vyberte **Rozšířený dotazu** pro zpřístupnění rozšířeného dotazu pro váš projekt.

       [![Tlačítko Rozšířený dotaz](./media/CDS-Advanced-Query.png)](./media/CDS-Advanced-Query.png)

2. Přidejte následující mapování.
    
    [![Mapování](./media/CDS-Mapping4.png)](./media/CDS-Mapping4.png)

    1. cdm_jobpositionnumber cdm_jobspositionnumb... = POSITIONID cdm_parentjobpositionid.cdm-jobpositionnumb... = PARENTPOSITIONID cdm_validfrom cdm_validfrom = VALIDFROM cdm_validto cdm_validto = VALIDTO
       
    2. Vyberte odkaz na **Filtrování a rozšířený dotaz** vedle pole **Vyhledat**.  

    3. Vyhledejte sloupec **cdm_parentjobpositionid.cdm_jobpositionnumber** a zvolte tlačítko se šipkou dolů na jeho pravé straně.

    4. V zobrazeném dialogovém okně vyberte **Odebrat prázdné**.

    5. Vyberte **Přidat sloupec \> Přidat podmíněný sloupec** pro přidání výchozí transformace hodnoty pro HIERARCHYTYPENAME.

        [![Příkaz přidání podmíněného sloupce](./media/Add-column.png)](./media/Add-column.png)

    6. V dialogovém okně **Přidat podmíněný sloupec** zadejte **HIERARCHYTYPENAME** jako název nového sloupce.
    7. V části podmínky **If** vyberte libovolné pole, použijte **je rovno** jako vztah a zadejte libovolnou hodnotu. V částech podmínky **Then** a **Otherwise** určete, jaká by měla být výchozí hodnota. V takovém případě zadejte **Řádek** do obou částí.

        [![Dialogové okno přidání podmíněného sloupce](./media/Add-conditional-column.png)](./media/Add-conditional-column.png)

    8. Vyberte **OK** a zavřete dialogové okno **Filtrování a rozšířený dotaz**.
    9. Na stránce **Úloha mapování** vyberte nový sloupec jako zdroj pro vytvoření jiného mapování pro HIERARCHYTYPENAME .

        [![Mapování](./media/CDS-Mapping5.png)](./media/CDS-Mapping5.png)
