---
title: Přehled typů plánů
description: Typ plánu v Microsoft Dynamics 365 Human Resources je skupina na vysoké úrovni pro specifické typy zaměstnaneckých výhod.
author: twheeloc
ms.date: 08/24/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6ca14156c165ca3f536fc0120ebd03883284eb18
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336848"
---
# <a name="plan-type-overview"></a>Přehled typů plánů

[!include [banner](../includes/preview-banner.md)]

Typ plánu je skupina na vysoké úrovni pro specifické typy zaměstnaneckých výhod. Každý typ plánu má kód typu plánu, který určuje pravidla pro typ plánu. Například typ **základního životního** plánu bude mít kód typu plánu **Životní**, protože se jedná o typ plánu životního pojištění a musí vyhovovat pravidlům stanoveným pro kód typu plánu **životního** pojištění. Jiný typ plánu může být **Doplňkové životní**. Tento typ plánu bude mít také **Životní** kód typu plánu.

Každý typ plánu určuje, zda může zaměstnanec zaregistrovat jeden nebo více plánů. Zaměstnanec by například mohl být schopen zaregistrovat se pro **základní** a **doplňkové životní** pojištění u typu plánu životní. Zaměstnanec by pravděpodobně mohl zaregistrovat pouze jednu pojistku typu Zdravotní.

Pokud typ plánu zahrnuje kontakty, typ plánu indikuje, zda jsou kontakty příjemci nebo závislé osoby. **Základní typ životního plánu** by měl mít například oprávněné osoby, zatímco základní typ lékařského plánu by měl závislé osoby. V některých případech nesmí mít plán žádné osobní kontakty. Jedná se například o pružný účet výdajů nebo doplatek za parkování.


Typ plánu může definovat možnosti pokrytí. Možnosti pokrytí jsou definovány ve stránce **Možnosti pokrytí**. Možnost pokrytí může určovat výši zaměstnanecké výhody nebo kontakty, které mají nárok na typ plánu. Je-li například typem kontaktu **příjemce**, možnost pokrytí by měla definovat podmínky, které má příjemce nárokovat, pokud je výhoda využívána. Je-li typ kontaktu **závislá osoba**, možnost pokrytí by měla definovat vztah mezi závislou osobou a zaměstnancem. 

> [!IMPORTANT]
> Stránka **Typy plánu** obsahuje klíčová data, která ovlivňují možnosti, které jsou k dispozici při vytváření nového plánu výhod:
>
> - **Kód typu plánu** - Toto pole ovlivňuje to, co je zobrazeno na kartě **Konfigurace**, když je nastavena skutečná výhoda.  
> - **Souběžná registrace** - Toto pole určuje, zda je povoleno více registrací. (U lékařského plánu je toto pole obvykle nastaveno na **Jedna registrace**.)
> - **Typ kontaktu** - Toto pole umožňuje přidat závislé osoby nebo příjemce do plánu. Pokud je nastaven na **Žádný**, zaměstnanci, kteří si zaregistrují výhody, nebudou mít možnost vybrat si příjemce nebo závislou osobu.
> - **Možnosti pokrytí** - Toto pole slouží k propojení možností pokrytí s typy plánů. Definuje buď jednotlivce, na které se bude tento typ plánu vztahovat, nebo částky krytí, které jsou pro tento typ plánu k dispozici. Můžete například určit, že krytí pro typ zdravotního plánu bude k dispozici pouze zaměstnanci, zaměstnanci a jedné další osobě nebo zaměstnanci a jejich rodině.

## <a name="create-plan-types"></a>Vytvoření typů plánu

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
   | **Změnit možnost pokrytí** | Určuje, zda zaměstnanec může během životní události změnit možnosti pokrytí. |
   | **Změnit na nový plán** | Určuje, zda zaměstnanec může během životní události změnit plány. |
   | **Automaticky znovu otevřít kontrolu způsobilosti** | Určuje, zda se má automaticky znovu otevřít kontrola způsobilosti registrace k zaměstnaneckým výhodám během životní události. |
   | **Období registrace životní události** | Určuje časový úsek pro vykazování životní události ve dnech. **Poznámka**: Pokud nezadáte částku, systém předpokládá okno sestavy jako nulové a nezpracuje životní událost. |
   | **Upravitelné pouze správci** | Určuje, zda správci mohou zrušit nebo upravit plán zaměstnaneckých výhod během životní události. Zaměstnanec nemůže provádět žádné změny v pracovním prostoru **Zaměstnanecká samoobsluha**. |
   | **Automaticky zrušit plán** | Určuje, zda má být plán během životní události automaticky zrušen. Po zpracování změn životních událostí možnost **Automaticky zrušit plán** zachová výběr plánu. Odstraněn bude pouze stav **Potvrzeno** nebo **Rezervováno**. Plán zůstává vybraný. Zaměstnanci, kteří si nevyberou plán během období registrace životní události, tedy o výběr plánu nepřijdou. 

5. Zvolte možnost **Uložit**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
