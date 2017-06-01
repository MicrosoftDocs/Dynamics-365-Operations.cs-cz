---
title: "Mobilní pracovní prostor prodejních objednávek"
description: "Toto téma obsahuje informace o mobilním pracovním prostoru prodejních objednávek, který je k dispozici pro mobilní aplikaci Microsoft Dynamics 365 for Operations. Tento pracovní prostor vám pomáhá mít přístup k vašim aktuálním prodejním objednávkám kdekoliv a kdykoliv."
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 11898146a13756a6bb22a769e37e8773484e0d04
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="sales-orders-mobile-workspace"></a>Mobilní pracovní prostor prodejních objednávek

[!include[banner](../includes/banner.md)]


Toto téma obsahuje informace o mobilním pracovním prostoru prodejních objednávek, který je k dispozici pro mobilní aplikaci Microsoft Dynamics 365 for Operations. Tento pracovní prostor vám pomáhá mít přístup k vašim aktuálním prodejním objednávkám kdekoliv a kdykoliv. 

<a name="overview-of-the-sales-orders-mobile-workspace"></a>Přehled mobilního pracovního prostoru prodejních objednávek
---------------------------------------------

Mobilní pracovní prostor **prodejních objednávek** přistupuje k aplikaci Microsoft Dynamics 365 for Operations a umožňuje vám zobrazit podrobné informace o jednotlivých prodejních objednávkách. Tyto informace zahrnují stav objednávky, kontaktní informace odběratele a kontaktní informace pro příjemce objednávky. Mobilní pracovní prostor **prodejních objednávek** poskytuje okamžitý přehled o prodejních objednávkách. Můžete zobrazit všechny prodejní objednávky, prodejní objednávky podle zákazníka nebo informace o konkrétní prodejní objednávce. 

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

## <a name="prerequisites"></a>Požadavky
Abyste mohli používat mobilní pracovní prostor **Prodejní objednávky**, musí správce systému zajistit splnění následujících předpokladů.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Předpoklad</th>
<th>Role</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Musí být implementována aplikace Dynamics 365 for Operations verze 1611 s aktualizací platformy 3 nebo novější.</td>
<td>Správce systému</td>
<td>Pokud nemáte aplikaci Dynamics 365 for Operations v organizaci nasazenou, správce systému by si měl přečíst téma <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment/">Nasazení ukázkového prostředí Microsoft Dynamics 365 for Operations</a>.</td>
</tr>
<tr class="even">
<td>Musí být implementován článek KB 4013633.</td>
<td>Správce systému</td>
<td>KB 4013633 (aktualizace X++ nebo oprava hotfix metadat) obsahuje čtyři mobilní pracovní prostory pro řízení řetězce dodávek. Před implementací KB 4013633 musí správce systému udělat toto:
<ol>
<li>Stáhněte KB 4013633 z webu Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Nainstalujte opravu hotfix metadat</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Vytvořte nasaditelný balíček</a>, který obsahuje model <strong>SCMMobile</strong>, a nahrajte ho do LCS.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Použijte nasaditelný balíček</a> v systému Dynamics 365 for Operations.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobilní pracovní prostor <strong>prodejních objednávek</strong> musí být publikovaný v mobilní aplikaci Dynamics 365 for Operations.</td>
<td>Správce systému</td>
<td><ol>
<li>Spusťte Dynamics 365 for Operations v prohlížeči.</li>
<li>Na stránce <strong>Systémové parametry</strong> vyberte <strong>Správa mobilních pracovních prostorů</strong>.</li>
<li>Vyberte pracovní prostor <strong>prodejních objednávek</strong>.</li>
<li>Klikněte na <strong>Publikovat mobilní pracovní prostor</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Stáhněte a nainstalujte mobilní aplikaci 365 Dynamics for Operations
Stáhněte aplikaci Microsoft Dynamics 365 for Operations z obchodu s mobilními aplikacemi.

-   Android: [Dynamics 365 for Operations - Warehousing v Google Play Store](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   iPhone: [Dynamics 365 for Operations v iTunes apps store](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Přihlaste se k mobilní aplikaci Dynamics 365 for Operations
1.  Spusťte aplikaci na svém mobilním zařízení.
2.  Zadejte adresu URL Dynamics 365 for Operations.
3.  Zadejte společnost, do které se chcete přihlásit. Například zadejte **USMF**.
4.  Při prvním přihlášení budete vyzváni k zadání uživatelského jména a hesla pro váš účet aplikace Microsoft Dynamics 365 for Operations. Zadejte své přihlašovací údaje.
5.  Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost. Všimněte si, že pokud správce systému později publikuje nový pracovní prostor, můžete vyžádat obnovení seznamu mobilních pracovních prostorů. 

    [![Vyžádání aktualizace](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-mobile-workspace"></a>Zobrazení informací o prodejních objednávkách pro odběratele s použitím mobilní pracovního prostoru
1.  Na svém mobilním zařízení vyberte pracovní prostor **Prodejní objednávky**.
2.  Vyberte **Zobrazení objednávek pro odběratele**
3.  Použijte informace o účtu nebo jménu odběratele k jeho vyhledání.
4.  Vyberte zákazníka.
5.  Vyberte **Kontaktní informace** nebo **Prodejní objednávky**. Pokud je vybraná možnost **Prodejní objednávky**, zobrazí se seznam prodejních objednávek pro zákazníka.
6.  Vyberte **Prodejní objednávka**. Zde můžete nyní zobrazit informace o řádcích prodejní objednávky, informace o dodávkách, kontaktní informace zákazníka a kontaktní informace příjemce objednávky.





