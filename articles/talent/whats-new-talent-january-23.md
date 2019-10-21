---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent – Core HR (23. ledna 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f1983d5a58fb2e6b1984727e1d7b44803b94cdce
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023969"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-january-23-2019"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Talent: Core HR (23. ledna 2019)

[!include [banner](includes/banner.md)]

**Sestavení 8.1.2121**

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.

## <a name="changes"></a>Změny

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a>Import fixní kompenzace zaměstnance nepracuje při vytváření nových záznamů fixní kompenzace
Byla provedena změna entity fixní kompenzace zaměstnance k příjmu úrovně kompenzace při importu. Před touto verzí byla zobrazena zpráva označující požadovalo úroveň.

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a>Odeberte pole Minimální zůstatek z dialogového okna požadavku na volno.
Pole **Minimální zůstatek** bylo odebráno z dialogového okna **Požadavek na časový posun**. Tato změna ovlivňuje všechny oblasti, kde lze požadovat volno.

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a>Upgrade dat pro úrovně odměňování se neaktualizuje ve všech scénářích
Byla provedena změna k aktualizaci úrovně odměňování v plánech fixního odměňování. Tato změna naplní úroveň odměňování ve fixních plánech pro práci přidělenou zaměstnanci.

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a>Mzdové informace na stránce správy změn je dostupná pouze při přihlášen jako správce systému
Tato změna zaměstnancům s rolí správce výplat umožňuje přístup k informacím o výplatám na stránce **Časová osa změn > Spravovat změny** pro danou pozici.

### <a name="job-fields-default-to-positions"></a>pole zakázky výchozí pro pozice
Při změně práce pro pozici, budou pole úlohy použita jako výchozí pro pozici. Zobrazí se výstražná zpráva s možností přijmout výchozí hodnoty nebo ponechat existující hodnoty pro tato pole.

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a>Období zaškolení a kalendáře se nezobrazují pro zaměstnance přijaté v budoucnu.
Při této změně byla přidána pole **Zkušební období** a **kalendář** na stránku **Správa změn** s cílem umožnit zadávání dat pro budoucí a minulé zaměstnance.

### <a name="platform-update-23-for-finance-and-operations"></a>Ajtzakuzace Platform Update 23 for Finance and Operations
Dílčí opravy chyb byly zahrnuty jako součást aktualizace Platform update 23 pro Finance and Operations. Další informace naleznete v tématu [Co je nového nebo změněného v Dynamics 365 Finance and Operations aktualizace platformy 23 (leden 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23). 
