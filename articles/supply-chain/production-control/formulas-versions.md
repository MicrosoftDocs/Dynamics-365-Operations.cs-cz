---
title: Receptury a verze receptury
description: Toto téma obsahuje informace o recepturách a verzích receptur. Receptura definuje materiály, suroviny a výsledky konkrétního procesu v procesu výroby. Receptury se používají k plánování a výrobě produktů ve výrobním procesu.
author: cvocph
ms.date: 09/12/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PlanActivity, ReqSupplyDemandSchedule, EcoResProductProdTypeFormulaNoActiveFormulaFormPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e8a168da2309709baaf9f8006880d738f754751d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809103"
---
# <a name="formulas-and-formula-versions"></a>Receptury a verze receptury

[!include [banner](../includes/banner.md)]

Receptura definuje materiály, suroviny a výsledky konkrétního procesu v procesu výroby. Spolu s odpovídajícími postupy receptura definuje celý proces ve výrobním procesu. Receptury se používají k plánování a výrobě produktů ve výrobním procesu.

Receptura se skládá ze surovin a množství, které jsou zapotřebí k vyrobení specifického množství položek receptury. V závislosti na prováděném úkolu můžete získat přístup k funkci receptury z modulů Řízení zásob a skladu nebo Řízení informací o produktech.

## <a name="formulas-and-formula-lines"></a>Receptury a řádky receptury 
Receptura je tvořena jedním nebo více řádky receptury, které identifikují suroviny nebo položky, z nichž se daná receptura skládá. Řádek receptury může obsahovat položky kusovníku, položky receptury, položky se skutečnou hmotností, zakoupené položky nebo vedlejší produkty. Vzhledem k tomu, že mnohé položky jsou používány ve více produktech, lze jednu položku použít ve více recepturách.

Příkladem receptury je recept na čokoládové sušenky. Suroviny pro danou recepturu používají více řádků, jako je například mouka, cukr, vejce, máslo a čokoláda. Receptura na čokoládové sušenky obsahuje suroviny, které se s největší pravděpodobností nachází i v jiných recepturách. Když připravujete čokoládové sušenky, můžou vám zůstat zbytky, jako například drobky, nebo některé sušenky mohou být nedopečené, či naopak připálené. Tyto položky lze nastavit jako vedlejší produkty, v závislosti na výrobních operacích.

Při vytvoření řádku receptury použijete typ řádku pro označení způsobu, jak má systém zpracovat řádek při spuštění hlavního plánování a vytvoření dávkových objednávek. Každý typ řádku povede k jiným výsledkům. Následující tabulka popisuje typy řádků, které můžete zvolit. 

| Typ řádku     | popis  |
|---------------|--------------|
| Zboží          | Pokud se jedná o položku suroviny nebo polotovaru vyzvednutou ze skladu nebo pokud je daná položka službou, vyberte volbu **Položka**. |
| Fiktivní       | Vyberte **Fiktivní**, pokud chcete rozpadnout libovolné položky receptury na nižší úrovni, které jsou obsaženy na řádcích receptury. Při odhadu dávkové objednávky a rozpadu položek receptury budou položky komponent uvedeny jako řádky receptury na dávkové objednávce. Kromě toho budou přidány odpovídající postupy do výrobního postupu. Položky receptury se rozbalí pomocí aktuální konfigurace. Pokud používáte typ řádku **Fiktivní**, můžete pracovat s konfiguracemi měření a výroby, které se nacházejí na různých úrovních receptury. Vyberete-li **Fiktivní** pro produkt na pevné záložce **Analýza** stránky **Podrobnosti o uvolněném produktu** a potom použijete tento produkt v receptuře, typ řádku receptury se změní na **Fiktivní**. Nelze vybrat **Fiktivní** pro položku se skutečnou hmotností nebo pro položky, které mají typ výroby **Souběžný produkt**, **Vedlejší produkt** nebo **Položka plánování**. |
| Doložená dodávka | Vyberte **Doložená dodávka** pro vytvoření dávkové objednávky, výrobní zakázky, kanbanu, převodního příkazu nebo nákupní objednávky pro surovinu obsaženou na řádku receptury. Související objednávka je určena na základě výchozího nastavení objednávky a výrobního typu suroviny a bude vytvořena při odhadu dávkové objednávky. Pro dávkovou objednávku jsou rezervována povinná množství suroviny. |
| Dodavatel        | Pokud je v rámci výrobního procesu použit subdodavatel a pokud chcete pro tohoto subdodavatele vytvořit dílčí výrobu nebo prodejní objednávku, vyberte volbu **Odběratel**. Služba nebo práce vykonaná tímto subdodavatelem musí být vytvořena pomocí položky receptury nebo položky služby. Lze ji připojit položku k nadřazené položce jako řádek receptury. Postup musí obsahovat operaci, která je přiřazena k provoznímu prostředku subdodavatele. Tato operace je připojena k řádku receptury pomocí pole **Číslo operace**. . |

## <a name="formula-versions"></a>Verze receptury
Pokud vytvoříte novou recepturu, musíte nejdříve vytvořit verzi receptury, než přidáte položky řádků receptury a jejich specifické vlastnosti. Každá receptura musí mít alespoň jednu verzi. Tlačítko **Schváleno** u verze receptury bude k dispozici až po úspěšném uložení záznamu verze. Každý záznam verze receptury je přidružen k jednomu nebo více souběžným a vedlejším produktům, které lze vyrobit při výrobě hotového výrobku. Mnoho výrobků lze vyrobit ze stejných surovin v různých velikostech dávky, v násobcích nebo pomocí různých výnosů. Můžete vytvářet tolik verzí receptury, kolik potřebujete.

Ke správě více aktivních verzí receptury použijte rozsahy dat platnosti nebo pole množství „od“. Více aktivních verzí receptury může existovat pouze v případě, když se rozsah dat a množství "od" nepřekrývají.

Na rozdíl od kusovníků, kde je jeden kusovník často přidružen k více verzím kusovníku, pro každou recepturu obvykle existuje pouze jedna verze receptury. Mějte na paměti, že pouze jednu verzi receptury lze aktivovat pro dimenze disponibility a množství pro daný produkt. Více verzí receptury však může existovat z jiných důvodů a je možné je vybrat ručně při vytváření dávkové objednávky.

## <a name="approve-and-activate-formulas-and-formula-versions"></a>Schválení a aktivování receptur a verzí receptur
Receptury a verze receptury musí být schváleny předtím, než mohou být použity pro plánování a výrobu. Receptury jsou obvykle aktivovány ještě před svým použitím. Při výrobě ale můžete vybrat verzi procedury, která je schválena, ale není ještě aktivována.

Chcete-li zabezpečit recepturu nebo verzi receptury, můžete nastavit parametry **Blokovat úpravy** a **Blokovat odebrání schválení** na stránce **Parametry modulu Řízení výroby**.

Vyberete-li **Blokovat úpravy** a receptura je schválená, nelze upravit nebo odstranit žádná pole na řádcích receptury. Pokud však odeberete schválení receptury, můžete odstranit a upravit řádky receptury. Můžete také vytvořit nové receptury a nové verze receptury.

Vyberete-li **Blokovat odebrání schválení**, nelze odebrat schválení schválené receptury nebo verze receptury. Můžete však vytvořit nové receptury a nové verze receptury a odebrat aktivaci verze receptury.

Můžete přidat více úrovní kontroly pomocí funkce elektronického podpisu. Pokud je uživatel nastaven tak, aby byl při schválení receptur požadován elektronický podpis, zobrazí se při aktivaci receptury stránka **Podpis**. Uživatel musí být autorizován pro elektronický podpis a certifikát musí být úspěšně ověřen před potvrzením změny. Pokud nemůže být podpis ověřen, schválení nebo odstranění schválení je odepřeno a změna, která zahájila schvalování nebo odebrání schválení je vrácena do svého původního stavu.

## <a name="use-the-scalable-feature"></a>Použití poměrné funkce
Poměrná funkce je k dispozici pouze tehdy, když jsou všechny komponenty položky v receptuře nastaveny na možnost **Variabilní spotřeba**. Tato funkce není dostupná, pokud jsou komponenty položky nastaveny na **Pevná spotřeba** nebo **Spotřeba kroku**. Při použití poměrné funkce se upraví množství jiných zvolených surovin, pokud změníte surovinu v receptuře. Velikost receptury je také upravena. Podobně pokud změníte velikost receptury, změní se množství všech poměrných surovin. Tato funkce slouží konkrétně pro vytvoření receptury a její údržbu. Neurčuje, zda se bude množství suroviny poměrně zvyšovat nebo snižovat na dávkové objednávce.

## <a name="use-step-consumption"></a>Použití spotřeby kroku
Spotřeba kroku eliminuje požadavek, kdy je nutné zadat množství suroviny na kartě **Řádek receptury**. Namísto toho je spotřeba kroku nakonfigurována tak, aby měla hodnoty **Od řady** a **Množství**. Je zvolena informace ze spotřeby kroku na záznam řady, který splňuje množství na dávkové objednávce. Spotřeba kroku je užitečná, když není poměr spotřeby lineární s ohledem na velikost dávkové objednávky a pouze navyšuje požadavek při dosažení určité prahové hodnoty množství. Chcete-li povolit tuto funkci pro novou recepturu, ve skupině **Výpočet spotřeby** změňte nastavení receptury pro použitelnou surovinu ze **Standardní** na **Krok**. Tuto metodu spotřeby určíte na kartě **nastavení** stránky **Řádek receptury**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]