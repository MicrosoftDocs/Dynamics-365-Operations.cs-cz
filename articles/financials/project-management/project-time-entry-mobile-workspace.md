---
title: "Mobilní pracovní prostor zadání času projektu"
description: "Toto téma obsahuje informace o mobilním pracovním prostoru zadání času projektu Tento pracovní prostor uživatelům umožňuje zadat a uložit čas na projekt pomocí svých mobilních zařízení."
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: c04ffccdcbf104b1d5db30a41116663fcedd4e1d
ms.contentlocale: cs-cz
ms.lasthandoff: 12/01/2017

---

# <a name="project-time-entry-mobile-workspace"></a>Mobilní pracovní prostor zadání času projektu

[!include[banner](../includes/banner.md)]

Toto téma obsahuje informace o mobilním pracovním prostoru **Zadání času projektu**. Tento pracovní prostor uživatelům umožňuje zadat a uložit čas na projekt pomocí svých mobilních zařízení.

Tento mobilní pracovní prostor je určen k použití s mobilní aplikací Microsoft Dynamics 365 for Unified Operations. 

## <a name="overview"></a>Přehled
Při své každodenní práci jsou zdroje projektu často buď na místě nebo cestují. Mobilní pracovní prostor **zadání času projektu** umožní uživatelům zadat jejich fakturovatelný nebo nefakturovatelný čas proti projektu na libovolném mobilním zařízení. Proto zmohou zdroje projektu zaznamenat časové vstupy kdykoliv a kdekoliv. Mohou také zobrazit časové vstupy, které již byly zaznamenány. 

Konkrétně v mobilním pracovním prostoru **Zadání času projektu** mohou uživatelé provádět tyto úlohy:

-   Pro jakékoliv vybrané datum zadejte počet hodin, které jste strávili na konkrétním úkolu.
-   Vyhledejte projekt, pro který chcete zadat čas, podle názvu projektu nebo odběratele.
-   Určete kategorii a aktivitu pro čas, který jste na úkolu strávili.
-   Zaznamenejte čas pro projekt jako fakturovatelný nebo nefakturovatelný.
-   Volitelně zadejte externí nebo interní poznámky.

## <a name="prerequisites"></a>Požadavky
Předpoklady se liší podle verze aplikace Microsoft Dynamics 365, která byla nasazena ve vaší organizaci.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Požadavky, pokud používáte aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition
Pokud je ve vaší organizaci nasazena aktualizace aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, správce systému musí mobilní pracovní prostor **Zadání času projektu** publikovat. Více pokynů naleznete v tématu [Publikování mobilního pracovního prostoru](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Požadavky, pokud používáte aplikaci Microsoft Dynamics 365 for Operations verze 1611 s aktualizací platformy 3 nebo novější
Pokud je ve vaší organizaci nasazena aplikace Microsoft Dynamics 365 for Operations verze 1611 s aktualizací platformy 3 nebo novější, správce systému musí dokončit následující předpoklady. 

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

<td>Implementujte opravu KB 4018050.</td>
<td>Správce systému</td>
<td>KB 4018050 je X ++ aktualizace nebo oprava hotfix metadat obsahující mobilní pracovní prostor <strong>zadání času projektu</strong>. Pro implementaci KB 4018050 musí správce systému provést tyto kroky:
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Stažení opravy hotfix metadat ze služby Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Nainstalujte opravu hotfix metadat</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Vytvořte nasaditelný balíček</a>, který obsahuje modely <strong>ApplicationSuite</strong> a <strong>ProjectMobile</strong> a odešlete ho do služby LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Použití nasaditelného balíčku</a></li>

</ol></td>
</tr>
<tr class="even">
<td>Publikujte mobilní pracovní prostor <strong>Zadání času projektu</strong>.</td>
<td>Správce systému</td>
<td>Viz téma <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publikování mobilního pracovního prostoru</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Stáhněte a nainstalujte mobilní aplikaci

Stáhněte a nainstalujte mobilní aplikaci 365 Dynamics for Unified Operations:

-   [Pro telefony Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Pro telefony iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Přihlaste se do mobilní aplikace
1.  Spusťte aplikaci na svém mobilním zařízení.
2.  Zadejte adresu URL aplikace Dynamics 365.
3.  Při prvním přihlášení se zobrazí výzva k zadání uživatelského jména a hesla. Zadejte své přihlašovací údaje.
4.  Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost. Všimněte si, že pokud správce systému později publikuje nový pracovní prostor, budete muset aktualizovat seznam mobilních pracovních prostorů.

[![Vyžádání aktualizace](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Zadejte čas pomocí mobilního pracovního prostoru zadání času projektu.
1.  Na svém mobilním zařízení vyberte pracovní prostor **zadání času projektu**.
2.  Vyberte **Časový záznam**. Zobrazí se kalendářní data pro aktuální týden.
3.  Pro vybrané datum zvolte možnosti **Akce**&gt;**Nový záznam**.
4.  Zadejte počet hodin, který chcete zaznamenat.
5.  Vyberte projekt pro časový záznam. Seznam uvádí projekty, které jsou načteny do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení je načteno 50 položek, ale vývojář může tuto hodnotu změnit. Další informace najdete v tématu [Mobilní platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  Není-li váš projekt v seznamu, vyberte možnost **Vyhledávat další**. Hledejte podle názvu nebo přepněte pro hledání podle názvu projektu nebo odběratele.
7.  Vyberte kategorii. Seznam uvádí kategorie, které jsou načteny do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení je načteno 50 položek, ale vývojář může tuto hodnotu změnit. Další informace najdete v tématu [Mobilní platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  Není-li vaše kategorie v seznamu, vyberte možnost **Vyhledávat další**. Hledejte podle kategorie nebo přepněte pro hledání podle názvu kategorie.
9.  Vyberte aktivitu. Seznam uvádí aktivity, které jsou načteny do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení je načteno 50 položek, ale vývojář může tuto hodnotu změnit. Další informace najdete v tématu [Mobilní platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. Není-li vaše aktivita v seznamu, vyberte možnost **Vyhledávat další**. Hledejte podle čísla aktivity nebo přepněte pro hledání podle účelu.

11. Zvolte vlastnost řádku.
12. Volitelně: Zadejte externí nebo interní poznámky.
13. Vyberte **Hotovo**.

