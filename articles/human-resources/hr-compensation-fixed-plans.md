---
title: Vytvoření plánů fixní kompenzace
description: Fixní kompenzace odkazuje na pravidelný hrubý plat nebo mzdy zaměstnance. Tento článek popisuje součásti, které je nutné nastavit před vytvořením plánu fixní kompenzace a přihlášením zaměstnanců.
author: andreabichsel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: cc6a639bd593b9a41217a054023a9de82f373c1f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465767"
---
# <a name="create-a-fixed-compensation-plans"></a>Vytvoření plánů fixní kompenzace

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Fixní kompenzace odkazuje na pravidelný hrubý plat nebo mzdy zaměstnance. Tento článek popisuje součásti, které je nutné nastavit před vytvořením plánu fixní kompenzace a přihlášením zaměstnanců.

Částky fixní kompenzace lze vypočítat pro zaměstnance na základě faktorů, jako je výkon, oblast a zvýšení rozpočtu. Dynamics 365 Human Resources podporuje typy kompenzace kroku, stupně a pásma.

## <a name="fixed-compensation-components"></a>Komponenty fixní kompenzace
### <a name="compensation-levels"></a>Úrovně kompenzace

**Úrovně kompenzace** můžete použít k nastavení kompenzací pro různé pracovní pozice, abyste pomohli zajistit, že zaměstnanci na těchto pozicích jsou placeni odpovídajícím způsobem. Na stránce **Úrovně kompenzace** lze nastavit úrovně kompenzace požadované pro každý krok, stupeň a pásmo. Použijte tlačítka **Nahoru** a **Dolů** k seřazení úrovní do správného pořadí podle typu. Nastavením úrovní kompenzace u pracovní pozice pomůžete zajistit, že jsou všichni zaměstnanci, kteří zastávají tuto pozici, zaplaceni na stejné úrovni.

### <a name="reference-points"></a>Referenční body

**Referenční body** jsou sloupce v mřížce definující rozsahy kompenzace pro každou úroveň. Úroveň kompenzace je řádek v mřížce. Typické referenční body pro plán typu stupeň jsou minimum, středový bod a maximum. Referenční body vytvoříte na stránce **Nastavení referenčních bodů**.

### <a name="compensation-grids"></a>Kompenzační mřížky

Po nastavení úrovní a referenčních bodů je lze zkombinovat a vytvořit **mřížku kompenzací**. Na stránce **Kompenzační mřížky** definujte informace o mřížce. Například určete, k čemu se má mřížka použít, pro jaký typ plánu se má použít a které referenční body nebo sloupce jsou v mřížce vyžadovány. Po dokončení zadávání informací klikněte na tlačítko **Struktura kompenzací** a přidejte úrovně a částky do mřížky. 

**Tip:** Použijte funkci **Změny hmotnosti** ve struktuře kompenzace, abyste nastavili počáteční částky a poté zvyšujte po procentech nebo částkách napříč úrovněmi či referenčními body.

### <a name="pay-frequencies"></a>Interval plateb

**Interval plateb** se používá k definici způsobu, jakým se určuje mzda zaměstnance (například 10 USD za hodinu nebo a 50 000 USD za rok) a převodu mezi hodinovými, týdenními, měsíčními (dvanáct měsíců) a ročními sazbami. Například společnost, která pro své hodinově placené zaměstnance používá 38hodinový pracovní týden, nastaví interval plateb, který má hodinovou sazbu 1, týdenní sazbu 38, měsíční sazbu 164,6666666667 a roční sazbu 1 976. Tyto převody se používají pro výpočet různých mzdových sazeb, které se objevují na zaměstnancově záznamu fixní kompenzace.

## <a name="fixed-compensation-plans"></a>Plány fixní kompenzace
Můžete navrhnout plán fixní kompenzace, abyste zkombinovali všechny nakonfigurované komponenty. Chcete-li vytvořit plán fixní kompenzace, otevřete stránku **Plány fixní kompenzace**. Zde můžete plán pojmenovat, přiřadit mu popis, zvolit typ plánu (krok, stupeň nebo pásmo), vybrat interval plateb, který se bude používat pro platební sazbu zaměstnance (částka za hodinu, částka za rok atd.), a nastavit možnosti, které určují způsob zpracování kompenzace. 

Nastavení **Tolerance mimo rozsah** umožňuje určit, jak důslední chcete být při dohledu, aby částky kompenzace byly mezi minimální a maximální částkou. **Pevná tolerance** vyžaduje, aby kompenzace byla v rozsahu definovaném pro danou úroveň. **Předběžná** tolerance upozorní, když je částka kompenzace mimo rozsah, ale umožní pokračovat. Nastavíte-li toleranci na hodnotu **Žádná**, můžete zadávat libovolné částky kompenzace pro zaměstnance bez zobrazení upozornění nebo chybových zpráv. 

Nastavení **Pravidlo zařazení** umožňuje určit, zda mají všichni zaměstnanci získat stejné zvýšení bez ohledu na datum, kdy byli přijati (**Pravidlo zařazení**  = **Žádné**), nebo zda mají získat procentuální odměnu podle toho, jak dlouho byli v cyklu zaměstnáni (**Pravidlo zařazení**  = **Procento**). 

**Matice využití rozsahu** je užitečná, pokud chcete buď zkrátit čas, který zaměstnanci potřebují k dosažení středového bodu rozsahu, nebo prodloužit dobu, kterou zaměstnanci potřebují k dosažení maximálního referenčního bodu v rozsahu. Například chcete přidělit zaměstnancům, kteří jsou v dolních 25 procentech svého rozsahu, 110 procent jejich cílové odměny, ale chcete přidělit zaměstnancům, kteří jsou v horních 25 procentech svého rozsahu, pouze 80 procent jejich cílové odměny, abyste jim zabránili stejně rychlého dosažení maxima. 

Po definování základů plánu fixní kompenzace můžete nastavit kompenzační strukturu plánu. Klikněte na **Nastavit kompenzaci**. Otevře se dialogové okno posuvníku obsahující tři možnosti:

-   Vytvoření nové kompenzační mřížky výběrem nastavení referenčního bodu a pojmenování mřížky.
-   Vytvoření nové kompenzační mřížky zkopírováním existující mřížky, kterou lze použít jako výchozí bod.
-   Použití existující kompenzační mřížky, která již byla definována. Všechny plány kompenzace, které používají stejnou mřížku, se při změně v této mřížce aktualizují.

Po výběru možnosti se otevře stránka **Struktura kompenzací**, na které můžete provést změny v nové nebo existující kompenzační mřížce.

## <a name="fixed-compensation-enrollment"></a>Přihlášení fixní kompenzace
### <a name="determine-who-is-eligible-for-the-plan"></a>Určení osob způsobilých pro plán

Prvním krokem při přihlašování zaměstnanců do plánu fixní kompenzace je určení, kdo má nárok na kompenzaci definovanou v plánu. Dokud způsobilost neurčíte, nebude možné přiřadit k plánu zaměstnance. Chcete-li nárok nastavit, otevřete stránku **Pravidla způsobilosti**. Můžete zde vytvořit nové pravidlo způsobilosti pro kompenzační plán a definovat kritéria, která musí zaměstnanec splňovat, aby měl na plán nárok. Způsobilost můžete omezit podle oddělení, odborů, oblasti kompenzace (umístění), pracovní pozice, pracovní funkce, typu práce nebo úrovně kompenzace. Zaměstnance lze zařadit do plánu kompenzace pouze v případě, že splňují všechny podmínky, které jsou nastaveny na pravidlo způsobilosti. 

**Poznámka:** Pravidla způsobilosti se používají pro určení způsobilosti u fixních i variabilních kompenzačních plánů. 

Pravidlo způsobilosti se bere v úvahu hodnoty polí v záznamech Práce, Pozice a Zaměstnanec a určí, zda je zaměstnanec způsobilý pro kompenzační plán.

-   Na stránce **Práce** bere pravidlo způsobilosti v úvahu následující pole:
    -   Pole **Práce**
    -   Na kartě **Klasifikace práce** pole **Funkce** a **Typ práce**
    -   Na kartě **Kompenzace** pole **Úroveň**
-   Na stránce **Pozice** bere pravidlo způsobilosti v úvahu pole **Oddělení** a **Oblast kompenzace**.

Pravidlo způsobilosti dále bere v úvahu odbory, které jsou přidruženy k zaměstnanci (na stránce **Zaměstnanci** na kartě **Pracovník** klikněte na **Osobní údaje** &gt; **Odbory**).

### <a name="define-fixed-compensation-actions"></a>Definování akcí fixní kompenzace

**Akce fixní kompenzace** se používají, pokud chcete nastavit nebo použít změny ve fixní kompenzaci zaměstnance. Akce fixních kompenzací vám umožňují zadat popisné názvy pro typy akcí, které může manažer kompenzací a zaměstnaneckých výhod provádět. Různé typy akcí mají specifickou logiku, aby je bylo možné provést v určitou dobu. 

Například při nastavení fixní kompenzace pro určitého zaměstnance lze použít pouze akce, které mají typ **Zařadit nebo znovu zařadit**. Tímto způsobem můžete například vytvořit tři různé akce typu **Zařadit nebo znovu zařadit** a nazvat je **Zařadit**, **Znovu zařadit** a **Převod**. Můžete mít tedy popisnější vysvětlení, proč se fixní kompenzace zaměstnanci přidělila nebo změnila.

### <a name="enroll-the-employee"></a>Přihlášení zaměstnance

Nyní můžete přiřadit zaměstnance k plánu fixní kompenzace. Otevřete stránku **Zaměstnanci** a vyberte zaměstnance, kterého chcete zařadit do plánu kompenzace. V podokně akcí klikněte na možnost **Kompenzace** &gt; **Fixní plán**. Nyní můžete vytvořit novou akci fixní kompenzace pro zaměstnance. 

**Poznámka:** pole plánu kompenzace zobrazí jen plány, pro které je zaměstnanec způsobilý podle pravidel způsobilosti nastavených pro každý plán. Není-li pro plán nastaveno žádné pravidlo způsobilosti, nebude pro něj způsobilý žádný zaměstnanec. 

Systém ověří, zda je zadaná částka kompenzace uvedená pro plán kompenzace typu stupeň nebo pásmo mezi minimálním a maximálním referenčním bodem úrovně kompenzace v dané pozici zaměstnance. Pokud je částka kompenzace mimo povolený rozsah, zobrazí se upozornění nebo chybová zpráva v závislosti na úrovni tolerance, která je nastavena v plánu fixní kompenzace.



[!INCLUDE[footer-include](../includes/footer-banner.md)]