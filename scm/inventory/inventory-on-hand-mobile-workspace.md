---
title: "Mobilní pracovní prostor zásob na skladě"
description: "Toto téma obsahuje informace o mobilním pracovním prostoru zásob na skladě, který je k dispozici pro mobilní aplikaci Microsoft Dynamics 365 for Operations. Tento mobilní pracovní prostor pomáhá získat mobilní přehled o rezervovaných a dostupných zásobách a je k dispozici kdykoli a kdekoli."
author: YuyuScheller
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e703ae80800b993ebca1c7bee455af1be41c7d5f
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="inventory-on-hand-mobile-workspace"></a>Mobilní pracovní prostor zásob na skladě

[!include[banner](../includes/banner.md)]


Toto téma obsahuje informace o mobilním pracovním prostoru zásob na skladě, který je k dispozici pro mobilní aplikaci Microsoft Dynamics 365 for Operations. Tento mobilní pracovní prostor pomáhá získat mobilní přehled o rezervovaných a dostupných zásobách a je k dispozici kdykoli a kdekoli.

<a name="overview-of-the-inventory-on-hand-mobile-workspace"></a>Přehled mobilního pracovního prostoru zásob na skladě
--------------------------------------------------

Firmy mají obvykle více dodávek a příjmů zásob každý den. Tyto pohyby neustále mění stav zásob na skladě. Mobilní centrum **zásob na skladě** umožňuje zobrazit stav zásob na skladě společnosti tak, aby bylo možné získat nejnovější přehled o skladových zásobách na mobilních zařízeních podle vašeho výběru. Bez ohledu na to, zda pracujete ve skladu, nákupu, prodeji, výrobě nebo řízení nebo mají jiné role, můžete přistupovat k datům na skladě kdykoli a kdekoli. Mobilní pracovní prostor poskytuje okamžitý přehled o stavu zásob mezi zařízeními. To umožňuje zobrazit zásoby na skladě mezi zařízeními, aktuální rezervace materiálu a nerezervované zásoby na skladě. Můžete také zadat čísla zboží k dotazování množství na skladě a provést filtrované vyhledávání produktů na skladě nebo variant. Mobilní pracovní prostor konkrétně poskytuje následující funkce:

-   Můžete vyhledávat podle čísla produktu nebo názvu produktu k zobrazení stavu zásob na skladě.
-   U vybraných produktů můžete zobrazit následující informace:
    -   Zásoby na skladě podle pracoviště
    -   Množství zásob podle skladu
    -   Zásoby na skladě podle pracoviště
    -   Zásoby na skladě podle šarže (pro kontrolované šarže produktů)
    -   Zásoby na skladě podle stavu zásob
-   Zásoby na skladě produktu jsou zobrazeny následujícím způsobem:
    -   Podle fyzické inventury (Toto zobrazení představuje celkovou částku).
    -   Podle fyzické rezervy (Toto zobrazení představuje rezervovanou částku).
    -   Fyzicky k dispozici (Toto zobrazení představuje částku k dispozici, která nemá žádné rezervace.)

## <a name="prerequisites"></a>Požadavky
Abyste mohli používat mobilní pracovní prostor **Zásoby na skladě**, musí správce systému zajistit splnění následujících předpokladů.

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
<td>Musí být implementována aplikace Microsoft Dynamics 365 for Operations verze 1611 s aktualizací platformy 3 nebo novější.</td>
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
<td>Mobilní pracovní prostor <strong>Zásoby na skladě</strong> musí být publikovaný v mobilní aplikaci Dynamics 365 for Operations.</td>
<td>Správce systému</td>
<td><ol>
<li>Spusťte Dynamics 365 for Operations v prohlížeči.</li>
<li>Na stránce <strong>Systémové parametry</strong> vyberte <strong>Správa mobilních pracovních prostorů</strong>.</li>
<li>Zvolte <strong>pracovní prostor zásob na skladě</strong>.</li>
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

## <a name="view-the-onhand-inventory-for-a-product-by-using-the-inventory-onhand-mobile-workspace"></a>Zobrazte množství na skladě pro produkt pomocí mobilního pracovního prostoru množství na skladě
1.  Na svém mobilním zařízení vyberte pracovní prostor **Zásoby na skladě**.
2.  Vyberte **Kontrola zásob na skladě pro položku**. Zobrazí se seznam produktů, které jsou načteny do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení je načteno 50 položek, ale vývojář může tuto hodnotu změnit. Další informace naleznou vývojáři v tématu [Mobilní platforma aplikace Dynamics 365 for Operations](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/).
3.  Pokud položka není v seznamu uvedena, vyberte **Hledat více**, chcete-li provést online hledat v Dynamics 365 for Operations. Vyhledávejte podle čísla produktu nebo přepněte do vyhledávání podle názvu produktu.
4.  Vyberte produkt. Pokud položka obsahuje obrázek, obrázek je zobrazen.
5.  Vyberte jednu z následujících možností k zobrazení stavu zásob na skladě:
    -   Zobrazení zásob na skladě podle pracoviště
    -   Zobrazení zásob na skladě podle skladu
    -   Zobrazení zásob na skladě podle místa
    -   Zobrazení zásob na skladě podle šarže (pro kontrolované šarže produktů)
    -   Zobrazení zásob na skladě podle zboží

    Zásoby na skladě produktu jsou zobrazeny následujícím způsobem:
    -   Podle fyzické inventury (Toto zobrazení představuje celkovou částku).
    -   Podle fyzické rezervy (Toto zobrazení představuje rezervovanou částku).
    -   Fyzicky k dispozici (Toto zobrazení představuje částku k dispozici, která nemá žádné rezervace.)






