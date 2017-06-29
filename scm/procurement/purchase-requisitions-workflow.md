---
title: "Workflow nákupního požadavku"
description: "Proces workflowu přesouvá nákupní žádanky v procesu kontroly od počátečního stavu Koncept do konečného stavu Schváleno. Když je nákupní požadavek odeslán ke kontrole, proces workflowu se spustí. Po schválení nákupního požadavku lze generovat nákupní objednávku pro řádky nákupního požadavku a odeslat ji dodavateli pro splnění zakázky."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqAuthorization, WorkflowParticipantExpenToken
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2234
ms.assetid: dad3ba5a-2892-45d2-874a-300896f59b34
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2d28e92fa853d155bc62932625e0e714cdf4edcc
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="purchase-requisition-workflow"></a>Workflow nákupního požadavku

[!include[banner](../includes/banner.md)]


Proces workflowu přesouvá nákupní žádanky v procesu kontroly od počátečního stavu Koncept do konečného stavu Schváleno. Když je nákupní požadavek odeslán ke kontrole, proces workflowu se spustí. Po schválení nákupního požadavku lze generovat nákupní objednávku pro řádky nákupního požadavku a odeslat ji dodavateli pro splnění zakázky.

Před tím, než bude možné odeslat nákupní žádanku ke kontrole, musíte nakonfigurovat workflow. Proces workflowu může zahrnovat jeden nebo více kroků kontroly v libovolném pořadí. Proces workflowu může být rovněž nakonfigurován na přeskočení kontroly a automatické schvalování nákupní žádanky. Můžete konfigurovat workflow pro směrování nákupní žádanky jako jeden dokument nebo můžete směrovat jednotlivé řádky nákupní žádanky odpovídajícím kontrolorům. Můžete také vytvořit scénář, kde je nákupní žádanka směrována jako jeden dokument některým kontrolorům, a vybrané řádky nákupní žádanky jsou směrovány jiným kontrolorům.  

Pokud probíhá kontrola řádků nákupní žádanky samostatně, je třeba před přesunutím workflowu do dalšího kroku procesu a před dokončením procesu revize nákupní žádanky dokončit proces přezkoumání všech řádků nákupní žádanky jako celku. Po dokončení kontroly nákupní žádanky a všech řádků bude celkový stav nákupní žádanky aktualizován na **Schváleno**.  

Můžete konfigurovat workflow tak, aby reprezentoval obchodní proces nákupních požadavků ve vaší organizaci. Při konfiguraci procesu workflowu nákupní žádanky zvažte následující otázky:

-   Jaké výdaje se musí zkontrolovat?
-   Jaké výdaje lze automaticky schválit?
-   Kdo musí zkontrolovat a schválit požadavky na výdaje? K jakým rolím jsou tito uživatelé přiřazeni?
-   Pokud kontrolor není k dispozici, jaký proces je třeba použít?

Následující příklady ilustrují dva způsoby, jak lze nastavit workflow pro nákupní požadavky.

## <a name="example-1-route-a-purchase-requisition-as-a-single-document-for-review"></a>Příklad 1: Směrování nákupní žádanky ke kontrole jako jeden dokument
Následující obrázek znázorňuje, jak můžete nákupní požadavek odeslat skrze proces kontroly workflowu jako jediný dokument. Řádky v nákupní žádance nejsou směrovány jednotlivě. V tomto příkladu jsou v procesu workflowu zahrnuty následující role:

-   **Žadatel**: Uživatel, který žádá o položky nebo služby. Žadatel může připravit nákupní žádanku nebo nákupní požadavek může jménem žadatele připravit jiný pracovník. Tento pracovník je pořizovatel. Pořizovatel je zodpovědný za správu nákupní žádanky během procesu kontroly. Pouze pořizovatel nákupního požadavku jej může změnit.

**Poznámka:** Pracovníkovi musí být udělena příslušná oprávnění pro vytvoření nákupní žádanky jménem někoho jiného. Použijte stránku **Oprávnění nákupní žádanky** k nastavení těchto oprávnění.

-   **Nákupčí**: Uživatel, který provádí kontrolu zásobování a může schválit dokument.
-   **Manažer žadatele**: Uživatel, který provádí manažerskou kontrolu a může schválit dokument.

![Proces kontroly workflowu nákupní žádanky](./media/purchreqworkflowoverview_submission.gif)  
V tomto příkladu obsahuje proces workflowu pro nákupní žádanku následující kroky:

1.  Pořizovatel odešle nákupní žádanku ke kontrole.
2.  Nákupčí obdrží oznámení. Nákupčí obdrží oznámení vyžadující ověření informací na nákupní žádance. Pokud chybí potřebné informace, nákupčí je může přidat nebo může vrátit nákupní žádanku pořizovateli, aby je přidal. Po zadání všech požadovaných údajů se může nákupní žádanka přesunout k dalšímu kroku procesu kontroly.
3.  Manažer žadatele nákupní požadavek ověří. Pokud například objem nákupního požadavku překročí výdajový limit žadatele pro nákupní požadavky, nákupní žádanka může být směrována na manažera žadatele. Manažer žadatele může schválit nebo odmítnout nákupní žádanku nebo ji vrátit pořizovateli, aby provedl potřebné změny.

## <a name="example-2-route-the-individual-purchase-requisition-lines-for-review"></a>Příklad 2: Směrování jednotlivých řádků nákupní žádanky ke kontrole
Následující obrázek znázorňuje, jak lze směrovat jednotlivé řádky nákupní žádanky skrze workflow. Obecně platí, že proces pro každý řádek je stejný jako proces pro nákupní žádanku, která je kontrolována jako jediný dokument. Každý řádek však musí dokončit workflow individuálně před celkovým dokončením workflowu pro celou nákupní žádanku.  

V tomto příkladu pracovník zadá požadavek na plakáty a trička do marketingové kampaně. Náklady na plakát jsou rozděleny mezi marketingové oddělení a prodejní oddělení. Pokud náklady na plakáty nebo trička překračují řádný podpisový limit pro vedoucí pracovníky oddělení, musí nákupní žádanku zkontrolovat také manažer skupiny.  

V tomto příkladu jsou v procesu workflowu zahrnuty následující role:

-   **Žadatel**: Uživatel, který žádá o položky nebo služby. Žadatel může připravit nákupní žádanku nebo nákupní požadavek může jménem žadatele připravit jiný pracovník. Tento pracovník je pořizovatel. Pořizovatel je zodpovědný za správu nákupní žádanky během procesu kontroly. Pouze pořizovatel nákupního požadavku jej může změnit.

**Poznámka:** Pracovníkovi musí být udělena příslušná oprávnění pro vytvoření nákupní žádanky jménem někoho jiného. Použijte stránku **Oprávnění nákupní žádanky** k nastavení těchto oprávnění.

-   **Nákupčí**: Uživatel, který provádí kontrolu zásobování a může schválit dokument.
-   **Manažer žadatele**: Uživatel, který provádí manažerskou kontrolu a může schválit dokument.
-   **Manažer oddělení**: Uživatel, který provádí výdajovou kontrolu a může schválit dokument.
-   **Manažer skupiny**: Uživatel, který provádí kontrolu podpisové autority a může schválit dokument.

![Proces kontroly workflowu na řádku nákupní žádanky](./media/purchreqlineworkflowoverview.gif)  
V tomto příkladu obsahuje proces workflowu pro řádky nákupní žádanky následující kroky:

1.  Pořizovatel odešle nákupní žádanku ke kontrole. Každý řádek je směrován kontrolorovi, který je nakonfigurován pro jeho příjem v rámci procesu workflowu.
2.  Nákupčí obdrží oznámení. Oznámení vyžaduje po nákupčím ověření informací v nákupní žádance a na řádcích nákupní žádanky. Při otevření nákupní žádanky nákupním agentem jsou viditelné všechny řádky, ale vizuální indikátor ukazuje, které řádky byly odeslány nákupčím ke kontrole. Pokud chybí potřebné informace, nákupčí je může přidat nebo může vrátit řádek nákupní žádanky pořizovateli, aby je přidal. Po zadání všech požadovaných údajů se může řádek nákupní žádanky přesunout k dalšímu kroku procesu kontroly. Řádky nákupního žádanky mohou pokračovat procesem kontroly nezávisle na sobě.
3.  Manažer žadatele pro řádky ověří a schválí řádky nákupního požadavku. Pokud například počet řádků nákupní žádanky překročí výdajový limit žadatele pro řádky nákupní žádanky, schválení může být směrováno na manažera žadatele. Manažer může schválit nebo zamítnout jeden nebo oba řádky nákupního požadavku.
4.  Manažer oddělení marketingu posuzuje řádky nákupní žádanky z hlediska jak plakátů, tak i triček. Manažer oddělení prodeje posuzuje řádky nákupního požadavku pouze z hlediska plakátů, protože to jsou jediné náklady, které budou účtovány obchodnímu oddělení.
5.  Manažer skupiny zkontroluje a schválí řádek nákupní žádanky pro trička pouze v případě, že je schválení od manažera skupiny povinné, například proto, že částka na řádku nákupní žádanky překročí limit ke schválení vedoucím oddělení. Správce skupiny nemusí schválit řádek nákupní žádanky pro plakáty.

## <a name="configuring-a-workflow-for-purchase-requisitions"></a>Konfigurace workflowu pro nákupní žádanky
Pokud chcete směrovat nákupní žádanku ke kontrole, je nutné nakonfigurovat procesy workflowu pro nákupní žádanku. Proces workflowu, který definujete, řídí interakci mezi uživatelem, který si vyžádal položku (žadatel) a kontrolorem a schvalujícím ve workflowu. Postup nákupní žádanky závisí na podmínkách, které jsou uvedeny v konfiguraci workflowu. Například tyto podmínky určují, kdy je třeba směrovat nákupní žádanku, roli, na kterou roli má být nákupní žádanka směrována, a akce, které mohou uživatelé provést.  

Příklady v tomto tématu ukazují, jak lze nákupní požadavek směrovat prostřednictvím workflowu jako jeden dokument nebo ve formě jednotlivých řádků nákupní žádanky. Můžete také konfigurovat workflow pro nákupní žádanky, který odráží interní kontroly řízení pro nákupní žádanky definované pro vaši organizaci.  

Účastníci nebo kontroloři, kterým je úloha přiřazena ve workflowu, mohou být členy určité skupiny uživatelů, uživateli, kteří mají konkrétní role zabezpečení, uživateli, kteří jsou přidružení k odesílateli v manažerské hierarchii, nebo jmenovanými uživateli nebo uživateli, kteří mají určité výdajové odpovědnosti.

### <a name="purchase-requisition-expenditure-reviewers"></a>Kontroloři výdajů nákupní žádanky

Konfigurace kontrolorů výdajů umožňují dynamické směrování výdajů ke kontrole podle uživatele, který je přiřazen k roli projektu, nebo finanční dimenze, kde jsou výdaje účtovány. Proces workflowu používá zadanou roli projektu nebo vlastníka finanční dimenze k určení, komu mají být výdaje směřovány.  

Při vytváření pracovního postupu můžete definovat jednu nebo více konfigurací kontrolora výdajů a potom vybrat konfiguraci. Můžete nakonfigurovat hodnoty recenzenta výdajů pro každou právnickou osobu ve vaší organizaci. Po definování konfigurací kontrolora výdajů přiřaďte konfiguraci k úkolu workflowu.  

Nemusíte definovat konfigurace kontrolora výdajů. Místo toho můžete určit určité uživatele nebo skupiny jako kontrolory při definování workflowu. Pokud však máte komplexní organizaci, kontroloři výdajů mohou zvýšit efektivitu schvalovacího procesu. Navíc platí, že pokud nastavíte kontrolory výdajů, nemusíte aktualizovat přiřazení kontrolorů workflowu pokaždé, když kontrolor změní role úlohy.  

Kontrolory výdajů můžete nastavit na stránce **Kontroloři výdajů nákupní žádanky**. Vytvořte konfiguraci kontrolora výdajů a zadejte hodnoty pro každou právnickou osobu ve vaší organizaci. Pro žádanky, které jsou přiřazeny k projektu, můžete určit roli, která je zodpovědná za kontrolu žádanek: manažer projektu, kontrolor projektu nebo projektový manažer prodeje. Výdaje budou směrovány na uživatele, který je přiřazen k určené roli. Zvolením možnosti odpovídající finanční dimenze na kartě **Rozdělení organizace** můžete také směrovat výdaje vlastníkovi finanční dimenze.  

Chcete-li použít jednoho z kontrolorů výdajů, které jste nastavili ve workflowu, je nutné nastavit možnost **Typ účastníka** na hodnotu **Účastníci výdajů** ve vlastnostech **Přiřazení** pro relevantní prvek workflowu.

<a name="see-also"></a>Viz také
--------

[Vytvořeni požadavku na využití (Průvodce záznamem úloh)](https://ax.help.dynamics.com/en/wiki/create-a-requisition-for-consumption/)

[Definování workflowů pracovních postupů pro nákupní žádanky](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[Workflowy zásobování a zdrojů](procurement-sourcing-workflows.md)

[Přehled nákupních žádanek](purchase-requisitions-overview.md)




