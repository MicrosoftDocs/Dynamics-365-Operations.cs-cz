---
title: Přehled životního cyklu produktu
description: Stav životního cyklu produktu dokumentuje životní cyklus uvolněného produktu nebo varianty produktu.
author: cvocph
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: conradv
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: b5b0ceb1926de6efda239fdbc69fb36a9d4b28e0
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934833"
---
# <a name="product-lifecycle-state-overview"></a>Přehled životního cyklu produktu

[!include [banner](../includes/banner.md)]

Stav životního cyklu produktu dokumentuje životní cyklus uvolněného produktu nebo varianty produktu. Stavy životního cyklu produktu definuje uživatel, obvykle manažer produktu nebo manažer hlavních dat produktu. Určité obchodní procesy, například hlavní plánování, mohou být ovlivněny konkrétním stavem životního cyklu.   

Uvolněný produkt nebo variantu produktu lze přidružit ke stavu životního cyklu produktu, který dokumentuje, v jakém stavu životního cyklu je momentálně určitý produktu nebo varianta. Přiřazením názvu stavu a popisu můžete definovat jakýkoliv počet stavů životního cyklu produktu. Můžete vybrat jeden stav životního cyklu jako výchozí stav pro nové uvolněné produkty. Uvolněné varianty produktu zdědí svůj stav životního cyklu produktu ze svého uvolněného hlavního produktu při jeho vytvoření. Při změně stavu životního cyklu uvolněného hlavního produktu můžete aktualizovat všechny existující varianty, které mají stejný původní stav.  

## <a name="create-a-new-product-lifecycle-state"></a>Vytvoření nového stavu životního cyklu produktu 

- Chcete-li vytvořit nový stav životního cyklu produktu, pusťte si nebo si přečtěte průvodce záznamem úloh **Vytvoření nového stavu životního cyklu produktu**. 

-  Chcete-li vytvořit výchozí stav životního cyklu produktu, pusťte si nebo si přečtěte průvodce záznamem úloh **Vytvoření výchozího stavu životního cyklu produktu**.   

## <a name="associate-product-lifecycle-states-to-released-products"></a>Přidružení stavů životního cyklu produktu k uvolněným produktům  

Existuje více způsobů, jak přidružit stav životního cyklu produktu k uvolněným produktům nebo variantám produktu.

-  Při vytvoření nového uvolněného produktu je automaticky přiřazen výchozí **Stav životního cyklu produktu**. 
-  Při uvolnění produktu do právnické osoby je automaticky přiřazen výchozí **Stav životního cyklu produktu**. 
-  Při uvolnění varianty produktu do právnické osoby je automaticky nové variantě přiřazen **Stav životního cyklu produktu** přidružený k uvolněnému základnímu produktu v této právnické osobě. 

Stav životního cyklu produktu lze aktualizovat ručně pomocí: 

-    Stránky se seznamem **Uvolněné produkty** nebo **Zobrazení podrobností**. 
-  Stránky se seznamem **Uvolněné varianty produkty** nebo **Zobrazení podrobností**. 
-  Najděte zastaralé produkty nebo varianty produktu na základě poptávky a přidružte stav životního cyklu.  

Podrobné informace o přidružení stavů životního cyklu produktu získáte přehráním nebo přečtením následujících dvou záznamů průvodcem úloh.

-  Chcete-li přidružit stav životního cyklu produktu k uvolněnému základnímu produktu, přehrajte si nebo přečtěte průvodce záznamem úloh **Přiřadit stav životního cyklu k uvolněnému hlavnímu produktu**. 

-  Chcete-li přidružit stav životního cyklu produktu k uvolněnému produktu, přehrajte si nebo přečtěte průvodce záznamem úloh **Přiřadit stav životního cyklu k uvolněnému produktu**. 

## <a name="impact-on-master-planning"></a>Dopad na hlavní plánování 

Stav životního cyklu produktu má pouze jeden kontrolní příznak: **Je aktivní pro plánování**. Ve výchozím nastavení je tato hodnota nastavena na **Ano** pro všechny vytvořené stavy životního cyklu produktu, ale lze ji změnit na **Ne**. Pokud je nastavena na **Ne**, přiřazené uvolněné produkty nebo uvolněné varianty produktu jsou: 

-  Vyloučeno z hlavního plánování. 
-  Vyloučeno z výpočtu úrovně kusovníku. 

Podrobné informace o použití stavu životního cyklu produktu k vyloučení produktů z hlavního plánování a výpočtu úrovně kusovníku získáte přehráním nebo přečtením průvodce záznamem úloh **Vytvoření stavu životního cyklu produktu k vyloučení produktů z hlavního plánování**.

> [!NOTE]
> Z důvodu výkonu doporučujeme přidružit všechny zastaralé uvolněné produkty nebo varianty produktu, zejména při práci s opětovně nepoužitelnými variantami konfigurace produktu ke stavu životního cyklu produktu, který je deaktivován pro hlavní plánování.  

## <a name="default-migration-import-and-export"></a>Výchozí migrace, export a import 

Stavy životního cyklu produktu jsou podporovány datovými entitami a stav životního cyklu lze nastavit na proměnlivý stav prostřednictvím datových entit uvolněného produktu nebo datových entit uvolněné varianty.

## <a name="find-obsolete-products-and-products-variants"></a>Nalezení zastaralých produktů a variant produktů 

Můžete spustit simulační analýzu, abyste nalezli zastaralé uvolněné produkty nebo varianty produktu, a poté aktualizovat jejich stav životního cyklu produktu. Chcete-li nalézt zastaralé produkty, přehrajte si nebo si přečtěte průvodce záznamem úloh **Nalezení zastaralých variant produktu a přiřazení stavu životního cyklus produktu**. Tento průvodce záznamem ukazuje, jak nalézt zastaralé uvolněné produkty nebo varianty produktu a jak přiřadit stav životního cyklu produktu k zastaralým produktům. Také ukazuje, jak zobrazit výsledky simulace, a vyhodnocuje počet produktů a variant produktů, který bude přidružen k novému stavu životního cyklu produktu při spuštění aktualizace bez simulace.  

Spuštěním analýzy v režimu simulace se zobrazí produkty a varianty produktů identifikované jako zastaralé v konkrétním formuláři, kde je lze snadno zkontrolovat. Analýza vyhledá transakce a konkrétní hlavní data k určení produktů, které nemají žádnou poptávku v rámci proměnného období a žádná hlavní data, která mohou mít za následek poptávku. Nové uvolněné produkty v rámci proměnného období lze vyloučit z analýzy. Když simulace analýzy vrátí očekávaný výsledek, může uživatel spustit analýzu a nastavit nový stav životního cyklu produktu pro všechny produkty identifikované analýzou jako zastaralé.  

> [!NOTE]
> Mějte na paměti, že všechny analýzy a aktualizace je třeba provést v rámci stejné právnické osoby.  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a>Kritéria pro výběr a aktualizaci uvolněných produktů nebo variant produktu 

Použijte následující kritéria pro výběr a aktualizaci uvolněných produktů nebo variant produktu: 

-    Stav životního cyklu produktu nebo variant produktu musí být odlišný od nového požadovaného stavu. 
-  Produkt nebo varianta produktu byly vytvořeny před několika dny na základě počtu dní, které zadáte do dialogového okna výběru. 
-  Neexistují žádné otevřené výrobní zakázky (= stav < ukončeno) pro produkt nebo variantu produktu. 
-  Neexistují otevřené skladové transakce (= stav výdeje ReservPhysical do QuotationIssue nebo stavu příjmu Registrered do QuotationReceipt) pro produkt nebo variantu produktu. 
-  Během posledních dní neexistují žádné skladové transakce pro produkt nebo variantu produktu. 
-  Neexistuje budoucí poptávka nebo prognóza dodávek pro produkt nebo variantu produktu.  
-  Nebyla nastavena minimální úroveň zásob v disponibilitě položky pro produkt nebo variantu produktu. 
-  Žádné aktivní kanbanové pravidlo pro pevné množství pro produkt nebo variantu produktu.  
-  Žádný řádek servisní zakázky pro produkt nebo variantu produktu. 
-  Žádný aktivní či budoucí řádky prodejní nebo nákupní smlouvy pro produkt nebo variantu produktu. 
-  Produkt nebo varianta produktu se nepoužívá v kusovníku, který je přidružený se schválenou verzí kusovníku, který ještě nevypršel, pro produkt nebo variantu, která jsou aktivní pro plánování.

## <a name="related-topics"></a>Související témata

-  [Vytvoření nového stavu životního cyklu produktu](tasks/new-product-lifecycle-state.md)
-  [Vytvoření výchozího stavu životního cyklu produktu](tasks/default-product-lifecycle-state.md)
-  [Přiřazení stavu životního cyklu produktu k uvolněnému hlavnímu produktu](tasks/product-lifecycle-state-released-product-master.md)
-  [Přiřazení stavu životního cyklu produktu k uvolněnému produktu](tasks/product-lifecycle-state-released-product.md)
-  [Nalezení zastaralých variant produktu a přiřazení stavu životního cyklu produktu](tasks/obsolete-product-variants.md)
-  [Vytvoření stavu životního cyklu produktu k vyloučení produktů z hlavního plánování](tasks/exclude-products-master-planning.md)
