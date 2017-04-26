---
title: "Nabíhání nákladů projektu na nákupní příjemky"
description: "Toto téma popisuje, jak časově rozlišených nákladů na projekt z nákupní příjemky lze sledovat v aplikaci Microsoft Dynamics 365 pro operace."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 27a0a71095dce46c0119b32a92f8c4dce0f42e43
ms.lasthandoff: 03/31/2017


---

# <a name="project-cost-accrual-on-purchase-receipts"></a>Nabíhání nákladů projektu na nákupní příjemky

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak časově rozlišených nákladů na projekt z nákupní příjemky lze sledovat v aplikaci Microsoft Dynamics 365 pro operace. 

Faktury pro projekt často přicházejí později než zboží a služby jsou dodávány, který může mít významný dopad na projekt klíčové ukazatele výkonu (KPI). Je důležité, aby bylo možné sledovat tyto transakce v obou finanční a projekt sestavy.

To ukazuje následující příklad scénáře. 

Konzultaci s contoso byl spuštěn nový projekt nasazení cloudu. Pokud chcete koupit počítač pro projekt je vytvořena nákupní objednávka. Počítače budou náklady na $1500 a instalační služby budou náklady na $150. Dodavatel má dodat a nainstalovat do počítače, ale fakturu ještě nedosáhla konzultaci Contoso. Vedoucí projektu chtěli nabíhání nákladů projektu z $1650 před dodáním faktury. Tyto náklady by projeví také v společnosti měsíc ukončení finanční výkazy. 

Časově rozlišené náklady musí být zaznamenány na finanční úrovni i na úrovni projektu pro účely vykazování. V 365 Dynamics pro operace lze sledovat finanční aktualizaci příjemky produktu pro kategorie zboží a zakázek. 

U položek na **parametry závazků** stránky, vyberte **zaúčtování příjemky produktu do knihy** možnost.
[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Pro kategorie zásobování na **pravidlo zásad kategorie** stránky, vyberte **nakupování** zásady a potom vyberte **časově rozlišených nákupní výdaj na příjemce** pro každou kategorii zásobování.
[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png) 

**Nákupní výdaj nefakturované** a **nákupu časového rozlišení** účtů v **nastavení účtování** bude použit při zaúčtování dokladů, které jsou spojené s touto příjemkou produktu.
[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png) 

Pomocí tohoto kanálu stejný scénář, podíváme se zaúčtování příjemky produktu bude vliv financí a informace o projektu. 

**Krok 1:** vytvořit a potvrďte novou nákupní objednávku pro projekt k zaznamenání nákupem počítače služby instalace a $1500 $150.
[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Při potvrzení nákupní objednávky potvrzené náklady transakce jsou vytvořeny pro projekt. 
[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Bude mít transakce potvrzené náklady **původ transakce** nastaveno na **nákupní objednávky**. Vytvoření a potvrzení nákupní objednávky nevytváří transakce pro projekt. 

**Krok 2:** doručení zboží a služeb a je registrována na příjemce produktu. 

Zaúčtování příjemky produktu generovat a zaúčtování dokladu do hlavní knihy. Doklad bude nákupní výdaje, nefakturované účet MD a Dal účet časového rozlišení nákupu. 
[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Zaúčtování příjemky produktu pomocí nastavení účtování pro kategorie zásobování produkty a nikoli nastavení účtování pro kategorie projektu. Správně odrážejí finanční dopad nákupní časové rozlišení, aby se toto nastavení musí být zarovnány. 

Je možné mapovat na kategorie zásobování kategorie projektu **kategorie zásobování** stránky.
[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)

**Krok 3:** vytvořit návrh faktury dodavatele. 

V 365 Dynamics pro operace zaúčtování příjemky produktu nemá vliv na informace o projektu. Tento problém odstraníte může generovat návrh faktury dodavatele přímo po zaúčtování nákupní příjemky. Přejděte **nákupní objednávky** stránku &gt;**faktura kartu**&gt;**generovat**&gt;**faktury**. Tím se vytvoří dokument čekající faktury, který aktualizuje informace o projektu. 

Vytvoření návrhu faktury dodavatele bude generovat čekající transakce projektu. 
[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png) 

V **potvrzené náklady** záznamy vytvořené v kroku 1 bude uzavřen a nové záznamy budou vytvořeny tak, aby odrážely náklady závazků přichází nevyřízené faktury dodavatele. **Původ transakce** pole potvrzené náklady bude nastavena na hodnotu **faktur dodavatele**.
[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)

Faktury dodavatele zůstanou ve stavu čekání, až přijde skutečná dodavatelské faktury.




