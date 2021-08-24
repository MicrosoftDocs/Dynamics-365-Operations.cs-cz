---
title: Definování pravidel a zásad nároků na zaměstnanecké výhody
description: Tento článek uvádí způsob, jakým můžete vytvořit pravidla nároku na zaměstnanecké výhody a zásady a přiřadit pravidla k zaměstnaneckým výhodám.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 57bcce908dec0b202880d865bbb6014ae13e385642dc2785b16c33abc4ab53bf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752050"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Definování pravidel a zásad nároků na zaměstnanecké výhody

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma uvádí způsob, jakým můžete vytvořit pravidla nároku na zaměstnanecké výhody a zásady a přiřadit pravidla k zaměstnaneckým výhodám.  

## <a name="create-benefit-eligibility-policy-rule-type"></a>Vytvoření typu pravidel zásad nároků na zaměstnanecké výhody

1. Přejděte na **Lidské zdroje > Výhody > Nárok > Typy pravidel zásad nároků na zaměstnanecké výhody**.
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Název pravidla**.
4. V poli **Popis** zadejte hodnotu.
5. V poli **Název dotazu** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Vyberte odkaz na vybraném řádku v seznamu.
7. Zvolte **Uložit**.
8. Zavřete stránku.

## <a name="benefit-eligibility-policy"></a>Zásady nároku na zaměstnaneckou výhodu

1. Přejděte na **Lidské zdroje > Výhody > Nárok > Zásady způsobilosti k zaměstnaneckým výhodám**.
2. Vyberte existující zásady pro zaměstnanecké výhody.
3. Vyberte odkaz na vybraném řádku v seznamu.
4. Přepněte rozšíření oddílů **Organizace zásad**. Zde můžete přidat nebo odebrat všechny organizace, které chcete zahrnout do zásad.
5. Rozbalte nebo sbalte část **Pravidla zásad**.
6. V seznamu vyhledejte pravidlo zásad, které již bylo vytvořeno.
7. Vyberte **Vytvořit pravidlo zásad**.
8. Do pole **Datum platnosti** zadejte datum, ke kterému chcete, aby tato zásada zahájila platnost.
    * Nastavení data platnosti a koncového data umožňuje provádět v budoucnu změny v pravidlech zásad a odstranit potřebu vracet se k zásadám, když budete chtít, aby se tyto změny projevily.  
9. V případě potřeby přidejte klauzuli where do pole **Přidat podmínku**.
    * Například pokud byste chtěli, aby se pravidlo vztahovalo pouze na manažery prodeje, je možné vytvořit klauzuli Where, tj.: popis pozice Where obsahuje manažera prodeje. Je možné používat logické výrazy And pro více výroků Where současně v pravidle.  
10. Vyberte **OK**.
11. Zavřete stránku.

## <a name="assign-rule-to-benefit"></a>Přiřazení pravidla k zaměstnaneckým výhodám

1. Přejděte k nabídce **Lidské zdroje > Výhody > Výhody**.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Vyberte odkaz na vybraném řádku v seznamu.
4. Rozbalte nebo sbalte část **Pravidla způsobilosti**.
5. Vyberte možnost **Upravit**.
6. V poli **Nárok** vyberte pravidlo.
7. V poli **Typ pravidla** vyberte vytvořené pravidlo.
9. Vyberte odkaz na vybraném řádku v seznamu.
10. Zvolte **Uložit**.
11. Zavřete formulář.



[!INCLUDE[footer-include](../includes/footer-banner.md)]