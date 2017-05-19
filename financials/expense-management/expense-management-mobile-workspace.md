---
title: "Mobilní pracovní prostor správy výdajů"
description: "Toto téma obsahuje informace o mobilním pracovním prostoru správy výdajů, který je k dispozici pro mobilní aplikaci Microsoft Dynamics 365 for Operations. Tento pracovní prostor umožňuje uživatelům zdokumentovat a odeslat účtenku, aby ji mohli připojit později k sestavě výdajů. Mobilní pracovní prostor také umožní uživatelům rychle vytvářet řádek výdajů pomocí připojené účtenky."
author: annbe
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: end user, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 8bc47c5b170fd7dd8f6288682aad6eae1d2dc09a
ms.openlocfilehash: 9d3b7a4d5184c3c4958f4298f1d3dd4de0cd06d6
ms.contentlocale: cs-cz
ms.lasthandoff: 04/26/2017


---

# <a name="expense-management-mobile-workspace"></a>Mobilní pracovní prostor správy výdajů

[!include[banner](../includes/banner.md)]

"[!include[banner](../includes/banner.md)]"


Toto téma obsahuje informace o mobilním pracovním prostoru správy výdajů, který je k dispozici pro mobilní aplikaci Microsoft Dynamics 365 for Operations. Tento pracovní prostor umožňuje uživatelům zdokumentovat a odeslat účtenku, aby ji mohli připojit později k sestavě výdajů. Mobilní pracovní prostor také umožní uživatelům rychle vytvářet řádek výdajů pomocí připojené účtenky.

<a name="overview-of-the-expense-management-mobile-workspace"></a>Přehled mobilního pracovního prostoru správy výdajů
---------------------------------------------------

Mnoho organizací vyžaduje, aby byla připojena k sestavě cestovních nebo obchodních výdajů kopie účtenky, kterou zaměstnanec podává k refundaci. Mobilní pracovní prostor **správy výdajů** umožňuje uživatelům rychlé vytvoření nových řádků výdajů na libovolném mobilním zařízení pomocí připojené fotografie účtenky. Případně mohou uživatelé pořídit fotografii účtenky a připojit ji k sestavě výdajů později. Konkrétně umožňuje mobilní pracovní prostor **správy výdajů** uživateli:

-   Pořiďte fotografii účtenky a odešlete ji do aplikace Microsoft Dynamics 365 for Operations. Uživatel může následně připojit uvedenou fotografii k sestavě výdajů později.
-   Odešlete soubor jako zdokumentovanou účtenku. Uživatel může následně připojit soubor k sestavě výdajů později.
-   Vytvořte nový řádek výdajů pomocí připojené účtenky. Uživatel pak můžete později přidat položku řádku k sestavě výdajů a odeslat ke schválení a refundaci.

Zbývající části tohoto tématu vysvětlují, jak implementovat a použít mobilní pracovní prostor **správy výdajů**.

## <a name="prerequisites"></a>Požadavky
Před implementací mobilního pracovního prostoru **správy výdajů** se ujistěte, že váš správce systému dokončil následující požadavky.

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
<td>Pokud nemáte aplikaci Dynamics 365 for Operations v organizaci nasazenou, váš správce systému by si měl přečíst téma <a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">Nasazení ukázkového prostředí Microsoft Dynamics 365 for Operations</a>.</td>
</tr>
<tr class="even">
<td>Musí být implementován článek KB 4019015.</td>
<td>Správce systému</td>
<td>KB 4019015 (aktualizace X++ nebo oprava hotfix metadat) obsahuje čtyři mobilní pracovní prostory pro řízení řetězce dodávek. Před implementací KB 4019015 musí správce systému udělat toto:
<ol>
<li>Stáhněte KB 4019015 z webu Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">Nainstalujte opravu hotfix metadat</a>.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">Vytvořte nasaditelný balíček</a>, který obsahuje modely <strong>ApplicationSuite</strong> a <strong>ExpenseMobile</strong> a odešlete ho do služby LCS.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">Použijte nasaditelný balíček</a> v systému Dynamics 365 for Operations.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobilní pracovní prostor <strong>správy výdajů</strong> musí být publikovaný v mobilní aplikaci Dynamics 365 for Operations.</td>
<td>Správce systému</td>
<td><ol>
<li>Spusťte Dynamics 365 for Operations v prohlížeči.</li>
<li>Na stránce <strong>Systémové parametry</strong> vyberte <strong>Správa mobilních pracovních prostorů</strong>.</li>
<li>Zvolte <strong>pracovní prostor správy výdajů</strong>.</li>
<li>Klikněte na <strong>Publikovat mobilní pracovní prostor</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Stáhněte a nainstalujte mobilní aplikaci 365 Dynamics for Operations
Stáhněte aplikaci Microsoft Dynamics 365 for Operations z obchodu s mobilními aplikacemi.

-   Android: [Dynamics 365 for Operations - Warehousing v Google Play Store](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   iPhone: [Dynamics 365 for Operations v iTunes apps store](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)
-   Pro Windows Phone (Universal Windows Platform \[UWP\]): Již brzy!

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Přihlaste se k mobilní aplikaci Dynamics 365 for Operations
1.  Spusťte aplikaci na svém mobilním zařízení.
2.  Zadejte adresu URL Dynamics 365 for Operations.
3.  Zadejte společnost, do které se chcete přihlásit. Například zadejte **USMF**.
4.  Při prvním přihlášení budete vyzváni k zadání uživatelského jména a hesla pro váš účet aplikace Dynamics 365 for Operations. Zadejte své přihlašovací údaje.
5.  Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost. Všimněte si, že pokud správce systému později publikuje nový pracovní prostor, můžete vyžádat obnovení seznamu mobilních pracovních prostorů. [![Vyžádání aktualizace](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Zdokumentování účtenky pomocí mobilního pracovního prostoru správy výdajů
1.  Na svém mobilním zařízení vyberte pracovní prostor **správy výdajů**.
2.  Vyberte možnost **Zdokumentovat účtenku**.
3.  Vyberte možnost **Pořídit fotografii** nebo **Zvolit obrázek**.
4.  Pokud jste vybrali **Pořídit fotografii**, postupujte následujícím způsobem:
    1.  Přejděte k fotoaparátu svého mobilního zařízení, abyste mohli pořídit fotografii účtenku. Poté, co jste pořídili fotografii, klikněte na tlačítko **OK** pro přijetí fotografie.
    2.  Volitelné: Zadejte název fotografie a poznámky.

     nebo pokud jste vybrali možnost **Zvolit obrázek**, postupujte následujícím způsobem:
    1.  V seznamu vyberte obrázek.
    2.  Volitelné: Zadejte název obrázku a poznámky.

5.  Vyberte **Hotovo**.

## <a name="quick-expense-entry-by-using-the-expense-management-mobile-workspace"></a>Rychlé zadání výdaje pomocí mobilního pracovního prostoru správy výdajů
1.  Na svém mobilním zařízení vyberte pracovní prostor **správy výdajů**.
2.  Vyberte **Rychlé zadání výdaje**.
3.  Zvolte kategorii pro výdaje. Zobrazí se seznam kategorií výdajů, které jsou načteny do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení je načteno až 50 položek, ale vývojář může tuto hodnotu změnit. Další informace naleznou vývojáři v tématu [Mobilní platforma aplikace Dynamics 365 for Operations](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/). Pokud kategorie není v seznamu uvedena, vyberte **Hledat**, chcete-li provést online hledat v Dynamics 365 for Operations. Hledejte kategorii výdaje nebo přepněte pro hledání podle typu výdaje.
4.  Zadejte datum transakce výdaje.
5.  Volitelné: Zadejte obchodníka pro výdaje.
6.  Zadejte částku výdaje.
7.  Vyberte měnu výdaje. Zobrazí se seznam kódů měn, které jsou načteny do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení je načteno až 400 měn, ale vývojář může tento počet změnit. Další informace naleznou vývojáři v tématu [Mobilní platforma aplikace Dynamics 365 for Operations](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/). Pokud měna není v seznamu uvedena, vyberte **Hledat**, chcete-li provést online hledat v Dynamics 365 for Operations. Hledejte podle měny nebo přepněte pro hledání podle názvu.
8.  Vyberte možnost **Pořídit fotografii** nebo **Zvolit obrázek**.
9.  Pokud zvolíte **Pořídit fotografii**, přejděte k fotoaparátu svého mobilního zařízení, abyste mohli pořídit fotografii účtenku. Poté, co jste pořídili fotografii, klikněte na tlačítko **OK** pro přijetí fotografie.  nebo pokud jste vybrali **Zvolit obrázek**, vyberte obrázek v seznamu.
10. Vyberte **Hotovo**.






