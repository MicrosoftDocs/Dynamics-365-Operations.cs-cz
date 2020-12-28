---
title: Uživatelé aplikace Attract nemohou žádat o zaměstnání z kariérního portálu
description: Toto téma vysvětluje, jak řešit problém, kdy uživatelé Attract nemohou žádat o zaměstnání z kariérního portálu.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460533"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a>Uživatelé aplikace Attract nemohou žádat o zaměstnání z kariérního portálu

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Výdej

Uživatelé aplikace Attract nemohou žádat o zaměstnání z kariérního portálu. Když se snaží ucházet o práci, která byla vytvořena v Dynamics 365 Talent: Attract, prohlížeč načítá stránku průběžně a nedokončí akci.

## <a name="cause"></a>Příčina

K tomuto problému dochází, když tým pro vztahy s talenty nemá uživatelskou roli Talent.

## <a name="resolution"></a>Rozlišení

Přiřaďte roli uživatele Talent týmu pro vztahy s talenty.

1. Přihlaste se do [centra pro správu Power Platform](https://admin.powerplatform.microsoft.com) s některým z následujících pověření správce:

   - Správce Dynamics 365
   - Globální správce
   - Správce Power Platform

2. V navigačním podokně vyberte **Prostředí** a poté vyberte prostředí, ve kterém přiřadíte uživatelskou roli Talent týmu pro vztahy s talenty.

   ![Výběr prostředí](./media/attract-troubleshoot-career-portal-select-environment.png)

3. V podokně **Prostředí** vyberte **Adresa URL prostředí** a přihlaste se k portálu pro správu prostředí (například https:<orgname>.crm.dynamics.com).

4. Vyberte **Nastavení**, vyberte **Systém** a potom vyberte **Zabezpečení**.

   ![Přechod na Zabezpečení](./media/attract-troubleshoot-career-portal-security.png)

5. Vyberte **Týmy**.

   ![Výběr položky Týmy](./media/attract-troubleshoot-career-portal-security-teams.png)

6. Do vyhledávacího pole zadejte **Tým pro vztahy s talenty** a poté vyberte tým z výsledků vyhledávání.

7. Z pásu karet vyberte **SPRAVOVAT ROLE**.

8. V dialogovém okně **Správa rolí týmu** vyberte **Uživatel Talent** ze seznamu dostupných rolí a poté vyberte **OK** pro použití role.

   ![Použití role](./media/attract-troubleshoot-career-portal-apply-role.png)

9. Otestujte změny:

   1. Přihlaste se na kariérní portál z nového okna prohlížeče.
   2. Požádejte o práci z kariérního portálu. 