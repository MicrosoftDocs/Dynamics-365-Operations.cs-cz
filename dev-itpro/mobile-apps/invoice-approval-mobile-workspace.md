---
title: "Mobilní pracovní prostor pro schválení faktur"
description: "Toto téma obsahuje informace o mobilním pracovním prostoru Schválení faktur. Tento pracovní prostor obsahuje seznam faktur, které vám byly přiřazeny v procesu workflowu záhlaví faktury dodavatele."
author: abruer
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 70f3e0fe53fc0b1daa471a7022f5659d09caa867
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="invoice-approvals-mobile-workspace"></a>Mobilní pracovní prostor pro schválení faktur

[!include[banner](../includes/banner.md)]

Toto téma obsahuje informace o mobilním pracovním prostoru **Schválení faktur**. Tento pracovní prostor obsahuje seznam faktur, které vám byly přiřazeny v procesu workflowu záhlaví faktury dodavatele. 

Tento mobilní pracovní prostor je určen k použití s mobilní aplikací Microsoft Dynamics 365 for Unified Operations.

## <a name="overview"></a>Přehled

V mobilním pracovním prostoru **Schválení faktur** si úředníci a manažeři v oblasti závazků mohou prohlížet faktury, které jim byly přiřazeny v rámci procesu workflowu záhlaví faktury dodavatele. Můžete si prohlížet informace o faktuře i podrobnosti o řádcích a distribuci, abyste se s jejich pomocí mohli lépe rozhodovat při schvalování. V pracovním prostoru můžete provádět příslušná opatření a posouvat faktury dále v procesu workflowu. 

## <a name="prerequisites"></a>Požadavky

Před použitím tohoto mobilního pracovního prostoru musí být splněny následující předpoklady.

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
<td>V organizaci musí být nasazena aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition s aktualizací z července 2017.</td>
<td>Správce systému</td>
<td>Viz část <a href="../deployment/deploy-demo-environment.md">Nasazení ukázkového prostředí</a>.
</td>
</tr>
<tr class="even">
<td>Mobilní pracovní prostor <strong>Schválení faktur</strong> musí být publikován.</td>
<td>Správce systému</td>
<td>Viz téma <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publikování mobilního pracovního prostoru</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Stáhněte a nainstalujte mobilní aplikaci

Stáhněte a nainstalujte mobilní aplikaci 365 Dynamics for Unified Operations:

-   [Pro telefony Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Pro telefony iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Přihlaste se do mobilní aplikace

1.  Spusťte aplikaci na svém mobilním zařízení.
2.  Zadejte adresu URL aplikace Microsoft Dynamics 365.
3.  Při prvním přihlášení se zobrazí výzva k zadání uživatelského jména a hesla. Zadejte své přihlašovací údaje.
4.  Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost. Všimněte si, že pokud správce systému později publikuje nový pracovní prostor, budete muset aktualizovat seznam mobilních pracovních prostorů.

    [![Vyžádání aktualizace](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a>Schválení faktur pomocí mobilního pracovního prostoru Schválení faktur
1.  Ve svém mobilním zařízení vyberte pracovní prostor **Schválení faktur**.
2.  Vyberte fakturu, která vám byla přiřazena procesem workflowu záhlaví faktury dodavatele.
3.  Na stránce **Podrobnosti faktury** zkontrolujte informace záhlaví faktury, například informace o dodavateli a datu.
4.  Výběrem řádku faktury zobrazíte podrobnější informace v zobrazení **Podrobnosti řádku faktury**.
5.  V zobrazení **Podrobnosti řádku faktury** můžete výběrem možnosti **Distribuce** zobrazit distribuce řádků. Zde si můžete prohlédnout účetnictví spojené s řádkem faktury. K zobrazeným informacím patří finanční dimenze a hlavní účet.
6.  Na stránce **Podrobnosti faktury** můžete výběrem možnosti **Distribuce** zobrazit všechny distribuce. Zde si můžete prohlédnout účetnictví spojené s celou fakturou. K zobrazeným informacím patří finanční dimenze a hlavní účty. 
7.  Výběrem možnosti **Přílohy** zobrazíte další poznámky nebo soubory, které jsou připojeny k faktuře.
8.  Na stránce **Podrobnosti faktury** vyberte požadovanou akci workflowu a dokončete tak proces kontroly.
9.  Vyberte **Hotovo**.

