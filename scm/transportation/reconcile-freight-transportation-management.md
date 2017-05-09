---
title: "Odsouhlasení nákladu ve správě přepravy"
description: "Tento článek popisuje proces odsouhlasení dopravného."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c85806132efb65c2d4bc85ef1921c003c5c7453b
ms.lasthandoff: 03/31/2017


---

# <a name="reconcile-freight-in-transportation-management"></a>Odsouhlasení nákladu ve správě přepravy

[!include[banner](../includes/banner.md)]


Tento článek popisuje proces odsouhlasení dopravného.

Odsouhlasení dopravného lze provádět ručně, nebo je můžete nastavit automaticky. Chcete-li použít automatické odsouhlasení dopravného, musíte vytvořit předlohu auditu, kde definujete kritéria určující, které účty dopravného jsou spárovány automaticky.

## <a name="the-freight-reconciliation-process"></a>Proces odsouhlasení dopravného
Sazby dopravného se vypočítají podle sazebního modulu, který je spojen s odpovídajícím dopravcem. Po potvrzení nákladu je generován účet dopravného, do kterého jsou přeneseny sazby za přepravu. Sazby za přepravu jsou rozděleny jako vedlejší náklady do příslušného zdrojového dokladu (nákupní objednávky, prodejní objednávky nebo převodní příkaz) v závislosti na nastavení, které se používá pro normální proces fakturace. Proces odsouhlasení dopravného (známý také jako proces spárování) můžete spustit ihned po přijetí faktury dopravného od dopravce. Fakturu lze přijímat elektronicky nebo papírově. Pokud je faktura přijata papírově, může vygenerovat elektronickou fakturu pomocí účtu dopravného coby předlohy. 

[![Proces odsouhlasení dopravného](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Ruční odsouhlasení
Pokud provádíte odsouhlasení dopravného ručně, musíte spárovat každý řádek faktury s řádkem/řádky účtu dopravného pro náklad, který se fakturuje. Toto párování provádíte na stránce **Spárování účtů dopravného a faktur**. Pokud částka na řádku faktury neodpovídá částce na účtu dopravného, je nutné vybrat důvod odsouhlasení pro tento rozdíl. Pokud existuje více důvodů k odsouhlasení, je možné rozdělit nespárované částky mezi ně. Důvod odsouhlasení určuje, jak jsou rozdílné částky zaúčtovány v hlavní knize. Pokud zohledňujete odsouhlasení celé fakturované částky, je částka odeslána ke schválení, a následně je zaúčtován deník. Následující obrázek ukazuje, jak generovat fakturu za dopravné a provádět odsouhlasení dopravného v Microsoft Dynamics 365 for Operations. 
[![Úkoly odsouhlasení dopravného v aplikaci Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)
## <a name="automatic-reconciliation"></a>Automatické odsouhlasení
Chcete-li použít automatické odsouhlasení, je nutné zadat plán odsouhlasení, stejně jako faktury a dopravce, které chcete použít. Párování řádků faktury a účtů dopravného se provádí podle nastavení v hlavním auditu a podle typu účtu dopravného. Po spuštění automatického odsouhlasení musíte zpracovat všechny faktury, které systém nespáruje. Tyto faktury musíte poté ručně zpracovat, než budete moci zaúčtovat všechny faktury pro platbu.




