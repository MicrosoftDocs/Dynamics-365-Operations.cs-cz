---
title: "Domovská stránka mobilní aplikace Dynamics 365 for Operations"
description: "Toto téma popisuje mobilní aplikaci Microsoft Dynamics 365 for Operations a poskytuje odkazy na zdroje, které vám mohou pomoci ji implementovat ve vaší organizaci."
author: sericks007
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e1a9e0eeb45f011ccb2aa091e68aff92782e1ae7
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="dynamics-365-for-operations-mobile-app-home-page"></a>Domovská stránka mobilní aplikace Dynamics 365 for Operations

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]


Toto téma popisuje mobilní aplikaci Microsoft Dynamics 365 for Operations a poskytuje odkazy na zdroje, které vám mohou pomoci ji implementovat ve vaší organizaci.

<a name="overview"></a>Přehled
--------

Mobilní aplikace Microsoft Dynamics 365 for Operations umožňuje vaší organizaci zpřístupnit své obchodní procesy na mobilních zařízeních. Jakmile váš správce IT povolí funkci mobilních pracovních prostorů pro vaši organizaci, mohou se uživatelé přihlásit k aplikaci a okamžitě začít pracovat s obchodními procesy ze svých mobilních zařízení. Mobilní aplikace Dynamics 365 for Operations obsahuje následující funkce, které vám mohou pomoci zvýšit produktivitu:

-   Uživatelé mohou zobrazit, upravit a reagovat na obchodní data, i v případě, kdy mají občasné síťové připojení nebo kdy jsou jejich mobilní zařízení zcela offline. Při obnovení připojení k síti se offline datové operace automaticky zesynchronizují s aplikací Dynamics 365 for Operations.
-   IT správci nebo vývojáři mohou vytvořit a publikovat mobilní pracovní prostory, které byly vytvořeny na míru pro jejich organizace. Aplikace používá vaše existující kódy majetku. Z toho vyplývá, že není nutné znovu zavádět vaše postupy ověření, obchodní logik nebo konfiguraci zabezpečení.
-   IT správci nebo vývojáři snadno navrhnou mobilní pracovní prostory pomocí „ukaž a klikni“ návrháře pracovního prostoru, který je součástí webového klienta aplikace Dynamics 365 for Operations.
-   IT správci nebo vývojáři mohou volitelně optimalizovat offline možnosti pracovního prostoru pomocí architektury rozšíření obchodní logiky. Vzhledem k tomu, že data se stále zpracovávají, i když je zařízení v režimu offline, vaše mobilní scénáře zůstávají bohaté a plynulé i tehdy, když nemají stálé síťové připojení.

## <a name="elements-of-the-mobile-app"></a>Prvky mobilní aplikace
Navigace v mobilní aplikaci se skládá ze čtyř jednoduchých konceptů: řídicího panelu, pracovních prostorů, stránek a akcí. 

[![Navigační koncepty v mobilní aplikaci](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

-   Při spuštění aplikace přejděte do **řídicího panelu**.
-   Na řídicím panelu můžete zobrazit seznam **pracovních prostorů**, které jsou publikovány ve vašem prostředí aplikace Dynamics 365 for Operations.
-   V každé pracovním prostoru se zobrazí seznam **stránek** dostupných pro daný pracovní prostor.
-   Na stránce můžete zobrazit data, která jsou shromažďována z jedné nebo více stránek aplikace Dynamics 365 for Operations.
-   Ze stránky můžete přejít na jiné stránky pro související data, jako jsou například podrobnosti entity nebo řádky.
-   Na stránce můžete také zobrazit seznam **akcí**, které jsou k dispozici pro danou stránku.
-   Akce vám umožňují vytvořit nebo upravit stávající data.

## <a name="implementation-process"></a>Proces implementace
Následující obrázek znázorňuje procesu implementace mobilní aplikace Dynamics 365 for Operations ve vaší organizaci. 

[![](./media/mobile-implementation-process_4.png)](./media/mobile-implementation-process_4.png) 

Následující tabulka obsahuje odkazy na zdroje, které vám mohou pomoci implementovat mobilní aplikaci Dynamics 365 for Operations ve vaší organizaci. Čísla v prvním sloupci odpovídají číslovaným krokům na předchozím obrázku.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Krok</th>
<th>Role</th>
<th>Akce</th>
<th>Prostředky umožňující dokončit akci</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Správce systému</td>
<td>Implementujte Dynamics 365 for Operations pro organizaci.</td>
<td>Pokud nemáte aplikaci Dynamics 365 for Operations v organizaci nasazenou, nahlédněte do tématu <a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Nasazení ukázkového prostředí Microsoft Dynamics 365 for Operations</a>.</td>
</tr>
<tr class="even">
<td>2</td>
<td>Správce systému</td>
<td>Stáhněte a nainstalujte články znalostní báze, které umožňují mobilní pracovní prostory poskytnuté společností Microsoft.</td>
<td>Nahlédněte do části &quot;Předpoklady&quot; v tématu o mobilním pracovním prostoru, který chce vaše organizace použít:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Mobilní pracovní prostory Řízení nákladů</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Mobilní pracovní prostor zásob na skladě</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Mobilní pracovní prostory prodejních objednávek</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Mobilní pracovní prostor dodavatelské spolupráce</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Mobilní pracovní prostor zadání času projektu</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>Správce systému</td>
<td>Publikujte mobilní pracovní prostory, které poskytuje společnost Microsoft.</td>
<td>Nahlédněte do části &quot;Předpoklady&quot; v tématu o mobilním pracovním prostoru, který chce vaše organizace použít:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Mobilní pracovní prostory Řízení nákladů</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Mobilní pracovní prostor zásob na skladě</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Mobilní pracovní prostory prodejních objednávek</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Mobilní pracovní prostor dodavatelské spolupráce</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Mobilní pracovní prostor zadání času projektu</a></li>
</ul></td>
</tr>
<tr class="even">
<td>4</td>
<td>Vývojáři nebo nezávislí výrobci softwaru</td>
<td>Použijte mobilní architekturu aplikace Dynamics 365 k vytváření vlastních mobilních pracovních prostorů.</td>
<td><ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Mobilní architektura aplikace Dynamics 365 for Operations</a></li>
<li><a href="http://ax.help.dynamics.com/en/wiki/operations-mobile-workspace-x-apis/">X ++ API pracovního prostoru aplikace Dynamics 365 for Operations</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV</td>
<td>Vytvořte nasaditelný balíček, který obsahuje vlastní mobilní pracovní prostory, a odešlete balíček do služby Microsoft Dynamics Lifecycle Services (LCS).</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Generování nasaditelného balíčku</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>Správce systému</td>
<td>Použijte nasaditelný balíček obsahující vlastní pracovní prostory, které poskytl nezávislý výrobce softwaru.</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Použití nasaditelného balíčku v systému Microsoft Dynamics 365 for Operations</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Správce systému</td>
<td>Publikujte vlastní mobilní pracovní prostory, které poskytuje nezávislý výrobce softwaru.</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publikování mobilního pracovního prostoru</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Uživatel</td>
<td>Stáhněte a nainstalujte mobilní aplikaci 365 Dynamics for Operations.</td>
<td><ul>
<li>Android: <a href="https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile">Dynamics 365 for Operations v Google Play Store</a></li>
<li>iPhone: <a href="https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8">Dynamics 365 for Operations v obchodě s aplikacemi iTunes</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>9</td>
<td>Uživatel</td>
<td>Přihlaste se a používejte mobilní aplikaci Dynamics 365 for Operations. Aplikaci zahrnuje mobilní pracovní prostory, které byly publikovány.</td>
<td>Společnost Microsoft poskytuje následující mobilní pracovní prostory:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Mobilní pracovní prostory Řízení nákladů</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Mobilní pracovní prostor zásob na skladě</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Mobilní pracovní prostory prodejních objednávek</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Mobilní pracovní prostor dodavatelské spolupráce</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Mobilní pracovní prostor zadání času projektu</a></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Viz také
--------

[Nedávno uvolněné mobilní pracovní prostory pro mobilní aplikaci Dynamics 365 for Operations](mobile-workspaces-released.md)





