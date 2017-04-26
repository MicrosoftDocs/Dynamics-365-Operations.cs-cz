---
title: "Auditní porušení zásad a případy"
description: "Tento článek popisuje, jak jsou generovány případy auditu z porušení pravidel zásad auditu. Dále zahrnuje informace o různých způsobech použití rozsahu dat pro výběr dokumentu v zásadách auditu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: ecd32549b6067ed4c1211996e846e210f77f5013
ms.openlocfilehash: 77f72c9414f1fad720055e58e3f704b9c713072f
ms.lasthandoff: 03/31/2017


---

# <a name="audit-policy-violations-and-cases"></a>Auditní porušení zásad a případy

[!include[banner](../includes/banner.md)]


Tento článek popisuje, jak jsou generovány případy auditu z porušení pravidel zásad auditu. Dále zahrnuje informace o různých způsobech použití rozsahu dat pro výběr dokumentu v zásadách auditu.

<a name="how-audit-cases-are-generated"></a>Způsob generování případů auditu
-----------------------------

Zásady auditu slouží k identifikaci výkazy výdajů, nákupních objednávek a faktur dodavatele, které nejsou v souladu s obchodními pravidly, která se definují a nakonfigurují jako pravidla zásad auditu. 

Zásady auditu se spouští v dávkovém režimu. Při spuštění zásad auditu se všechna pravidla zásad, které jsou součástí zásady, spustí současně.

Každé pravidlo zásad vyhodnocuje sadu dokumentů. Pravidlo zásad vybere dokumenty, které se nacházejí v rozsahu dat pro výběr dokumentu, a přiřadí zadaná kritériím. Například jedno pravidlo zásad může vybrat výkazy výdajů, které mají stravování překračující 50,00. Jiné pravidlo zásad může vybrat dodavatelské faktury, které jsou splatné určitému dodavateli. Pro každý dokument, který je vybrán v sadě, se generuje porušení. Toto porušení je záznam, že určitý dokument, jako je například faktura 12345, nesplňuje pravidlo zásad. 

Vícenásobné záznamy o porušení auditu seskupeny a přidruženy k auditním případům. Ve výchozím nastavení se případy pro každou zásadu auditu seskupí podle pravidla zásad auditu. V případě potřeby můžete vybrat další kritéria pro seskupování pomocí stránky **Kritéria seskupování případu**. Záhlaví výdajů můžete například seskupit podle faktur projektu ID a dodavatele podle účtu dodavatele. V tomto případě všechny porušení záhlaví výdajů, které mají stejné ID projektu budou seskupeny ve stejném případě a ve stejném případě budou seskupeny všechny faktury dodavatele, které mají stejný účet dodavatele. 

> [!NOTE]
> Pro pravidla zásad auditu, které jsou založeny na **duplicitní** dotaz typu porušení nejsou seskupeny pomocí pravidla zásady nebo kritéria, která jsou určena na **kritéria seskupování případu** stránky. Místo toho se seskupují podle kritérií, která jsou součástí pravidla zásad auditu. Pokud například pravidlo zásad vyhodnocuje ve výkazech výdajů duplicitní výdaje se stelnou částkou, ID obchodníka a datem, všechny výdaje, které mají stejné hodnoty v těchto polích, budou jeden případ. Veškeré výdaje, které mají různé hodnoty, budou samostatný případ.

Auditní případy se po vygenerování zpracují pomocí typických procesů správy případů.

## <a name="document-selection-date-ranges"></a>Časová rozmezí pro výběr dokumentů
Po spuštění zásad auditu vybere každé pravidlo zásad dokumenty zadaného typu, které mají datum v rámci rozsahu dat pro výběr dokumentu. Rozsah dat pro výběr dokumentu je zadán na stránce **Další možnosti**. Mnoho dokumentů má přidruženo více než jedno datum. Pole data, která pravidlo zásad auditu používá, je zadáno na stránce **Typ pravidla zásad**.

Zde je několik dalších způsobů, které zásady auditu používají u rozsahu dat pro výběr dokumentu:

-   Zásady použijí verzi pravidla zásad, která je platná k poslednímu dni rozsahu dat pro výběr dokumentu. Data účinnosti můžete pro každé pravidlo zásad zobrazit na stránce se seznamem **Zásady auditu**.
-   Zásady používají organizační uzly, které jsou přidruženy k zásadám v poslední den rozsahu dat pro výběr dokumentu. Pouze organizační uzly, které jsou aktuálně přidruženy k zásadám, se zobrazují na stránce se seznamem **Zásady auditu**.
-   Pro pravidla zásad, která jsou založena na typu dotazu **Vyhledávání seznamu**, pravidla vyhodnocují v dokumentech sledované entity, které jsou účinné v poslední den rozsahu dat pro výběr dokumentu.


Další informace naleznete v tématu [pravidla zásad auditu](audit-policy-rules.md)




