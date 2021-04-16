---
title: Mobilní pracovní prostor Řízení nákladů
description: Toto téma obsahuje informace o mobilním pracovním prostoru řízení nákladů. Tento pracovní prostor umožňuje manažerům nákladového střediska zobrazit informace o výkonu nákladového střediska kdykoli a odkudkoli.
author: AndersGirke
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMMobileCostObjectOverviewDetailsCurrentPeriod, CAMMobileCostObjectList, CAMMobileCostObjectOverviewDetailsPreviousPeriod, CAMMobileCostObjectOverview, CAMMobileCostObjectOverviewDetailsYearToDate, CAMMobileCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 6ab1edf6f3c1053f65c6d89786de5bfcc6c268e9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822944"
---
# <a name="cost-controlling-mobile-workspace"></a>Mobilní pracovní prostor Řízení nákladů

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o mobilním pracovním prostoru **Řízení nákladů**. Tento pracovní prostor umožňuje manažerům nákladového střediska zobrazit informace o výkonu nákladového střediska kdykoli a odkudkoli.

Tento mobilní pracovní prostor je určen k použití s mobilní aplikací Finance and Operations.

## <a name="overview"></a>Přehled
Mobilní pracovní prostor **Řízení nákladů** poskytuje okamžitý přehled o aktuálním výkonu nákladových středisek porovnáním skutečných nákladů s rozpočtovými náklady. Můžete přejít na podrobnosti stavů jednotlivých prvků nákladů.

Zaměstnanec například obdrží pozvánku na mezinárodní konferenci, ale organizace musí pokrývat všechny cestovní výdaje. Zaměstnanec se zeptá svého manažera, zda se může konference zúčastnit. Manažer rychle otevře mobilní pracovní prostor **řízení nákladů** na svém mobilním telefonu a zjistí, zda má rozpočet pro zaměstnance k účasti na konferenci.

### <a name="data-security"></a>Zabezpečení dat
Data v mobilním pracovním prostoru **řízení nákladů** jsou zabezpečena pomocí pověření uživatele. Manažeři nákladového střediska mohou vidět data pouze pro své nákladové středisko. Úroveň zabezpečení přístupu je spravována v rámci modulu **Nákladové účetnictví**.

Účetní definují konfiguraci mobilního pracovního prostoru **řízení nákladů** v modulu **Nákladové účetnictví**. Po publikování pracovního prostoru do mobilní aplikace bude v aplikaci pracovní prostor k dispozici. Všichni manažeři nákladových středisek v organizaci tak mohou prohlížet data ve stejném formátu.

### <a name="actions-views-and-links"></a>Akce, zobrazení a odkazy
Mobilní pracovní prostor **Řízení nákladů** poskytuje následující akce, zobrazení a odkazy:

-   **Akce:**

    -   Pomocí možnosti **Vybrat konfiguraci** vyberte rozložení.
    -   Pomocí možnosti **Vybrat nákladový objekt** vyberte nákladová střediska, podle kterých budete filtrovat data.
    
        > [!NOTE]
        > Nákladová střediska, která jsou zobrazená v seznamu závisí na přístupu, který je udělený v modulu **Nákladové účetnictví**.

-   **Zobrazení:** Podle toho, jaké akce jsou vybrané a jaká je konfigurace v modulu **Nákladové účetnictví**, můžete zobrazit následující informace na kartách:

    -   Skutečnost a rozpočet (aktuální období)
    -   Skutečnost a revidovaný rozpočet (aktuální období)
    -   Skutečnost vs. rozpočet (předchozí období)
    -   Skutečnost vs. revidovaný rozpočet (předchozí období)
    -   Skutečnost vs. rozpočet (od začátku roku)
    -   Skutečnost vs. revidovaný rozpočet (od začátku roku)

    Na každé kartě jsou zobrazeny následující hodnoty: Skutečné, Rozpočet, Odchylka a Odchylka v %.

-   **Odkazy:**

    -   Podrobnosti za aktuální období
    -   Podrobnosti za předchozí období
    -   Podrobnosti za období od začátku roku

    Při výběru odkazu se zobrazí karta pro každý nákladový prvek. Na každé kartě jsou uvedeny následující částky: skutečnost, rozpočet, odchylka rozpočtu, % odchylky rozpočtu, revidovaný rozpočet, odchylka revidovaného rozpočtu a % odchylky revidovaného rozpočtu.
    
    [![Karta pro prvek nákladů ](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>Předpoklady
Předpoklady se liší podle verze aplikace Microsoft Dynamics 365, která byla nasazena ve vaší organizaci.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a>Předpoklady při použití Microsoft Dynamics 365 Finance
Pokud je ve vaší organizaci nasazena aplikace Finance, správce systému musí publikovat mobilní pracovní prostor **Řízení nákladů**. Více pokynů naleznete v tématu [Publikování mobilního pracovního prostoru](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Předpoklady při použití verze 1611 s aktualizací Platform Update 3 nebo vyšší
Pokud je ve vaší organizaci nasazena verze 1611 s aktualizací Platform update 3 nebo novější, správce systému musí dokončit následující předpoklady.

<table>
<thead>
<tr class="header">
<th>Předpoklad</th>
<th>Role</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementujte opravu KB 4013633.</td>
<td>Správce systému</td>

<td>KB 4013633 je X ++ aktualizace nebo oprava hotfix metadat obsahující mobilní pracovní prostor <strong>Řízení nákladů</strong>. Pro implementaci KB 4013633 musí správce systému provést tyto kroky:
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Stažení oprav hotfix z Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Nainstalujte opravu hotfix metadat</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Vytvořte nasaditelný balíček</a>, který obsahuje model <strong>SCMMobile</strong>, a nahrajte ho do LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Použití nasaditelného balíčku</a></li>

</ol></td>
</tr>
<tr class="even">
<td>Publikování mobilního pracovního prostoru <strong>Řízení nákladů</strong>.</td>
<td>Správce systému</td>
<td>Viz téma <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publikování mobilního pracovního prostoru</a>.</td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a>Stáhněte a nainstalujte mobilní aplikaci
Stáhněte a nainstalujte mobilní aplikaci Finance and Operations:

-   [Pro telefony Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Pro telefony iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Přihlaste se do mobilní aplikace

1.  Spusťte aplikaci na svém mobilním zařízení.
2.  Zadejte adresu URL aplikace Dynamics 365.
3.  Při prvním přihlášení se zobrazí výzva k zadání uživatelského jména a hesla. Zadejte své přihlašovací údaje.
4.  Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost. Všimněte si, že pokud správce systému později publikuje nový pracovní prostor, budete muset aktualizovat seznam mobilních pracovních prostorů.

[![Vyžádání aktualizace](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a>Zobrazení výkonu nákladového střediska pomocí mobilního pracovního prostoru řízení nákladů

1.  Na svém mobilním zařízení vyberte pracovní prostor **Řízení nákladů**.
2.  Vyberte **Řízení objektu nákladů**.
3.  Vyberte **Akce**.
4.  Vyberte **Vybrat konfiguraci** pro výběr rozvržení řízení nákladů.
5.  Vyberte **Hotovo**.
6.  Vyberte **Akce**.
7.  Vyberte tlačítko **Zvolit objekt nákladů** a vyberte nákladová střediska, ke kterým vám byl udělen přístup.
8.  Vyberte **Hotovo**.
9.  Zobrazte celkovou výkonnost vašeho nákladového střediska.
10. Vyberte odkaz **Podrobnosti pro aktuální období**.
11. Zobrazte výkonnost jednotlivých prvků nákladů.
12. Můžete také vyhledat konkrétní prvky nákladů.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]