---
title: "Mobilní pracovní prostor Řízení nákladů"
description: "Toto téma obsahuje informace o mobilním pracovním prostoru Řízení nákladů, který je k dispozici pro mobilní aplikaci Microsoft Dynamics 365 for Operations. Tento pracovní prostor umožňuje manažerům nákladového střediska zobrazit informace o výkonu nákladového střediska kdykoli a odkudkoli."
author: YuyuScheller
manager: AnnBe
ms.date: 05/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 31a9650774b2ddb70827ffa210154ca10c761236
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="cost-controlling-mobile-workspace"></a>Mobilní pracovní prostor Řízení nákladů

[!include[banner](../includes/banner.md)]


Toto téma obsahuje informace o mobilním pracovním prostoru Řízení nákladů, který je k dispozici pro mobilní aplikaci Microsoft Dynamics 365 for Operations. Tento pracovní prostor umožňuje manažerům nákladového střediska zobrazit informace o výkonu nákladového střediska kdykoli a odkudkoli. 

<a name="overview-of-the-cost-controlling-mobile-workspace"></a>Přehled mobilního pracovního prostoru řízení nákladů
-------------------------------------------------

Mobilní pracovní prostor **Řízení nákladů** poskytuje okamžitý přehled o aktuálním výkonu nákladových středisek porovnáním skutečných nákladů s rozpočtovými náklady. Můžete přejít na stavy jednotlivých prvků nákladů. Zaměstnanec například obdrží pozvánku na mezinárodní konferenci, ale organizace musí pokrývat všechny cestovní výdaje. Zaměstnanec se zeptá svého manažera, zda se může konference zúčastnit. Manažer rychle otevře mobilní pracovní prostor **řízení nákladů** na svém mobilním telefonu a zjistí, zda má rozpočet pro zaměstnance k účasti na konferenci.

### <a name="data-security"></a>Zabezpečení dat

Data v mobilním pracovním prostoru **řízení nákladů** jsou zabezpečena pomocí pověření uživatele. Manažeři nákladového střediska mohou vidět data pouze pro své nákladové středisko. Úroveň zabezpečení přístupu je spravována v rámci modulu **Nákladové účetnictví**. Účetní definují konfiguraci mobilního pracovního prostoru **řízení nákladů** v modulu **Nákladové účetnictví**. Po publikování pracovního prostoru do mobilní aplikace Microsoft Dynamics 365 for Operations bude v aplikaci pracovní prostor k dispozici. Všichni manažeři nákladových středisek v organizaci tak mohou prohlížet data ve stejném formátu.

### <a name="actions-views-and-links"></a>Akce, zobrazení a odkazy

Mobilní pracovní prostor **řízení nákladů** pro aplikaci Dynamics 365 for Operations nabízí následující akce, zobrazení a odkazy:

-   **Akce:**
    -   Pomocí možnosti **Vybrat konfiguraci** vyberte rozložení.
    -   Pomocí možnosti **Vybrat nákladový objekt** vyberte nákladová střediska, podle kterých budete filtrovat data. **Poznámka:** Nákladová střediska, která jsou zobrazená v seznamu závisí na přístupu, který je udělený v modulu **Nákladové účetnictví**.
-   **Zobrazení:** Podle toho, jaké akce jsou vybrané a jaká je konfigurace v modulu **Nákladové účetnictví**, můžete zobrazit následující informace na kartách.
    -   Skutečnost vs. rozpočet (aktuální období)
    -   Skutečnost vs. revidovaný rozpočet (aktuální období)
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
    
    [![Karta pro prvek nákladů ](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="prerequisites"></a>Požadavky
Abyste mohli používat mobilní pracovní prostor **Řízení nákladů**, musí správce systému zajistit splnění následujících předpokladů.

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
<td>Pokud nemáte aplikaci Dynamics 365 for Operations v organizaci nasazenou, správce systému by si měl přečíst téma <a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">Nasazení ukázkového prostředí Microsoft Dynamics 365 for Operations</a>.</td>
</tr>
<tr class="even">
<td>Musí být implementován článek KB 4013633.</td>
<td>Správce systému</td>
<td>KB 4013633 (aktualizace X++ nebo oprava hotfix metadat) obsahuje čtyři mobilní pracovní prostory pro řízení řetězce dodávek. Před implementací KB 4013633 musí správce systému udělat toto:
<ol>
<li>Stáhněte KB 4013633 z webu Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">Nainstalujte opravu hotfix metadat</a>.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">Vytvořte nasaditelný balíček</a>, který obsahuje model <strong>SCMMobile</strong>, a nahrajte ho do LCS.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">Použijte nasaditelný balíček</a> v systému Dynamics 365 for Operations.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobilní pracovní prostor <strong>Řízení nákladů</strong> musí být publikovaný v mobilní aplikaci Dynamics 365 for Operations.</td>
<td>Správce systému</td>
<td><ol>
<li>Spusťte Dynamics 365 for Operations v prohlížeči.</li>
<li>Na stránce <strong>Systémové parametry</strong> vyberte <strong>Správa mobilních pracovních prostorů</strong>.</li>
<li>Vyberte pracovní prostor <strong>Přehled objektu nákladů</strong>.</li>
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





