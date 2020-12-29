---
title: Mobilní pracovní prostor pro schválení faktur
description: Toto téma obsahuje informace o mobilním pracovním prostoru Schválení faktur. Tento pracovní prostor obsahuje seznam faktur, které vám byly přiřazeny v procesu workflowu záhlaví faktury dodavatele.
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 8d4b40c7ce8939248e85b6b6f3d359bd16e35b0d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683401"
---
# <a name="invoice-approvals-mobile-workspace"></a>Mobilní pracovní prostor pro schválení faktur

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o mobilním pracovním prostoru **Schválení faktur**. Tento pracovní prostor obsahuje seznam faktur, které vám byly přiřazeny v procesu workflowu záhlaví faktury dodavatele. 

Tento mobilní pracovní prostor je určen k použití s mobilní aplikací Finance and Operations.

## <a name="overview"></a>Přehled

V mobilním pracovním prostoru **Schválení faktur** si úředníci a manažeři v oblasti závazků mohou prohlížet faktury, které jim byly přiřazeny v rámci procesu workflowu záhlaví faktury dodavatele. Můžete si prohlížet informace o faktuře i podrobnosti o řádcích a distribuci, abyste se s jejich pomocí mohli lépe rozhodovat při schvalování. V pracovním prostoru můžete provádět příslušná opatření a posouvat faktury dále v procesu workflowu. 

## <a name="prerequisites"></a>Požadavky

Před použitím tohoto mobilního pracovního prostoru musí být splněny následující předpoklady.

<table>
<thead>
<tr class="header">
<th>Předpoklad</th>
<th>Role</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Microsoft Dynamics 365 Finance musí být nasazen ve vaší organizaci.</td>
<td>Správce systému</td>
<td>Viz část <a href="../deployment/deploy-demo-environment.md">Nasazení ukázkového prostředí</a>.
</td>
</tr>
<tr class="even">
<td>Mobilní pracovní prostor <strong>Schválení faktur</strong> musí být publikován.</td>
<td>Správce systému</td>
<td>Viz téma <a href="publish-mobile-workspace.md">Publikování mobilního pracovního prostoru</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Stáhněte a nainstalujte mobilní aplikaci

Stáhněte a nainstalujte mobilní aplikaci Finance and Operations:

-   [Pro telefony Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Pro telefony iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Přihlaste se do mobilní aplikace

1.  Spusťte aplikaci na svém mobilním zařízení.
2.  Zadejte URL adresu Microsoft Dynamics 365.
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
