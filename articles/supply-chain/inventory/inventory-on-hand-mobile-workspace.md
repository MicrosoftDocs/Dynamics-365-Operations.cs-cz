---
title: Mobilní pracovní prostor zásob na skladě
description: Toto téma obsahuje informace o mobilním pracovním prostoru Zásoby na skladě. Tento mobilní pracovní prostor pomáhá získat mobilní přehled o rezervovaných a dostupných zásobách a je k dispozici kdykoli a kdekoli.
author: yufeihuang
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yufeihuang
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: b380da99b02fe9b7cd834eabac3498ee3b8e54a4
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811459"
---
# <a name="inventory-on-hand-mobile-workspace"></a>Mobilní pracovní prostor zásob na skladě

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Toto téma obsahuje informace o mobilním pracovním prostoru **Zásoby na skladě**. Díky tomuto pracovnímu prostor získáte přehled o rezervovaných a dostupných zásobách, a to kdykoli a kdekoli.

Tento mobilní pracovní prostor je určen k použití s mobilní aplikací Finance and Operations (Dynamics 365).

## <a name="overview"></a>Přehled
Firmy mají obvykle více dodávek a příjmů zásob každý den. Tyto pohyby neustále mění stav zásob na skladě. Mobilní pracovní prostor **Zásoby na skladě** umožňuje zobrazit stav zásob na skladě ve společnosti. Můžete tak získat nejnovější informace o skladových zásobách na mobilních zařízeních vašeho výběru. Bez ohledu na to, zda pracujete ve skladu, nákupu, prodeji, výrobě nebo řízení nebo mají jiné role, můžete přistupovat k datům na skladě kdykoli a kdekoli. 

Mobilní pracovní prostor poskytuje okamžitý přehled o stavu zásob mezi zařízeními. To umožňuje zobrazit zásoby na skladě mezi zařízeními, aktuální rezervace materiálu a nerezervované zásoby na skladě. Můžete také zadat čísla zboží k dotazování množství na skladě a provést filtrované vyhledávání produktů na skladě nebo variant. 

Mobilní pracovní prostor konkrétně poskytuje následující funkce:

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

## <a name="prerequisites"></a>Předpoklady
Předpoklady se liší podle verze aplikace Supply Chain Management, která byla nasazena ve vaší organizaci.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Předpoklady při použití aplikace Supply Chain Management
Pokud je ve vaší organizaci nasazena aplikace Supply Chain Management, správce systému musí publikovat mobilní pracovní prostor **Zásoby na skladě**. Více pokynů naleznete v tématu [Publikování mobilního pracovního prostoru](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-platform-update-3-or-later"></a>Předpoklady při použití Platform Update 3 nebo vyšší 
Pokud je ve vaší organizaci nasazena Platform Update 3 nebo novější, správce systému musí splnit následující předpoklady. 

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

<td>KB 4013633 je aktualizace X++ nebo oprava hotfix metadat obsahující mobilní pracovní prostor <strong>Zásoby na skladě</strong>. Pro implementaci KB 4013633 musí správce systému provést tyto kroky:
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Stažení oprav hotfix z Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Nainstalujte opravu hotfix metadat</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Vytvořte nasaditelný balíček</a>, který obsahuje model <strong>SCMMobile</strong>, a nahrajte ho do LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Použití nasaditelného balíčku</a></li>

</ol></td>
</tr>
<tr class="even">
<td>Publikujte mobilní pracovní prostor <strong>Zásoby na skladě</strong>.</td>
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

## <a name="view-the-on-hand-inventory-for-a-product-by-using-the-inventory-on-hand-mobile-workspace"></a>Zobrazení množství zásob produktu na skladě pomocí mobilního pracovního prostoru Zásoby na skladě

1.  Na svém mobilním zařízení vyberte pracovní prostor **Zásoby na skladě**.

2.  Vyberte **Kontrola zásob na skladě pro položku**. Zobrazí se seznam produktů, které jsou načteny do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení je načteno 50 položek, ale vývojář může tuto hodnotu změnit. Další informace pro vývojáře najdete v tématu [Mobilní platforma](../../fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
3.  Není-li vaše položka v seznamu, vyberte možnost **Vyhledávat další**. Vyhledávejte podle čísla produktu nebo přepněte do vyhledávání podle názvu produktu.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
