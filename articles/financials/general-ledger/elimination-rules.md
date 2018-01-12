---
title: Pravidla eliminace
description: "V tomto tématu jsou informace o pravidlech eliminace a různých možnostech pro vytváření sestav o eliminacích."
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 818572a8d1f790aaa7c6e4befc1d2222a1c35c50
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="elimination-rules"></a>Pravidla eliminace

[!include[banner](../includes/banner.md)]


V tomto tématu jsou informace o pravidlech eliminace a různých možnostech pro vytváření sestav o eliminacích.

Transakce eliminací se používají v případech, kdy nadřazená právnická osoba obchoduje s některými dceřinými právnickými osobami a přitom je používáno konsolidované finanční vykazování. Konsolidované finanční výkazy musí zahrnovat pouze transakce, které probíhají mezi konsolidovanou organizací a dalšími entitami mimo dané organizace. Transakce mezi právnickými osobami, které jsou součástí stejné organizace, je proto třeba odebrat nebo odstranit z hlavní knihy tak, aby se nezobrazily ve finančních výkazech. Existuje několik způsobů, jak vykázat eliminace:

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
Při nastavování pravidel eliminace v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition doporučujeme, abyste vytvořili finanční dimenzi konkrétně pro účely eliminace. Většina zákazníků jí nazývá obchodní partner nebo podobně. Pokud se rozhodnete nepoužít finanční dimenzi, pak je nutné mít hlavní účty, které jsou specifické pro pouze mezipodnikové transakce. 

Nastavení pro eliminace naleznete v části Nastavení modulu Konsolidace. Jakmile zadáte popis pravidla, je třeba vybrat společnost, do které bude deník eliminace účtovat. Mělo by se jednat o společnost, která má vybranou volbu **Použít pro proces finanční eliminace** v nastavení právnické osoby. 

Můžete nastavit datum, kdy se pravidlo eliminace stane platným, a v případě potřeby i datum jeho vypršení. Musíte nastavit volbu **Aktivní** na **Ano**, pokud chcete, aby byla k dispozici v procesu návrhu eliminace. Vyberte název deníku, který má typ **Eliminace**.

Po definování základů můžete určit skutečná pravidla zpracování kliknutím na možnost **Řádky**. Existují dvě možnosti pro eliminace - eliminace změny čisté částky nebo určení pevné částky. 

Vyberte svůj zdrojový účet. Jako zástupný znak můžete použít hvězdičku (\*). Například hodnota 1\* by zvolila jako zdroj dat pro přidělení všechny účty začínající číslem 1. 

Po výběru svých zdrojových účtů určí položka **Specifikace účtu** účet z cílové společnosti, která je použita. Vyberte **Zdroj**, pokud chcete použít stejný hlavní účet definovaný v účtu **Zdroj**. Vyberete-li možnost **Definováno uživatelem**, pak je nutné zadat cílový účet. 

Specifikace dimenze funguje stejným způsobem. Vyberete-li **Zdroj**, použijí se v cílové společnosti stejné dimenze jako ve zdrojové společnosti. Vyberete-li **Definováno uživatelem**, je třeba určit dimenze v cílové společnosti kliknutím na položku nabídky **Cílové dimenze**. 

Vyberte zdrojové dimenze, finanční dimenze a hodnoty, které slouží jako zdroj eliminace.

## <a name="process-elimination-transactions"></a>Zpracování eliminační transakce
Existují dva způsoby zpracování transakcí eliminace - během konsolidovaného online procesu nebo vytvořením deníku eliminace a spuštěním procesu návrhu eliminace. Tato část se zaměřuje na vytváření deníku a spuštění procesu eliminace. 

Ve společnosti určené jako společnost eliminace vyberte možnost **Deník eliminace** v modulu Konsolidace. Po vybrání názvu deníku klikněte na položku **Řádky**. Návrh lze spustit výběrem nabídky **Návrhy** a potom výběrem možnosti **Návrh eliminace**.

Vyberte společnost, která je zdrojem konsolidovaných dat, a pak vyberte pravidlo, které chcete zpracovat. Zadejte počáteční datum pro zahájení vyhledávání částek eliminace a koncové datum pro ukončení hledání data pro odstranění částky. Pole **Datum zaúčtování do hlavní knihy** představuje datum použité pro zaúčtování deníku do hlavní knihy. Po kliknutí na tlačítko **OK** můžete zkontrolovat částky a zaúčtovat deník.




