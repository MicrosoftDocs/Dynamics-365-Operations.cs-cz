--- 
title: "Definování pravidel a zásad nároků na zaměstnanecké výhody"
description: "Tento záznam zobrazí způsob, jakým můžete vytvořit pravidla nároku na zaměstnanecké výhody a zásady a přiřadit pravidla k zaměstnaneckým výhodám."
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d346c3277e8f19020d6aa96cf6961c4c52ac28fb
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Definování pravidel a zásad nároků na zaměstnanecké výhody

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento záznam zobrazí způsob, jakým můžete vytvořit pravidla nároku na zaměstnanecké výhody a zásady a přiřadit pravidla k zaměstnaneckým výhodám.  

K vytvoření tohoto záznamu jsou použita ukázková data společnosti USMF.


## <a name="create-benefit-eligibility-policy-rule-type"></a>Vytvoření typu pravidel zásad nároků na zaměstnanecké výhody
1. Přejděte na Lidské zdroje > Výhody > Nárok > Typy pravidel zásad nároků na zaměstnanecké výhody.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název pravidla.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Název dotazu kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. Klikněte na položku Uložit.
8. Zavřete stránku.

## <a name="benefit-eligibility-policy"></a>Zásady nároku na zaměstnaneckou výhodu
1. Přejděte na Lidské zdroje > Výhody > Nárok > Zásady způsobilosti k zaměstnaneckým výhodám.
2. Vyberte existující zásady pro zaměstnanecké výhody.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Přepněte rozšíření oddílů Organizace zásad.  Zde můžete přidat nebo odebrat všechny organizace, které chcete zahrnout do zásad.
5. Rozbalte nebo sbalte část Pravidla zásad.
6. V seznamu vyhledejte pravidlo zásad, které již bylo vytvořeno.
7. Klikněte na Vytvořit pravidlo zásad.
8. Do pole Datum platnosti zadejte datum, ke kterému chcete, aby tato zásada zahájila platnost.
    * Nastavení data platnosti a koncového data umožňuje provádět v budoucnu změny v pravidlech zásad a odstranit potřebu vracet se k zásadám, když budete chtít, aby se tyto změny projevily.  
9. 
    * Například pokud byste chtěli, aby se pravidlo vztahovalo pouze na manažery prodeje, je možné vytvořit klauzuli Where, tj.: popis pozice Where obsahuje manažera prodeje.  Je možné používat logické výrazy And nebo Or pro více výroků Where současně v pravidle.  
10. Klikněte na tlačítko OK.
11. Zavřete stránku.
12. Zavřete stránku.

## <a name="assign-rule-to-benefit"></a>Přiřazení pravidla k zaměstnaneckým výhodám
1. Přejděte k nabídce Lidské zdroje > Výhody > Výhody.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Rozbalte nebo sbalte část Pravidla způsobilosti.
5. Klikněte na možnost Upravit.
6. V poli Nárok vyberte ze seznamu možnost „Podle pravidel“.
7. V poli Typ pravidla kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
8. V seznamu vyhledejte a vyberte pravidlo, které již bylo vytvořeno.
9. Klikněte na odkaz na vybraném řádku v seznamu.
10. Klikněte na položku Uložit.
11. Zavřete formulář.


