---
title: Přehled převodu standardních nákladů
description: V tomto článku je popsán přehled usnadňující nastavení a spuštění převodu standardních nákladů. Uvedené kroky jsou určeny k dokončení po dokončení předběžných kroků nutných pro převod standardních nákladů.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "78212"
- intro-internal
ms.assetid: d601d9d5-1de3-4868-aff4-534dca01d624
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85f2c623255b8fec17acfcf7da7adbb105e921c7
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/03/2021
ms.locfileid: "6336528"
---
# <a name="standard-cost-conversion-overview"></a>Přehled převodu standardních nákladů

[!include [banner](../includes/banner.md)]

V tomto článku je popsán přehled usnadňující nastavení a spuštění převodu standardních nákladů. Uvedené kroky jsou určeny k dokončení po dokončení předběžných kroků nutných pro převod standardních nákladů. 

Použitím stránky **Převody standardních nákladů** můžete převést skladový model pro dávku vybraných položek z aktuálního nákladového přístupu na standardní nákladový přístup. Postup převodu zahrnuje předběžnou uzávěrku skladu, provedení několika kroků při vlastním převodu (interval definovaný počátečním datem a datem plánovaného převodu), provedení vlastního převodu a přidružení uzávěrky skladu.

-   Uzávěrka skladu před obdobím převodu – uzávěrka skladu představuje přípravný krok, protože vyrovnává otevřené transakce položky pomocí původní metody ocenění. Během období převodu můžete zadat a účtovat zpětně datované transakce, jako jsou například faktury, a můžete tak uzavřít předchozí období. Datum uzávěrky skladu musí být jeden den před počátečním datem převodu, aby bylo možné zajistit čisté přestávky z původní metody ocenění.
-   Kroky převodu během období převodu – pomocí stránky **Převody standardních nákladů** lze vytvořit záznam převodu, který také obsahuje uživatelem definovaný identifikátor pro novou nákladovou verzi. Označte položky, které mají být převedeny, a zadejte nevyřízené standardní náklady položky v rámci nové nákladové verze. Provedením kontroly vybraných položek identifikujte případné problémy, které by mohly zabránit v převodu, a zjištěné potíže před provedením další kontroly odstraňte. Poté, co položky prošly úspěšně kontrolami, upravte stav převodu na hodnotu **Připraveno**. K plánovanému datu převodu proveďte převod a volitelně zahrňte uzávěrku skladu. Pohyby skladových položek během přechodného období budou zaúčtovány a oceněny podle původního skladového modelu. Poté po úspěšném dokončení převodu budou skladové pohyby přehodnoceny na standardní náklady.
-   Uzávěrka skladu před převodem. Uzávěrku skladu lze zahrnout do převodního postupu k plánovanému datu převodu, případně ji lze provést jako samostatný krok před převodem.

Po úspěšném dokončení převodu bude mít každá položka standardní nákladový model skladu a standardní náklady položek budou povoleny. Následné skladové transakce budou oceněny podle standardních nákladů položky. Kromě toho systém převede fyzické skladové transakce na příjmy a uvede standardní náklady podle data převodu. Systém také převede finanční údaje skladovaných položek na standardní náklady a zaúčtuje rozdíl v hodnotě podle přecenění skladu. Všechny transakce po převodu jsou oceňovány podle standardních nákladů položek. Nelze přistupovat ke starším transakcím před datem převodu, protože den před datem převodu musí být provedena povinná uzávěrka skladu. Převod lze provést pouze tehdy, když den před převodem byla provedena uzávěrka skladu. Uzávěrku skladu nelze zrušit.

## <a name="1-define-a-standard-cost-conversion-record-and-the-associated-costing-version"></a>1. Definujte převod standardních nákladů a přidruženou nákladovou verzi.
Pomocí stránky **Převody standardních nákladů** vytvořte záznam převodu. Nový záznam převodu lze vytvořit pouze po dokončení stávajících záznamů převodu. Trvání plánovaného období převodu je definováno podle počátečního data převodu a plánovaného data převodu. Plánované období převodu může trvat pouze jeden den. Plánované období převodu pomáhá zajistit, aby byl dostatek času pro dokončení všech jeho kroků v rámci procesu převodu. Jeden den před počátečním datem převodu je nutné provést uzávěrku skladu, aby bylo možné ještě před spuštěním procesu převodu zajistit vyrovnání. Aby bylo jisté, že počáteční datum převodu a datum uzávěrky skladu se řádně shoduje, můžete změnit počáteční datum převodu na jeden den po stávající uzávěrce skladu, nebo provést uzávěrku skladu. Při zadávání záznamu převodu zadáte také uživatelský identifikátor pro novou nákladovou verzi, která bude obsahovat standardní náklady pro převedené položky. Nákladová verze je generována automaticky při uložení záznamu převodu.

## <a name="2-review-and-change-the-new-costing-version-for-the-conversion-record"></a>2. Zkontrolujte a upravte novou nákladovou verzi pro záznam převodu
Nová nákladová verze je vyhrazená pro záznam převodu, tak, jak stanovuje typ převodu **Konverze**. Vyhrazená nákladová verze funguje jako nákladová verze pro standardní náklady a bude obsahovat nákladové záznamy položek přidružených k záznamu převodu. Vyhrazená nákladová verze pro záznam převodu má následující nastavení, které je vhodné podle potřeby zkontrolovat a upravit na různých kartách:

-   **Typ nákladů:** toto pole je třeba nastavit na **Standardní náklady**.
-   **Verze:** identifikátor zobrazuje údaje zadané v záznamu převodu pro ID nákladové verze.
-   **Název:** ve výchozím nastavení je název prázdný. Volitelně můžete zadat název.
-   **Blokovat:** toto pole je třeba nastavit na **Ne**. Do nákladové verze můžete zadávat nákladové záznamy, dokud nedojde ke změně záznamu převodu do stavu **Připraveno**. Stav **Připraveno** znamená, že vybrané položky byly zkontrolovány a nákladové záznamy již nelze upravovat.
-   **Blokovat aktivaci:** toto pole je třeba nastavit na **Ano**. Nevyřízený nákladový záznam ve vyhrazené nákladové verzi nelze ručně aktivovat. K aktivaci dojde při provedení převodu.
-   **Od data:** počáteční datum odpovídá plánovanému datu převodu, které jste zadali do záznamu převodu.
-   **Pracoviště:** toto pole ponechejte prázdné, aby záznamy nákladů bylo možné zadat pro libovolné pracoviště.
-   **Povolit skupinu polí typu ceny:** toto pole nastavíte na **Ano**, aby bylo možné zadat pouze záznamy nákladové ceny.
-   **Záložní princip:** toto pole nastavte na **Žádný**. Upravte záložní princip na **Aktivní**, pokud chcete, aby byly nákladové informace aktivovány v jiných nákladových verzích. Pro výpočet nákladů vyráběných položek budou vyžadovány nákladové informace o součástech, nákladových kategoriích a nepřímých nákladech.
-   **Záložní nákladová verze:** ponechejte toto pole prázdné.

Nákladové informace položky ve vyhrazené nákladové verzi lze udržovat pouze na stránce **Převody standardních nákladů**. K výpočtu nákladů pro nákladovou verzi při převodu nelze použít **Nastavení nákladové verze** ani stránku **Údržba nákladové verze**. Můžete však tyto stránky použít k údržbě vyhrazené nákladové verze po dokončení procesu převodu.

## <a name="3-identify-the-items-to-convert-to-standard-cost"></a>3. Identifikujte položky, které převádíte na standardní náklady
Použijte stránku **Převody standardních nákladů** pro identifikaci jednotlivých položek, které by měly být převedeny na standardní náklady. Můžete přidat více položek pomocí stránky **Přidat položky do převodu standardních nákladů**. Obecně byste měli zahrnout všechny vyrobené položky do jednoho záznamu převodu pro zajištění správného výpočtu nákladů.

## <a name="4-enter-or-calculate-the-pending-standard-cost-for-each-item-that-is-being-converted"></a>4. Zadejte výpočet nevyřízených standardních nákladů pro jednotlivé převáděné položky
Na stránce **Cena položky** zadejte nevyřízené standardní náklady v rámci vyhrazené nákladové verze pro nakoupené a převedené položky. Nákladové záznamy jsou specifické pro pracoviště a nevyřízené náklady položky je nutné zadat pro každé pracoviště. Pomocí stránky **Cena položky** můžete vypočítat nevyřízené standardní náklady pro vyráběné položky. Nevyřízené náklady pro vyráběné položky by se měly vypočítat pro všechna výrobní pracoviště, pokud se nejedná o převodní pracoviště. V takovém případě by se nevyřízené náklady měly zadat ručně. Některé položky mohou mít vlastnosti dimenze produktu, jako je barva, velikost nebo konfigurace. Na stránce **Převody standardních nákladů** popisuje pole **Použít nákladovou cenu podle varianty** standardní náklady pro každou kombinaci dimenzí produktu. Pokud zaškrtnutí tohoto políčka zrušíte, je zapotřebí zadat pouze nevyřízené náklady pro položku.

## <a name="5-check-and-resolve-any-issues-for-the-items-that-are-being-converted"></a>5. Zkontrolujte a odstraňte všechny potíže s převáděnými položkami
Pomocí hlášení **Kontroly převodu standardních nákladů** určete problémy pro převáděné položky. Pokud je položka bezproblémová, její stav v záznamu převodu je zobrazený jako **Zkontrolováno**. V případě, že jsou s položkou spojeny potíže, je nutné problémy vyřešit a pak sestavu znovu spustit a počkat, než se stav změní na **Zkontrolováno**. Pokud nedokážete potíže s položkami včas vyřešit, můžete volitelně položky odstranit ze záznamu převodu a převést je v budoucnosti.

## <a name="6-change-the-status-of-the-conversion-record-to-ready"></a>6. Změňte stav záznamu převodu na Připraveno.
Změnou stavu záznamu převodu na **Připraveno** provedete výslednou kontrolu před spuštěním standardního převodu nákladů. Stav se změní na **Připraveno** pouze v případě, že jsou splněny následující podmínky:

-   Každá položka v záznamu převodu má stav **Zkontrolováno**.
-   Jeden den před počátečním datem převodu je provedena uzávěrka skladu. Aby bylo jisté, že počáteční datum převodu a datum uzávěrky skladu se řádně shoduje, můžete změnit počáteční datum převodu na jeden den po stávající uzávěrce skladu, nebo provést uzávěrku skladu.

## <a name="7-back-up-the-database-before-conversion"></a>7. Vytvořte zálohu databáze před převodem
Záloha umožňuje obnovit databázi v případě, že během převodu dojde k chybám.

## <a name="8-perform-the-conversion-when-the-conversion-record-has-a-ready-status"></a>8. Převod proveďte, když má záznam převodu stav Připraveno.
Proces převodu vyžaduje, aby den před plánovaným datem převodu byla provedena uzávěrka skladu. Tento požadavek zaručuje, že do intervalu převodu nebudou zahrnuty transakce datované do minulosti. Pokud uzávěrka skladu nebyla dosud provedena, zobrazí se dotaz, zda chcete uzávěrku provést v rámci procesu převodu. Proces převodu zpracovává vždy jednu položku současně. Začíná u nejnižší položky ve struktuře produktů na základě kódu položky nejnižší úrovně. Když bude položka úspěšně převedena, její stav v záznamu převodu se změní na **Převedeno**. Jestliže dojde k převedení procesu převodu, položky s neúspěšným převodem budou mít stav **Zkontrolováno**. Úspěšné dokončení procesu převodu má následující důsledky:

-   Stav záznamu převodu se změní ze stavu **Připraveno** do stavu **Dokončeno** a stav jednotlivých vybraných položek se změní z hodnoty **Zkontrolováno** do stavu **Převedeno**.
-   Skupina modelů položky pro převedené položky byla upravena, takže odpovídá nové skupině se skladovým modelem standardních nákladů.
-   Standardní náklady pro převedené položky byly povoleny s vyhrazenou nákladovou verzí.
-   Typ nákladové verze se změní ze stavu **Převod** na **Standardní náklady** a nákladová verze nyní funguje jako jakákoli jiná verze standardních nákladů.

## <a name="9-validate-and-reconcile-the-inventory-values-for-the-converted-items"></a>9. Ověřte a odsouhlaste skladové hodnoty pro převedené položky
Hlášení **Výkaz analýzy odchylek** umožňuje analyzovat odchylky přecenění a hlášení **Hodnota zásob** umožňuje zobrazit hodnoty zásob k určitému datu.

-   Analyzujte odchylky přecenění. Otevřete sestavu **Výkaz analýzy odchylek**, ve které zobrazíte odchylky přecenění skladu pro převedené položky. Můžete také použít stránku **Transakce standardních nákladů**, na které si můžete prohlédnout transakce přecenění skladu pro převedené položky ve skladu.
-   Analyzujte hodnotu skladu před počátečním datem převodu. Otevřete sestavu **Hodnota zásob**, ve které zobrazíte skladové hodnoty pro převedené položky. Jako datum „Do data“ pro sestavu použijte datum o jeden den před datem zahájení převodu.
-   Analyzujte hodnotu skladu před datem převodu. Otevřete sestavu **Hodnota zásob**, ve které zobrazíte skladové hodnoty pro převedené položky. Jako datum „Do data“ pro sestavu použijte datum odpovídající jednomu dni před datem zahájení převodu.
-   Analyzujte skladovou hodnotu v datu převodu. V sestavě **Skladová hodnota** je uvedena skladová hodnota k datu převodu. Hodnoty Od data i Do data v sestavě by měly odpovídat datu převodu. Kritéria výběru sestavy by měla odpovídat převedeným položkám.
-   Analyzujte zpětně datované skladové pohyby. Otevřete sestavu **Skladová hodnota**, ve které jsou zobrazeny zpětně datované skladové pohyby zadané po převodu. Hodnoty Od data i Do data v sestavě by měly odpovídat počátečnímu datu převodu a datu převodu (bez jednoho dne). Kritéria výběru sestavy by měla odpovídat převedeným položkám. V sestavě jsou zobrazeny pohyby skladu provedené za standardní náklady před obdobím převodu.


## <a name="additional-resources"></a>Další zdroje

[Předpoklady pro převod standardních nákladů](prerequisites-standard-cost-conversion.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]