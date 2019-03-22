---
title: Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (7. února 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 23386d04fac5a41682d3ced448ce07e6729def3c
ms.sourcegitcommit: b3b21795f36e5852ffe18200d6fe0b93363b1cbd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/08/2019
ms.locfileid: "377725"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-7-2019"></a>Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (7. února 2019)

[!include [banner](includes/banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

### <a name="interview-scheduling-enhancements"></a>Vylepšení plánování pohovoru
Byla provedena vylepšení rozhraní pro plánování celého procesu pohovoru. Nyní můžete vidět dostupnost kalendáře interního kandidáta a použít kalendář interního kandidáta pro doporučení plánu. Další informace naleznete v tématu [Plánování pohovoru a zpětná vazba](interview-scheduling-feedback.md).

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a>Publikování pracovní nabídky na LinkedIn – problémy s neshodou společností byly opraveny
Byl opraven problém, kdy se nabídky práce publikované na LinkedIn z aplikace Attract zobrazovaly pod chybným názvem společnosti. Další informace naleznete v tématu [Vytvoření, schválení a publikování pracovních míst v aplikaci Attract](creating-jobs-attract.md).

### <a name="career-site-url-displayed-in-admin-settings"></a>Adresa URL kariérního webu zobrazená v nastavení pro správu
URL adresa domovské stránky kariérního webu se nyní zobrazuje v **Nastavení pro správu** pod položkou **Správa kariérního webu**.

## <a name="changes-in-core-hr"></a>Změny v Core HR

**Sestavení 8.1.2134**

### <a name="multiple-compensation-levels-supported-on-jobs"></a>Více úrovní kompenzací podporováno u prací
Tato změna umožňuje definovat více než jednu úroveň kompenzace pro práci, což umožňuje rozsahy fixní kompenzace zaměstnance, které se mohou lišit mezi plány při použití stejné práce. 

Například:    
*Práce* -Account manažer *Přidružené úrovně kompenzace:* B1 a B2 – Každá úroveň má definovaný rozsah hodnot. B1 = Min 50,000, Stř 60,000, Max 75,000 a B2 = Min 65,000, Stř 74,000, Max 85,000. Při vytváření fixní kompenzace pro zaměstnance, na základě definovaných pravidel nároku, může každý fixní plán nyní poukazovat na stejné pracovní místo a na různé úrovně pracovního místa. To umožňuje definovat plány v různých regionech/společnostech a poukazovat na stejnou práci, ale na rozdílné rozsahy, aniž by se zohledňovala duplicitní pracovní místa.

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a>Bylo přidáno pole úrovně kompenzace pro entitu fixní kompenzace zaměstnance 
Díky této aktualizaci byla entita fixní kompenzace zaměstnance aktualizována, aby zahrnovala pole **Úroveň kompenzace**. Toto přidání usnadňuje aktualizaci plánů fixní kompenzace zaměstnance. 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a>Aktualizace skupiny prací při aktualizaci a vytváření nových pozic
Při změně práce na pozici bude nyní ve výchozím nastavení **Skupina prací** na základě zvolené práce.

### <a name="performance-improvements-when-rendering-workspaces"></a>Zlepšení výkonu při vykreslování pracovního prostoru
Karta analýzy na pracovních prostorech se nyní načte pouze pří přístupu na tyto stránky. Během úvodního vykreslování stránky v levém horním rohu stránky se zobrazí indikátor.
