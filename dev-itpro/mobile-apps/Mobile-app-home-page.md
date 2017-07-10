---
title: "Domovská stránka mobilní aplikace"
description: "Toto téma popisuje mobilní aplikaci Microsoft Dynamics 365 for Unified Operations a poskytuje odkazy na zdroje, které vám mohou pomoci ji implementovat ve vaší organizaci."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 663a03dc37cc1631bd285a76ef564993a34ed057
ms.contentlocale: cs-cz
ms.lasthandoff: 06/20/2017


---

# <a name="mobile-app-home-page"></a>Domovská stránka mobilní aplikace

[!include[banner](../includes/banner.md)]

Toto téma popisuje mobilní aplikaci Microsoft Dynamics 365 for Unified Operations a poskytuje odkazy na zdroje, které vám mohou pomoci ji implementovat ve vaší organizaci.

> [!NOTE]
> Aplikace měla dříve název *Microsoft Dynamics 365 for Finance and Operations*.

<a name="overview"></a>Přehled
--------

Mobilní aplikace umožňuje vaší organizaci zpřístupnit své obchodní procesy na mobilních zařízeních. Jakmile váš správce IT povolí mobilní pracovní prostory pro vaši organizaci, mohou se uživatelé přihlásit k aplikaci a okamžitě začít pracovat s obchodními procesy ze svých mobilních zařízení. Mobilní aplikace obsahuje následující funkce, které vám mohou pomoci zvýšit produktivitu:

- Uživatelé mohou zobrazit, upravit a reagovat na obchodní data, i v případě, kdy mají občasné síťové připojení nebo kdy jsou jejich mobilní zařízení zcela offline. Poté, co zařízení obnoví připojení k síti, offline datové operace se automaticky synchronizují s aplikací Dynamics 365 for Finance and Operations, Enterprise edition nebo Microsoft Dynamics 365 for Finance and Operations.
- IT správci nebo vývojáři mohou vytvořit a publikovat mobilní pracovní prostory, které byly vytvořeny na míru pro jejich organizace. Aplikace používá vaše existující kódy majetku. Z toho vyplývá, že není nutné znovu zavádět vaše postupy ověření, obchodní logik nebo konfiguraci zabezpečení.
- IT správci nebo vývojáři mohou snadno navrhnout mobilní pracovní prostory pomocí „ukaž a klikni“ návrháře pracovního prostoru, který je součástí webového klienta.
- IT správci nebo vývojáři mohou volitelně optimalizovat offline možnosti pracovního prostoru pomocí architektury rozšíření obchodní logiky. Vzhledem k tomu, že data se stále zpracovávají, i když je zařízení v režimu offline, vaše mobilní scénáře zůstávají bohaté a plynulé i tehdy, když nemají stálé síťové připojení.

## <a name="elements-of-the-mobile-app"></a>Prvky mobilní aplikace
Navigace v mobilní aplikaci se skládá ze čtyř základních konceptů: řídicího panelu, pracovních prostorů, stránek a akcí. 

[![Navigační koncepty v mobilní aplikaci](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

1. Při spuštění aplikace přejděte do **řídicího panelu**.
2. Na řídicím panelu můžete zobrazit seznam **pracovních prostorů**, které jsou publikované.
3. V každé pracovním prostoru se zobrazí seznam **stránek** dostupných pro daný pracovní prostor.
4. Jakmile se dostanete na stránku, můžete provést několik akcí. Několik příkladů:

    - Zobrazení podrobných dat
    - Přechod na jiné stránky pro související data, jako jsou například podrobnosti entity nebo řádky.
    - Zobrazení seznamu **akcí**, které jsou k dispozici pro danou stránku. Akce vám umožňují vytvořit nebo upravit stávající data.

## <a name="implementation-process"></a>Proces implementace
Následující obrázek znázorňuje proces implementace mobilních pracovních prostorů, které poskytuje společnost Microsoft, a vlastních mobilních pracovních prostorů. 

![Proces implementace mobilní aplikace](./media/Mobile-implementation-process-5.png)

Následující tabulka obsahuje odkazy na zdroje, které vám mohou pomoci při implementaci mobilních pracovních prostorů poskytovaných společností Microsoft a vlastních mobilních pracovních prostorů Čísla v prvním sloupci odpovídají číslovaným krokům na předchozím obrázku.

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
<td>Implementace aplikace Finance and Operations nebo Finance and Operations ve vaší organizaci.</td>
<td><ul><li>Pokud jste dosud nenainstalovali verzi aplikace Microsoft Dynamics 365, podívejte se do části <a href="../deployment/deploy-demo-environment.md">Nasazení prostředí pro ukázku</a>.</li><li>Pokud chcete zobrazit seznam mobilních pracovních prostorů, které lze použít, přejděte do tématu <a href="mobile-workspaces-released.md">Nedávno vydané mobilní pracovní prostory</a>.</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>Správce systému</td>
<td><strong>Pokud používáte aplikaci Microsoft Dynamics 365 for Finance and Operations verze 1611:</strong> Stáhněte si a nainstalujte články znalostní báze umožňující mobilní pracovní prostory, které poskytuje Microsoft.</td>
<td>Další informace naleznete v následujících tématech:
<ul>

<li><a href="/dynamics365/unified-operations/financials/cost-accounting/cost-controlling-mobile-workspace">Mobilní pracovní prostory Řízení nákladů</a></li>
<li><a href="/dynamics365/unified-operations/supply-chain/inventory/inventory-on-hand-mobile-workspace">Mobilní pracovní prostor zásob na skladě</a></li>
<li><a href="/dynamics365/unified-operations/supply-chain/sales-marketing/sales-orders-mobile-workspace">Mobilní pracovní prostory prodejních objednávek</a></li>
<li><a href="/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Mobilní pracovní prostor dodavatelské spolupráce</a></li>
<li><a href="/dynamics365/unified-operations/financials/project-management/project-time-entry-mobile-workspace">Mobilní pracovní prostor zadání času projektu</a></li>
<li><a href="/dynamics365/unified-operations/financials/expense-management/expense-management-mobile-workspace">Mobilní pracovní prostor Správa výdajů</a></li>

</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>Správce systému</td>
<td>Publikujte mobilní pracovní prostory, které poskytuje společnost Microsoft.</td>
<td><a href="publish-mobile-workspace.md">Publikování mobilního pracovního prostoru</a>
</td>
</tr>
<tr class="even">
<td>4</td>
<td>Vývojáři nebo nezávislí výrobci softwaru</td>
<td>Použijte mobilní architekturu k vytváření vlastních mobilních pracovních prostorů.</td>
<td><ul>
<li><a href="mobile-platform.md">Mobilní architektura</a></li>
<li><a href="http://ax.help.dynamics.com/en/wiki/operations-mobile-workspace-x-apis/">Pracovní prostor X++ rozhraní API</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV</td>
<td>Vytvořte nasaditelný balíček, který obsahuje vlastní mobilní pracovní prostory, a odešlete balíček do služby Microsoft Dynamics Lifecycle Services (LCS).</td>
<td><a href="../deployment/create-apply-deployable-package.md">Vytvoření nasaditelného balíčku</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>Správce systému</td>
<td>Použijte nasaditelný balíček obsahující vlastní pracovní prostory, které poskytl nezávislý výrobce softwaru (ISV).</td>
<td><a href="../deployment/apply-deployable-package-system.md">Použití nasaditelného balíčku</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Správce systému</td>
<td>Publikujte vlastní mobilní pracovní prostory, které poskytuje nezávislý výrobce softwaru.</td>
<td><a href="publish-mobile-workspace.md">Publikování mobilního pracovního prostoru</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Uživatel</td>
<td>Stáhněte a nainstalujte mobilní aplikaci.</td>
<td><ul>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850662">Pro telefony Android</a></li>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850663">Pro telefony iPhone</a></li></ul>
</td>
</tr>
<tr class="odd">
<td>9</td>
<td>Uživatel</td>
<td>Přihlaste se do mobilní aplikace a použijte ji. Aplikaci zahrnuje mobilní pracovní prostory, které byly publikovány správcem systému.</td>
<td>Pokud chcete zobrazit seznam mobilních pracovních prostorů poskytnutých společností Microsoft, přejděte do tématu <a href="mobile-workspaces-released.md">Nedávno vydané mobilní pracovní prostory</a>.
</td>
</tr>
</tbody>
</table>

