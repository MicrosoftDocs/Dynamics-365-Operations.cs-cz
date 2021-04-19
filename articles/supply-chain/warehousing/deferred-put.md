---
title: Odložené zpracování práce skladu
description: Toto téma popisuje funkci, která umožňuje odložené zpracování operací vložení práce v aplikaci Dynamics 365 Supply Chain Management.
author: josaw1
ms.date: 11/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-6-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3dad97e13624449d287ded74e7e25f94eb0dbde3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838315"
---
# <a name="deferred-processing-of-warehouse-work"></a>Odložené zpracování práce skladu

[!include [banner](../includes/banner.md)]

Toto téma popisuje funkci, která umožňuje odložené zpracování operací vložení práce u skladové práce dostupné v aplikaci Dynamics 365 Supply Chain Management.

Funkce odloženého zpracování umožňují pracovníkům skladu pokračovat v práci i v době, kdy na pozadí běží operace vložení. Odložené zpracování je užitečné, pokud je nutné zpracovat mnoho řádků práce a pracovník může nechat zpracování běžet asynchronně. Je také užitečná v případě, kdy server může mít v době zpracování ad hoc nebo neplánovaný nárůst doby zpracování a ta může ovlivnit produktivitu uživatele.

Zpracování na pozadí je dosaženo pomocí systému SysOperation. Další informace získáte v části [Přehled systému SysOperation](https://docs.microsoft.com/dynamicsax-2012/developer/sysoperation-framework-overview).

## <a name="configuring-the-work-processing-policies"></a>Konfigurace zásad zpracování pracovních postupů

Chcete-li použít odložené zpracování, je nutné nakonfigurovat a použít zásady zpracování pracovních postupů.

Zásady jsou konfigurovány na stránce **Zásady zpracování pracovních postupů**. Následující tabulka popisuje pole na této stránce.

| Pole                           | Popis |
|---------------------------------|-------------|
| Název zásady zpracování práce     | Název zásad zpracování pracovního postupu. |
| Typ pořadí pracovních činností                 | Typ pracovního příkazu, u kterého jsou zásady použity. |
| Operace                       | Operace, která je zpracována pomocí zásad. |
| Metoda zpracování práce          | Metoda používaná pro zpracování řádku práce. Pokud je metoda nastavena na **Okamžitě**, chování se podobá chování, když pro zpracování řádku nejsou použity žádné zásady zpracování práce. Je-li metoda nastavena na **odloženo**, použije se odložené zpracování využívající dávkový systém. |
| Prahová hodnota odloženého zpracování   | Hodnota **0** (nula) označuje, že neexistuje žádná prahová hodnota. V tomto případě se použije odložené zpracování, pokud jej lze použít. Pokud je výpočet specifické prahové hodnoty nižší než práh, použije se metoda Immediate. V opačném případě se použije metoda odloženo, pokud ji lze použít. V případě práce související s prodejem a převodem je prahová hodnota vypočtena jako počet přidružených řádků zatížení zdroje, které jsou pro práci zpracovávány. Pro práci doplnění se práh vypočítá jako počet řádků práce, které jsou doplněny prací. Nastavením prahové hodnoty, například **5** pro prodej, nebudou menší práce, které mají méně než pět počátečních zdrojových řádků vytížení, používat odložené zpracování, ale větší práce jej budou používat. Prahová hodnota se uplatní pouze v případě, že je metoda zpracování práce nastavena na hodnotu **Odloženo**. |
| Skupina dávky odloženého zpracování |Skupina dávky používaná pro úlohy zpracování vlny. |

Pro odložené úlohy zpracování jsou podporovány následující typy pracovních příkazů: prodejní objednávka, výdej převodního příkazu a doplnění.

## <a name="assigning-the-work-creation-policy"></a>Přiřazení zásad vytváření pracovních míst

Zásady vytváření pracovních míst lze přiřadit k parametrům řízení skladu. Lze je také přiřadit na úrovni jednotlivých skladů. Pokud jsou tyto zásady přiřazena ke skladu, budou použity pouze na práci vytvořenou pro daný sklad. Pokud na úrovni skladu nejsou přiřazeny žádné zásady, použijí se zásady z parametrů správce skladu.

## <a name="viewing-the-deferred-put-processing-tasks"></a>Zobrazení odložených úloh zpracování operací

Pozastavené úkoly vložení lze zobrazit na stránce **Odložené úlohy zpracování**.

Ve výchozím nastavení jsou zobrazeny **dokončené** úkoly.

| Pole            | Popis |
|------------------|-------------|
| Stav           | Stav úlohy. |
| Stav dávkové úlohy | Stav vybrané související dávkové úlohy. Pokud byla dávková úloha zpracována, historie dávky obsahuje protokol a informace z dávkové úlohy. |

Následuje vysvětlení možných stavů:

- **Čekání** – související dávková úloha čeká na zpracování na dávkovém serveru.
- **Neúspěšné** – zpracování se nezdařilo. Úlohu lze znovu zpracovat pomocí akce **zpracovat odložené vložení** nebo ji lze zrušit pomocí akce **zrušit odložené vložení**.
- **Dokončeno** – úloha byla dokončena.

## <a name="impact-on-closed-work-dates"></a>Dopad na data uzavřené práce

Je-li použito odložené zpracování, je datum uzavření pracovní doby nastaveno jako datum a čas vytvoření odložených úloh zpracování. Je použito uzavřené pracovní datum, protože se jedná o nejlepší odhad pro dobu dokončení operace vložení.

## <a name="reprocessing-a-failed-task"></a>Přepracování neúspěšné úlohy

Neúspěšnou úlohu můžete znovu zpracovat tak, že ji vyberete na stránce a pak vyberete možnost **Zpracovat odložené vložení**. Přepracování odpovídá situaci, kdy uživatel dokončí vložení z mobilního zařízení, jako by byl nastaven pro okamžité zpracování.

## <a name="canceling-failed-tasks"></a>Zrušení neúspěšných úloh

Zrušit lze pouze neúspěšné úlohy. Pokud úkol zrušíte, můžete jej přiřadit novému uživateli. Případně může úkol zůstat přiřazen uživateli, který práci zpracoval. Zrušení odpovídá situaci, kdy je práce přenesena zpět do mobilního zařízení, jako kdyby byl právě dokončen poslední krok vyskladnění a práce musela být odložena. Uživatel však bude moci určit, zda je práce "odlišná", protože bude mít pouze krok odložení a zda skladové místo bude odpovídat lokaci, kterou měl první uživatel, který zpracoval tuto práci, jako konečnou lokaci vložení.

Je-li úkol zrušen, není již práce blokována tímto důvodem pro odložené zpracování vložení. Může být přepracovávána pomocí mobilního zařízení.

Záznam úkolu je odstraněn, jakmile je úkol zrušen.

## <a name="configuring-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Konfigurace nabídky mobilního zařízení pro přeskočení zásady odloženého zpracování

Položku nabídky mobilního zařízení můžete nakonfigurovat tak, aby se nepoužila zásada odloženého zpracování. Práce je pak zpracována tak, jak je, když nejsou použity žádné zásady odloženého zpracování. Tato funkce umožňuje nadřízenému použít určitou položku nabídky, ve které není použito odložené vložení. Chcete-li jej nakonfigurovat, nastavte pole **zásady odloženého zpracování** na **Přepsat nastavení a proces vložit synchronně**. 

## <a name="restrictions-when-the-deferred-put-processing-isnt-applied"></a>Omezení při nepoužití odloženého zpracování

Existuje několik scénářů, kdy odložené zpracování není použito, i když je tato zásada nakonfigurována. Několik příkladů:

- Použije se ruční doplňování práce.
- Práce je dokončena pomocí automatického dokončování.
- Používají se šablony auditu.


## <a name="monitoring-the-deferred-processing-tasks-from-the-outbound-work-monitoring-workspace"></a>Sledování úkolů odloženého zpracování z pracovního prostoru Sledování odchozích prací

Pracovní prostor **sledování odchozích prací** obsahuje dvě dlaždice, které usnadňují sledování odložených úloh zpracování.

- **Neúspěšné úlohy odloženého zpracování** – tato dlaždice zobrazuje počet neúspěšných úkolů. Pokud existují neúspěšné úlohy, správce skladu je musí buď znovu zpracovat, nebo zrušit, protože nebude automaticky zpracován.
- **Čekání na odložené úlohy vložení** – tato dlaždice zobrazuje počet úkolů, které byly ve stavu **čekání** déle než 10 minut. Pokud se na dlaždici zobrazí číslo, může to znamenat, že během dávkového zpracování došlo k problému. **Čekající** úkoly můžete ručně zpracovat. Pokud je dávková úloha pro úkol zpracována později, bude pouze neúspěšná, protože již byla zpracována. Žádný dopad nebude.

## <a name="deleting-completed-tasks"></a>Odstranění dokončených úkolů

Odložené úlohy zpracování vložení můžete odstranit tak, že je vyberete a odstraníte na stránce.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]