---
title: Vytvoření typů plánu
description: Typ plánu v Microsoft Dynamics 365 Human Resources je skupina na vysoké úrovni pro specifické typy zaměstnaneckých výhod. Každý typ plánu má kód typu plánu, který určuje pravidla pro typ plánu.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 88a6d89bf98ea145bbb6a4eb8f4e052e5f4088e5
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429927"
---
# <a name="create-plan-types"></a>Vytvoření typů plánu

Typ plánu v Microsoft Dynamics 365 Human Resources je skupina na vysoké úrovni pro specifické typy zaměstnaneckých výhod. Každý typ plánu má kód typu plánu, který určuje pravidla pro typ plánu. Například typ základního životního plánu by měl mít kód typu plánu Životní, protože se jedná o druh plánu životního pojištění a musí vyhovovat pravidlům stanoveným pro kód typu plánu životního pojištění. Jiným typem plánu může být Doplňkové životní, rovněž s kódem typu plánu Životní.

Každý typ plánu určuje, zda může zaměstnanec zaregistrovat jeden nebo více plánů. Zaměstnanec by například mohl být schopen zaregistrovat se pro základní a doplňkové životní pojištění u typu plánu životní. Zaměstnanec by pravděpodobně mohl zaregistrovat pouze jednu pojistku typu Zdravotní.

Pokud typ plánu zahrnuje kontakty, typ plánu indikuje, zda jsou kontakty příjemci nebo závislé osoby. Základní typ životního plánu by měl mít například oprávněné osoby, zatímco základní typ lékařského plánu by měl závislé osoby. V některých případech nesmí mít plán žádné osobní kontakty. Jedná se například o pružný účet výdajů nebo doplatek za parkování.

Typ plánu může definovat možnosti pokrytí. Možnosti pokrytí jsou definovány ve formuláři možnosti pokrytí. Možnost pokrytí může určovat výši zaměstnanecké výhody nebo kontakty, které mají nárok na typ plánu. Je-li například typem kontaktu příjemce, možnost pokrytí by měla definovat podmínky, které má příjemce nárokovat, pokud je výhoda využívána. Je-li typ kontaktu závislá osoba, možnost pokrytí by měla definovat vztah mezi závislou osobou a zaměstnancem. 

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **typy plánu**.

2. Zvolte **Nové**.

3. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- |
   | **Typ plánu** | Jedinečný název, který identifikuje typ plánu. |
   | **Popis** | Popis typu plánu. |
   | **Kód typu plánu** | Z rozevíracího seznamu hodnot vyberte kód typu plánu. V seznamu kódů typu plánu se zobrazí všechny typy plánů, které jsou podporovány v aktuální verzi. |
   | **Souběžná registrace** | Určuje, zda může zaměstnanec registrovat více plánů zaměstnaneckých výhod stejného typu nebo pouze jeden plán zaměstnaneckých výhod na typ plánu. |
   | **Typ kontaktu** | Určuje úlohu osobního kontaktu. Hodnoty jsou prázdné, závislá osoba a příjemce. **Typ kontaktu** lze ponechat prázdný, pokud jeho typ plánu nevyžaduje závislou osobu nebo příjemce na základě možnosti pokrytí. |

4. Chcete-li konfigurovat možnosti události životního cyklu, vyberte možnost **Akce** a pak vyberte možnost **Možnosti události životního cyklu**. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- |
   | **Typ plánu** | Typ plánu pro konfiguraci možností životní události. |
   | **ID typu životních událostí** | ID typu životní události. |
   | **Povolit zrušení** | Určuje, zda zaměstnanec může během životní události zrušit plán zaměstnaneckých výhod. |
   | **Změnit možnost pokrytí** | Určuje, zda zaměstnanec může během životní události změnit možnosti pokrytí. |
   | **Změnit na nový plán** | Určuje, zda zaměstnanec může během životní události změnit plány. |
   | **Automaticky zrušit plán** | Určuje, zda má být během životní události plán automaticky zrušen. |
   | **Automaticky znovu otevřít kontrolu způsobilosti** | Určuje, zda se má automaticky znovu otevřít kontrola způsobilosti registrace k zaměstnaneckým výhodám během životní události. |
   | **Časový úsek pro vykazování** | Určuje časový úsek pro vykazování životní události ve dnech. **Poznámka**: Pokud nezadáte částku, systém předpokládá okno sestavy jako nulové a nezpracuje životní událost. |

5. Zvolte **Uložit**. 
