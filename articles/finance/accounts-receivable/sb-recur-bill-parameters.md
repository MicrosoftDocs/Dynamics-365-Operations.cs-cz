---
title: Parametry opakované fakturace smlouvy
description: Tento článek vysvětluje, jak nastavit výchozí hodnoty pro plány fakturace, které jsou vytvořeny v rámci opakované fakturace smlouvy. Vysvětluje také, jak vytvořit skupiny plánů fakturace.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: cb60253f3cbb8c991ef2e106abdb1c685bf22171
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903327"
---
# <a name="recurring-contract-billing-parameters"></a>Parametry opakované fakturace smlouvy

Na stránce **Parametry opakované fakturace smlouvy** nastavíte výchozí hodnoty pro plány fakturace, které jsou vytvořeny v rámci opakované fakturace smlouvy. Všechny plány fakturace, které vytvoříte, budou zpočátku používat tyto výchozí hodnoty. Hodnoty v tomto poli však můžete podle potřeby změnit pro každý plán fakturace.

## <a name="general-tab"></a>Karta Obecné

1. Na stránce **Parametry opakované fakturace smlouvy** na kartě **Obecné** v poli **Skupina plánů fakturace** vyberte skupinu plánů fakturace. Informace, jak nastavit skupiny plánů fakturace najdete v části [Skupiny plánů fakturace](#set-up-billing-schedule-groups) dále v tomto článku.
2. V poli **Typ ukončení** vyberte způsob výpočtu konečné faktury po ukončení plánu fakturace:

    - **Upravit plán** – Přerušte plán fakturace k datu ukončení, změňte stav plánu na **Poslední fakturace** a upravte přidružený plán odkladu zrušením částky, kterou už dále není třeba uznat. Pokud datum zahájení fakturace spadá až za datum ukončení, zbývající fakturační období se odstraní.
    - **Fakturovat zbývající** – Přidejte zbývající částky v plánu fakturace do období ukončení, změňte stav plánu na **Poslední fakturace** a aktualizujte plán odkladu. Pokud datum zahájení fakturace spadá až za datum ukončení, celková částka všech zbývajících fakturačních období se přičte k fakturačnímu období a zbývající fakturační období se odstraní.
    - **Žádná úprava** – Ukončete plán fakturace k datu ukončení. V plánu fakturace se neprovedou žádné úpravy.

3. V poli **Jedinečný typ plánu** volbou **Žádný** zadejte, že zákazníci jsou omezeni na jeden plán fakturace. Volbou **Na zákazníka** nebo **Na koncového uživatele** zadejte, že zákazníci jsou omezeni na jedinečný plán.
4. Nastavením možnosti **Vyrovnat podle měsíce** na **Ano** vyrovnáte řádky podrobností plánu fakturace s koncem měsíce, kdy je plán fakturace vytvořen nebo aktualizován. Nastavením této možnosti na **Ne** použijete přírůstková data.
5. Nastavením možnosti **Období částečného poměrného rozdělení** na **Ano** přidělíte částky fakturace na základě počtu dní v období. Nastavením této možnosti na **Ne** budete mít stejnou částku v každém fakturačním období bez ohledu na počet dní.
6. Pokud nastavíte možnost **Období částečného poměrného rozdělení** na **Ano**, pole **Způsob poměrného rozdělení** nastavte na **Denně**, čímž rozdělíte částky podle počtu dní v období. Pokud ji nastavíte na **Měsíční**, každý měsíc budete mít stejnou částku.
7. Zadejte, zda jsou nově vytvořené plány fakturace ve výchozím nastavení blokováno.

    > [!NOTE]
    > Chcete-li odebrat blokování plánu fakturace, musí být uživatel součástí skupiny uživatelů. Vyberte **Odebrat přepsání blokované skupiny uživatelů** k vytvoření skupiny uživatelů, kde je povolena možnost **Povolit odstranění blokace**.

8. V poli **Typ transakce faktury** vyberte výchozí typ transakce faktury pro nové plány fakturace.
9. Nastavením možnosti **Vyrovnat odklad s fakturací** na **Ano** vyrovnáte odpovídající plán odkladu tak, aby používal stejná data jako plán fakturace. Nastavením této možnosti na **Ne** budete mít různá data.
10. Pokud používáte funkci rozdělení výnosů, možnost nastavte **Automaticky vytvořit rozdělení výnosů** nastavte na **Ano**, když jsou položky přidány do plánu fakturace. Pokud je položka nastavena jako položka rozdělení výnosů, automaticky je zaškrtnuto políčko **Rozdělení výnosů** na řádku plánu fakturování. Nastavte tuto možnost na **Ne**, pokud chcete ručně zaškrtnout políčko **Rozdělení výnosů**.
11. Nastavte pole pro vytvoření prodejní objednávky:

    - Faktury lze konsolidovat podle období, zákazníka nebo položky. Jakákoli kombinace hodnot **Ano** a **Ne** lze nastavit. Faktury lze také rozdělit podle skupin položek.
    - Pro faktury jsou k dispozici následující možnosti zaúčtování:

        - **Vytvořit prodejní objednávku** – Vytvoření pouze prodejní objednávky.
        - **Zobrazit zaúčtování faktur** – Fakturace prodejní objednávky a otevření stránku, kde můžete fakturu ručně zaúčtovat.
        - **Vytvořit volnou fakturu** – Tuto možnost vyberte, pokud používáte faktury s volným textem.
        - **Zaúčtovat fakturu automaticky** – Fakturace prodejní objednávky a její automatické zaúčtování.

    - Možnost **Přidat data fakturace do popisu položky** nastavte na **Ano**, chcete-li přidat popis, který obsahuje počáteční a koncové datum fakturace.
    - Možnost **Vyloučit nulovou spotřebu** nastavte na **Ano**, chcete-li vyloučit řádky plánu fakturace, které nemají žádnou spotřebu. Nastavte ji na **Ne**, chcete-li zahrnout tyto řádky do prodejní objednávky.
    - Možnost **Netisknout podřízené položky** nastavte na **Ano**, pokud nechcete tisknout podřízené položky rozdělení výnosů na prodejní zakázce. Na faktuře se zobrazí pouze nadřazená položka. Pokud je čistá částka (skrytých) podřízených položek nenulový součet, čistá částka nadřazeného řádku zobrazuje souhrn podřízených řádků. Nastavte tuto možnost na **Ne**, pokud chcete vytisknout všechny podřízené položky pod nadřazenou položkou na prodejní faktuře.

12. Nastavte pole pro podporu a obnovení:

    - Možnost **Automaticky povolit podporu a obnovení** nastavte na **Ano**, chcete-li automaticky použít funkce podpory a obnovení na prodejní objednávku.
    - V poli **Úroveň podpory a obnovy** vyberte výchozí úroveň podpory a obnovení.
    - V poli **Množství podpory a obnovy** zadejte výchozí množství podpory a obnovení.
    - V poli **Výchozí počáteční datum podpory a obnovení** zadejte datum, které se má použít jako výchozí počáteční datum podpory a obnovení:

        - **Datum transakce** – Použije se datum transakce jako počáteční datum.
        - **Začátek aktuálního měsíce** – Jako počáteční datum použijte první z aktuálního měsíce.
        - **Začátek následujícího měsíce** – Jako počáteční datum použijte první z následujícího měsíce. Pokud je datum transakce první, použije se první aktuálního měsíce.
        - **Pravidlo 15** – Pokud je datum transakce mezi prvním a patnáctým, jako počáteční datum použijte první z aktuálního měsíce. Pokud je datum transakce česnáctého nebo pozdější, je počátečním datem první den následujícího měsíce.

    - Nastavte možnost **Zahrnout slevu do výpočtu** na **Ano**, chcete-li zahrnout částku slevy do částky podpory nebo obnovení. Nastavte ji na **Ne**, chcete-li vyloučit částku slevy.
    - V polích **Frekvence podpory** a **Frekvence obnovení** vyberte frekvenci, která se má použít, když jsou položky podpory a obnovení přidány do plánu fakturace: **Denně**, **Měsíčně**, **Čtvrtletně**, **Pololetně** nebo **Každoročně**.
    - Nastavte možnost **Vyrovnat podle skupiny položek** na **Ano**, chcete-li vyrovnat počáteční a koncová data nových položek se stávajícími položkami na základě skupiny položek.
    - Nastavte možnost **Vyrovnat na další nefakturované období** na **Ano**, abyste určili datum vyrovnání pro položku obnovení na základě data příštího nefakturovaného období po zahájení obnovy.
    - Nastavte možnost **Kopírovat sériové číslo** na **Ano**, chcete-li zkopírovat sériové číslo položky z počátečního řádku prodejní objednávky do odpovídajícího řádku plánu fakturace.

13. Pokud v plánu fakturace používáte eskalaci, vyberte metodu, která se použije pro výpočet indexu spotřebitelských cen.
14. Nastavte možnost **Sledovat změnu ceny** na **Ano**, pokud chcete záznam o změnách cen na řádcích plánu fakturace. Pokud se řádek plánu fakturace ručně změní ze standardního na pevný a zadá se nová cena, informace o auditu jsou sledovány na řádku plánu fakturace. Nastavte ji tuto možnost na **Ne**, pokud nechcete sledovat tyto změny.
15. Zadejte, zda jsou záznamy ve výchozím nastavení filtrovány podle počátečního nebo koncového data na stránce **Generovat fakturu**.
16. Pokud použijete funkci **Nevyfakturované výnosy**, zadejte možnosti, které se použijí:

    - Nastavte možnost **Automaticky zaúčtovat hlavní deník** na **Ano**, pokud chcete, aby byl obecný deník vytvořen a zaúčtován současně. Nastavte tuto možnost na **Ne**, pokud chcete vytvořit obecný deník a poté jej ručně zaúčtovat.
    - V poli **Výchozí název deníku** vyberte výchozí název deníku, který se použije při vytváření obecného deníku.
    - V poli **Metoda krátkodobého nevyfakturování** vyberte metodu krátkodobého nevyfakturování, pokud ji používáte. Pokud vyberete **Žádná**, u nevyfakturovaných příjmů se nepoužije krátkodobá metoda. Vyberte **Období prosazení**, aby se vždy používalo 12 měsíců, **Pevný rok**, aby se používal fiskální rok.

17. Zadejte možnosti, které se použijí při ukončení plánu fakturování a jeho řádků:

    - **Vydat dobropis** – Vytvořte dobropis, když je plán fakturace nebo jeho řádek ukončen.
    - **Úprava kreditu** – Vytvořte úpravu kreditu pro plán fakturace, když je řádek ukončen. Úprava kreditu se objeví v budoucím fakturačním období plánu fakturace. Úprava kreditu automaticky aktualizuje částku faktury pro další fakturační období, dokud nebude dokončeno použití kreditu v plánu fakturace.
    - **Žádný kredit** – Když je plán fakturace nebo jeho řádek ukončen, nevytvoří se úprava kreditu ani dobropis. Tato možnost je dostupná, pouze když použijete možnost **Žádná úprava** k ukončení plánu fakturace.

## <a name="sequence-number-tab"></a>Karta Číselná řada

Použijte kartu **Pořadové číslo** na stránce **Parametry opakované fakturace smlouvy** pro nastavení výchozí hodnoty pro čísla plánu fakturace. Výchozí hodnoty jsou nastaveny na stránce **Číselné řady** (**Správa organizace \> Číselné řady \> Číselné řady**).

## <a name="set-up-billing-schedule-groups"></a>Nastavení skupin plánů fakturace

Použijte stránku **Skupina plánů fakturace** pro vytvoření skupiny plánů fakturace pro opakovanou fakturaci smlouvy. Když se vytvoří nový plán fakturace a použije se na něj skupina plánů fakturace, hodnoty, které jsou definovány na stránce **Skupina plánů fakturace**, jsou zadány jako výchozí hodnoty pro plán fakturace. Můžete změnit kteroukoli z výchozích hodnot pro konkrétní plán fakturace, který vytvoříte. Můžete nastavit více skupin plánů fakturace a pak jednu z nich přiřadit jako výchozí skupinu plánů fakturace na stránce **Parametry opakované fakturace smlouvy**.

Chcete-li vytvořit skupinu plánů fakturace pro opakovanou fakturaci smlouvy, postupujte takto.

1. Na stránce **Skupina plánů fakturace** vyberte **Nový**, čímž vytvoříte skupinu plánů fakturace.
2. Do pole **Skupina plánů fakturace** zadejte jedinečný identifikátor.
3. Zadejte popis do pole **Popis**.
4. Do pole **Četnost fakturace** zadejte, jak často se zákazníkovi fakturuje plán fakturace: **Jednou**, **Denně**, **Měsíčně**, **Čtvrtletně**, **Pololetně** nebo **Každoročně**.
5. V poli **Interval fakturace** zadejte interval fakturace. Například nastavte pole **Četnost fakturace** na **Měsíčně** a pole **Interval fakturace** na **2**, aby fakturace probíhala každý druhý měsíc.
6. V poli **Metoda cenových kalkulací** vyberte výchozí metodu cenových kalkulací pro položky v plánu fakturace:

    - **Standardní** – Vypočítejte jednotkovou cenu na základě celkového zadaného množství a použijte standardní cenu ze stránky **Vydané produkty** v části Správa informací o produktech.
    - **Paušální** – Použití paušální ceny, která je zadána na řádku plánu fakturace.
    - **Úroveň** – Vypočítejte jednotkovou cenu pomocí pevného množství v různých cenových hladinách. Každá úroveň musí být vyplněna před přechodem do další cenové skupiny.
    - **Paušální vrstva** – Vypočítejte jednotkovou cenu pomocí pevného množství a částky rozšířené ceny pro různé cenové hladiny. Cena účtovaná v období fakturace používá rozšířenou cenu, která odpovídá úrovni, kde existuje fakturační množství.

7. V poli **Typ položky** vyberte typ položky pro fakturační skupinu:

    - **Standardní** – Tuto hodnotu vyberte, pokud je množství statické.
    - **Využití** – Tuto hodnotu vyberte pro měřené položky nebo položky spotřebního typu. Pokud vyberete tuto hodnotu, nastavte pole **Možnost čtení využití** na **Čtení**, aby bylo možné zadat hodnotu (odečet) za fakturační období na měřidle nebo zařízení. Spotřebovaná hodnota bude vypočítána na základě předchozího fakturačního období a aktuálního odečtu, který zadáte.
    - **Milník** – Tuto hodnotu vyberte, chcete-li použít funkci Vyúčtování po milnících. Pokud vyberete tuto hodnotu, v poli **Šablona milníku** vyberte šablonu milníku, pokud ji používáte.
    - **Spotřeba** – Tuto hodnotu vyberte, chcete-li zadat hodnotu, která je spotřebována za fakturační období.

8. Nastavte možnost **Faktura odděleně** na **Ano**, čímž vytvoříte kombinaci konsolidovaných faktur a samostatných faktur pro stejného zákazníka. Zákazník má například pět plánů fakturace. Tři z nich budou sloučeny do jedné faktury, ale každá z ostatních dvou vyžaduje samostatnou fakturu. Nastavte tuto možnost na **Ne**, chcete-li pro zákazníka vytvořit pouze jednu konsolidovanou fakturu.
9. Nastavte možnost **Automaticky obnovit** na **Ano**, chcete-li automaticky obnovit plán fakturace pro další fakturační období, když je vytvořena faktura. Nastavte tuto možnost na **Ne**, čímž plán fakturace budete muset obnovit ručně. V poli **Řádky, které se mají přidat na obnovení** zadejte, kolik řádků se má přidat pro každé obnovení.
10. Nastavte možnost **Eskalace** na **Ano**, pokud chcete použít *eskalace* (zvýšení ceny) na plány fakturace přidružené k této skupině plánů účtování.
