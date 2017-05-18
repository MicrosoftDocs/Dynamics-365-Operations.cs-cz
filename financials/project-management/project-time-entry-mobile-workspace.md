---
title: "Mobilní pracovní prostor zadání času projektu pro aplikaci Microsoft Dynamics 365 for Operations"
description: "Toto téma obsahuje informace o mobilním pracovním prostoru zadání času projektu Tento pracovní prostor uživatelům umožňuje zadat a uložit čas na projekt pomocí svých mobilních zařízení."
author: annbe
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e3e0be36c045acc3750efbb739d79d81ab937c65
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="project-time-entry-mobile-workspace"></a>Mobilní pracovní prostor zadání času projektu

[!include[banner](../includes/banner.md)]

"[!include[banner](../includes/banner.md)]"


Toto téma obsahuje informace o mobilním pracovním prostoru zadání času projektu, který je k dispozici pro mobilní aplikaci Microsoft Dynamics 365 for Operations. Tento pracovní prostor uživatelům umožňuje zadat a uložit čas na projekt pomocí svých mobilních zařízení.

<a name="overview-of-the-project-time-entry-mobile-workspace"></a>Přehled mobilního pracovního prostoru zadání času projektu
---------------------------------------------------

Při své každodenní práci jsou zdroje projektu často buď na místě nebo cestují. Mobilní pracovní prostor **zadání času projektu** umožní uživatelům zadat jejich fakturovatelný nebo nefakturovatelný čas proti projektu na libovolném mobilním zařízení. Proto zmohou zdroje projektu zaznamenat časové vstupy kdykoliv a kdekoliv. Mohou také zobrazit časové vstupy, které již byly zaznamenány. 

Mobilní pracovní prostor **zadání času projektu** poskytuje konkrétně následující funkce:

-   Pro jakékoliv vybrané datum zadejte počet hodin, které jste strávili na konkrétním úkolu.
-   Vyhledejte projekt, pro který chcete zadat čas, podle názvu projektu nebo odběratele.
-   Určete kategorii a aktivitu pro čas, který jste na úkolu strávili.
-   Zaznamenejte čas pro projekt jako fakturovatelný nebo nefakturovatelný.
-   Volitelně zadejte externí nebo interní poznámky.

Pro implementaci mobilního pracovního prostoru **zadání času projektu** nahlédněte do následujících částí v tomto tématu.

## <a name="prerequisites"></a>Požadavky
Před implementací mobilního pracovního prostoru **zadání času projektu** se ujistěte, že váš správce systému dokončil následující požadavky.

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
<td>Pokud nemáte aplikaci Dynamics 365 for Operations v organizaci nasazenou, váš správce systému by si měl přečíst téma <a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Nasazení ukázkového prostředí Microsoft Dynamics 365 for Operations</a>.</td>
</tr>
<tr class="even">
<td>Musí být implementován článek KB 4018050.</td>
<td>Správce systému</td>
<td>KB 4018050 je X ++ aktualizace nebo oprava hotfix metadat obsahující mobilní pracovní prostor <strong>zadání času projektu</strong>. Pro implementaci KB 4018050 musí správce systému provést tyto kroky:
<ol>
<li>Stáhněte KB 4018050 z webu Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Nainstalujte opravu hotfix metadat</a>.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Vytvořte nasaditelný balíček</a>, který obsahuje modely <strong>ApplicationSuite</strong> a <strong>ProjectMobile</strong> a odešlete ho do služby LCS.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Použijte nasaditelný balíček</a> v systému Dynamics 365 for Operations.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobilní pracovní prostor <strong>zadání času projektu</strong> musí být publikovaný v mobilní aplikaci Dynamics 365 for Operations.</td>
<td>Správce systému</td>
<td><ol>
<li>Spusťte Dynamics 365 for Operations v prohlížeči.</li>
<li>Na stránce <strong>Systémové parametry</strong> na kartě <strong>Spravovat mobilní pracovní prostory</strong> vyberte pracovní prostor <strong>zadání času projektu</strong>.</li>
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

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Zadejte čas pomocí mobilního pracovního prostoru zadání času projektu.
1.  Na svém mobilním zařízení vyberte pracovní prostor **zadání času projektu**.
2.  Vyberte **Časový záznam**. Uvidíte data kalendáře pro aktuální týden.
3.  Pro vybrané datum zvolte možnosti **Akce**&gt;**Nový záznam**.
4.  Zadejte počet hodin, který chcete zaznamenat.
5.  Vyberte projekt pro časový záznam. Zobrazí se seznam projektů, které jsou načteny do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení je načteno 50 položek, ale vývojář může tuto hodnotu změnit. Další informace naleznou vývojáři v tématu [Mobilní platforma aplikace Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
6.  Pokud projekt není v seznamu uveden, vyberte **Hledat**, chcete-li provést online hledat v Dynamics 365 for Operations. Hledejte podle názvu nebo přepněte pro hledání podle názvu projektu nebo odběratele.
7.  Vyberte kategorii. Zobrazí se seznam kategorií, které jsou načteny do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení je načteno 50 položek, ale vývojář může tuto hodnotu změnit. Další informace naleznou vývojáři v tématu [Mobilní platforma aplikace Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
8.  Pokud kategorie není v seznamu uvedena, vyberte **Hledat**, chcete-li provést online hledat v Dynamics 365 for Operations. Hledejte podle kategorie nebo přepněte pro hledání podle názvu kategorie.
9.  Vyberte aktivitu. Zobrazí se seznam aktivit, které jsou načteny do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení je načteno 50 položek, ale vývojář může tuto hodnotu změnit. Další informace naleznou vývojáři v tématu [Mobilní platforma aplikace Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
10. Pokud aktivita není v seznamu uvedena, vyberte **Hledat**, chcete-li provést online hledat v Dynamics 365 for Operations. Hledejte podle čísla aktivity nebo přepněte pro hledání podle účelu.
11. Zvolte vlastnost řádku.
12. Volitelně: Zadejte externí nebo interní poznámky.
13. Vyberte **Hotovo**.






