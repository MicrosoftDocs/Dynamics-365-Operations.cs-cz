---
title: Odložené výnosy a výdaje ve fakturaci předplatného
description: Toto téma vysvětluje, jak nastavit odložené výnosy a výdaje ve fakturaci předplatného.
author: JodiChristiansen
ms.date: 11/04/2021
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
ms.openlocfilehash: 5ff8d2f4663c53bf6dece1ef9af6609d5f0c5b50
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544483"
---
# <a name="revenue-and-expense-deferrals-in-subscription-billing"></a>Odložené výnosy a výdaje ve fakturaci předplatného

Toto téma vysvětluje, jak nastavit a používat odložené výnosy a výdaje ve fakturaci předplatného. Harmonogramy odkladů jsou vždy založeny na podkladovém původním dokumentu nebo rozvrhu fakturace a závisí na nich. Protože jsou vytvářeny na základě výchozích hodnot, nelze je zadávat ani vytvářet samostatně.

Proces nastavení a použití odložených příjmů a výdajů probíhá na několika stránkách:

- Na stránce **Parametry odložení výnosů a nákladů** můžete definovat firemní preference.
- Na stránce **Výchozí hodnoty odkladu** můžete nastavit výchozí účty a šablony, které se používají pro plány odkladu.
- Na stránkách **Šablony odkladu** a **Šablony odkladu založené na událostech** můžete definovat šablony, které se používají pro plány odkladů.
- Na stránce **Všechny plány odkladů** můžete zobrazit a upravit jakýkoli plán odkladu.

Odložení výnosů a nákladů lze použít společně s opakovanou fakturací smlouvy.

## <a name="revenue-and-expense-deferral-parameters"></a>Parametry časového rozlišení výnosů a výdajů

Stránka **Parametry odložení výnosů a nákladů** obsahuje následující pole.

| Pole | Popis |
|---|---| 
| Karta **Plán** | |
| Stejné za období | <p>Zadejte, zda se při výpočtu částky za období pro plán odkladu použije počet dní v období:</p><ul><li>**Ano** – Částka pro každé období je stejná, bez ohledu na počet dní v období. Dílčí období (jako jsou období na začátku nebo na konci plánu odkladu) budou poměrná.</li><li>**Ne** - Částka se počítá na základě počtu dní v každém období.</li></ul><p>Toto nastavení můžete přepsat na úrovni transakce.</p> |
| Prodejní sleva možnosti odkladu | <p>Určete, zda jsou pro slevu a částky prodejní objednávky vytvořeny samostatné plány odkladu:</p><ul><li>**Samostatný plán pro slevu** – Částka slevy je uchovávána odděleně od částky výnosu.<p>V tomto případě se při vytvoření a následném zaúčtování prodejní objednávky vytvoří dva plány odložení. Částky slev a výnosů budou zaúčtovány na různé účty časového rozlišení.</p></li><li>**Sloučit slevu s příjmem** – Částka slevy je kombinována s částkou výnosu. Vytvoří se jeden plán odkladu a částka slevy i částka výnosu se zaúčtují na stejný účet odkladu.<p>V tomto případě se při vytvoření a následném zaúčtování prodejní objednávky vytvoří jeden plán odložení. Částka slevy i částka výnosu se zaúčtují na stejný účet odkladu.</p></li></ul><p>**Poznámka:** Chcete-li uplatnit slevy na položky, které používají funkci nevyfakturovaných příjmů, vyberte možnost **Samostatný plán pro slevu**. Slevy pak lze uplatnit na všechny položky bez ohledu na to, zda je použita funkce nevyfakturovaných příjmů. Pokud je vybrána volba **Sloučit slevu s příjmem**, nelze slevy uplatnit na položky, které používají funkci nevyfakturovaných příjmů.</p> |
| Nákupní sleva možnosti časově rozlišené položky | <p>Vyberte, zda jsou pro slevu a částky nákupní objednávky vytvořeny samostatné plány odkladu:</p><ul><li>**Samostatný plán pro slevu** – Částka slevy je uchovávána odděleně od částky výdaje.<p>V tomto případě se při vytvoření a následném zaúčtování nákupní objednávky vytvoří dva plány odložení. Částky slev a výdajů jsou zaúčtovány na různé účty časového rozlišení.</p></li><li>**Sloučit slevu s příjmem** – Částka slevy je kombinována s částkou výdaje. Vytvoří se jeden plán odkladu a částka slevy i částka výdaje se zaúčtují na stejný účet odkladu.<p>V tomto případě se při vytvoření a následném zaúčtování nákupní objednávky vytvoří jeden plán odložení. Částka slevy i částka výdaje se zaúčtují na stejný účet odkladu.</p></li></ul> |
| Konsolidovat předchozí období | <p>Určete, zda jsou konsolidované řádky plánu odkladu za předchozí období:</p><ul><li>**Ano** – Pokud je datum zahájení odkladu v období před datem transakce, všechny částky až do období data transakce se sloučí do jednoho řádku plánu odkladu.</li><li>**Ne** – Částky ze všech období jsou vedeny na samostatných řádcích časového plánu odkladu.<p>Pokud je datum zahájení odkladu ve stejném období nebo pozdější období než datum transakce, tato možnost nemá žádný účinek.</p></li></ul><p>Toto nastavení lze aktualizovat na úrovni transakce.</p> |
| Výchozí počáteční datum odkladu | <p>Vyberte pravidlo, které se používá k určení počátečního data plánu odkladu:</p><ul><li>**Datum transakce** – Použije se datum transakce jako počáteční datum.</li><li>**Začátek aktuálního měsíce** – Jako počáteční datum použijte první z aktuálního měsíce. Pokud je datum transakce první v libovolném měsíci, je počátečním datem první aktuální měsíc.</li><li>**Začátek následujícího měsíce** – Jako počáteční datum použijte první z následujícího měsíce. Pokud je datum transakce prvního, použije se datum transakce. V opačném případě se použije první den následujícího měsíce.</li><li>**Pravidlo 15** – Pokud je datum transakce mezi prvním a patnáctým, použijte jako počáteční datum první z aktuálního měsíce. Pokud je datum transakce česnáctého nebo pozdější, je počátečním datem první den následujícího měsíce.</li></ul><p>Toto nastavení lze aktualizovat na úrovni transakce.</p> |
| Metoda krátkodobého odkladu | <p>Vyberte způsob krátkodobého odložení: **Žádný**, **Klouzavá období**, nebo **Pevný rok**.</p><p>|
| Metoda odloženého zaúčtování | <p>Vyberte metodu, která je používaná k tvorbě transakcí odkladu:</p><ul><li>**Rozvaha** – Použijte metodu účtování v rozvaze k vytvoření odložených transakcí.</li><li>**Zisk a ztráta** - Použijte metodu účtování zisku a ztrát pro vytvoření odložených transakcí. Když jsou transakce zaúčtovány, můžete zkontrolovat doklad faktury, abyste viděli další položky, které vyvažují částky počátečního uznání a kompenzace uznání.</li></ul> |
| Reverzní zisk a ztráta z úvěru | <p>**Poznámka:** Toto pole je k dispozici pouze v případě, když je pole **Metoda účtování odkladu** nastaveno na hodnotu **Zisk a ztráta**.</p><p>Určete, zda se částky zisku a ztráty stornují, když je zrušení, ukončení nebo refundace aplikováno na plán fakturace nebo prodejní objednávku:</p><ul><li>**Ano** – Změňte částky zisků a ztrát a použijte částku úpravy kreditu na plán odkladu.<p>Pokud ke zrušení dojde v polovině zúčtovacího období, částky jsou poměrné.</p></li><li>**Ne** - Pro zisk a ztrátu se nevytvoří žádné reverzní transakce, když je zrušení, ukončení nebo refundace aplikováno na plán fakturace nebo prodejní objednávku.</li></ul> |
| Karta **Uznání** | |
| Automaticky zaúčtovat hlavní deníky | <p>Určete, zda se mají automaticky účtovat zápisy do deníku, které jsou vytvořeny odložením výnosů a výdajů:</p><ul><li>**Ano** - Automaticky účtovat zápisy do deníku, které jsou vytvořeny odložením výnosů a výdajů.<p>**Tip:** Výběrem **Ano** můžete pomoci předejít účetním nesrovnalostem, které jsou způsobeny ručními změnami poukázek.</p></li><li>**Ne** - Zápisy do deníku, které jsou vytvořeny odložením výnosů a výdajů, se neúčtují automaticky. Jakékoliv deníky musíte zaúčtovat ručně.</li></ul> |
| Shrnout deník uznání | <p>Určete, zda jsou poukázky uznání konsolidovány ve výchozím nastavení:</p><ul><li>**Ano** – Vytvořte jednu poukázku pro všechny řádky rozpoznávání, které mají stejné datum. Všechny řádky v poukazu, které mají stejný účet, jsou sloučeny do jednoho řádku.</li><li>**Ne** – Vytvořte voucher pro každý řádek rozpoznání.</li></ul><p>Toto nastavení můžete aktualizovat na stránce **Zpracování uznání**.</p> |
| Výchozí název deníku | Vyberte název deníku pro deníky, které jsou vytvořeny z procesů odložení výnosů a výdajů, jako je zpracování uznání. |
| Uznání popisu řádku deníku | <p>Vyberte popis, který se objeví v popisu řádku dokladu deníku:</p><ul><li>**Data řádků plánu** – Zobrazte data řádků plánu v popisu řádku deníku.</li><li>**Podrobnosti původní transakce** – Zobrazit informace o původní transakci v popisu řádku deníku.<p>**Příklad:** USMF-0001, CIV-00839, výnosy ze softwaru</p></li></ul> |
| Karta **Číselné řady** | Tato záložka slouží k nastavení výchozích hodnot pro číselné řady leasingu. Průvodce generováním číselné řady se používá k automatickému generování a přiřazování číselných řad. Číselnou řadu nemusíte měnit, pokud nechcete provádět ruční změny vygenerovaných číselných řad. |
| Číslo plánu | Číselná řada, která se používá pro plány odložení. |

## <a name="deferral-templates"></a>Šablony odkladu

Použijte stránku **Šablony odkladu** k definování přímých šablon, které se používají pro plány odkladu.

Zde jsou některé z výhod použití šablony:

* Délka odkladu se vypočítá automaticky.
* Povolíte plány odložení, které mají období, kdy je rozpoznání přeskočeno.
* Odložení můžete automatizovat přiřazením šablony k produktu, skupině produktů, kategorii produktů, zákazníkům nebo skupině zákazníků. Přiřazení šablony se provádí ze stránky **Výchozí hodnoty odkladu**.

Pro šablony je k dispozici několik frekvencí období: denní, měsíční nebo fiskální období.

Řádky šablony se skládají z typu (**Uznáno** nebo **Přeskočeno**) a délky období. Vynechané řádky mají na řádcích odloženého plánu hodnotu 0 (nula). Toto chování může být užitečné, pokud nechcete uznat výnosy ve všech obdobích.

### <a name="create-a-deferral-template"></a>Vytvoření šablony odkladu

Při vytváření šablony odkladu postupujte takto.

1. Na stránce **Šablony odkladu** zvolte **Nová**.
2. Do pole **Šablona** zadejte název.
3. Zadejte popis do pole **Popis**.
4. V poli **Frekvence období** vyberte frekvenci období.
5. Vyberte **Přidat**, chcete-li přidat řádek na začátek seznamu řádků, nebo vyberte **Připojit** pro přidání řádku na konec seznamu.
6. V poli **Typ** vyberte typ období.
7. V poli **Délka období** zadejte délku období.
8. Opakujte kroky 5 až 7 pro každý další řádek, který požadujete.
9. Zvolte možnost **Uložit**.

## <a name="deferral-defaults"></a>Výchozí hodnoty odkladu

Použijte stránku **Výchozí hodnoty odkladu** k nastavení výchozích účtů pro odložení pro položky a přiřazení výchozích šablon k odloženým položkám. Můžete také nastavit účty odkladu pro poplatky a přiřadit šablony poplatkům příštího období.

**Odložit podle položky**

U transakcí, které mají položku (například prodejní objednávky), můžete přiřadit účty a šablony konkrétním položkám a zákazníkům. Tato nastavení budou použita jako výchozí hodnoty při odložení transakce. Aby byla transakce ve výchozím nastavení odložená, musíte nastavit položky na stránce **Odložitelné položky**.

**Odložit podle účtu**

Pro transakce, které nemají položky (například obecné deníky), můžete zadat účty odložení. Při použití těchto účtů na transakčním řádku je transakce automaticky označena jako odložená. Odpovídající šablona a rozpoznávací účet budou přiřazeny k transakční řadě.

**Všechny typy transakcí (například na kartách Prodejní objednávka, Nákup a Obecný deník)**

Účty na stránce jsou hlavní účty, které nemají finanční dimenze. Finanční dimenze účtu uznání pocházejí od zákazníka nebo položky na základě vaší organizace.

Každý řádek šablony musí mít buď přímou šablonu, nebo šablonu založenou na události. Nemůže mít obojí.

### <a name="for-sales-orders"></a>Pro prodejní objednávky

Chcete-li zadat výchozí hodnoty odložení pro prodejní objednávky, postupujte takto.

1. Na kartě **Prodejní objednávka** vyberte typ odložení.
2. Chcete-li přidat řádek, vyberte **Přidat řádek**.
3. V poli **Kód položky** vyberte kód položky. Kód položky určuje, jak se použijí výchozí hodnoty odložení.
4. Zadejte, jak se použije kód položky:

    * Pokud je pole **Kód položky** nastaveno na **Tabulku** nebo **Skupinu**, vyberte vztah položky v poli **Vztah položky**.
    * Pokud jste vybrali **Kategorie** v poli **Kód položky**, v poli **Vztah položky** vyberte vztah položky.
    * Pokud je pole **Kód položky** nastaveno na **Všechny**, výchozí hodnoty platí pro všechny příslušné záznamy.

5. Zadejte, jak se použije kód účtu:

    * Pokud je pole **Kód účtu** nastaveno na **Tabulku** nebo **Skupinu**, vyberte vztah účtů v poli **Vztah účtů**.
    * Pokud je pole **Kód účtu** nastaveno na **Všechny**, účet platí pro všechny záznamy.

6. V poli **Hlavní účet** vyberte hlavní účet pro odklad.
7. Pokud je pole **Metoda zaúčtování odkladu** nastaveno na **Zisk a ztráta**, vyberte počáteční příjmový účet v poli **Účet počátečních příjmů** a účet kompenzace výnosů v poli **Protiúčet příjmů**.
8. Pokud je pole **Metoda krátkodobého odkladu** nastaveno na **Klouzavá období** nebo **Pevný rok**, vyberte účet krátkodobého odkladu v poli **Účet krátkodobého odkladu**.
9. U šablony můžete vybrat **Přidat** a přidat řádek.
10. V poli **Kód položky** vyberte kód položky.
11. Zadejte, jak se použije kód položky:

    * Pokud je pole **Kód položky** nastaveno na **Tabulku** nebo **Skupinu**, vyberte vztah položky v poli **Vztah položky**.
    * Pokud jste vybrali **Kategorie** v poli **Kód položky**, v poli **Vztah položky** vyberte vztah položky.
    * Pokud je pole **Kód položky** nastaveno na **Všechny**, výchozí hodnoty platí pro všechny příslušné záznamy.

12. Zadejte, jak se použije kód účtu:

    * Pokud je pole **Kód účtu** nastaveno na **Tabulku** nebo **Skupinu**, vyberte vztah účtů v poli **Vztah účtů**.
    * Pokud je pole **Kód účtu** nastaveno na **Všechny**, účet platí pro všechny příslušné záznamy.
    * Vyberte šablonu rovné čáry v poli **Šablona rovné čáry** nebo šablonu založenou na události v poli **Šablona založená na události**.

13. Zvolte možnost **Uložit**.

### <a name="for-purchase-orders"></a>Pro nákupní objednávky

Chcete-li zadat výchozí hodnoty odložení pro nákupní objednávky, postupujte takto.

1. Na kartě **Nákup** vyberte typ odložení.
2. Chcete-li přidat řádek, vyberte **Přidat řádek**.
3. V poli **Kód položky** vyberte kód položky.
4. Zadejte, jak se použije kód položky:

    * Pokud je pole **Kód položky** nastaveno na **Tabulku** nebo **Skupinu**, vyberte vztah položky v poli **Vztah položky**.
    * Pokud jste vybrali **Kategorie** v poli **Kód položky**, v poli **Vztah položky** vyberte vztah položky.
    * Pokud je pole **Kód položky** nastaveno na **Všechny**, výchozí hodnoty platí pro všechny příslušné záznamy.

5. Zadejte, jak se použije kód účtu:

    * Pokud je pole **Kód účtu** nastaveno na **Tabulku** nebo **Skupinu**, vyberte vztah účtů v poli **Vztah účtů**.
    * Pokud je pole **Kód účtu** nastaveno na **Všechny**, účet platí pro všechny příslušné záznamy.

6. V poli **Hlavní účet** vyberte hlavní účet pro odklad.
7. Pokud je pole **Metoda zaúčtování odkladu** nastaveno na **Zisk a ztráta**, vyberte počáteční příjmový účet v poli **Účet počátečních příjmů** a účet kompenzace výnosů v poli **Protiúčet příjmů**.
8. Pokud je pole **Metoda krátkodobého odkladu** nastaveno na **Klouzavá období** nebo **Pevný rok**, vyberte účet krátkodobého odkladu v poli **Účet krátkodobého odkladu**.
9. U šablony vyberte **Přidat** a přidejte řádek. 
10. V poli **Kód položky** vyberte kód položky.
11. Zadejte, jak se použije kód položky:

    * Pokud je pole **Kód položky** nastaveno na **Tabulku** nebo **Skupinu**, vyberte vztah položky v poli **Vztah položky**.
    * Pokud jste vybrali **Kategorie** v poli **Kód položky**, v poli **Vztah položky** vyberte vztah položky.
    * Pokud je pole **Kód položky** nastaveno na **Všechny**, výchozí hodnoty platí pro všechny příslušné záznamy.

12. Zadejte, jak se použije kód účtu:

    * Pokud je pole **Kód účtu** nastaveno na **Tabulku** nebo **Skupinu**, vyberte vztah účtů v poli **Vztah účtů**.
    * Pokud je pole **Kód účtu** nastaveno na **Všechny**, účet platí pro všechny příslušné záznamy.
    * Vyberte šablonu rovné čáry v poli **Šablona rovné čáry** nebo šablonu založenou na události v poli **Šablona založená na události**.

13. Zvolte možnost **Uložit**.

### <a name="for-general-journals"></a>U hlavních deníků

Chcete-li zadat výchozí hodnoty odložení pro položky hlavního deníku, postupujte takto.

1. Zvolte kartu **Hlavní deník**.
2. Pro odklad vyberte **Přidat** a přidejte řádek.
3. Pokud je pole **Metoda krátkodobého odkladu** nastaveno na **Klouzavá období** nebo **Pevný rok**, vyberte účet krátkodobého odkladu v poli **Účet krátkodobého odkladu**.
4. V poli **Účet odkladu** vyberte účet odkladu.
5. V poli **Účet uznání** vyberte účet uznání.
6. Pokud je pole **Metoda zaúčtování odkladu** nastaveno na **Zisk a ztráta**, vyberte počáteční příjmový účet v poli **Účet počátečních příjmů** a účet kompenzace výnosů v poli **Protiúčet příjmů**.
7. Vyberte šablonu rovné čáry v poli **Šablona rovné čáry** nebo šablonu založenou na události v poli **Šablona založená na události**.
8. Zvolte možnost **Uložit**.

### <a name="for-free-text-invoices"></a>Pro volné faktury

Chcete-li zadat výchozí hodnoty odložení pro volné faktury, postupujte takto.

1. Vyberte kartu **Volná faktura**.
2. Pro odklad vyberte **Přidat** a přidejte řádek.
3. Zadejte, jak se použije kód účtu:

    * Pokud je pole **Kód účtu** nastaveno na **Tabulku** nebo **Skupinu**, vyberte vztah účtů v poli **Vztah účtů**.
    * Pokud je pole **Kód účtu** nastaveno na **Všechny**, kód účtu platí pro všechny příslušné záznamy.

4. V poli **Účet odkladu** vyberte účet odkladu.
5. Pokud je pole **Metoda krátkodobého odkladu** nastaveno na **Klouzavá období** nebo **Pevný rok**, vyberte účet krátkodobého odkladu v poli **Účet krátkodobého odkladu**.
6. V poli **Účet uznání** vyberte účet uznání.
7. Pokud je pole **Metoda zaúčtování odkladu** nastaveno na **Zisk a ztráta**, vyberte počáteční příjmový účet v poli **Účet počátečních příjmů** a účet kompenzace výnosů v poli **Protiúčet příjmů**.
8. Vyberte šablonu rovné čáry v poli **Šablona rovné čáry** nebo šablonu založenou na události v poli **Šablona založená na události**.
9. Zvolte možnost **Uložit**.

### <a name="for-invoice-journals"></a>Pro deníky faktur

Chcete-li zadat výchozí hodnoty odložení pro položky deníku faktur, postupujte takto.

1. Zvolte kartu **Deník faktur**.
2. Pro odklad vyberte **Přidat** a přidejte řádek.
3. Zadejte, jak se použije kód účtu:

    * Pokud je pole **Kód účtu** nastaveno na **Tabulku** nebo **Skupinu**, vyberte vztah účtů v poli **Vztah účtů**.
    * Pokud je pole **Kód účtu** nastaveno na **Všechny**, kód účtu platí pro všechny příslušné záznamy.

4. V poli **Účet odkladu** vyberte účet odkladu.
5. Pokud je pole **Metoda krátkodobého odkladu** nastaveno na **Klouzavá období** nebo **Pevný rok**, vyberte účet krátkodobého odkladu v poli **Účet krátkodobého odkladu**.
6. V poli **Účet uznání** vyberte účet uznání.
7. Pokud je pole **Metoda zaúčtování odkladu** nastaveno na **Zisk a ztráta**, vyberte počáteční příjmový účet v poli **Účet počátečních příjmů** a účet kompenzace výnosů v poli **Protiúčet příjmů**.
8. Vyberte šablonu rovné čáry v poli **Šablona rovné čáry** nebo šablonu založenou na události v poli **Šablona založená na události**.
9. Zvolte možnost **Uložit**.

### <a name="items-that-are-deferred-by-default"></a>Položky, které jsou ve výchozím nastavení odložené

Použijte stránku **Položky jsou ve výchozím nastavení odložené** a definujte, které položky jsou ve výchozím nastavení odloženy. Můžete nastavit typy transakcí, u kterých budou položky odloženy. Můžete určit, zda bude odložena jedna položka nebo celá skupina položek nebo kategorie.

Když nastavíte položky jako odložené, vyberte výchozí účty a šablony na stránce **Výchozí hodnoty odkladu**. Pokud nejsou vybrány účty a šablony, transakční řádky, kde jsou tyto položky zadány, nebudou odloženy.

U položek, které jsou odloženy na základě kategorie prodeje nebo nákupu, ke které jsou přidruženy, jsou nastavení odložení založena na kategorii. Pokud však kategorie není vybrána v poli **Vztah kategorie**, použijí se nastavení odložení kategorie, která má vyšší pořadí. Například přidáte kategorii prodeje **Domácí video**, ale ne kategorii prodeje **Televize**. Když přidáte odloženou položku, která je spojena s kategorií **Televize**, nastavení odložení **Domácí video** se používají pro položku.

### <a name="set-up-deferred-items"></a>Nastavit odložené položky

Chcete-li nastavit položky, které jsou ve výchozím nastavení odložené, postupujte takto.

1. Na stránce **Položky jsou ve výchozím nastavení odložené** vyberte kartu, kterou chcete: **Prodejní objednávka** nebo **Nákup**.
2. Chcete-li přidat řádek, vyberte **Přidat řádek**.
3. V poli **Kód položky** vyberte kód položky.
4. Zadejte, jak se použije kód položky:

    * Pokud je pole **Kód položky** nastaveno na **Skupinu** nebo **Tabulku**, vyberte vztah položky v poli **Vztah položky**.
    * Pokud jste vybrali **Kategorie** v poli **Kód položky**, v poli **Vztah položky** vyberte vztah položky.

5. Opakujte kroky 2 až 4 pro každý další řádek, který požadujete.
6. Zvolte možnost **Uložit**.

## <a name="deferred-charges"></a>Odložené poplatky

Použijte stránku **Poplatky za odklad** pro definici, které poplatky jsou ve výchozím nastavení odloženy.

> [!NOTE]
> * V současné době jsou odložené poplatky dostupné pouze pro prodejní objednávky.
> * Poplatky lze odložit pouze na úrovni řádku. Chcete-li odložit poplatek na úrovni záhlaví prodejní objednávky, můžete nastavit platbu jako odloženou položku na samostatném řádku na prodejní objednávce.
> * Chcete-li odložit poplatek za fakturu s volným textem, musíte poplatek zadat jako samostatný řádek odložené faktury.
> * Tato funkce není k dispozici pro poplatky za podporu a funkci rozdělení příjmů.

### <a name="set-up-deferred-charges"></a>Nastavení odložených poplatků

Chcete-li nastavit odložené poplatky, postupujte následujícím způsobem.

1. Na stránce **Odložené poplatky** vyberte **Přidat** a přidejte řádek.
2. V poli **Kód poplatku** vyberte kód poplatku
3. V poli **Vztah poplatku** vyberte vztah poplatku
4. Opakujte kroky 1 až 3 pro každý další řádek, který požadujete.
5. Zvolte možnost **Uložit**.

## <a name="event-based-deferral-templates"></a>Šablony odkladu založené na událostech

Použijte stránku **Šablony odkladu založené na událostech**, chcete-li definovat šablony odkladu založené na událostech, které můžete použít v transakcích odložení a přiřadit je na stránce **Výchozí hodnoty odkladu**.

### <a name="create-an-event-based-template"></a>Vytvořte šablonu založenou na události

Při vytváření šablony založené na události postupujte takto.

1. Na stránce **Šablony odkladu založené na události** zvolte **Nová**.
2. Do pole **Šablona** zadejte jedinečný název šablony.
3. Zadejte popis do pole **Popis**.
4. V poli **Typ přiřazení** vyberte typ přiřazení.

    * **Variabilní částka** – Přidělte konkrétní částku pro každý zadaný řádek.
    * **Stejnéá částka** – Přidělte stejnou částku pro každý zadaný řádek. 
    * **Procento** – Přidělte částku, která je založena na procentuální hodnotě zadané pro každý řádek.
    * **Procento dokončení** – Pro každý vložený řádek přiřaďte kumulativní hodnotu dokončení.
    * **Variabilní množství** – Přidělte konkrétní množství pro každý zadaný řádek.

5. Nastavte možnost **Vytvořte samostatné události pro každou jednotku** na **Ano**, pokud chcete, aby byl každý řádek události rozdělen rovnoměrně podle počtu jednotek na fakturační transakci. Nastavte ji na **Ne**, pokud nechcete rozdělit řádky událostí.
6. V poli **Účet expirace** vyberte účet expirace.
7. Vyberte **Přidat**, chcete-li přidat řádek na začátek seznamu řádků, nebo vyberte **Připojit** pro přidání řádku na konec seznamu.
8. Do pole **Popis** zadejte popis události.
9. Pokud je pole **Typ přiřazení** nastaveno na **Procento**, zadejte v poli **Procento přiřazení** procento přidělení pro každý řádek. Procento musí být mezi 0 (nula) a 100. Pokud necháte pole **Procento přidělení** prázdné, procento se považuje za 0. Součet všech procent se zobrazí v poli **Celkové procento** ve spodní části stránky a musí se rovnat 100.
10. V poli **Měsíce do vypršení platnosti** zadejte počet měsíců, po které je událost platná. Na základě této hodnoty se automaticky zadává datum vypršení platnosti odkladu transakce.
11. Vyberte zaškrtávací políčko **Rozpoznat při zaúčtování** pro automatické rozpoznání výnosů při zaúčtování transakce. Pokud necháte zaškrtávací políčko nezaškrtnuté, musí být výnos rozpoznán ručně.
12. V poli **Účet pro uznání** vyberte účet uznání pro událost, pokud událost používá jiný účet než celý plán odkladu. Toto pole se používá společně se zaškrtávacím políčkem **Rozpoznat při zaúčtování**.
13. Opakujte kroky 7 až 12 pro každý další řádek, který požadujete.
14. Zvolte možnost **Uložit**.
