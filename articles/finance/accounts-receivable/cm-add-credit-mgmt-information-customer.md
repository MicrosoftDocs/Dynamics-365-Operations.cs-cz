---
title: Přidání informací o správě úvěru pro odběratele
description: Tento článek vysvětluje, jak přidat informace o správě úvěru pro odběratele.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5cdbae5e1fae8cb1922e165d30dd555a4ef375d9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861582"
---
# <a name="add-credit-management-information-for-customers"></a>Přidání informací o správě úvěru pro odběratele

[!include [banner](../includes/banner.md)]

Po nastavení parametrů, které řídí správu úvěru, můžete přidat další podrobnosti pro jednotlivé odběratele. Tyto podrobnosti určují procesy správy úvěru a také poskytují další informace, které pomáhají členům inkasního týmu při správě odběratelů.

## <a name="customer-information"></a>Informace o odběrateli

Podrobnosti o odběrateli lze přidat na pevné záložce **Úvěr a inkasa** na stránce **Všichni odběratelé** (**Pohledávky \> Odběratelé \> Všichni odběratelé**).

1. Nastavte možnost **Neomezený limit úvěru** na **Ano**, nemá-li být odběratel omezen žádnými testy limitu úvěru.
2. Nastavte možnost **Vyloučit ze správy úvěru** na **Ano** pro vyloučení odběratele ze všech úkonů, které jsou obvykle prováděny během procesů správy úvěru.
3. Vyberte skupinu správy úvěru pro odběratele.
4. Pro výpočet limitu úvěru v měně odběratele zadejte do pole **Limit úvěru v měně odběratele** limit úvěru odběratele. Limit úvěru v měně společnosti bude převeden s použitím směnných kurzů, které jsou definovány typem směnného kurzu limitu úvěru vybraným v rámci **parametrů správy úvěru**.
5. Do pole **Datum poslední kontroly** zadejte datum, kdy byl limit úvěru odběratele naposledy zkontrolován správcem úvěru.
6. Do pole **Datum příští plánované kontroly** zadejte datum, kdy je plánována kontrola a aktualizace úvěru odběratele.
7. Do pole **Přípustný limit úvěru** zadejte nejvyšší limit úvěru, který může být přidělen odběrateli na základě vaší kontroly úvěrové historie tohoto odběratele. Přípustný limit úvěru se může lišit od limitu úvěru, který se zobrazuje na pevné záložce **Úvěr a inkasa**.
8. Do pole **Měna přípustného limitu úvěru** zadejte měnu přípustného limitu úvěru.
9. Do pole **Datum přípustného limitu úvěru** zadejte datum vytvoření přípustného limitu úvěru.
10. Do pole **Stav úvěrového účtu** zadejte stav úvěrového účtu odběratele.
11. Do pole **Důvod stavu** zadejte důvod, který je spojen se stavem účtu.
12. Chcete-li označit, že je odběratel momentálně přiřazen k úvěrové agentuře, nastavte možnost **S agenturou** na **Ano**. Tato hodnota je určena pouze pro informaci. Není používána v žádných procesech správy úvěru.
13. Chcete-li označit, že je název držen pro společnost, nastavte možnost **Název držen** na **Ano**. Tato hodnota je určena pouze pro informaci. Není používán v žádném procesu správy úvěru.
14. Do pole **Datum zahájení podnikání** zadejte datum, kdy odběratel poprvé zahájil podnikání. Tyto informace se používají při vytváření hodnocení rizik.
15. Do pole **Odběratelem od** zadejte datum, kdy byly zpracovány první transakce pro tohoto odběratele. Tyto informace se používají při vytváření hodnocení rizik.
16. Zadejte poznámky, které může úvěrový tým použít k dalšímu vyhodnocení úvěrové způsobilosti odběratele.

> [!Note] 
> Některé informace zobrazené na stránce **Odběratel** jsou vytvořeny jiným procesem:

- V poli **Datum vypršení platnosti limitu úvěru** se zobrazuje datum, kdy vyprší platnost limitu úvěru. Pokud toto pole nenastavíte, platnost limitu úvěru odběratele nevyprší.
- V poli **Datum limitu úvěru** se zobrazuje datum, kdy byl limit úvěru vytvořen. Toto pole je aktualizováno při každé úpravě limitu úvěru.
- Dočasné limity úvěru ruší limit úvěru odběratele po určitou dobu. Používají se místo limitu úvěru k výpočtu celkového limitu úvěru. Tento údaj se zobrazí pouze v případě, že existuje aktivní limit úvěru. Dočasné limity úvěru můžete přidávat prostřednictvím úprav limitů úvěru.
- V poli **Pojištění a záruky** se zobrazuje celková hodnota pojištění a záruk, která může zvýšit limit úvěru odběratele.
- V poli **Celkový limit úvěru** se zobrazuje konečný limit úvěru odběratele. Celkový limit úvěru zahrnuje pojištění a záruky a dočasné limity úvěru.

## <a name="temporary-credit-limits"></a>Dočasné limity úvěru

Dočasné limity úvěru ruší limity úvěru odběratele po stanovenou dobu. Dočasné limity úvěru můžete přidávat pomocí úprav limitů úvěru. Úpravy limitu úvěru umožňují správcům úvěrů aktualizovat limity úvěru a data vypršení platnosti jednoho odběratele, skupiny odběratelů nebo všech odběratelů prostřednictvím procesu zaúčtování.

Položky úprav limitu úvěru můžete vytvořit na stránce **Úpravy limitu úvěru** (**Správa úvěru \> Úpravy limitu úvěru \> Úpravy limitu úvěru**).

## <a name="create-insurance-policies-and-guarantees"></a>Vytvoření pojistek a záruk

Pro každého odběratele lze vytvořit jednu nebo více pojistek a záruk. Poté je můžete použít k výpočtu expozice, kterou má vaše společnost při nabízení úvěru odběrateli. Pojistky a záruky lze rovněž zahrnout do limitu úvěru odběratele.

Na stránce **Všichni odběratelé** (**Pohledávky \> Odběratelé \> Všichni odběratelé**) můžete vytvořit pojistky a záruky. Vyberte odběratele a poté v podokně Akce na záložce **Správa úvěru** zvolte možnost **Pojištění a záruky**.

> [!NOTE]
> V rámci níže uvedeného postupu zvolte pojistitele nebo ručitele z globálního adresáře. Proto je před zahájením tohoto postupu nutné zajistit, aby pojistitelé a ručitelé byli přidáni do globálního adresáře.

1. Do pole **Identifikátor** zadejte **Záruka** nebo **Pojištění**.
2. V poli **Typ záruky/pojištění** zvolte jeden z typů záruky nebo pojištění, který jste předtím nastavili.
3. V poli **Pojistitel/ručitel** zvolte pojistitele nebo ručitele z globálního adresáře. 
4. Pokud jste zvolili možnost **Pojištění** v poli **Identifikátor**, v poli **Typ krytí pojistky**, zvolte jeden z typů krytí , který jste předtím nastavili. Nelze zvolit typ krytí pojistky pro záruku.
5. Do pole **Identifikace** zadejte ID pojistky. Toto ID je obvykle číslo pojistky.
6. Do pole **Účinnost** zadejte počáteční datum pojistky nebo záruky.
7. Do pole **Vypršení platnosti** zadejte datum vypršení platnosti pojistky nebo záruky .
8. Do pole **Hodnota** zadejte hodnotu pojistky nebo záruky. Tato hodnota představuje úplnou hodnotu pojistky.
9. V poli **Měna** vyberte měnu pro hodnotu pojistky. 
10. V poli **Aktualizovat limit úvěru** uveďte procentní hodnotu **0** až **100**. Tato procentní hodnota bude použita pro hodnotu pojistky a výsledná částka bude použita ke zvýšení limitu úvěru, který se používá při výpočtech limitu úvěru. Vypočtená hodnota se zobrazí pod položkou **Celkový limit úvěru, pojištění a záruka** na pevné záložce **Úvěr a inkasa** na stránce **Odběratelé**.

    Následuje příklad:

    - Limit úvěru (A) je 100 000.
    - Hodnota pojistky (B) je 50 000.
    - Procentní hodnota **Aktualizovat limit úvěru** (C) je 50,00.
    
    V tomto případě je účinný limit úvěru 125 000 (= A + \[B × C\]).

11. Označením políčka **Zahrnuto v expozici** snížíte limit úvěru, který se používá při výpočtech limitu úvěru o celou hodnotu pojistky. Je-li označeno toto políčko, nebude při výpočtech limitu úvěru použita hodnota vypočtená při uvedení procentní hodnoty **Aktualizovat limit úvěru**.

    Následuje příklad:

    - Limit úvěru (A) je 100 000.
    - Hodnota pojistky (B) je 50 000.
    - Procentní hodnota **Aktualizovat limit úvěru** (C) je 50,00.

    V tomto případě je účinný limit úvěru 125 000 (= A + \[B × C\]).
    
    Pokud však zvolíte políčko **Zahrnuto v expozici**, bude hodnota **Aktualizovat limit úvěru** 50 000 (= 50,00 % ze 100 000) odebrána a hodnota expozice je 75 000 (= A + \[B × C\] – B).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
