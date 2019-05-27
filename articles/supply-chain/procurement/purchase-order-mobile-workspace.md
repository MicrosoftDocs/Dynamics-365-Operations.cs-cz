---
title: Mobilní pracovní prostor schvalování nákupních objednávek
description: Toto téma obsahuje informace o mobilním pracovním prostoru Schválení nákupní objednávky, který umožňuje zobrazit nákupní objednávky a odpovědět na ně prostřednictvím akce. Nákupní objednávky můžete například schválit nebo odmítnout.
author: mkirknel
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 75a38b99fe0aee7d4dd386191be236e54097e867
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561252"
---
# <a name="purchase-order-approval-mobile-workspace"></a>Mobilní pracovní prostor schvalování nákupních objednávek

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Toto téma obsahuje informace o mobilním pracovním prostoru **Schválení nákupní objednávky**. Tento pracovní prostor vám umožní zobrazit nákupní objednávky a reagovat na ně pomocí akcí. Nákupní objednávky můžete například schválit nebo odmítnout.
 
## <a name="overview"></a>Přehled 
Nákupní objednávky, které vyžadují schválení, procházejí workflowem schválení. Workflow může obsahovat různé kroky, které vyžadují, aby jedna nebo více osob provedly akci. Osoba může například muset dokončit úlohu nebo schválit nákupní objednávku. 

Mobilní pracovní prostor **Schválení nákupní objednávky** umožňuje snadno zobrazit a odpovědět na nákupní objednávky z mobilního zařízení. Tento pracovní prostor také umožňuje přijmout stejné akce workflowu, které lze provést z webového klienta Microsoft Dynamics 365 for Finance and Operations.

## <a name="prerequisites"></a>Předpoklady
Předpoklady se liší podle verze aplikace Finance and Operations, která byla nasazena ve vaší organizaci.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a>Předpoklady při použití Microsoft Dynamics 365 for Finance and Operations 
Pokud je ve vaší organizaci nasazena aplikace Microsoft Dynamics 365 for Finance and Operations, správce systému musí publikovat mobilní pracovní prostor **Schválení nákupní objednávky**. Více pokynů naleznete v tématu [Publikování mobilního pracovního prostoru](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Předpoklady při použití Microsoft Dynamics 365 for Operations verze 1611 s aktualizací Platform Update 3 nebo vyšší
Pokud je ve vaší organizaci nasazena aplikace Microsoft Dynamics 365 for Operations verze 1611 s aktualizací Platform update 3 nebo novější, správce systému musí dokončit následující předpoklady. 

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
<td>Implementujte opravu KB 4017918.</td>
<td>Správce systému</td>
<td>KB 4017918 je X ++ aktualizace nebo oprava hotfix metadat obsahující mobilní pracovní prostor <strong>Schválení nákupní objednávky</strong>. Pro implementaci KB 4017918 musí správce systému provést tyto kroky:
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Stažení oprav hotfix z Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Nainstalujte opravu hotfix metadat</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Vytvořte nasaditelný balíček</a>, který obsahuje model <strong>SCMMobile</strong>, a nahrajte ho do LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Použití nasaditelného balíčku</a></li>
</ol></td>
</tr>
<tr class="even">
<td>Publikujte mobilní pracovní prostor <strong>Schválení nákupní objednávky</strong>.</td>
<td>Správce systému</td>
<td>Viz téma <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publikování mobilního pracovního prostoru</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Stáhněte a nainstalujte mobilní aplikaci
Stáhněte a nainstalujte mobilní aplikaci Microsoft Dynamics 365 for Unified Operations:

- [Pro telefony Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Pro telefony iPhone](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a>Přihlaste se do mobilní aplikace

1. Spusťte aplikaci na svém mobilním zařízení.
2. Zadejte URL adresu Microsoft Dynamics 365.
3. Při prvním přihlášení se zobrazí výzva k zadání uživatelského jména a hesla. Zadejte své přihlašovací údaje.
4. Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost. Všimněte si, že pokud správce systému později publikuje nový pracovní prostor, budete muset aktualizovat seznam mobilních pracovních prostorů.

![Pracovní prostor Schválení nákupní objednávky v seznamu dostupných pracovních prostorů](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a>Zobrazení objednávek, které jsou vám přiřazeny
1. Ve svém mobilním zařízení vyberte pracovní prostor **Schválení nákupní objednávky**.
2. Vyberte **objednávky přiřazené mně** k zobrazení všech nákupních objednávek, u kterých jste byli vyzváni k provedení akce ve workflowu schválení nákupní objednávky.
3. Vyberte objednávku. Na stránce **Podrobnosti objednávky** se zobrazí informace v záhlaví objednávky a řádky. Můžete také vyhledat pokyny z úlohy workflowu.
4. Vyberte možnost **Rozúčtování** k otevření stránky **Rozúčtování v záhlaví**.
5. Vraťte se na stránku **Podrobnosti objednávky** a vyberte řádek. Z podrobností o řádku objednávky můžete také zkoumat rozúčtování specifické pro řádek.

## <a name="complete-an-action-on-the-purchase-order"></a>Dokončení akce u nákupní objednávky
Poté, co jste navštívili nákupní objednávku, která je vám přiřazena, a přečetli si pokyny workflowu, měli byste být připravení k provedení akce.

1. Ve svém mobilním zařízení vyberte pracovní prostor **Schválení nákupní objednávky**.
2. Vyberte **objednávky přiřazené mně** k zobrazení všech nákupních objednávek, u kterých jste byli vyzváni k provedení akce ve workflowu schválení nákupní objednávky.
3. Vyberte objednávku a zobrazte stránku podrobností.
4. Vyberte **Akce** pro zobrazení dostupných akcí. Akce, které jsou k dispozici, závisí na úloze, která vám byla přiřazena.

    | Akce úlohy    | Akce schválení  |
    |----------------|------------------|
    | Dokončit       | Schválit          |
    | Vrácení         | Zamítnout           |
    | Požadavek na změnu | Požadavek na změnu   |
    | Zástupce       | Zástupce         |

5. Vyberte odpovídající akci.
6. Na stránce **Dokončit úkol** zadejte komentář. Všimněte si, že pokud jste vybrali akci **Delegovat**, je nutné vybrat uživatele, kterému má být úkol delegován.
7. Vyberte **Hotovo**. Po aktualizaci pracovního prostoru již nákupní objednávka nebude v tomto seznamu. 
