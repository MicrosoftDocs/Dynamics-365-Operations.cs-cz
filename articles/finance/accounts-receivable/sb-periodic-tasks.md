---
title: Periodické úkoly v opakované fakturaci smlouvy
description: Tento článek popisuje periodické úkoly, které jsou k dispozici v rámci opakované fakturace smlouvy.
author: JodiChristiansen
ms.date: 04/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: d834d1d7aa34448b4ef21606974538eb294b5d7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904781"
---
# <a name="periodic-tasks-in-recurring-contract-billing"></a>Periodické úkoly v opakované fakturaci smlouvy

Tento článek popisuje periodické úkoly, které jsou k dispozici v rámci opakované fakturace smlouvy.

## <a name="generate-invoice"></a>Generovat fakturu

Stránku **Generovat fakturu** používejte k vytváření hromadných měsíčních opakujících se faktur z informací, které jste nastavili na stránkách **Všechny plány fakturace** a **Zobrazit podrobnosti fakturace**. Když je vytvořena faktura, popis položky pro řádek zpracování prodejní objednávky se aktualizuje popisem položky a daty zahájení a ukončení fakturace pro řádek plánu, který je fakturován.

## <a name="generate-invoice-batch-processing"></a>Generovat dávkové zpracování faktur

Stránku **Generovat dávkové zpracování faktur** používejte k vytvoření opakujících se faktur pomocí opakovaného dávkového zpracování. Parametry, které jsou k dispozici, jsou stejné jako parametry na stránce **Generovat fakturu**, ale lze je uložit do dávkového procesu, který lze spustit vícekrát.

## <a name="price-update"></a>Aktualizace ceny

Pomocí nástroje Aktualizace ceny můžete aktualizovat ceny několika položek ve více plánech fakturace v jediné akci. Ceny lze aktualizovat buď na základě určitého procenta nebo stanovené částky. Seznam řádků zobrazuje pouze aktuální jednotkové ceny položek. Nezobrazuje ceny po jejich aktualizaci.

K nástroji pro aktualizaci cen přidáváme několik poznámek:

- Pokud již byla prodejní objednávka pro určitý rok vytvořena (tj. položky byly vyúčtovány), cena řádkových položek není ovlivněna.
- Nástroj pro aktualizaci ceny lze použít pro řádkové položky, které mají stav **Aktivní** nebo **Pozastaveno**. U položek, které jsou pozastaveny, musí být možnost **Upravit rozvrh** při použití blokování nastavena na **Ne**.
- Nástroj pro aktualizaci ceny nelze použít na řádkové položky, které jsou položkami použití, které používají eskalace, fakturaci po milnících nebo rozdělení výnosů.

### <a name="price-update-example"></a>Ukázka aktualizace ceny

Vytvoří se plán fakturace a přidá se položka obnovení. Cena za jednotku je 750 USD. První rok položky se platí 15. prosince 2021. Pro období od 1. ledna do 31. prosince 2022 je vytvořen plán fakturace.

V době obnovy vytvoří proces **Generovat fakturu** vytvoří prodejní objednávku pro rok 2022. Po spuštění nástroje pro aktualizaci ceny se cena aktualizuje ze 750 na 800 USD.

Prodejní objednávka a plán fakturace na rok 2022 nejsou ovlivněny a jednotková cena zůstává 750 USD, protože plán fakturace na rok 2022 již byl vyúčtován. Řádek plánu fakturace a podrobnosti řádku pro rok 2023 jsou aktualizovány na 800 USD, protože plán fakturace na rok 2023 ještě nebyl vyúčtován.

### <a name="update-prices--flat-pricing-method"></a>Aktualizace cen – metoda paušálních cen

Když aktualizujete ceny položek, které používají metodu paušálních cen, můžete určit procento nebo částku pro zvýšení ceny.

Chcete-li spustit nástroj pro aktualizaci ceny na položkách, které používají metodu paušálních cen, postupujte takto.

1. Na stránce nástroje **Aktualizace ceny** vyberte **Paušální** metodu stanovení ceny.
2. V poli **Metoda zvýšení** metodu zvýšení, která se používá k aktualizaci ceny položek.
3. V závislosti na zvolené metodě zvýšení zadejte procento v poli **Procento** nebo částku v poli **Částka**.
4. Na pevné záložce **Záznamy k zahrnutí** přidejte pomocí tlačítka **Filtr** datové filtry.
5. Vyberte **Zobrazit náhled** pro zobrazení rozsahu záznamů.
6. Pokud nechcete zpracovat některé řádky, vyberte je a poté vyberte **Odstranit**.
7. Vyberte **OK**.

### <a name="update-prices--standard-pricing-method"></a>Aktualizace cen – metoda standardních cen

Pokud byla v záznamu položky změněna cena položky, lze ji aktualizovat ve všech řádcích plánu fakturace, pokud položka používá standardní metodu stanovení ceny.

1. Na stránce nástroje **Aktualizace ceny** vyberte **Standardní** metodu stanovení ceny.
2. Na pevné záložce **Záznamy k zahrnutí** přidejte pomocí tlačítka **Filtr** datové filtry.
3. Vyberte **Zobrazit náhled** pro zobrazení rozsahu záznamů.
4. Pokud nechcete zpracovat některé řádky, vyberte je a poté vyberte **Odstranit**.
5. Vyberte **OK**.

## <a name="mass-hold-processing"></a>Zpracování hromadného blokování

Pokud chcete aplikovat volby pozastavení na několik plánů fakturace současně, použijte stránku **Hromadné blokování**.

Chcete-li pozastavit pouze jeden plán fakturace nebo jeden řádek plánu fakturace, otevřete stránku **Všechny plány fakturace** a vyberte možnost **Blokovat**. Chcete-li odebrat blokování, použijte stránku **Odebrat blokování**.

### <a name="put-billing-schedules-on-hold"></a>Pozastavení plánu fakturace

Chcete-li pozastavit několik plánů fakturace, postupujte takto.

1. Na stránce **Hromadné blokování** nastavte **Možnost zpracování** na **Použít blokování**.
2. V poli **Kód důvodu** vyberte kód důvodu.
3. Nastavte možnost **Upravit plán**:

    - **Ano** – Pokud nastavíte možnost na **Ano**, zadejte datum blokování v poli **Datum blokování**. Všechny řádky plánu fakturace následující po datu pozastavení budou odebrány.
    - **Ne** – Řádky plánu fakturace se nezmění. Změní se pouze stav. Je aktualizován na **Pozastaveno**.

4. Na pevné záložce **Záznamy k zahrnutí** přidejte pomocí tlačítka **Filtr** datové filtry.
5. Vyberte **Zobrazit náhled** pro zobrazení rozsahu záznamů.
6. Pokud nechcete zpracovat některé řádky, vyberte je a poté vyberte **Odstranit**.
7. Vyberte **OK**.

Když se vrátíte do seznamu plánů fakturace, měli byste vidět, že jejich stav byl změněn na **Pozastaveno**.

### <a name="remove-a-hold-from-several-billing-schedules"></a>Ukončení blokování u několika plánů fakturace

1. Na stránce **Hromadné blokování** nastavte **Možnost zpracování** na **Odebrat blokování**.
2. V poli **Kód důvodu** zadejte kód důvodu.
3. Do pole **Datum odebrání** zadejte datum, kdy má být blokování odebráno.
4. Aktualizujte pole **Datum pokračování** a **Datum odkladu** podle potřeby. Datum odkladu se přidá ke všem řádkům, které jsou odložitelné.
5. Na pevné záložce **Záznamy k zahrnutí** přidejte pomocí tlačítka **Filtr** datové filtry.
6. Vyberte **Zobrazit náhled** pro zobrazení rozsahu záznamů.
7. Pokud nechcete zpracovat některé řádky, vyberte je a poté vyberte **Odstranit**.
8. Vyberte **OK**.

> [!NOTE]
> Chcete-li odebrat blokování, musíte nastavit hodnotu **Odebrat přepsání blokované skupiny uživatelů** na stránce **Parametry opakované fakturace smlouvy**.

Fakturační řádek má například datum zahájení 1. února 2022 a datum ukončení 28. února 2022. Fakturovaná částka je 200 USD. Pole **Datum blokování** je stanoveno na 10. února 2022. Únorové období je proto upraveno tak, aby vylučovalo jakékoli datum po 10. únoru. Nové období je od 1. února do 9. února a částka je 64,29 USD (vypočtená prostřednictvím denního poměru). Všechny řádky plánu fakturace s datem 10. února nebo pozdějším budou odebrány.

Když je proces **Odebrat blokování** dokončen a pole **Datum odebrání** je nastaveno na 10. února 2022, budou existovat dvě zúčtovací období. První zúčtovací období trvá od 1. února do 9. února a částka je 64,29 USD. Druhé zúčtovací období trvá od 10. února do 28. února a částka je 135,71 USD.

## <a name="mass-termination-processing"></a>Zpracování hromadného ukončení

Stránku **Hromadné ukončení** použijte k ukončení řádků rozvrhu fakturace, které se aktuálně zobrazují, zadáním data ukončení.

Pokud používáte odklady příjmů a výdajů, plány fakturace s polem **Datum ukončení** nastaveným na **Upravit rozvrh** na stránce **Všechny plány fakturace** mají nárok na vrácení peněz.

Plány fakturace, které používají funkci přidělení více prvků (MEA), se nezobrazují na stránce **Hromadné ukončení**. Jednotlivý plán fakturace můžete vždy ukončit pomocí funkce ukončení v plánu fakturace.

> [!NOTE]
> Řádky plánu fakturace, které jsou aktuálně zahrnuty do dávky **Generovat fakturu**, nejsou pro tento proces k dispozici.

Informace o každém poli a procesu najdete v tématu [Ukončení plánů fakturace](terminate-billing-schedule.md).

## <a name="mass-archive-process"></a>Proces hromadné archivace

K archivaci více plánů fakturace použijte stránku **Hromadné archivace**. Archivovat lze pouze ukončené plány fakturace.

Po archivaci plánu fakturace nastanou následující události:

- Stav se změní na **Archivováno**.
- Plány fakturace jsou trvale uzamčeny.
- Řádky plánu fakturace již nejsou dostupné na stránkách s dotazy.

> [!NOTE]
> Archivace plánu fakturace je trvalá akce a nelze ji vrátit zpět.

Při archivaci plánu fakturace postupujte takto.

1. Na stránce **Hromadná archivace** určete v poli **Datum ukončení fakturace** datum ukončení fakturace. Chcete-li zobrazit všechny ukončené plány fakturace, ponechte toto pole prázdné.
2. Chcete-li omezit sadu zobrazených záznamů, použijte tlačítko **Filtr** na záložce **Záznamy, které mají být zahrnuty**.
3. Zvolte **Zobrazit náhled**.
4. Pokud nechcete archivovat některé záznamy, vyberte je a poté vyberte **Odebrat**.
5. Výběrem **OK** archivujte záznamy na stránce.

## <a name="mass-stubbing-process"></a>Proces hromadného přerušení

Stránku **Hromadné přerušení** použijte k označení všech vybraných řádků plánu fakturace jako fakturovaných (přerušení) nebo nefakturovaných (vrácení přerušení). Přerušení nebo vrácení přerušení se nejčastěji provádí u importovaných řádků plánu fakturace, které byly dříve účtovány v jiném systému. Přerušené řádky plánu fakturace se zobrazují jako nefunkční a nevytvoří fakturu pro zákazníka.

### <a name="stub-records"></a>Záznamy o přerušení

1. Na stránce **Hromadné přerušení** v poli **Možnosti zpracování** vyberte **Přerušit**.
2. V poli **Datum přerušení** nastavte datum přerušení k určení řádků, na které chcete proces použít. Zobrazí se pouze záznamy, u kterých je datum zahájení fakturace stejné nebo starší než zadané datum přerušení.
3. Vyberte **Zobrazit náhled**, aby se zobrazily řádky, které chcete přerušit.
4. Chcete-li řádek vyloučit z procesu, označte ho a poté vyberte **Odebrat**.
5. Tlačítkem **Zpracovat** přerušíte řádky.

### <a name="reverse-stub-records"></a>Vrácení přerušených záznamů

1. Na stránce **Hromadné přerušení** v poli **Možnosti zpracování** vyberte **Vrátit přerušení**.
2. V poli **Datum přerušení** nastavte datum přerušení k určení řádků, na které chcete proces použít. Zobrazí se pouze záznamy, u kterých je datum zahájení fakturace stejné nebo starší než zadané datum přerušení.
3. Vyberte **Zobrazit náhled**, aby se zobrazily řádky, jejichž přerušení chcete vrátit zpět.
4. Chcete-li řádek vyloučit z procesu, označte ho a poté vyberte **Odebrat**.
5. Tlačítkem **Zpracovat** vrátíte přerušení řádků zpět.

## <a name="update-completion-date-process"></a>Aktualizovat proces data dokončení

Stránku **Datum dokončení aktualizace** použijte k aktualizaci data dokončení konkrétních položek milníku ve více plánech fakturace nebo u více uživatelů. Můžete také aktualizovat procento dokončení položek v šablonách milníků, které používají metodu **Procento dokončení**.

1. Na stránce **Datum dokončení aktualizace** přejděte na **Zpracování milníku** a vyberte **Procento dokončení aktualizace**.
2. V poli **Procentní částka** zadejte celkové procento, které bylo dokončeno.
3. Vyberte číslo položky související s šablonou milníku.
4. Na pevné záložce **Záznamy k zahrnutí** vyberte **Filtr** a v něm konkrétní hodnotu **Účet koncového uživatele**, **Číslo plánu fakturace** nebo **Čísla položek** jako kritérium filtru.
5. Tlačítkem **OK** zpracujete změnu. Po dokončení zpracování se do přidělení milníku přidá nový řádek. Tento řádek představuje procento, které bylo u šablony milníku dokončeno.

## <a name="unbilled-revenue-mass-processing"></a>Hromadné zpracování nevyfakturovaných výnosů

Na stránce **Hromadné zpracování nevyfakturovaných výnosů** vytvářejte záznamy deníku nevyfakturovaných výnosů nebo přerušte záznam deníku pro jeden nebo více vybraných plánů fakturace nebo řádků podrobností fakturace.

- **Vytvořit položku deníku** – Vytvářejte záznamy deníku nevyfakturovaných výnosů pro více řádků plánu fakturace. Chcete-li vybrat rozsah záznamů, které se zobrazí v seznamu, použijte tlačítko **Filtr** na záložce **Záznamy k zahrnutí**. Seznam zobrazuje pouze řádky plánu fakturace, pro které nebyly vytvořeny položky deníku nevyfakturovaných výnosů. Počáteční položky deníku jsou vytvořeny. Pro položky časového rozlišení se také vytvářejí plány časového rozlišení.
- **Přerušit položku deníku** – Označte řádky plánu fakturace, pro které již byly vytvořeny nefakturované položky deníku. Tato možnost se používá v případě, že nevyfakturovaný záznam deníku byl již zaúčtován v jiném systému. Označí deník nevyfakturovaných výnosů jako přerušený a nezaúčtuje transakci do hlavní knihy.
- **Vrátit přerušení položky deníku** – Vrátí přerušení položek deníku, které byly zpracovány. Pokud došlo k chybě při zpracování příkazu **Přerušit položku deníku**, tato možnost vypne zaškrtávací políčko **Přerušeno** řádku plánu fakturace.
- **Přerušit řádek s podrobnostmi fakturace** – Tento proces použijte, když byly nevyfakturované výnosy zpracovány v externím systému a některé řádky podrobností fakturace již byly fakturovány. Tento proces zajistí, že se na účtech nevyfakturovaných výnosů objeví správná částka.
- **Vrátit přerušení řádku s podrobnostmi fakturace** – Vrátí zpět jakékoli akce **Přerušit řádek s podrobnostmi fakturace**.

Pole **Název deníku** slouží k zaúčtování operace **Vytvořit položku deníku** do hlavní knihy.

> [!NOTE]
> Proces přerušení nezaúčtuje částky do hlavní knihy. Pole **Název deníku** není k dispozici u všech procesů přerušení a vrácení přerušení.

### <a name="unbilled-revenue-stub-example"></a>Příklad přerušení nevyfakturovaných výnosů

Plán fakturace je nastaven na jeden rok, od října 2021 do září 2022. Nevyfakturovaný výnos již byla zpracován v externím systému. Devět měsíců plánu fakturace již bylo vyúčtováno. Částka každého fakturačního období je 250 USD. Na začátku roku je celková částka, která byla zaúčtována do nevyfakturovaných výnosů, rovná 3 000 USD. Po devíti měsících již bylo vyfakturováno 2 250 USD a v nevyfakturovaných výnosech zůstává 750 USD.

Chcete-li nastavit plán fakturace, kde zbývají nevyfakturované výnosy pouze za tři měsíce, postupujte takto.

1. Na stránce **Zobrazit podrobnosti fakturace** vytvořte plán fakturace na období od října 2021 do září 2022, číslo položky S0001 a částku 250 USD za měsíc.
2. Vyberte možnost **Vytvořit položku deníku** pro plán fakturace. Částka 3 000 USD je zaúčtována do nevyfakturovaných výnosů.
3. Vyberte možnost **Přerušit řádek s podrobnostmi fakturace** a uveďte datum transakce v červnu 2022 (devět měsíců). Řádky plánu fakturace se v náhledu nezobrazí. Ovlivněné řádky jsou založeny na datu transakce.
4. Vyberte **OK**.

Prvních devět měsíců, které byly fakturovány, se nachází v přerušeném stavu.

[![Zobrazení přerušení řádku s podrobnostmi.](./media/01_View-billing-detail-stub.png)](./media/01_View-billing-detail-stub.png)

Částka 3 000 USD je stornována z nevyfakturovaných výnosů a zaúčtuje se zbývajících 750 USD v nevyfakturovaných výnosech. Chcete-li zobrazit zaúčtování nevyfakturovaných výnosů, vyberte možnost **Audit zápisu do deníku nevyfakturovaných výnosů** na kartě **Obnovení** stránky s podrobnostmi řádku.

[![Audit zápisu do deníku nevyfakturovaných výnosů.](./media/02_Unbilled-rev-journal-audit.png)](./media/02_Unbilled-rev-journal-audit.png)

> [!NOTE]
> Záznam deníku nevyfakturovaných výnosů lze vytvořit pro jakékoli období obnovení za předpokladu, že byly vyúčtovány všechny řádky podrobností fakturace z předchozího období. Například řádek plánu fakturace má měsíční frekvenci fakturace po dobu 12 měsíců, od ledna do prosince 2021. Řádek má tři časové horizonty: počáteční období, druhé období (leden až prosinec 2022) a třetí období (leden až prosinec 2023). Po vytvoření faktury pro všechny řádky podrobností fakturace z prvních 12 měsíců v roce 2021 lze vytvořit zápis do deníku pro nevyfakturované výnosy druhého období.
>
> U položek časového rozlišení, které využívají funkci nevyfakturovaných výnosů, se zpracuje fakturační řádek a řádky slev. Pro tyto položky se vytvoří zápis do deníku nevyfakturovaných výnosů a plán časového rozlišení pro řádek fakturace a řádek slevy.
>
> Zápisy do deníku, které jsou vytvořeny pro položky bez časového rozlišení a položky s časovým rozlišením, účtují dobropis na různé účty výnosů.
