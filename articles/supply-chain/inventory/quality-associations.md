---
title: Přiřazení kvality
description: Toto téma popisuje, jak můžete použít přidružení kvality v Microsoft Dynamics 365 Supply Chain Management k automatickému generování objednávek kvality, které souvisejí s vašimi procesy prodeje, nákupu a výroby.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b0705af8f8c40db82e412f294f45f704b7a628c1ced679cef25ce77d49642feb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724837"
---
# <a name="quality-associations"></a>Přiřazení kvality

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak můžete použít přidružení kvality v Microsoft Dynamics 365 Supply Chain Management k automatickému generování objednávek kvality, které souvisejí s vašimi procesy prodeje, nákupu a výroby.

Přidružení kvality určuje pro vygenerovanou objednávku kvality tyto informace:

- Událost transakce
- Sada testů, které je nutné u položky vykonat
- Přijatelná úroveň kvality (AQL)
- Plán vzorkování

Přiřazení kvality je nutné definovat pro každou variantu obchodního procesu, který vyžaduje automatické generování objednávky kvality. Objednávky kvality lze generovat například v obchodních procesech pro nákupní objednávky, karanténní příkazy, prodejní objednávky a výrobní zakázky.

## <a name="working-with-quality-associations"></a>Práce s přidruženími kvality

Obchodní proces, který používá přidružení kvality, může být přiřazen k různým zdrojovým dokumentům, jako například k nákupním objednávkám, prodejním objednávkám nebo výrobním zakázkám.

Každý záznam o přidružení kvality určuje sadu testů, přijatelnou úroveň kvality a plán vzorkování, které platí pro vygenerované objednávky kvality. Je nutné definovat záznam o přidružení kvality pro každou variantu v obchodním procesu. Můžete například nastavit přidružení kvality, které vygeneruje objednávku kvality při aktualizaci příjemky produktu nákupní objednávky. V závislosti na nastavení plánu provádění může být samotný spouštěcí proces blokován, pokud existuje otevřená objednávka kvality. Můžete také blokovat následné procesy, jako je fakturace nákupní objednávky.

> [!NOTE]
> Pokud existují otevřené objednávky kvality, skladová množství jsou automaticky blokována před vydáním. V závislosti na nastavení pole **Úplné blokování** na stránce **Vzorkování položky** se množství rovná buď množství na objednávce kvality, nebo množství na řádku zdrojového dokumentu. Další informace viz [Vzorkování položek řízení jakosti](quality-item-sampling.md).

Pro určitý obchodní proces určuje záznam o přidružení kvality událost a podmínky, pro které je objednávka kvality generována. Podmínky mohou být specifické buď pro pracoviště, nebo pro právnickou osobu. Objednávku kvality, která zahrnuje destrukční testy, je možné generovat, jen když pro tuto událost existují zásoby.

Chcete-li pracovat s přidruženími kvality, přejděte na **Řízení zásob \> Založit \> Kontrola kvality \> Přidružení kvality**. Následující příklady ukazují způsob definování záznamu o přidružení kvality pro varianty každého obchodního procesu. Pro každý příklad jsou v následující tabulce shrnuty události a podmínky, kterou jsou definovány v záznamu o přidružení kvality.

<table>
<thead>
<tr>
<th>Typ odkazu</th>
<th>Typ události</th>
<th>Spuštění</th>
<th>Blokování události</th>
<th>Odkaz na dokument</th>
</tr>
</thead>
<tbody>
<tr>
<td>Zásoby</td>
<td>Nelze použít</td>
<td>Nelze použít</td>
<td>Žádné</td>
<td>Vše</td>
</tr>
<tr>
<td rowspan="7">Prodeje</td>
<td rowspan="4">Proces vyskladnění je naplánován.</td>
<td rowspan="4">Před</td>
<td>Žádné</td>
<td rowspan="22">Specifické ID, Skupina nebo Vše</td>
</tr>
<tr>
<td>Proces vyskladnění</td>
</tr>
<tr>
<td>Dodací list</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="3">Dodací list</td>
<td rowspan="3">Před</td>
<td>Žádné</td>
</tr>
<tr>
<td>Dodací list</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="15">Nákup</td>
<td rowspan="7">Příjemka</td>
<td rowspan="4">Před</td>
<td>Žádné</td>
</tr>
<tr>
<td>Příjemka</td>
</tr>
<tr>
<td>Příjemka produktu</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="3">Po</td>
<td>Žádné</td>
</tr>
<tr>
<td>Příjemka produktu</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="3">Registrace</td>
<td rowspan="3">Nelze použít</td>
<td>Žádné</td>
</tr>
<tr>
<td>Příjemka produktu</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="5">Příjemka produktu</td>
<td rowspan="3">Před</td>
<td>Žádné</td>
</tr>
<tr>
<td>Příjemka produktu</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="2">Po</td>
<td>Žádné</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="8">Výroba</td>
<td rowspan="3">Registrace</td>
<td rowspan="3">Nelze použít</td>
<td>Žádné</td>
<td rowspan="12">Vše</td>
</tr>
<tr>
<td>Ohlásit jako dokončené</td>
</tr>
<tr>
<td>Konec</td>
</tr>
<tr>
<td rowspan="5">Ohlásit jako dokončené</td>
<td rowspan="3">Před</td>
<td>Žádné</td>
</tr>
<tr>
<td>Ohlásit jako dokončené</td>
</tr>
<tr>
<td>Konec</td>
</tr>
<tr>
<td rowspan="2">Po</td>
<td>Žádné</td>
</tr>
<tr>
<td>Konec</td>
</tr>
<tr>
<td rowspan="4">Karanténa</td>
<td rowspan="3">Ohlásit jako dokončené</td>
<td rowspan="2">Před</td>
<td>Ohlásit jako dokončené</td>
</tr>
<tr>
<td>Konec</td>
</tr>
<tr>
<td>Po</td>
<td>Konec</td>
</tr>
<tr>
<td>Konec</td>
<td>Před</td>
<td>Konec</td>
</tr>
<tr>
<td rowspan="3">Operace postupu</td>
<td rowspan="3">Oznámit jako dokončené</td>
<td rowspan="2">Před</td>
<td>Není</td>
<td rowspan="3">Specifické ID, Skupina nebo Vše a Podle prostředku, Skupina nebo Vše</td>
</tr>
<tr>
<td>Oznámit jako dokončené</td>
</tr>
<tr>
<td>Po</td>
<td>Není</td>
</tr>
<tr>
<td rowspan="3">Výroba vedlejších produktů</td>
<td>Registrace</td>
<td>Nelze použít</td>
<td rowspan="3">Není</td>
<td rowspan="3">Vše</td>
</tr>
<tr>
<td rowspan="2">Oznámit jako dokončené</td>
<td>Před</td>
</tr>
<tr>
<td>Po</td>
</tr>
</tbody>
</table>

> [!NOTE]
> Funkce *Správa kvality pro procesy skladu* přidává možnosti zpracování objednávky kvality pro výrobu s polem **Typ události** nastaveným jako *Oznámit jako dokončené* a polem **Spuštění** nastaveným jako *Po dokončení*, a pro nákupy s polem **Typem události** nastaveným jako *Registrace*. Další informace viz [Správa kvality pro procesy skladu](quality-management-for-warehouses-processes.md).

V následující tabulce jsou uvedeny další informace o způsobu, jak lze generovat objednávky kvality pro určité typy procesů.

<div class="tableSection">
<table>
<thead>
<tr>
<th>Typ procesu</th>
<th>Kdy lze objednávku kvality generovat automaticky</th>
<th>Kdy lze objednávku kvality generovat v případě, že je vyžadován destrukční test</th>
<th>Informace o podmínkách</th>
<th>Informace o ručním generování</th>
</tr>
</thead>
<tbody>
<tr>
<td>Nákupní objednávka</td>
<td>Před tím nebo po tom, co je příjemka produktu pro přijatý materiál zaúčtována</td>
<td>Po tom, co je příjemka produktu pro přijatý materiál zaúčtována, protože materiál musí být k dispozici pro destrukční testy</td>
<td>Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, dodavatele nebo kombinace těchto podmínek.</td>
<td>Ručně vygenerovaná objednávka kvality, která odkazuje na nákupní objednávku, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</td>
</tr>
<tr>
<td>Karanténní příkaz</td>
<td>Před tím nebo po tom, co je karanténní příkaz vykázán jako dokončený nebo ukončený</td>
<td>Objednávky kvality, které vyžadují provedení destrukčních testů, nelze generovat. Předpokládá se, že funkce karanténního příkazu zpracovává likvidaci materiálu, který je zničen.</td>
<td>Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, dodavatele nebo kombinace těchto podmínek.</td>
<td>Ručně vygenerovaná objednávka kvality, která odkazuje na karanténní příkaz, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</td>
</tr>
<tr>
<td>Prodejní objednávka</td>
<td>Před naplánovaným procesem vyskladnění nebo aktualizací dodacího listu pro položky, které byly právě dodány</td>
<td>Při jakémkoli kroku</td>
<td>Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, odběratele nebo kombinace těchto podmínek.</td>
<td>Ručně vygenerovaná objednávka kvality, která odkazuje na prodejní objednávku, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</td>
</tr>
<tr>
<td>Výrobní zakázka</td>
<td>Před tím nebo po tom, co je vykázáno dokončené množství pro výrobní zakázku</td>
<td>Po tom, co je vykázáno dokončené množství pro výrobní zakázku</td>
<td>Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, nebo kombinace těchto podmínek.</td>
<td>Ručně vygenerovaná objednávka kvality, která odkazuje na výrobní zakázku, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</td>
</tr>
<tr>
<td>Výrobní zakázka s operací postupu</td>
<td>Před tím nebo po tom, co je dokončeno ohlášení pro operaci</td>
<td>Po tom, co je pro poslední operaci dokončeno ohlášení výrobní zakázky</td>
<td>Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, provozního prostředku nebo kombinace těchto podmínek.</td>
<td>Ručně vygenerovaná objednávka kvality, která odkazuje na operaci postupu, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</td>
</tr>
<tr>
<td>Zásoby</td>
<td>Objednávku kvality nelze automaticky generovat pro transakci v deníku zásob ani pro transakce převodních příkazů.</td>
<td></td>
<td></td>
<td>Objednávku kvality je možné vytvořit ručně pro množství položky na skladě. Jsou vyžadovány fyzické zásoby na skladě.</td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Příklady automatického generování objednávek kvality

### <a name="purchasing"></a>Nákup

Pokud v nákupu nastavíte pole **Typ události** na hodnotu *Příjemka produktu* a pole **Spuštění** na *Po* na stránce **Přidružení kvality**, získáte následující výsledky:

- Pokud je možnost **Podle aktualizovaného množství** nastavená na *Ano*, objednávka kvality se vygeneruje pro každý příjem na základě nákupní objednávky podle přijatého množství a nastavení ve vzorku položky. Při každém příjmu množství na základě nákupní objednávky jsou nové objednávky kvality generovány na základě nově přijatého množství.
- Pokud je možnost **Podle aktualizovaného množství** nastavená na *Ne*, objednávka kvality se vygeneruje pro první příjem na základě nákupní objednávky podle přijatého množství a nastavení ve vzorku položky. Dále se vytvoří jedna nebo více objednávek kvality na základě zbývajícího množství v závislosti na sledovacích dimenzích. Objednávky kvality nejsou vygenerovány pro následné příjmy s nákupní objednávkou.

### <a name="production"></a>Výrobní

Pokud ve výrobě nastavíte pole **Typ události** na hodnotu *Vykázat jako dokončené* a pole **Spuštění** na *Po* na stránce **Přidružení kvality**, získáte následující výsledky:

- Pokud je možnost **Podle aktualizovaného množství** nastavená na *Ano*, objednávka kvality se vygeneruje podle každého dokončeného množství a nastavení ve vzorku položky. Při každém vykázání množství jako dokončeného na základě výrobní zakázky jsou nové objednávky kvality generovány na základě nově dokončeného množství. Tato logika generování je konzistentní s nákupem.
- Pokud je možnost **Podle aktualizovaného množství** nastavená na *Ne*, objednávka kvality se vygeneruje při přvní vykázání množství jako dokončeného na základě dokončeného množství. Dále se vytvoří jedna nebo více objednávek kvality na základě zbývajícího množství v závislosti na sledovacích dimenzích vzorku položky. Objednávky kvality nejsou vygenerovány pro následná dokončená množství.

<table>
<thead>
<tr>
<th>Specifikace kvality</th>
<th>Na aktualizované množství</th>
<th>Na sledovací dimenzi</th>
<th>Výsledek</th>
</tr>
</thead>
<tbody>
<tr>
<td>Počet procent: 10 %</td>
<td>Ano</td>
<td>
<p>Číslo dávky: Ne</p>
<p>Sériové číslo: Ne</p>
</td>
<td>
<p>Množství na objednávce: 100</p>
<ol>
<li>Vykázat jako dokončené pro 30
<ul>
<li>Objednávka kvality 1 na 3 (10 % z 30)</li>
</ul>
</li>
<li>Vykázat jako dokončené pro 70
<ul>
<li>Objednávka kvality 2 na 7 (10 % ze zbývajícího množství objednávky, které se v tomto případě rovná 70)</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Fixní množství: 1</td>
<td>Žádný</td>
<td>
<p>Číslo dávky: Ne</p>
<p>Sériové číslo: Ne</p>
</td>
<td>Množství na objednávce: 100
<ol>
<li>Vykázat jako dokončené pro 30
<ul>
<li>Objednávka kvality 1 pro 1 (pro první vykázané množství jako dokončené, které má pevnou hodnotu 1)</li>
<li>Objednávka kvality 2 pro 1 (pro zbývající množství, které má stabilně pevnou hodnotu 1)</li>
</ul>
</li>
<li>Vykázat jako dokončené pro 10
<ul>
<li>Nejsou vytvořeny žádné objednávky kvality.</li>
</ul>
</li>
<li>Vykázat jako dokončené pro 60
<ul>
<li>Nejsou vytvořeny žádné objednávky kvality.</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Fixní množství: 1</td>
<td>Ano</td>
<td>
<p>Číslo dávky: Ano</p>
<p>Sériové číslo: Ano</p>
</td>
<td>
<p>Množství na objednávce: 10</p>
<ol>
<li>Zpráva o dokončení pro 3: 1 pro číslo šarže b1, sériové číslo s1; 1 pro číslo šarže b2, sériové číslo s2; a 1 pro číslo šarže b3, sériové číslo s3
<ul>
<li>Pořadí kvality 1 pro 1 z dávky b1, sériové číslo s1</li>
<li>Pořadí kvality 2 pro 1 z dávky b2, sériové číslo s2</li>
<li>Pořadí kvality 3 pro 1 z dávky b3, sériové číslo s3</li>
</ul>
</li>
<li>Zpráva o dokončení pro 2: 1 pro číslo šarže b4, sériové číslo s4; a 1 pro číslo šarže b5, sériové číslo s5
<ul>
<li>Pořadí kvality 4 pro 1 z dávky b4, sériové číslo s4</li>
<li>Pořadí kvality 5 pro 1 z dávky b5, sériové číslo s5</li>
</ul>
</li>
</ol>
<p><strong>Poznámka:</strong> Dávku lze znovu použít.</p>
</td>
</tr>
<tr>
<td>Fixní množství: 2</td>
<td>Žádný</td>
<td>
<p>Číslo dávky: Ano</p>
<p>Sériové číslo: Ano</p>
</td>
<td>
<p>Množství na objednávce: 10</p>
<ol>
<li>Zpráva o dokončení pro 3: 1 pro číslo šarže b1, sériové číslo s1; 1 pro číslo šarže b2, sériové číslo s2; a 1 pro číslo šarže b3, sériové číslo s3; a 1 pro číslo šarže b4, sériové číslo s4
<ul>
<li>Pořadí kvality 1 pro 1 z dávky b1, sériové číslo s1</li>
<li>Pořadí kvality 2 pro 1 z dávky b2, sériové číslo s2</li>
<li>Pořadí kvality 3 pro 1 z dávky b3, sériové číslo s3</li>
<li>Pořadí kvality 4 pro 1 z dávky b4, sériové číslo s4</li>
</ul>
<ul>
<li>Objednávka kvality 5 pro 2, bez reference na dávku a sériové číslo</li>
</ul>
</li>
<li>Zpráva o dokončení pro 6: 1 pro číslo šarže b5, sériové číslo s5; 1 pro číslo šarže b6, sériové číslo s6; 1 pro číslo šarže b7, sériové číslo s7; 1 pro číslo šarže b8, sériové číslo s8; 1 pro číslo šarže b9, sériové číslo s9; a 1 pro číslo šarže b10, sériové číslo s10
<ul>
<li>Nejsou vytvořeny žádné objednávky kvality.</li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Další prostředky

- [Procesy správy kvality](quality-management-processes.md)
- [Povolit správu kvality a neshod](enable-quality-management.md)
- [Správa kvality pro procesy skladu](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
