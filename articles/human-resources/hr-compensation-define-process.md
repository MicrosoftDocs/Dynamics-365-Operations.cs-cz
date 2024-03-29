---
title: Definovat proces kompenzací a vypočítat výsledky
description: Procesy kompenzace slouží k určení částek nové kompenzace a odměn pro zaměstnance, které jsou přihlášené do plánů fixní i variabilní kompenzace.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompProcess, HRMCompProcessLine, HRMCompEvent, HRMCompEventEmpl, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 196c907521bba5440f12149abcb2fc446c2aa523
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687044"
---
# <a name="define-compensation-process-and-calculate-results"></a>Definovat proces kompenzací a vypočítat výsledky


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Procesy kompenzace slouží k určení částek nové kompenzace a odměn pro zaměstnance, které jsou přihlášené do plánů fixní i variabilní kompenzace. Procesy kompenzace mohou být spuštěny více než jednou k provedení analýzy „co když“ a ověření správnosti všech změn a nastavení. Tento postup vytvoří proces kompenzace, spustí proces a zobrazí výsledky. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="create-a-compensation-process"></a>Vytvořit proces kompenzace
1. Jděte na **Správa kompenzace** > **Proces** > **Proces kompenzace**.
2. Klikněte na **Nový proces kompenzace**.
3. Zadejte hodnotu do **pole Proces**.
4. Zadejte hodnotu do pole **Popis**.
5. Vyberte možnost v poli **Typ zpracování**.
    * Cyklus určuje časové období vyhodnocené ke stanovení kompenzace. Hodnocení bere v úvahu pozice, které byly využito zaměstnanci, která hodnocení výkonnosti se mají zahrnout, výpočet procenta času, kdy byl zaměstnanec během cyklu zaměstnán a další. Příkladem data začátku cyklu může být první den uplynulého fiskálního roku.  
6. Zadejte datum do pole **Počátek cyklu**.
    * Koncové datum cyklu je důležité, protože se jedná o datum používané k určení, kteří zaměstnanci byli aktivně zaměstnaní a zařazeni do jednoho nebo několika plánů kompenzace.  
7. Zadejte datum do pole **Konec cyklu**.
    * Aktivní datum transakce je datum, kdy mají být uplatněny nové míry kompenzací. Mnoho společností zahrnuje několik měsíců mezi jejich koncem cyklu a časem uplatnění nových kurzů kompenzací. Zpracování a kontrola nové kompenzace vyžaduje další čas.  
8. Zadejte datum do pole **Aktivní datum transakce**.
    * Datum časového okamžiku slouží pro plány variabilní kompenzace, které určují částku odměny zaměstnance na základě jeho míry kompenzace v daném okamžiku.  
    * Fixní mzda v poměru k datu zařazení je použita s plány fixní kompenzace s pravidlem zařazení **Procento**. Zaměstnanci, kteří jsou přijati mezi počátkem cyklu a fixní mzda v poměru k datu zařazení obdrží 100 % svého vypočteného zvýšení kompenzace namísto procenta navýšení.  
9. Do pole **Fixní mzda v poměru k datu zařazení** zadejte datum.
    * Termín kontroly je datum, dokdy musí zkontrolovat všechny výsledky procesu tak, aby mohly být načteny do záznam kompenzace zaměstnance před aktivním datem transakce. Toto pole slouží pouze k informačním účelům.  
10. Zadejte datum do pole **Zkontrolovat termín**.
11. Klikněte na tlačítko **Uložit**.

## <a name="set-up-the-compensation-plans-and-actions-for-a-compensation-process"></a>Nastavení plánů kompenzace a akcí pro proces kompenzace
1. Klikněte na možnost **Nastavení**.
    * Stránku **Nastavení** lze použít k výběru, které plány mají být zpracovány jako součást tohoto procesu kompenzace a které akce se mají provést pro každý plán.  
2. V poli **Plán** zadejte nebo vyberte hodnotu.
3. Klikněte na tlačítko **Uložit**.
4. Klikněte na tlačítko **Přidat**.
5. V poli **Akce** vyberte typ **jmění** akce.
6. Klikněte na tlačítko **Přidat**.
7. V poli **Akce** vyberte typ **významu** akce.
    * Akce kompenzace může být „svázána“ dohromady pomocí pole **Použít předchozí výsledek** k označení, zda vybraná akce má použít základní mzdy zaměstnanců nebo výsledek předchozí akce jako výchozí bod pro výpočet této akce.  
8. Vyberte možnost **Ano** v poli **Použít předchozí výsledek**.
9. Klikněte na tlačítko **Přidat**.
10. V poli **Akce** vyberte pro akci typ **Obecné**.
    * Různé typy akcí kompenzací umožňují povolit různá pole. Pro hlavní typ akce kompenzace lze zadat procento zvýšení nebo částku zvýšení.  
11. Vyberte možnost **Vybrat částku zvýšení**.
12. Zadejte číslo do pole **částka zvýšení**.
13. Klikněte na tlačítko **Přidat**.
14. V poli **Akce** vyberte typ akce **povýšení**.
    * Typy akcí Povýšení a Změna jiné úrovně umožňují uživatelům provádět ruční úpravy kompenzace zaměstnanců. U těchto typů akcí je možné aktivovat doporučení i další typy akcí, abyste mohli pro zaměstnance zadávat nové doporučené hodnoty kompenzace.  
15. Klikněte na tlačítko **Přidat**.
16. Vyberte volbu v poli **Typ**.
    * Plány fixní i variabilní kompenzace můžete spustit ve stejném procesu kompenzace.  
17. V poli **Plán** zadejte nebo vyberte hodnotu.
    * Zaškrtnutím políčka **Povolit mzdy za výkonnost** můžete určit, zda musí být částky variabilní a fixní kompenzace upraveny podle hodnocení výkonnosti zaměstnance.  
    * Účinek může být přepsán podle plánu variabilních kompenzací.  
18. Klikněte na tlačítko **Uložit**.
19. Klikněte na tlačítko **Přidat**.
20. Zavřete stránku.

## <a name="run-the-compensation-process"></a>Spustit proces kompenzace
1. Klikněte na **Spustit proces**.
    * Ovládací prvek **Zobrazit výsledky zpracování** slouží ke zobrazení zpráv zpracování kompletního procesu kompenzace po dokončení zpracování.  
2. V poli **Zobrazit výsledky zpracování** vyberte hodnotu **Ano**.
3. Klikněte na tlačítko **OK**.

## <a name="view-the-results"></a>Zobrazit výsledky
1. Klikněte na **výsledky zpracování**.
2. Klikněte na **Výsledky zaměstnance**.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
4. Rozbalte část **Fixní kompenzace**.
    * Chcete-li zobrazit výsledky v procesu, rozbalte pevné záložky. Pokud byla označena možnost **Povolení doporučení** pro akci kompenzace, budou pro tuto akci povolena pole **Doporučení**.  
5. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Výsledky lze pro jednoho zaměstnance zobrazit kliknutím na tlačítko **Zobrazit výsledky**.  
    * Můžete přepsat vypočtenou částku kompenzace nastavením procenta nebo zvýšením částky v polích **Doporučení**.  
6. Zadejte číslo do pole pro **doporučená procenta**.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
8. Zadejte číslo do pole pro **doporučená procenta**.
    * Přepočet lze použít k ignorování změn provedených v existujících záznamech a k vygenerování nového výsledku kompenzace pro vybraného zaměstnance.  
    * Po dokončení všech změn zaměstnance změňte stav na **Schváleno**.  
9. Klikněte na položku **Změnit stav**.
10. Klikněte na **Schváleno**.
    * Po schválení záznamu může být načten do záznamu oficiální kompenzace zaměstnance. Nová kompenzace bude platná k datu transakce, které je nastaveno v procesu kompenzace.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
