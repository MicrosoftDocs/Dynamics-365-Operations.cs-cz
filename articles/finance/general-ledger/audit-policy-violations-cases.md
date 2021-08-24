---
title: Auditní porušení zásad a případy
description: Tento článek popisuje, jak jsou generovány případy auditu z porušení pravidel zásad auditu. Dále zahrnuje informace o různých způsobech použití rozsahu dat pro výběr dokumentu v zásadách auditu.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 057cb8afe0da5e0810a2d1c87f7cdbe73bc88b9819ca81631d889bfa1cc55e6c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758094"
---
# <a name="audit-policy-violations-and-cases"></a>Auditní porušení zásad a případy

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak jsou generovány případy auditu z porušení pravidel zásad auditu. Dále zahrnuje informace o různých způsobech použití rozsahu dat pro výběr dokumentu v zásadách auditu.

## <a name="how-audit-cases-are-generated"></a>Způsob generování případů auditu

Zásady auditu slouží k identifikaci výkazy výdajů, nákupních objednávek a faktur dodavatele, které nejsou v souladu s obchodními pravidly, která se definují a nakonfigurují jako pravidla zásad auditu. 

Zásady auditu se spouští v dávkovém režimu. Při spuštění zásad auditu se všechna pravidla zásad, které jsou součástí zásady, spustí současně.

Každé pravidlo zásad vyhodnocuje sadu dokumentů. Pravidlo zásad vybere dokumenty, které se nacházejí v rozsahu dat pro výběr dokumentu, a přiřadí zadaná kritériím. Například jedno pravidlo zásad může vybrat výkazy výdajů, které mají stravování překračující 50,00. Jiné pravidlo zásad může vybrat dodavatelské faktury, které jsou splatné určitému dodavateli. Pro každý dokument, který je vybrán v sadě, se generuje porušení. Toto porušení je záznam, že určitý dokument, jako je například faktura 12345, nesplňuje pravidlo zásad. 

Vícenásobné záznamy o porušení auditu seskupeny a přidruženy k auditním případům. Ve výchozím nastavení se případy pro každou zásadu auditu seskupí podle pravidla zásad auditu. V případě potřeby můžete vybrat další kritéria pro seskupování pomocí stránky **Kritéria seskupování případu**. Můžete například seskupit záhlaví výdajů podle ID projektu a faktury dodavatele podle účtu dodavatele. V takovém případě se všechna porušení záhlaví výdajů se stejným ID projektu seskupí do stejného případu a všechny faktury dodavatele, které mají stejný účet dodavatele, se seskupí do stejného případu. 

> [!NOTE]
> U pravidel zásad auditu, která jsou založena na dotazu typu **Duplicitní**, se porušení neseskupují podle pravidla zásad nebo kritérií zadaných na stránce **Kritéria seskupování případu**. Místo toho se seskupují podle kritérií, která jsou součástí pravidla zásad auditu. Pokud například pravidlo zásad vyhodnocuje ve výkazech výdajů duplicitní výdaje se stelnou částkou, ID obchodníka a datem, všechny výdaje, které mají stejné hodnoty v těchto polích, budou jeden případ. Veškeré výdaje, které mají různé hodnoty, budou samostatný případ.

Auditní případy se po vygenerování zpracují pomocí typických procesů správy případů.

## <a name="document-selection-date-ranges"></a>Časová rozmezí pro výběr dokumentů
Po spuštění zásad auditu vybere každé pravidlo zásad dokumenty zadaného typu, které mají datum v rámci rozsahu dat pro výběr dokumentu. Rozsah dat pro výběr dokumentu je zadán na stránce **Další možnosti**. Mnoho dokumentů má přidruženo více než jedno datum. Pole data, která pravidlo zásad auditu používá, je zadáno na stránce **Typ pravidla zásad**.

Zde je několik dalších způsobů, které zásady auditu používají u rozsahu dat pro výběr dokumentu:

-   Zásady použijí verzi pravidla zásad, která je platná k poslednímu dni rozsahu dat pro výběr dokumentu. Data účinnosti můžete pro každé pravidlo zásad zobrazit na stránce se seznamem **Zásady auditu**.
-   Zásady používají organizační uzly, které jsou přidruženy k zásadám v poslední den rozsahu dat pro výběr dokumentu. Pouze organizační uzly, které jsou aktuálně přidruženy k zásadám, se zobrazují na stránce se seznamem **Zásady auditu**.
-   Pro pravidla zásad, která jsou založena na typu dotazu **Vyhledávání seznamu**, pravidla vyhodnocují v dokumentech sledované entity, které jsou účinné v poslední den rozsahu dat pro výběr dokumentu.


Další informace naleznete v tématu [Pravidla zásad auditu](audit-policy-rules.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]