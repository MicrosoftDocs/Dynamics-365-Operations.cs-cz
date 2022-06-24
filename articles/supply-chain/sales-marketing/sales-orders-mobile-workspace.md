---
title: Mobilní pracovní prostor prodejních objednávek
description: Tento článek obsahuje informace o mobilním pracovním prostoru Prodejní objednávky. Tento pracovní prostor vám pomáhá mít aktuální přehled o prodejních objednávkách kdekoliv a kdykoliv.
author: Henrikan
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: henrikan
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: fc04a90c0c071508c9ebee57862a029de0e58f9a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844757"
---
# <a name="sales-orders-mobile-workspace"></a>Mobilní pracovní prostor prodejních objednávek

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Tento článek obsahuje informace o mobilním pracovním prostoru **Prodejní objednávky**. Tento pracovní prostor vám pomáhá mít aktuální přehled o prodejních objednávkách kdekoliv a kdykoliv. 

Tento mobilní pracovní prostor je určen k použití s mobilní aplikací Finance and Operations (Dynamics 365).

## <a name="overview"></a>Přehled
Mobilní pracovní prostor **Prodejní objednávky** umožňuje zobrazit podrobné informace o jednotlivých prodejních objednávkách. Tyto informace zahrnují stav objednávky, kontaktní informace odběratele a kontaktní informace pro příjemce objednávky. Mobilní pracovní prostor **prodejních objednávek** poskytuje okamžitý přehled o prodejních objednávkách. Můžete zobrazit všechny prodejní objednávky, prodejní objednávky podle zákazníka nebo informace o konkrétní prodejní objednávce. 

Mobilní pracovní prostor obsahuje dvě zobrazení, která vám umožní analyzovat prodejní objednávky do hloubky.

### <a name="view-all-sales-orders"></a>Zobrazit všechny prodejní objednávky
Toto zobrazení obsahuje seznam všech prodejních objednávek.

-   Použijte jeden z následujících filtrů pro výběr prodejních objednávek, které se mají zobrazit:

    -   Hledat podle prodejní objednávky
    -   Hledat podle odběratele
    -   Hledat podle jména odběratele
    -   Hledat podle stavu
    -   Hledat podle stavu storna
    -   Hledat podle data a času vytvoření
    
-   Po výběru prodejních objednávek můžete zobrazit podrobnosti o konkrétních objednávkách. Konkrétně můžete zobrazit následující informace:

    -   Informace o názvu a adrese zákazníka
    -   Různá data pro prodejní objednávku, jako je například požadované datum expedice a potvrzené datum expedice
    -   Kontaktní informace pro příjemce objednávky
    -   Kontaktní informace odběratele
    -   Řádky objednávky
    -   Dodávky, které ukazují, jak a kdy byla prodejní objednávka dodána

### <a name="view-orders-for-a-customer"></a>Zobrazení objednávek pro odběratele
Toto zobrazení uvádí seznam prodejních objednávek podle odběratele.

-   Chcete-li zobrazit objednávky pro odběratele, použijte jeden z následujících filtrů:

    -   Hledat podle jména
    -   Hledat podle účtu

-   Po výběru odběratele můžete zobrazit následující informace:

    -   Název skupinu odběratelů
    -   Kontaktní informace odběratele
    -   Prodejní objednávky zákazníka a podrobnosti těchto prodejních objednávek:
    
        -   Informace o názvu a adrese zákazníka
        -   Různá data prodejních objednávek
        -   Kontaktní informace pro příjemce objednávky
        -   Kontaktní informace odběratele
        -   Řádky objednávky
        -   Dodávky, které ukazují, jak a kdy byla prodejní objednávka dodána

## <a name="prerequisites"></a>Předpoklady
Předpoklady se liší podle verze aplikace Microsoft Dynamics 365, která byla nasazena ve vaší organizaci.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Předpoklady při použití aplikace Supply Chain Management 
Pokud je ve vaší organizaci nasazena aplikace Supply Chain Management, správce systému musí publikovat mobilní pracovní prostor **Prodejní objednávky**. Více pokynů naleznete v tématu [Publikování mobilního pracovního prostoru](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Předpoklady při použití Dynamics 365 for Operations verze 1611 s aktualizací Platform Update 3 nebo vyšší
Pokud je ve vaší organizaci nasazena aplikace Dynamics 365 for Operations verze 1611 s aktualizací platformy 3 nebo novější, správce systému musí dokončit následující předpoklady. 

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

<td>KB 4013633 je X ++ aktualizace nebo oprava hotfix metadat obsahující mobilní pracovní prostor <strong>Prodejní objednávky</strong>. Pro implementaci KB 4013633 musí správce systému provést tyto kroky:
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Stažení oprav hotfix z Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Nainstalujte opravu hotfix metadat</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Vytvořte nasaditelný balíček</a>, který obsahuje model <strong>SCMMobile</strong>, a nahrajte ho do LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Použití nasaditelného balíčku</a></li>

</ol></td>
</tr>
<tr class="even">
<td>Publikujte mobilní pracovní prostor <strong>Prodejní objednávky</strong>.</td>
<td>Správce systému</td>
<td>Viz téma <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publikování mobilního pracovního prostoru</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Stáhněte a nainstalujte mobilní aplikaci
Stáhněte a nainstalujte mobilní aplikaci Finance and Operations (Dynamics 365):

-   [Pro telefony Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Pro telefony iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Přihlaste se do mobilní aplikace

1.  Spusťte aplikaci na svém mobilním zařízení.
2.  Zadejte adresu URL aplikace Dynamics 365.
3.  Při prvním přihlášení se zobrazí výzva k zadání uživatelského jména a hesla. Zadejte své přihlašovací údaje.
4.  Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost. Všimněte si, že pokud správce systému později publikuje nový pracovní prostor, budete muset aktualizovat seznam mobilních pracovních prostorů.

[![Vyžádání aktualizace.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-sales-order-mobile-workspace"></a>Zobrazení informací o prodejních objednávkách pro odběratele s použitím mobilního pracovního prostoru Prodejní objednávky

1.  Na svém mobilním zařízení vyberte pracovní prostor **Prodejní objednávky**.
2.  Vyberte **Zobrazení objednávek pro odběratele**
3.  Použijte informace o účtu nebo jménu odběratele k jeho vyhledání.
4.  Vyberte zákazníka.
5.  Vyberte **Kontaktní informace** nebo **Prodejní objednávky**. Pokud je vybraná možnost **Prodejní objednávky**, zobrazí se seznam prodejních objednávek pro zákazníka.
6.  Vyberte **Prodejní objednávka**. Zde můžete nyní zobrazit informace o řádcích prodejní objednávky, informace o dodávkách, kontaktní informace zákazníka a kontaktní informace příjemce objednávky.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
