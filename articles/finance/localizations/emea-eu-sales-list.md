---
title: Souhrnné hlášení EU
description: V tomto článku jsou informace o souhrnném hlášení pro Evropskou unii (EU).
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EUSalesList
audience: Application User
ms.reviewer: kfend
ms.custom: 12811
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1e9a566b7dc4dc2ed1970294a22e72b0bd21a7c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003002"
---
# <a name="eu-sales-list-reporting"></a>Souhrnné hlášení EU

[!include [banner](../includes/banner.md)]

V tomto článku jsou informace o souhrnném hlášení pro Evropskou unii (EU).

<a name="eu-sales-list-reporting"></a>Souhrnné hlášení EU
-----------------------

Dodavatel, který provádí intrakomunitární plnění dodávek zboží nebo služeb společnostem, které jsou vytvořeny v Evropské unii (EU), musí dodat přehled interních dodávek (souhrnné hlášení EU neboli ESL). Obecně platí, že přehled ESL je nutné podat finančnímu úřadu nejpozději poslední den v měsíci po kalendářním období, ke kterému se přehled ESL vztahuje. Dodavatel musí uvést své daňové identifikační číslo (DIČ) na formuláři ESL a musí také uvést následující informace o odběrateli:

-   Daňové identifikační číslo odběratele v EU
-   Celková hodnota intrakomunitárního plnění dodávek zboží a služeb pro daného odběratele v EU za dané období. Dodavatel musí také oddělit běžnou dodávku zboží od dodávky v rámci trojstranného obchodu. Trojstranné obchodní transakce zahrnují přímou dodávku zboží od dodavatelova dodavatele k zákazníkovi, když jsou obě strany registrovány v jiných členských státech EU.

Pomocí formuláře ESL mohou finanční úřady jednotlivých členských států EU ověřovat, zda bylo zaplaceno DPH za každou intrakomunitární transakci. Kombinace výpisů a vrácení DPH umožňuje členským státům EU vyměňovat si informace o pohybu zboží v rámci EU.

## <a name="overview-of-the-eu-sales-list-reporting-process"></a>Přehled procesu vykazování souhrnného hlášení EU
K dispozici máte následující úkony pro souhrnné hlášení EU:

-   Shromažďování informací o intrakomunitárních obchodních transakcích. Intrakomunitární obchodní transakce může být prodejní faktura, volná faktura, projektová faktura nebo dodavatelská faktura. Transakce je identifikována na základě země/oblasti protistrany. Intrakomunitární obchodní transakce různých typů jsou shromažďovány v tabulce souhrnného hlášení EU, v němž jsou reprezentovány v běžné formuláře. Každý záznam v tabulce ESL představuje jednu transakci a obsahuje DIČ protistrany a celkovou hodnotu zboží a služeb, které byly dodány.
-   (Volitelně) Zobrazení sestavy **Souhrnné hlášení (EU)**. Můžete zobrazit a ověřit sestavu **Souhrnné hlášení (EU)** pro dané období ve formuláři sešitu aplikace Microsoft Excel
-   Vygenerování sestavy **Souhrnné hlášení (EU)**. Sestava **Souhrnné hlášení (EU)** je generována ve formě elektronického souboru s konkrétním formátem, který je specifický pro každý členský stát EU. Obecně sestava **Souhrnné hlášení (EU)** obsahuje základní informace o vykazující straně a hodnotách dodávek zboží a služeb. Informace jsou seskupovány podle země a DIČ protistrany.
-   Uzavření období vykazování souhrnného hlášení EU. Po vygenerování sestavy **Souhrnné hlášení (EU)** a odeslání úřadům, je možné označit záznamy tabulky ESL jako **Uzavřené**. Tyto transakce nebudou zahrnuty v dalších sestavách.

## <a name="prerequisites"></a>Požadavky
Následující tabulka zobrazuje požadavky, které musí být splněny, než začnete.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategorie</th>
<th>Předpoklad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Nastavení:</strong> Právnická osoba</td>
<td>Primární adresa právnické osoby musí být v členském státě EU. Na stránce <strong>Právnické osoby</strong> (klikněte na <strong>Správa organizace</strong> &gt; <strong>Organizace</strong> &gt; <strong>Právnické osoby</strong>) vyberte právnickou osobu. Na pevné záložce <strong>Adresy</strong> vytvořte adresu, vyberte zemi/oblast a ostatní součásti adresy a označte adresu jako <strong>Primární</strong>. Na pevné záložce <strong>Daňová registrace</strong> v poli <strong>Daňové registrační číslo</strong> zadejte daňové identifikační číslo (DIČ) vaší společnosti.</td>
</tr>
<tr class="even">
<td><strong>Nastavení:</strong> Parametry identifikace osvobození od daně</td>
<td>Nastavte parametry identifikace osvobození od daně na stránce <strong>Parametry země/oblasti</strong> (klikněte na <strong>Daň</strong> &gt; <strong>Nastavení</strong> &gt; <strong>DPH</strong> &gt; <strong>Parametry země/oblasti</strong>). Pro jednotlivé země/oblasti, kde máte protistrany, vytvořte záznam na stránce a zadejte následující informace:
<ul>
<li><strong>Země/oblast</strong> – vyberte zemi nebo oblast, kterou chcete přidružit k identifikaci osvobození od daně.</li>
<li><strong>DPH</strong> – zadejte identifikační číslo daňového osvobození (tedy předponu čísla osvobození od daně) pro vybranou zemi/oblast.</li>
<li><strong>Kontrolovat číslo osvobození od daně</strong> – toto políčko zaškrtněte, chcete-li ověřit identifikaci osvobození od daně pro vybranou zemi/oblast.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Nastavení: </strong>Čísla osvobození od daně</td>
<td>Vytvořte čísla osvobození od daně pro vaše protistrany na stránce <strong>Čísla osvobození od daně</strong> (klikněte na <strong>Daň</strong> &gt; <strong>Nastavení</strong> &gt; <strong>DPH</strong> &gt; <strong>Čísla osvobození od daně</strong>). Pro každé číslo osvobození od daně vytvořte záznam na stránce a zadejte následující informace:
<ul>
<li><strong>Země/oblast </strong>– vyberte zemi/oblast daňové registrace protistrany.</li>
<li><strong>Číslo osvobození od daně</strong> – zadejte číslo osvobození od daně protistrany.</li>
<li><strong>Název společnosti</strong> – (volitelné) Zadejte název protistrany.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Nastavení: </strong>Daňová registrace protistran</td>
<td>Nastavte informace o daňové registraci protistran buď na stránce <strong>Všichni odběratelé</strong> (klikněte na položky <strong>Prodej a marketing</strong> &gt; <strong>Odběratelé</strong> &gt; <strong>Všichni odběratelé</strong>, vyberte záznam odběratele a klikněte na položky <strong>Možnosti</strong> &gt; <strong>Změnit zobrazení</strong> &gt; <strong>Zobrazení podrobností</strong>) , nebo na stránce <strong>Dodavatelé</strong> (klikněte na položky <strong>Zásobování a zdroje</strong> &gt; <strong>Dodavatelé</strong> &gt; <strong>Dodavatelé</strong>, vyberte záznam dodavatele a klikněte na položky <strong>Možnosti</strong> &gt; <strong>Změnit zobrazení</strong> &gt; <strong>Zobrazení podrobností</strong>). Na pevné záložce <strong>Faktury a dodávky</strong> v poli <strong>Číslo osvobození od daně</strong> vyberte číslo daňové registrace.</td>
</tr>
<tr class="odd">
<td><strong>Nastavení: </strong>DPH</td>
<td>Nastavte kódy daně k zahrnutí do sestavy <strong>Souhrnné hlášení (EU)</strong> na stránce <strong>Kódy DPH</strong> (klikněte na položky <strong>Daň</strong> &gt; <strong>Nepřímé daně</strong> &gt; <strong>DPH</strong> &gt; <strong>Kódy DPH</strong>). Na pevné záložce <strong>Nastavení sestavy</strong> pro každý kód DPH, který bude zahrnut v sestavě, zrušte zaškrtnutí políčka <strong>Vyloučeno</strong>. Nastavte parametry DPH pro položky na stránce <strong>Skupiny DPH položky</strong> (klikněte na položky <strong>Daň</strong> &gt; <strong>Nepřímé daně</strong> &gt; <strong>DPH</strong> &gt; <strong>Skupiny DPH položky</strong>). Pro každou skupinu DPH položky vyberte hodnotu v poli <strong>Typ vykazování</strong>. Hodnota, kterou jste vybrali, určuje sloupec částky ESL, ve kterém bude částka řádku zahrnuta.
<ul>
<li><strong>Prázdné</strong> – částka řádku bude zahrnuta ve sloupci <strong>Nepřiřazená hodnota</strong>.</li>
<li><strong>Zboží</strong> – částka řádku bude zahrnuta ve sloupci <strong>Hodnota zboží</strong>.</li>
<li><strong>Služba</strong> – částka řádku bude zahrnuta ve sloupci <strong>Hodnota služeb</strong>.</li>
<li><strong>Investice</strong> – částka řádku bude zahrnuta ve sloupci <strong>Hodnota investice</strong>. Tento sloupec je relevantní pouze pro Belgii.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Nastavení:</strong> Konfigurace vykazování ESL</td>
<td>Importujte nebo vytvořte konfigurace elektronického výkaznictví pro ESL. Informace o postupu vytvoření a údržby konfigurací elektronického výkaznictví naleznete v dokumentaci k elektronickému vykazování.</td>
</tr>
<tr class="odd">
<td><strong>Nastavení: </strong>Obecné parametry</td>
<td>Nastavte parametry vykazování ESL na stránce <strong>Parametry zahraničního obchodu</strong> (klikněte na položky <strong>Daň</strong> &gt; <strong>Nastavení</strong> &gt; <strong>Zahraniční obchod</strong> &gt; <strong>Parametry zahraničního obchodu</strong>). Zadejte následující parametry:
<ul>
<li>Karta <strong>Souhrnné hlášení (EU)</strong>:
<ul>
<li><strong>Výkaz platební slevy</strong> – toto políčko zaškrtněte, pokud má být platební sleva zahrnuta do hodnoty při zahrnutí transakce do sestavy ESL.</li>
<li><strong>Převést nákupy</strong> – zaškrtnutím tohoto políčka můžete zahrnout nákupy do sestavy ESL.</li>
<li><strong>Mapování formátu souboru</strong> – vyberte formát elektronického vykazování pro použití při generování elektronického souboru pro sestavu ESL.</li>
<li><strong>Mapování formátu sestavy</strong> – vyberte formát elektronického vykazování pro použití při generování náhledu sestavy pro sestavu ESL.</li>
<li><strong>Pravidlo zaokrouhlování</strong> – zadejte reálné číslo k použití pro zaokrouhlení. Částky ESL budou zaokrouhlovány na násobky tohoto čísla.</li>
<li><strong>Metoda zaokrouhlení</strong> – vyberte způsob zaokrouhlení pro použití při zaokrouhlování částek ESL (<strong>Normální</strong>, <strong>Dolů</strong> nebo <strong>Zaokrouhlení nahoru</strong>).</li>
<li><strong>Použít minimální hodnotu</strong> – toto políčko zaškrtněte, pokud chcete, aby částky, které jsou menší než hodnota <strong>Pravidlo zaokrouhlení</strong>, byly zaokrouhleny nahoru na hodnotu <strong>Pravidlo zaokrouhlení</strong>.</li>
<li><strong>Počet desetinných míst</strong> – zadejte počet desetinných míst pro zobrazení částek ESL (v elektronických souborech i na sestavě <strong>Náhled sestavy ESL</strong>).</li>
</ul></li>
<li>Karta <strong>Parametry země/oblasti</strong>: Identifikujte členské státy EU. Pro každý členský stát EU vytvořte záznam na stránce a zadejte následující informace:
<ul>
<li><strong>Země/oblast</strong> – vyberte zemi nebo oblast.</li>
<li><strong>Typ země/oblasti</strong> – pokud hodnota <strong>Země/oblast</strong> představuje zemi či oblast, ve které je vaše společnost registrovaná, vyberte hodnotu <strong>Domácí</strong>. Pokud je hodnota <strong>Země/oblast</strong> členským státem EU mimo zemi či oblast, ve které je vaše společnost registrovaná, vyberte hodnotu <strong>EU</strong>. Pokud hodnota <strong>Země/oblast</strong> není členským státem EU, vyberte možnost <strong>Třetí země/oblast</strong>.</li>
</ul></li>
<li>Karta <strong>Číselné řady</strong>: V řádku, kde má položka <strong>Odkaz</strong> hodnotu <strong>Souhrnné hlášení (EU)</strong>, vyberte kód číselné řady.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Související transakce</strong></td>
<td><ul>
<li>Zaregistrujte prodej odběrateli v jiném členském státu EU.</li>
<li>Zaregistrujte volnou fakturu pro odběratele v jiném členském státu EU.</li>
<li>Zaregistrujte projektovou fakturu pro odběratele v jiném členském státu EU.</li>
<li>Zaregistrujte fakturu od dodavatele v jiném členském státu EU.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="working-with-the-esl"></a>Práce se sestavou ESL
### <a name="collecting-information-about-intra-community-trade-transactions"></a>Shromažďování informací o intrakomunitárních obchodních transakcích

Za intrakomunitární obchodní transakce lze považovat transakce následujících typů:

-   Prodejní faktury
-   Volné faktury
-   Faktury projektu
-   Faktury dodavatele

Transakce je považována za intrakomunitární obchodní transakci, pokud je dodací adresa transakce v členském státu EU. Pro tyto země/oblasti by měl existovat záznam na kartě **Parametry země/oblasti** na stránce **Parametry zahraničního obchodu** a položku **Typ země/oblasti** je třeba nastavit na hodnotu **EU**. Intrakomunitární obchodní transakce jsou označeny v poli **Kód seznamu**. Pomocí tohoto pole lze také oddělit obecné intrakomunitární obchodní transakce od trojstranných obchodních transakcí. Můžete shromažďovat informace o intrakomunitárních obchodních transakcích na stránce **Souhrnné hlášení (EU)** (klikněte na položky **Daň** &gt; **Přiznání** &gt; **Zahraniční obchod** &gt; **Souhrnné hlášení (EU)**) pomocí funkce **Převod**. Tato funkce umožňuje zahrnout transakce, které mají částky různých typů vykazování (například zboží nebo služby), podle skupin DPH položek, které jsou určeny pro řádky transakcí. Můžete také použít jiné filtry k definování transakcí, které mají být zahrnuty. Funkce **Převod** vytvoří záznam na stránce **Souhrnné hlášení (EU)** pro každou intrakomunitární obchodní transakci, která je zahrnuta, a určí číslo účtu protistrany, zemi/oblast, číslo osvobození od daně, číslo faktury, datum a celkové částky řádků dle typu vykazování. Dále zkopíruje hodnotu **Kód seznamu** z transakce. Kód seznamu pro transakci lze ručně změnit na stránce **Souhrnné hlášení (EU)**. Funkce **Převod** vytvoří záznamy, kde je položka **Stav vykazování** nastaven na hodnotu **Zahrnuto**. Můžete ověřit informace, které jsou shromažďovány na stránce **Souhrnné hlášení (EU)** pomocí funkce **Ověřit**.

### <a name="generating-the-eu-sales-list-report"></a>Vygenerování sestavy Souhrnné hlášení (EU)

Můžete generovat sestavu **Souhrnné hlášení (EU)** pomocí funkce **Vykazování** na stránce **Souhrnné hlášení (EU)**. Funkce umožňuje vybrat období vykazování a pomocí filtrů definovat záznamy ESL, které mají být zahrnuty. Kromě toho můžete použít další parametry, které jsou specifické pro jednotlivé země/oblasti. Dále je možné generovat náhled sestavy, elektronický soubor nebo obojí. Funkce **Vykazování** použije nastaveními sestavy a formátu souboru uvedené na stránce **Parametry zahraničního obchodu**. Obecně platí, že sestava **Souhrnné hlášení (EU)** se skládá ze samostatných řádků, které uvádí celkové částky dodávek podle země/oblasti protistrany, čísla osvobození od daně a typ vykazování (budou zahrnuty trojstranné obchodní transakce). Po vytvoření sestavy **Souhrnné hlášení (EU)** za určité období můžete označit záznamy ESL, které jsou zahrnuty do sestavy nastavením položky **Stav vykazování** na hodnotu **Hlášeno**. Tento stav lze nastavit použitím funkce **Označit jako ohlášené** na stránce **Souhrnné hlášení (EU)**.

### <a name="closing-the-eu-sales-list-reporting-period"></a>Uzavření období vykazování souhrnného hlášení EU

Po dokončení procesu vykazování za určité období (například pokud finanční úřady přijaly sestavu **Souhrnné hlášení (EU)**), lze označit záznamy ESL, které jsou zahrnuty do sestavy za dané období, nastavením položky **Stav vykazování** na hodnotu **Uzavřené**. Tento stav lze nastavit použitím funkce **Označit jako uzavřené** na stránce **Souhrnné hlášení (EU)**. Pokud vrátíte uzávěrku období, můžete označit záznamy ESL nastavením položky **Stav vykazování** na hodnotu **Zahrnuto**. Tyto záznamy pak mohou být znovu zahrnuty v sestavě **Souhrnné hlášení (EU)**. Tento stav lze nastavit použitím funkce **Označit jako** **zahrnuto** na stránce **Souhrnné hlášení (EU)**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]