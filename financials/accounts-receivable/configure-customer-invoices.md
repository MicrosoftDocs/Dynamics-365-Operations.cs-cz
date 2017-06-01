---
title: "Vytvoření faktury odběratele"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: fd89921a97782c4d09807a730ab077809304159f
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="create-a-customer-invoice"></a>Vytvoření faktury odběratele

[!include[banner](../includes/banner.md)]




**Faktura odběratele pro prodejní objednávku** je účet, který se vztahuje k prodeji a který organizace předává odběrateli. Tento typ faktury odběratele se vytváří na základě prodejní objednávky, která zahrnuje řádky objednávky a čísla položek. Čísla položek jsou specifikována a zaúčtována v hlavní knize. Položky dílčího hlavního deníku nejsou k dispozici pro fakturu odběratele pro prodejní objednávku. 

**Faktura s volným textem** nesouvisí s prodejní objednávkou. Obsahuje řádky objednávky zahrnující účty hlavní knihy, textové popisy a vámi zadanou částku prodeje. Číslo položky nelze u tohoto druhu faktury zadat. Je však nutné zadat příslušné informace o DPH. Hlavní účet pro prodej je uveden na každém řádku faktury, který můžete rozdělit do několika účtů hlavní knihy kliknutím na možnost **Distribuovat částky** na stránce **Volná faktura**. Zůstatek odběratele je navíc zaúčtovány do souhrnného účtu z účetního profil, který se používá pro volnou fakturu.

**Proforma faktura** je faktura připravená jako odhad skutečných částek faktury před zaúčtováním faktury. Proforma fakturu lze vytisknout buď pro fakturu odběratele pro prodejní objednávku, nebo pro volnou fakturu.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>Zaúčtování a tisk jednotlivých faktur odběratele založených na prodejních objednávkách
Pomocí tohoto procesu můžete vytvořit fakturu založenou na prodejní objednávce. Můžete tak učinit, pokud chcete odeslat fakturu odběrateli před dodáním zboží nebo služeb. 

Při zaúčtování faktury je množství v poli **Zůstatek faktury** u každé položky aktualizováno celkovým fakturovaným množstvím z vybrané prodejní objednávky. Pokud bude množství **Zůstatek faktury** i množství **Zbývá dodat** pro všechny položky na prodejní objednávce nulové (0), stav prodejní objednávky se změní na hodnotu **Fakturováno**. Pokud množství v poli **Zůstatek faktury** není nulové (0), stav prodejní objednávky se nezmění a k této objednávce je možné zadat další faktury.

Na stránce se seznamem **Všechny prodejní objednávky** si můžete zobrazit stav prodejních objednávek. Na stránce se seznamem **Otevřené faktury odběratele** si můžete zobrazit faktury, které jste zaúčtovali.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>Zaúčtování a tisk jednotlivých faktur odběratele založených na dodacích listech a datu
Tento proces použijte, když byl pro danou prodejní objednávku zaúčtován alespoň jeden dodací list. Faktura odběratele je založena na těchto dodacích listech a odráží na nich uvedená množství. Finanční údaje pro fakturu jsou založeny na údajích zadaných při zaúčtování faktury. 

Můžete vytvořit fakturu odběratele založenou na položkách řádku dodacího listu, které byly odeslány k určitému datu, a to i když všechny položky pro určitou prodejní objednávku nebyly dosud odeslány. To lze provést například v situaci, kdy daná právnická osoba vystavuje každému odběrateli jednu fakturu měsíčně, která zahrnuje všechny dodávky za daný měsíc. Každý dodací list odpovídá částečné nebo úplné dodávce položek na prodejní objednávce. 

Při zaúčtování faktury bude množství **Zůstatek faktury** pro každou položku aktualizováno o souhrn dodaných množství z vybraných dodacích listů. Pokud bude množství **Zůstatek faktury** i množství **Zbývá dodat** pro všechny položky na prodejní objednávce nulové (0), stav prodejní objednávky se změní na hodnotu **Fakturováno**. Pokud množství v poli **Zůstatek faktury** není nulové (0), stav prodejní objednávky se nezmění a k této objednávce je možné zadat další faktury. 

Skladové transakce budou aktualizovány číslem faktury a stav v poli **Stav řádku** na prodejní objednávce se změní na hodnotu **Fakturováno**. 

Na stránce se seznamem **Všechny prodejní objednávky** si můžete zobrazit stav prodejních objednávek.

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>Konsolidace prodejních objednávek nebo dodacích listů pro zaúčtování
Tento proces použijte, když jsou některé prodejní objednávky připraveny k fakturaci a vy je chcete sloučit do jedné faktury. 

Na stránce se seznamem **Prodejní objednávka** můžete vybrat více faktur a poté použít možnost **Generovat faktury** k jejich konsolidaci. Na stránce **Zaúčtování faktury** můžete změnit nastavení položky **Souhrnná objednávka** tak, aby bylo shrnutí provedeno podle čísla objednávky (pokud existuje více dodacích listů pro jednu prodejní objednávku) nebo podle účtu faktury (pokud existuje více prodejních objednávek pro jeden účet faktury). Tlačítkem **Uspořádat** konsolidujte prodejní objednávky do jedné faktury na základě nastavení v poli **Souhrnná objednávka**.

## <a name="additional-settings-that-change-the-posting-behavior"></a>Další nastavení, která mění chování zaúčtování
Následující pole mění chování procesu zaúčtování.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Pole</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Množství</td>
<td>Vyberte množství, na nichž chcete založit zaúčtování dokumentu. Dostupnost různých možností závisí na typu účtovaného dokumentu (například dodací list nebo faktura).
<ul>
<li><strong>Dodat nyní</strong> – výběr všech množství, která jsou zadána v poli <strong>Dodat nyní</strong>. Tato možnost se používá pro potvrzení nebo dodání částečné objednávky.</li>
<li><strong>Vyskladněno</strong> – výběr všech množství, která byla vyskladněna.</li>
<li><strong>Vše</strong> – výběr všech množství na prodejních objednávkách, která ještě nebyla aktualizována podle typu aktuálního dokumentu.</li>
<li><strong>Dodací list</strong> – výběr všech množství, která byla aktualizována podle dodacího listu.</li>
<li><strong>Vybráno množství a neskladované produkty</strong> – výběr všech množství, která byla vyskladněna, a všech množství produktu, která nejsou na skladě.</li>
</ul></td>
</tr>
<tr class="even">
<td>Zaúčtování</td>
<td><ul>
<li>Tuto možnost vyberte, chcete-li do deníku zapsat prodejní objednávky.</li>
<li>Zrušte výběr této možnosti pro tisk proformy prodejní objednávky. <strong>Poznámka:</strong> Pokud jste uzavřeli dohodu o platebním kalendáři, tento platební kalendář se na proforma prodejní objednávce nezobrazí. Platební kalendáře se zobrazí pouze na aktuálních prodejních objednávkách.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pozdější výběr</td>
<td>Výběrem této možnosti použijete vybraný dotaz později. Tato možnost se využívá pro dávkové úlohy. Dotaz se spustí při spuštění dávkové úlohy.</td>
</tr>
<tr class="even">
<td>Snížit množství</td>
<td>Tuto možnost vyberte, chcete-li automaticky snížit dodané množství při zaúčtování dokumentu tak, aby dodané množství se rovnalo dostupným zásobám.</td>
</tr>
<tr class="odd">
<td>Tisk</td>
<td>Vyberte, kdy chcete tisknout dokumenty:
<ul>
<li><strong>Aktuální</strong> – tisk dokumentů po aktualizaci každé faktury.</li>
<li><strong>Po</strong> – tisk dokumentů po aktualizaci všech faktur.</li>
</ul>
<strong>Poznámka</strong>: Pole <strong>Tisk</strong> je k dispozici jen tehdy, vyberete-li možnost <strong>Tisk faktury</strong>, <strong>Tisk potvrzení</strong>, <strong>Tisk výdejky</strong> nebo <strong>Tisk dodacího listu</strong>. Na stránce <strong>Třídění formuláře</strong> jste například nastavili, aby systém třídil informace podle účtu faktury. Poté můžete vybrat možnost <strong>Po</strong> a vytisknout dokumenty v dávce seřazené podle účtu faktury. V ostatních případech budou dokumenty tištěny před dokončením zpracování a nebudou uspořádány v pořadí, které je zadáno na stránce <strong>Třídění formuláře</strong>.</td>
</tr>
<tr class="even">
<td>Tisk faktury</td>
<td>Volbou této možnosti zapnete tisk faktury. Pokud je tato možnost vypnuta, můžete zaúčtovat fakturu bez tisku.</td>
</tr>
<tr class="odd">
<td>Odeslat e-mail</td>
<td>Tuto možnost vyberte, pokud chcete faktury pro prodejní objednávku po zaúčtování odeslat odběrateli jako přílohu e-mailu. Přílohy jsou odesílány jako soubory PDF a XML. Tato možnost je k dispozici pouze v případě, že jste na stránce <strong>Parametry elektronických faktur</strong> vybrali možnost <strong>Povolit CFD (elektronické faktury)</strong>. <strong>Poznámka:</strong> (MEX) Tento ovládací prvek je k dispozici pouze pro právnické osoby, jejichž primární adresa je v Mexiku.</td>
</tr>
<tr class="even">
<td>Použít cíl správy tisku</td>
<td>Tuto možnost vyberte, chcete-li použít nastavení tisku zadané na stránce <strong>Nastavení správy tisku</strong> pro transakce, dokument nebo modul.</td>
</tr>
<tr class="odd">
<td>Zkontrolovat limit úvěru</td>
<td>Vyberte informace, které se budou analyzovat při provádění kontroly limitu úvěru.
<ul>
<li><strong>Žádný</strong> – nejsou požadavky na kontrolu limitu úvěru.</li>
<li><strong>Zůstatek</strong> – limit úvěru se kontroluje vůči zůstatku odběratele.</li>
<li><strong>Zůstatek + dodací list nebo příjemka produktu</strong> – limit úvěru se kontroluje vůči zůstatku odběratele a dodávkám.</li>
<li><strong>Zůstatek + vše</strong> – limit úvěru se kontroluje vůči zůstatku odběratele, dodávkám a otevřeným objednávkám.</li>
</ul></td>
</tr>
<tr class="even">
<td>Úvěrové vyrovnání</td>
<td>Chcete-li v transakcích dokladu dobropis zobrazit jako MD, vyberte tuto možnost.</td>
</tr>
<tr class="odd">
<td>Kreditovat zbývající množství</td>
<td>Pokud účtujete dobropis, výběrem této možnosti ponecháte zbývající množství na objednávce. Pokud je zrušen výběr této možnosti, bude zbývající množství nastaveno na hodnotu 0 (nula).</td>
</tr>
<tr class="even">
<td>Souhrnná aktualizace pro</td>
<td>Vyberte, jak má být shrnuto více prodejních objednávek:
<ul>
<li><strong>Žádný</strong> – nedělat souhrn prodejních objednávek. Pro každou prodejní objednávku bude například vytvořena samostatná faktura.</li>
<li><strong>Účet faktury</strong> – vytvořit souhrn všech vybraných objednávek podle kritérií nastavených na stránce <strong>Parametry souhrnné aktualizace</strong>.</li>
<li><strong>Objednávka</strong> – sumarizovat vybraný rozsah objednávek do jedné objednávky, kterou zadáte. Vytvoří se souhrn objednávek podle kritérií nastavených na stránce <strong>Parametry souhrnné aktualizace</strong>. Je-li vybrána tato možnost, je nutné vybrat některou možnost v poli <strong>Prodejní objednávka</strong>.</li>
<li><strong>Automatické shrnutí</strong> – jestliže byly na stránce <strong>Parametry souhrnné aktualizace</strong> určeny všechny souhrnné aktualizace, vytvoří se souhrn všech vybraných objednávek na základě kritérií nastavených na stránce <strong>Parametry souhrnné aktualizace</strong>. Pokud nebyly souhrnné aktualizace určeny, objednávka se zaúčtuje samostatně.</li>
<li><strong>Dodací list</strong> – pro každý dodací list se vytvoří souhrn vybraného rozsahu objednávek do jedné faktury. Tato možnost je k dispozici jen tehdy, je-li v poli <strong>Množství</strong> vybrána možnost <strong>Dodací list</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>






