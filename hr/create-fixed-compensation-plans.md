---
title: "Vytvoření plánů fixní kompenzace"
description: "Fixní kompenzace odkazuje na pravidelný hrubý plat nebo mzdy zaměstnance. Tento článek popisuje součásti, které je nutné nastavit před vytvořením plánu fixní kompenzace a přihlášením zaměstnanců."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: bbf08a9620dbc8ad928fe40a3ae5e9b2a2fcb373
ms.lasthandoff: 03/31/2017


---

# <a name="create-fixed-compensation-plans"></a>Vytvoření plánů fixní kompenzace

[!include[banner](includes/banner.md)]


Fixní kompenzace odkazuje na pravidelný hrubý plat nebo mzdy zaměstnance. Toto téma popisuje součásti, které musí být nastaveny před vytvoření plánu fixní kompenzace zaměstnance zapsat.

Částky fixní kompenzace lze vypočítat pro zaměstnance na základě faktorů, jako je výkon, oblast a zvýšení rozpočtu. 365 Microsoft Dynamics pro operace podporuje krok, třídy a typy band kompenzací.

## <a name="fixed-compensation-components"></a>Komponenty fixní kompenzace
### <a name="compensation-levels"></a>Úrovně kompenzace

Můžete použít **úrovně kompenzace** nastavení kompenzace pro různé úlohy, k zajištění, aby zaměstnanci, kteří jsou držiteli těchto úloh jsou vypláceny poměrně. Na **úrovně kompenzace** stránky, můžete nastavit úrovně kompenzace, které jsou požadovány pro každý krok, jakost a plán pásma. Použijte tlačítka **Nahoru** a **Dolů** k seřazení úrovní do správného pořadí podle typu. Nastavením úrovní kompenzace u pracovní pozice pomůžete zajistit, že jsou všichni zaměstnanci, kteří zastávají tuto pozici, zaplaceni na stejné úrovni.

### <a name="reference-points"></a>Referenční body

**Referenční body** jsou sloupce v mřížce definující rozsahy kompenzace pro každou úroveň. Úroveň kompenzace je řádek v mřížce. Typický referenční body pro plán typu třídy jsou minimum, střední bod a maximální. Vytvoření referenčních bodů na **nastavení referenčních bodů** stránky.

### <a name="compensation-grids"></a>Kompenzační mřížky

Po nastavení úrovní a referenčních bodů je lze zkombinovat a vytvořit **mřížku kompenzací**. Na stránce **Kompenzační mřížky** definujte informace o mřížce. Například určete, k čemu se má mřížka použít, pro jaký typ plánu se má použít a které referenční body nebo sloupce jsou v mřížce vyžadovány. Po dokončení zadávání informací klikněte na tlačítko **Struktura kompenzací** a přidejte úrovně a částky do mřížky. 

**Tip:** Použijte funkci **Změny hmotnosti** ve struktuře kompenzace, abyste nastavili počáteční částky a poté zvyšujte po procentech nebo částkách napříč úrovněmi či referenčními body.

### <a name="pay-frequencies"></a>Interval plateb

**Interval plateb** se používá k definici způsobu, jakým se určuje mzda zaměstnance (například 10 USD za hodinu nebo a 50 000 USD za rok) a převodu mezi hodinovými, týdenními, měsíčními (dvanáct měsíců) a ročními sazbami. Například společnost, která pro své hodinově placené zaměstnance používá 38hodinový pracovní týden, nastaví interval plateb, který má hodinovou sazbu 1, týdenní sazbu 38, měsíční sazbu 164,6666666667 a roční sazbu 1 976. Tyto převody se používají pro výpočet různých mzdových sazeb, které se objevují na zaměstnancově záznamu fixní kompenzace.

## <a name="fixed-compensation-plans"></a>Plány fixní kompenzace
Můžete navrhnout plán fixní kompenzace, abyste zkombinovali všechny nakonfigurované komponenty. Chcete-li vytvořit plán fixní kompenzace, otevřete stránku **Plány fixní kompenzace**. Zde můžete plán pojmenovat, přiřadit mu popis, zvolit typ plánu (krok, stupeň nebo pásmo), vybrat interval plateb, který se bude používat pro platební sazbu zaměstnance (částka za hodinu, částka za rok atd.), a nastavit možnosti, které určují způsob zpracování kompenzace. 

Nastavení **Tolerance mimo rozsah** umožňuje určit, jak důslední chcete být při dohledu, aby částky kompenzace byly mezi minimální a maximální částkou. **Pevná tolerance** vyžaduje, aby kompenzace byla v rozsahu definovaném pro danou úroveň. **Předběžná** tolerance upozorní, když je částka kompenzace mimo rozsah, ale umožní pokračovat. Nastavíte-li toleranci na hodnotu **Žádná**, můžete zadávat libovolné částky kompenzace pro zaměstnance bez zobrazení upozornění nebo chybových zpráv. 

**Pravidla zařazení** nastavení umožňuje určit, zda všechny zaměstnance, by měl dostat stejné zvýšení, a to bez ohledu na datum, které byly přijaty (**pravidla zařazení** = **žádný**), nebo zda zaměstnanci měli obdržet podíl zakázky založené na jak dlouho byli zaměstnáni během cyklu (**pravidla zařazení** = **%**). 

**Matice využití rozsahu** je užitečná, pokud chcete buď zkrátit čas, který zaměstnanci potřebují k dosažení středového bodu rozsahu, nebo prodloužit dobu, kterou zaměstnanci potřebují k dosažení maximálního referenčního bodu v rozsahu. Například chcete přidělit zaměstnancům, kteří jsou v dolních 25 procentech svého rozsahu, 110 procent jejich cílové odměny, ale chcete přidělit zaměstnancům, kteří jsou v horních 25 procentech svého rozsahu, pouze 80 procent jejich cílové odměny, abyste jim zabránili stejně rychlého dosažení maxima. 

Po definování základů plánu fixní kompenzace můžete nastavit kompenzační strukturu plánu. Klepněte na tlačítko **nastavit kompenzaci**. Jezdec dialogové okno otevře, jsou tři možnosti:

-   Vytvoření nové kompenzační mřížky výběrem nastavení referenčního bodu a pojmenování mřížky.
-   Vytvoření nové kompenzační mřížky zkopírováním existující mřížky, kterou lze použít jako výchozí bod.
-   Použití existující kompenzační mřížky, která již byla definována. Všechny plány kompenzace, které používají stejnou mřížku, se při změně v této mřížce aktualizují.

Po výběru možnosti se otevře stránka **Struktura kompenzací**, na které můžete provést změny v nové nebo existující kompenzační mřížce.

## <a name="fixed-compensation-enrollment"></a>Přihlášení fixní kompenzace
### <a name="determine-who-is-eligible-for-the-plan"></a>Určení osob způsobilých pro plán

Prvním krokem při přihlašování zaměstnanců do plánu fixní kompenzace je určení, kdo má nárok na kompenzaci definovanou v plánu. Dokud způsobilost neurčíte, nebude možné přiřadit k plánu zaměstnance. Otevřete nastavení nároku, **pravidla způsobilosti** stránky. Zde vytvoříte nové způsobilosti pro plán kompenzace pravidla a definovat kritéria, která musí splňovat zaměstnanec způsobilé k plánu. Způsobilost můžete omezit podle oddělení, odborů, oblasti kompenzace (umístění), pracovní pozice, pracovní funkce, typu práce nebo úrovně kompenzace. Zaměstnance lze zařadit do plánu kompenzace pouze v případě, že splňují všechny podmínky, které jsou nastaveny na pravidlo způsobilosti. 

**Poznámka:** Pravidla způsobilosti se používají pro určení způsobilosti u fixních i variabilních kompenzačních plánů. 

Pravidlo způsobilosti se bere v úvahu hodnoty polí v záznamech Práce, Pozice a Zaměstnanec a určí, zda je zaměstnanec způsobilý pro kompenzační plán.

-   Na stránce **Práce** bere pravidlo způsobilosti v úvahu následující pole:
    -   Pole **Práce**
    -   Na kartě **Klasifikace práce** pole **Funkce** a **Typ práce**
    -   Na kartě **Kompenzace** pole **Úroveň**
-   Na stránce **Pozice** bere pravidlo způsobilosti v úvahu pole **Oddělení** a **Oblast kompenzace**.

Pravidla způsobilosti se považuje také odbory, které jsou spojeny s zaměstnance (na **zaměstnanci** na stránky **pracovní** karta, klepněte na tlačítko **osobní údaje**&gt;**odbory**).

### <a name="define-fixed-compensation-actions"></a>Definování akcí fixní kompenzace

**Akce fixní kompenzace** se používají, pokud chcete nastavit nebo použít změny ve fixní kompenzaci zaměstnance. Akce fixních kompenzací vám umožňují zadat popisné názvy pro typy akcí, které může manažer kompenzací a zaměstnaneckých výhod provádět. Různé typy akcí mají specifickou logiku, aby je bylo možné provést v určitou dobu. 

Například při nastavení fixní kompenzace pro určitého zaměstnance lze použít pouze akce, které mají typ **Zařadit nebo znovu zařadit**. Tímto způsobem můžete například vytvořit tři různé akce typu **Zařadit nebo znovu zařadit** a nazvat je **Zařadit**, **Znovu zařadit** a **Převod**. Můžete mít tedy popisnější vysvětlení, proč se fixní kompenzace zaměstnanci přidělila nebo změnila.

### <a name="enroll-the-employee"></a>Přihlášení zaměstnance

Nyní můžete přiřadit zaměstnance k plánu fixní kompenzace. Otevřete stránku **Zaměstnanci** a vyberte zaměstnance, kterého chcete zařadit do plánu kompenzace. V podokně akcí klepněte na tlačítko **kompenzace**&gt;**dlouhodobého plánu**. Nyní můžete vytvořit nové akce fixní kompenzace pro zaměstnance. 

**Poznámka:** pole plánu kompenzace zobrazí jen plány, pro které je zaměstnanec způsobilý podle pravidel způsobilosti nastavených pro každý plán. Není-li pro plán nastaveno žádné pravidlo způsobilosti, nebude pro něj způsobilý žádný zaměstnanec. 

Systém ověří, zda je zadaná částka kompenzace uvedená pro plán kompenzace typu stupeň nebo pásmo mezi minimálním a maximálním referenčním bodem úrovně kompenzace v dané pozici zaměstnance. Pokud je částka kompenzace mimo povolený rozsah, zobrazí se upozornění nebo chybová zpráva v závislosti na úrovni tolerance, která je nastavena v plánu fixní kompenzace.

<a name="see-also"></a>Viz také
--------

[Plány kompenzace](compensation-plans.md)




