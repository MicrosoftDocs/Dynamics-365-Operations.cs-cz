---
title: Pravidla eliminace
description: "Toto téma obsahuje informace o pravidla eliminace a různé možnosti pro vytváření zpráv o vyloučení."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: db4b05bc55d735513d7580ca5908a1e84eb760c6
ms.openlocfilehash: 152b63fdfc78b3c4e79b93340d18c5cf69257024
ms.lasthandoff: 03/31/2017


---

# <a name="elimination-rules"></a>Pravidla eliminace

[!include[banner](../includes/banner.md)]


Toto téma obsahuje informace o pravidla eliminace a různé možnosti pro vytváření zpráv o vyloučení.

Transakce eliminací se používají v případech, kdy nadřazená právnická osoba obchoduje s některými dceřinými právnickými osobami a přitom je používáno konsolidované finanční vykazování. Konsolidované finanční výkazy musí zahrnovat pouze transakce, které probíhají mezi konsolidovanou organizací a dalšími entitami mimo dané organizace. Transakce mezi právnickými osobami, které jsou součástí stejné organizace musí být proto odstraněny, nebo odstraněna z hlavní knihy, neobjeví se na finanční sestavy. Existuje několik způsobů, jak vykázat eliminace:

-   Pravidlo eliminace lze vytvořit a zpracovat v konsolidaci nebo eliminaci společnosti.
-   Finanční sestavy slouží k zobrazení účtů a dimenzí eliminací u konkrétního řádku nebo sloupce.
-   Samostatnou právnickou osobu lze použít k zaúčtování položek transakce ke sledování eliminací.

Toto téma se zaměřuje na pravidla eliminace, která jsou zpracována ve společnosti konsolidace nebo eliminace. Můžete konfigurovat pravidla eliminace pro vytvoření transakcí eliminace u právnické osoby, která je určena jako cílová právnická osoba pro eliminace. Tato cílová právnická osoba se také nazývá právnická osoba eliminace. Deníky eliminace lze vygenerovat během procesu konsolidací nebo pomocí návrhu deníku eliminace. Před nastavením pravidel eliminace se doporučuje důkladné obeznámení s následujícími termíny:

-   **Zdrojová právnická osoba** – právnická osoba, pro kterou byly zaúčtovány částky, které jsou právě eliminovány.
-   **Cílová právnická osoba** - právnická osoba, pro kterou jsou zaúčtována pravidla eliminace.
-   **Právnická osoba eliminace** - právnická osoba určená jako cílová právnická osoba pro eliminace.
-   **Konsolidační právnická osoba** - právnická osoba vytvořená s cílem vykazování finančních výsledků pro určitou skupinu právnických osob. K této právnické osoby jsou konsolidována finanční data z daných právnických osob a poté je na základě kombinovaných dat vytvořena finanční sestava.

V následující tabulce jsou uvedeny typy transakcí, které mohou mít eliminace.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Typ transakce</th>
<th>Příklad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Zadání a fakturace prodejní objednávky (centralizované zpracování)</td>
<td>Prodej produktu odběrateli v zastoupení jiné právnické osoby ve vaší organizaci.</td>
</tr>
<tr class="even">
<td>Zadání prodejní objednávky (mezi společnostmi/v rámci jedné společnosti) a fakturace</td>
<td>Prodej produktů mezi právnickými osobami ve vaší organizaci.</td>
</tr>
<tr class="odd">
<td>Nákupní objednávky (centralizované zpracování)</td>
<td>Nákup skladových zásob, materiálu, služeb, dlouhodobého majetku a dalších produktů od dodavatele v zastoupení jiné právnické osoby ve vaší organizaci.</td>
</tr>
<tr class="even">
<td>Řízení zásob (mezi různými společnostmi/v rámci jedné společnosti)</td>
<td><ul>
<li>Převod zásob jedné právnické osoby na dlouhodobý majetek jiné právnické osoby ve vaší organizaci.</li>
<li>Převod zásob jedné právnické osoby na zásoby jiné právnické osoby ve vaší organizaci.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Sledování zásob během tranzitu</td>
<td>Převod položek mezi sklady stejné právnické osoby, která se ale nachází na různých místech.</td>
</tr>
<tr class="even">
<td>Centralizované zpracování faktur s ohledem na závazky</td>
<td>Zaznamenání faktury v zastoupení jiné právnické osoby ve vaší organizaci.</td>
</tr>
<tr class="odd">
<td>Centralizované zpracování plateb s ohledem na závazky</td>
<td>Zaplacení faktury v zastoupení jiné právnické osoby ve vaší organizaci.</td>
</tr>
<tr class="even">
<td>Řízení hotovosti a pokladna (centralizované zpracování)</td>
<td><ul>
<li>Zpracování plateb daní, refundací daní, účtování úroků, půjček, záloh, vyplácení dividend a předem placených honorářů nebo provizí.</li>
<li>Zaplacení výdajů v zastoupení jiné právnické osoby ve vaší organizaci. Faktura je zadána do knihy cílové právnické osoby a je nutné zajistit kombinované vyrovnání mezi právnickými osobami. Například jedna právnická osoba zaplatí výdaje vyúčtované zaměstnanci u jiné právnické osoby. V tomto případě vyúčtování výdajů zaměstnanci bude obsahovat výdaje, které se vztahují k jiné právnické osobě.</li>
<li>Převod hotovosti od jedné právnické osoby jiné v rámci organizace.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pohledávky (centralizované zpracování)</td>
<td>Příjem hotovosti za odběratelskou fakturu jiné právnické osoby a uložení šeku na bankovní účet této právnické osoby.</td>
</tr>
<tr class="even">
<td>Mzdy (centralizované zpracování, mezipodnikové/vnitropodnikové)</td>
<td><ul>
<li>Platba mezd jiné právnické osoby. Právnická osoba může například vyplácet vlastní mzdy svým zaměstnancům, avšak nechá si v rámci zpracování mezd proplatit práci, kterou daný zaměstnanec vykonal pro jinou právnickou osobu. Případně určitý zaměstnanec pracoval na půl úvazku pro právnickou osobu A a na půl úvazku pro právnickou osobu B – výhody se vztahují na celou mzdu. V takovém případě zahrnuje mzda zaměstnance platbu od obou právnických osob. Nejsou zaúčtovány pouze vlastní platy, ale také daně, výhody (benefity), srážky a časové rozlišení platů.</li>
<li>Převody pracovních smluv z jednoho oddělení (divize) do jiného oddělení (divize).</li>
</ul></td>
</tr>
<tr class="odd">
<td>Dlouhodobý majetek (mezipodnikový/vnitropodnikový)</td>
<td>Převod dlouhodobého majetku na dlouhodobý majetek nebo zásoby jiné právnické osoby.</td>
</tr>
<tr class="even">
<td>Alokace (mezipodnikové/vnitropodnikové)</td>
<td>Zpracování podnikových přidělení. Přidělení jsou aktivity prováděné pro libovolný přidělený účet, bez ohledu na zdrojový modul.</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Příklad
Vaše právnická osoba, právnická osoba A prodává určité produkty jiné právnické osobě ve vaší organizaci, právnické osobě B. Následující příklad ukazuje, jak lze eliminovat transakce mezi dvěma právnickými osobami:

-   Právnická osoba A prodá produkt v ceně 10,00 jednotek právnické osobě B za cenu 10,00 jednotek.
-   Právnická osoba A prodává produkt v ceně 10,00 jednotek právnické osobě B za 10,00 jednotek plus 2,00 jednotky jako náklady na dopravu.
-   Právnická osoba A prodává produkt v ceně 10,00 jednotek právnické osobě B za cenu 15,00 jednotek a nárokuje si marži z prodeje.
-   Právnická osoba A prodává produkt v ceně 10,00 jednotek právnické osobě B za cenu 15,00 jednotek a nárokuje si polovinu marže z prodeje. Právnická osoba B si nárokuje druhou polovinu marže z prodeje. Proto je výnos rozdělen. Rozdělení výnosů přináší motivaci pro objednávku od jiné právnické osoby v rámci organizace namísto objednávky od externí organizace.

Všechny tyto operace vedou k tomu, že vnitropodnikové transakce jsou zaúčtovávány na debetní a kreditní účty. Kromě toho mohou tyto transakce zahrnovat částky přirážek nebo srážek, zejména pokud výše vnitropodnikových prodejů neodpovídá nákladům na prodané zboží.

## <a name="set-up-elimination-rules"></a>Nastavení pravidel eliminace
Při nastavování pravidla eliminace v 365 Dynamics pro operace, doporučujeme vytvoření finanční dimenze pro účely vyloučení. Většina zákazníků název obchodního partnera nebo něco podobného. Pokud se rozhodnete použít finanční dimenze, pak je nutné mít hlavní účty, které jsou specifické pro pouze mezipodnikové transakce. 

Nastavení pro vyloučení naleznete v části Nastavení modul konsolidace. Jakmile zadáte popis pravidla, je třeba vybrat společnost, která bude účtovat v deníku eliminace. To by mělo být ve společnosti, která má **použít pro proces finanční eliminace** v nastavení právního subjektu vybrána. 

Datum lze nastavit v platnosti pravidlo eliminace a kdy jeho platnost vypršela, v případě potřeby. Je nutné nastavit **Active** k **Ano** Pokud chcete, aby byla k dispozici v návrhu procesu eliminace. Vyberte název deníku, který má typ **eliminace**.

Po definování základy skutečné zpracování pravidel můžete definovat klepnutím na **řádky**. Existují dvě možnosti pro eliminace odstranění částka pohybu nebo definování pevnou částku. 

Vyberte zdrojový účet. Můžete použít hvězdičku (\*) jako zástupný. Například 1\* by vyberte všechny účty, které začínají 1 jako zdroj dat pro přidělení. 

Po výběru zdrojových účtů, **specifikace účtu** Určuje účet z cílové společnosti, která je použita. Vyberte **zdroje** Pokud chcete použít stejnou hlavní účet definovaný v **zdroje** účet. Vyberete-li **uživatelem definované**, pak je nutné zadat cílový účet. 

Specifikace dimenze funguje stejným způsobem. Vyberete-li **zdroje**, v cílové společnosti jako zdrojová společnost bude používat stejné dimenze. Vyberete-li **uživatelem definované**, je třeba určit rozměry v cílové společnosti klepnutím **cílové dimenze** položky nabídky. 

Vyberte zdrojové dimenze a finanční dimenze a hodnoty, které slouží jako zdroj eliminace.

## <a name="process-elimination-transactions"></a>Zpracování eliminační transakce
Dvěma způsoby pro zpracování transakcí eliminace, během procesu online konsolidovat nebo vytvořením deníku eliminace a návrh procesu eliminace. Tato část se zaměřuje na vytváření deníku a spuštění procesu eliminace. 

Ve společnosti rozumí společnost odstranění, vyberte **deníku eliminace** modul konsolidace. Po výběru názvu deníku, klepněte na tlačítko **řádky**. Návrh lze spustit výběrem **návrhy** nabídky a potom výběrem **návrh eliminace**.

Vyberte společnost, která je zdrojem sloučená data a pak vyberte pravidlo, které chcete zpracovat. ENTER zahájíte hledání pro odstranění částky počáteční datum a koncové datum ukončení hledání datum pro odstranění částky. **Datum zaúčtování do hlavní knihy** pole je datum pro zaúčtování deníku do hlavní knihy. Po klepnutí na tlačítko **OK**, můžete zkontrolovat množství a zaúčtujte deník.




