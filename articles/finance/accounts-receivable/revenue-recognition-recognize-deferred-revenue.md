---
title: Uznání odložených výnosů
description: Toto téma obsahuje informace o tom, jak uznat výnosy pomocí funkce uznání výnosů.
author: kweekley
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 42e9aa20eb6f4a1c14f83c5a18a4699489a932a3
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725925"
---
# <a name="recognize-deferred-revenue"></a>Uznání odložených výnosů

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Funkci uznání výnosů nelze zapnout prostřednictvím správy funkcí. V současné době ji aktivujete pomocí konfiguračních klíčů.

Toto téma popisuje proces uznání výnosů v plánu uznání výnosů. Po zaúčtování faktury pro prodejní objednávku se pro každý řádek prodejní objednávky, který má plán výnosů, vytvoří plán uznání výnosů. Plán výnosů na řádku se používá k určení, zda by měl být výnos řádku odložen.

## <a name="view-revenue-recognition-schedule-details"></a>Zobrazení podrobností plánu uznání výnosů

Existují dva způsoby přístupu k podrobnostem plánu uznání výnosů.

- Plán uznání výnosů můžete otevřít přímo z fakturované prodejní objednávky. V tomto případě se informace v plánu výnosů filtrují, aby se zobrazovaly podrobnosti pouze pro vybranou prodejní objednávku. Tento přístup je užitečný, když ověřujete podrobnosti plánu pro prodejní objednávku.
- Plán uznání výnosů můžete otevřít přímo ze stránky **Uznání výnosů \> Periodické úlohy**. Tento přístup se často používá, když jsou výnosy uznány na konci období. Při prvním otevření stránky se nezobrazí žádné informace. Pomocí filtrů nad mřížkou definujte kritéria pro podrobnosti plánu, které by se měly zobrazit. Data na faktuře můžete filtrovat zadáním časového období, prodejní objednávky, odběratele, ID projektu nebo stavu.

[![Obrázek znázorňující stránku Plány výnosů](./media/revenue-recognition-schedule-page.png)](./media/revenue-recognition-schedule-page.png)

Záložka s náhledem **Finanční dimenze** pod mřížkou obsahuje finanční dimenze řádku prodejní objednávky. Tyto dimenze byly brány v úvahu při účtování do odložených výnosů. Zohledňují se také při uznání výnosů. Použité hodnoty dimenze závisí na účetní struktuře, která je přiřazena k hlavním účtům výnosů a odložených výnosů.

## <a name="recognize-revenue"></a>Uznání výnosů

Uznáváte výnosy spuštěním procesu **Vytvořit deníku** ze stránky **Uznání výnosů**. Tuto stránku můžete otevřít buď z prodejní objednávky nebo z **Periodických úkolů**. Pokud je proces spuštěn z prodejní objednávky, uznává výnosy pouze pro vybranou prodejní objednávku. Proces se obvykle místo toho spouští z **Periodických úkolů**, takže uznává výnosy pro všechny zaúčtované faktury za prodejní objednávky.

Chcete-li definovat kritéria pro výběr a účtování výnosů, vyberte **Vytvořit deník** a otevřete dialogové okno **Vytvořit deník**.

[![Vytvoření možností parametrů deníku](./media/revenue-recognition-create-journal.png)](./media/revenue-recognition-create-journal.png)

V dialogovém okně použijte možnosti ve skupině polí **Datum zpracování** a definujte datum zaúčtování, které se použije při uznání výnosů. Pokud zvolíte **Vybrané datum**, můžete zadat datum zaúčtování v poli **Datum transakce**. Pokud vyberete **Datum plánu výnosů**, datum transakce se nepoužije. Místo toho se jako datum zaúčtování použije hodnota pole **Datum uznání** na každém řádku plánu.

Dále zadejte v poli **Od data** datum „od“ pro uznání výnosů. Budou uznány všechny řádky plánu, ve kterých je datum uznání zapnuto nebo před datem „od“, za předpokladu, že nejsou pozastaveny.

Po dokončení definování dat vyberte v dialogovém okně **OK** a vytvořte deník. Obdržíte informační zprávu, která ukazuje počet transakcí, které byly vytvořeny, a deník, kde byly vytvořeny. Deník není automaticky zaúčtován. Manažer uznání výnosů má proto čas ověřit, které řádky plánu jsou uznány.

Po spuštění procesu jsou řádky v plánu, které byly přeneseny do deníku, označeny jako **Zpracováno**. Příznak **Zpracováno** označuje, že řádky byly přeneseny do deníku, ale mohou být zaúčtovány nebo nezaúčtovány. Po zaúčtování deníku uznání výnosů příznak **Zpracováno** zůstává. Pokud je deník uznání výnosů odstraněn, nebo pokud je odstraněn řádek, bude příznak **Zpracováno** odstraněn. Tímto způsobem lze řádek uznat, když se proces **Vytvořit deník** znovu spustí.

[![Stránka plánů uznání výnosů](./media/revenue-recognition-rev-recog-schedule-02.png)](./media/revenue-recognition-rev-recog-schedule-02.png)

Na stránce **Deník uznání výnosů** (**Uznání výnosů \> Položky deníku \> Deník uznání výnosů**), otevřete **Řádky** pro zobrazení podrobností o tom, co se uznává. Pro každý řádek uznávaného plánu je vždy vytvořena samostatná transakce, i když jsou všechny řádky zaúčtovány ve stejnému datum pomocí stejných účtů hlavní knihy.

[![Stránka dokladu deníku](./media/revenue-recognition-journal-voucher.png)](./media/revenue-recognition-journal-voucher.png)

Sloupec **Účet** zobrazuje účet hlavní knihy odložených výnosů. Tento účet hlavní knihy nelze upravit. Toto omezení pomáhá zaručit, že je uvolněn správný účet hlavní knihy odložených výnosů. Tento účet hlavní knihy není ověřen proti účetní struktuře, protože se mohl od posledního zaúčtování na účet hlavní knihy odložených výnosů změnit.

Sloupec **Protiúčet** zobrazuje účet hlavní knihy výnosů. Ve výchozím nastavení je účet hlavní knihy výnosů převzat z profilů účtování zásob a finanční dimenze jsou převzaty z řádku prodejní objednávky. Účetní hlavní knihy je ověřen proti aktuální účetní struktuře. Lze ho však upravit, pokud se účetní struktura změnila a vyžaduje další finanční dimenze.

Výchozí částka je z odpovídajícího řádku plánu a nelze ji změnit.

Ve výchozím nastavení, pokud má prodejní objednávka více měn, je směnný kurz nastaven na směnný kurz z faktury. Toto chování pomáhá zaručit úplné uvolnění částek zúčtovací měny a měny vykazování. Z důvodu zaokrouhlování se směnný kurz pro poslední řádek plánu může mírně lišit od kurzu na faktuře.

Po zaúčtování deníku uznání výnosů je na plánu zadán doklad. Pokud pro stejný řádek plánu existuje více než jeden doklad, objeví se na řádku hvězdička (\*). Chcete-li zobrazit doklady, které byly zaúčtovány pro tento řádek, vyberte **Transakce dokladu**.

## <a name="modify-the-revenue-recognition-schedule-details"></a>Úprava podrobností plánu uznání výnosů

Většinu dat v podrobnostech plánu výnosů nelze upravit. Nové řádky nelze přidat do plánu a stávající řádky nelze odstranit. Podrobnosti plánu výnosů pro každý řádek prodejní objednávky musí být zachovány, aby se zajistilo, že v průběhu času organizace uzná stejnou částku, která byla odložena.

### <a name="edit-schedule-lines"></a>Úprava řádků plánu

Na řádcích plánu jsou povoleny některé úpravy. Na řádcích lze změnit následující pole:

- **Blokováno** – Tento příznak lze nastavit nebo vymazat před zpracováním řádku. Chcete-li vymazat příznak, zvolte řádek a poté vyberte **Odstranit blokování**. Výnosy nelze uznat na řádcích, které jsou blokovány. Řádky lze automaticky zablokovat, pokud je plán výnosů nastaven na automatická blokování.

    [![Plány výnosů - úprava řádků plánu](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)

- **Datum uznání** – Datum uznání lze změnit před zpracováním řádku. Když je spuštěn proces, který vytváří deník pro uznání výnosů, je do pole **Uznat výnosy od data** zadáno datum. Toto datum se porovná s datem v poli **Datum uznání**, aby se určilo, které řádky se mají uznat.
- **Částka k uvolnění** – Částku, která bude uvolněna, lze změnit před zpracováním řádku. Částku uznaných výnosů můžete snížit, ale nemůžete ji navýšit. Toto pole umožňuje organizaci uznat část výnosů v den uznání. Pokud se částka změní, částka v poli **Zbývající částka** ukazuje, kolik výnosů musí být ještě uznáno.
- **Množství k uvolnění** – Pokud je plán výnosů nastaven na jeden výskyt nebo jeden měsíc, pole **Množství k uvolnění** zobrazuje množství pro řádek prodejní objednávky. Toto pole lze také upravit a poskytuje další způsob uznání části výnosů. Pokud je například množství na řádku 5, můžete přepsat množství tak, aby bylo menší než 5. Částka v poli **Částka k uvolnění** se aktualizuje poměrově.

### <a name="update-contract-terms"></a>Aktualizace smluvních podmínek

Podrobnosti o plánu výnosů jsou vytvářeny na základě plánu výnosů, který je při zaúčtování faktury přiřazen k řádku prodejní objednávky. Pokud je plán výnosů na řádku prodejní objednávky nesprávný, nelze jej po fakturaci prodejní objednávky na objednávce změnit. Místo toho musíte použít tlačítko **Aktualizovat smluvní podmínky** pro změnu plánu výnosů. Plán výnosů lze změnit buď před nebo po uznání výnosů.

Chcete-li změnit plán, zvolte jakýkoliv řádek plánu pro položku, kterou měníte. Na následujícím obrázku je vybrán řádek pro položku S0008, který byl zaúčtován pomocí 12měsíčního plánu výnosů. Pokud vyberete **Aktualizovat smluvní podmínky**, zobrazí dialogové okno datum zahájení a ukončení smlouvy a plán výnosů.

[![Počáteční a koncové datum smlouvy](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)

Změňte data zahájení a ukončení smlouvy tak, aby odrážela správné časové období. Když změníte časové období, musí se hodnota v poli **Počet výskytů** shodovat s plánem výnosů, který byl definován v systému. Protože smlouva byla v tomto příkladu změněna na smlouvu na 24 měsíců, musí být stanoven plán výnosů na 24 měsíců. Protože existuje 24měsíční plán výnosů, je zadán ve výchozím nastavení a smlouvu lze změnit. Pokud neexistuje plán výnosů s odpovídajícím počtem výskytů, nelze smlouvu změnit. Po dokončení aktualizace smluvních podmínek a plánu výnosů podle potřeby vyberte v dialogovém okně **OK** pro uložení změn.

[![Aktualizované období smlouvy](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)

Změny smlouvy mají následující dopady na podrobnosti plánu výnosů:

- Pokud pro produkt nebyly uznány žádné výnosy, budou všechny předchozí podrobnosti plánu odstraněny a nahrazeny novými podrobnostmi plánu výnosů. Například položka S0008 měla původně 12 řádků v podrobnostech plánu. Těchto 12 řádků je na základě nového plánu výnosů odstraněno a nahrazeno 24 řádky.
- Pokud byly pro produkt uznány výnosy, byly některé výnosy nesprávně uznány, protože uznání bylo založeno na nesprávném plánu výnosů. Tyto řádky musí být stornovány a znovu uznány na základě nového plánu. V tomto scénáři jsou vytvořeny nové řádky plánu výnosů, které mají záporné částky k původnímu datu uznání. Poté jsou vytvořeny nové řádky pro uznání částek na základě nového plánu výnosů. Například 8. srpna 2019 jste uznali výnosy za 10,53 USD. 8. září 2019 jste uznali výnosy za 13,16 USD. Proto jsou pro tyto dny vytvořeny dva nové řádky. Jeden řádek na -10,53 USD a druhý řádek na -13,16 USD. Poté je vytvořeno dvacet čtyři nových řádků a celkový odložený výnos 160,61 USD je přidělen mezi ně. Storno řádky můžete zaúčtovat spuštěním procesu **Vytvořit deník**.

[![Plán uznání výnosů](./media/revenue-recognition-rev-recog-schedule-03.png)](./media/revenue-recognition-rev-recog-schedule-03.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
