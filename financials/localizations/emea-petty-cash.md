---
title: "Pokladní hotovost pro východní Evropu"
description: "Toto téma obsahuje informace o funkci pokladní hotovost, která umožňuje uživatelům v České republiky, Estonska, Litvy, Maďarska, Lotyšska, Polska a Ruska projevily pokladních operací v systému."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RCashBalance, RCashCountStatementForm, RCashPosting, RCashRemainLimit, RCashReportJour_PL, RCashTable, RCashTableBalance, RCashTableCredLimit, RCashTableLastRevaluation, RCashTableTransactions, RCashTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268504
ms.assetid: ff2ea7b0-8de2-48c5-8f9f-5d95d9924925
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: e843abff91f74ff8c2c577f499fa829821fc56ee
ms.lasthandoff: 03/31/2017


---

# <a name="petty-cash-for-eastern-europe"></a>Pokladní hotovost pro východní Evropu

[!include[banner](../includes/banner.md)]


Toto téma obsahuje informace o funkci pokladní hotovost, která umožňuje uživatelům v České republiky, Estonska, Litvy, Maďarska, Lotyšska, Polska a Ruska projevily pokladních operací v systému.

Pokladní hotovost funkce slouží k automatizaci operací pro příjmy a výdaje v hotovosti, vytváření primárních dokumentů a tisku související zprávy. Pokladní hotovost funkce umožňuje provádět následující operace:

-   Účet příjmu a výdajů k dispozici hotovostní aktiva.
-   Generovat běžné platební formuláře: pokladní refundační doklady, hotovostní výdajové doklady a deník registrace pro pokladní doklady.
-   Řízení maximální peněžní částku, která je povolena pro operace se zákazníky, dodavateli a tak dále.
-   Pokladní operace v různých měnách se odráží v systému.
-   Převeďte částky pokladních operací v cizí měně na výchozí měnu k poskytování účetního výkaznictví.
-   Generovat **pokladní knihy** sestavy a sestavy pokladníka.

## <a name="prerequisites"></a>Předpoklady
Před použitím funkce pokladní hotovost, je nutné dokončit následující předpoklady:

-   Nastavte účty hotovosti.
-   Nastavte účetní profily pro hotovost.
-   Nastavte číselné řady pro číslování pokladního dokladu.
-   Nastavit výchozí hodnoty pro peněžní a bankovní parametry správy.
-   Nastavte platební názvy deníků v hlavní knihy.

### <a name="set-up-cash-accounts"></a>Nastavit platební účty

Chcete-li nastavit hotově, otevřete **řízení hotovosti a banky**&gt;**bankovní účty**&gt;**pokladní účty**a zadejte následující informace.

| Pole                 | popis                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| Hotovost                  | Zadejte kód, který identifikuje účet hotovosti (hotovost).                                                                    |
| Jméno                  | Zadejte popis pokladní účet.                                                                             |
| Měna              | Vyberte výchozí kód měny pro hotovostní transakce.                                                              |
| Skupina číselné řady | Pokud číslování pokladních dokladů musí lišit od číslování, který je určen v parametrech, zadejte kód. |
| Více měn       | Zaškrtněte toto políčko Povolit měn, které se liší od zúčtovací měna k zaúčtování.                     |
| Záporná hotovost         | Zaškrtněte toto políčko Povolit záporné peněžní zůstatky v jakékoliv měně.                                               |

Ovládací prvek nastavit zůstatek hotovosti pravidla pro pokladní účet, vyberte pokladní účet a poté v podokně akcí na **pokladní účet** klepněte v **limitu salda** seskupit, klikněte na **limitu salda**. Zadejte následující informace.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Pole</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Typ měny</td>
<td>Vyberte typ měny:
<ul>
<li><strong>Zúčtovací měna</strong> – použít základní firemní kód měny.</li>
<li><strong>Uvedené měny</strong> – použijte kód měny, který se liší od základní firemní kód měny.</li>
</ul></td>
</tr>
<tr class="even">
<td>Měna</td>
<td>Pokud jste vybrali <strong>uvedené měny</strong> v <strong>typ měny</strong> vyberte kód měny. Toto pole není k dispozici, pokud jste vybrali <strong>zúčtovací měna</strong> v <strong>typ měny</strong> pole.</td>
</tr>
<tr class="odd">
<td>Typ limitu zůstatku</td>
<td>Vyberte jednu z dostupných hodnot:
<ul>
<li><strong>Maximální</strong> – zůstatek hotovosti by nemělo překročit <strong>limitu salda</strong> částka pro pokladní účet (horní mez).</li>
<li><strong>Minimální</strong> – zůstatek hotovosti by nemělo být povoleno pod <strong>limitu salda</strong> částka pro pokladní účet (vázaný dole).</li>
</ul></td>
</tr>
<tr class="even">
<td>Zkontrolovat limit salda</td>
<td>Vyberte, co se děje během procesu schvalování pokladních dokladů-li <strong>limitu salda</strong> pro pokladní účet je překročena částka:
<ul>
<li><strong>Přijmout</strong> – může být překročen limit.</li>
<li><strong>Upozornění:</strong> – může být překročen limit, ale uživatel obdrží zprávu s upozorněním. Pokladní doklad je potvrzena nebo schválena.</li>
<li><strong>Chyba</strong> – nemůže být překročen limit. Uživatel obdrží chybovou zprávu a pokladní doklad není potvrzena nebo schválena.</li>
</ul>
Další informace o procesu schvalování pokladních dokladů naleznete &quot;platební transakce schválení a zaúčtování&quot; oddílu dále v tomto tématu.</td>
</tr>
<tr class="odd">
<td>Limit salda</td>
<td>Zadejte limit pro hotovostní zůstatek účtu. Částka by měla být v měně, kterou jste zadali.</td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-posting-profiles"></a>Nastavit účetní profily pro hotovost

Pokladní, účetní profily definujte zaúčtování do hlavní knihy. Chcete-li nastavit pokladní, účetní profil, přejděte na **platební****řízení banky a**&gt;**nastavení**&gt;**hotovosti účetní profily**a vyberte nebo vytvořte účetní profil. Zadejte následující informace.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Pole</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Platné pro</td>
<td>Vyberte, zda se účetní profil týká konkrétní pokladní účet nebo pro všechny účty hotovosti:
<ul>
<li><strong>Tabulka</strong> – Pokud je řádek profilu zaúčtování pro pokladní účet, tento řádek slouží k zaúčtování platební transakce.</li>
<li><strong>Všechny</strong> – neexistuje žádný řádek profilu zaúčtování pro pokladní účet.</li>
</ul></td>
</tr>
<tr class="even">
<td>Hotovost</td>
<td>Pokud jste vybrali <strong>tabulka</strong> v <strong>platné pro</strong> pole, zadat účet hotovosti. Toto pole zůstane prázdné, pokud jste vybrali <strong>všech</strong> v <strong>platné pro</strong> pole.</td>
</tr>
<tr class="odd">
<td>Účet hlavní knihy</td>
<td>Zadejte číslo účtu hlavní knihy, který chcete použít jako součtový účet pro pokladní účet.</td>
</tr>
</tbody>
</table>

### <a name="set-up-number-sequences-for-cash-documents"></a>Nastavte číselné řady pro pokladní doklady

Chcete-li nastavit číselné řady pro pokladní doklady, přejděte na **řízení hotovosti a banky**&gt;**nastavení**&gt;**parametry řízení hotovosti a banky**. Na **Číselná řada** karta, zadat kódy číselných řad pro **refundační platební**, **výdajové pokladní**, **Opravný hotovostní doklad**, a **vyrovnání kurzových rozdílů** dokumenty a pro **hotovosti číslo zprávy**.

### <a name="set-up-default-values-for-cash-and-bank-management-parameters"></a>Parametry správy banky a nastavit výchozí hodnoty pro hotovost

Chcete-li nastavit výchozí hodnoty pro peněžní a bankovní parametry správy pro funkci pokladní hotovost, přejděte na **řízení hotovosti a banky**&gt;**nastavení**&gt;**parametry řízení hotovosti a banky**. Na **platební**, zadejte následující informace.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Pole</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hotovost</td>
<td>Vyberte výchozí účet hotovosti v denících.</td>
</tr>
<tr class="even">
<td>Účtování hotovosti</td>
<td>Zadejte výchozí hotovost, účetní profil, který se používá, pokud je zadán jiný účetní profil.</td>
</tr>
<tr class="odd">
<td>Kontrola použitých dokladů</td>
<td>Vyberte, co se stane, pokud jsou nalezeny duplicitní čísla při kontrole číslo pokladního dokladu:
<ul>
<li>Zamítnout duplikaci</li>
<li>Zamítnout duplikaci v rámci fiskálního roku</li>
<li>Akceptovat duplicity</li>
<li>Upozornit v případě duplicit</li>
</ul></td>
</tr>
<tr class="even">
<td>Zkontrolovat limit operací</td>
<td>Určete, co se stane při překročení limitu pro operace s protistrany:
<ul>
<li><strong>Přijmout</strong> – může být překročen limit.</li>
<li><strong>Upozornění:</strong> – může být překročen limit, ale uživatel obdrží zprávu s upozorněním. Operace je zaúčtována.</li>
<li><strong>Chyba</strong> – nemůže být překročen limit. Uživatel obdrží chybovou zprávu a operace není zaúčtován.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Metoda ověření</td>
<td>Vyberte metodu ověření, který slouží k řízení byl překročen limit částky pro operace:
<ul>
<li><strong>Operace</strong> – ověření se provádí za transakci</li>
<li><strong>Dohoda</strong> – ověření se provádí na transakci, která má zadané zakázky s protistranou.</li>
</ul></td>
</tr>
<tr class="even">
<td>Limit operací</td>
<td>Zadejte maximální částku povolenou pro operace s protistrany v hotovosti.</td>
</tr>
<tr class="odd">
<td>Zaúčtování k dřívějšímu datu</td>
<td>Zaškrtněte toto políčko Povolit platební transakce k zaúčtování před datem poslední platební transakce.</td>
</tr>
<tr class="even">
<td>Dimenze</td>
<td>Zadejte rozměry v <strong>kód oddělení</strong>, <strong>analytické kód</strong>, a <strong>účel kódu</strong> pole. Ve formuláři Tisk pokladních dokladů bude odrážet tyto informace.</td>
</tr>
<tr class="odd">
<td>Použít stav potvrzení</td>
<td>Toto políčko zaškrtněte, chcete-li použít další stav, <strong>potvrzeno</strong>, během procesu schvalování pokladních dokladů. (Další informace naleznete &quot;platební transakce schválení a zaúčtování&quot; oddílu.)</td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-journal-names-in-general-ledger"></a>Nastavení názvů deníků hotovosti v hlavní knize

Chcete-li vytvořit deník pro zaúčtování platební transakce, přejděte na **financí**&gt;**nastavení deníku**&gt;**názvy deníku**a vytvoření nového záznamu. V **typ deníku** pole, zadejte **platební**. Definujte další parametry výchozí deník jak požadujete.

## <a name="daily-cash-operations-via-a-slip-journal"></a>Denní pokladní operace prostřednictvím deníku dokladů
Chcete-li vytvořit pokladní doklad prostřednictvím deníku dokladů, přejděte na **řízení hotovosti a banky**&gt;**platební transakce**&gt;**deník**a vytvořte nový deník. V podokně akcí klepněte na tlačítko **řádky**. Přidat nový řádek a zadejte následující informace.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Pole</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Datum</td>
<td>Zadejte datum pro transakce.</td>
</tr>
<tr class="even">
<td>Účet</td>
<td>Zvolte pokladní účet. Výchozí pokladní účet podle parametry řízení hotovosti a banky.</td>
</tr>
<tr class="odd">
<td>popis</td>
<td>Zadejte vysvětlující text transakce.</td>
</tr>
<tr class="even">
<td>Debet kredit</td>
<td>Zadejte částku pokladního dokladu v jednom z těchto polí:
<ul>
<li><strong>MD</strong> – toto pole použít k registraci přijatou hotovost a hotovostní refundační doklad.</li>
<li><strong>Dal</strong> – toto pole slouží k evidenci výdajů hotovost a hotovostní výdajový doklad.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Typ protiúčtu protiúčet</td>
<td>Vyberte číslo účtu posun a typ protiúčtu.</td>
</tr>
<tr class="even">
<td>Měna</td>
<td>Vyberte kód pro měnu transakce.</td>
</tr>
<tr class="odd">
<td>Doklad</td>
<td>Toto pole je vyplněno automaticky na základě nastavení deníku.</td>
</tr>
<tr class="even">
<td>Číslo objednávky</td>
<td>Pokud žádná číselná řada je nastaven pro pokladní účet, toto pole je vyplněno automaticky, založené na číselné řadě, která je určena v parametrech. V tomto poli můžete ručně zadat číslo objednávky, které požadujete. Zabránit inconsistence v číslování pokladního dokladu, platí následující ovládací prvek: číslo pokladního dokladu, který má starší datum operace nemůže být vyšší než počet pokladních dokladů, které má pozdější datum operace. Pokud není tento ovládací prvek, vyberte <strong>zaúčtování k dřívějšímu datu</strong> políčko v parametry řízení hotovosti a banky.</td>
</tr>
<tr class="odd">
<td>Stav schválení</td>
<td>První stav transakce je <strong>žádný</strong>. Informace o tom, jak nastavit stav transakce naleznete &quot;platební transakce schválení a zaúčtování&quot; oddílu.</td>
</tr>
<tr class="even">
<td>Typ dokumentu </td>
<td>Toto pole na <strong>pokladní doklad</strong> kartu je vyplněno automaticky na základě množství, které jste zadali pro pokladní doklad:
<ul>
<li><strong>Refundační doklad hotovosti</strong> – tato hodnota se používá, pokud jste zadali množství v <strong>MD</strong> pro pokladní účet.</li>
<li><strong>Pokladní výdajový doklad</strong> – tato hodnota se používá, pokud jste zadali množství v <strong>Dal</strong> pro pokladní účet</li>
<li><strong>Oprava</strong> – buď zadáte zápornou částku <strong>MD</strong> pole nebo <strong>Dal</strong> pro pokladní účet.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skupina prodejní daně</td>
<td>Zadejte skupinu DPH pro výpočet daně z operace.</td>
</tr>
<tr class="even">
<td>Skupina DPH zboží</td>
<td>Určete skupinu DPH položky k výpočtu daní na operaci.</td>
</tr>
<tr class="odd">
<td>Důvod</td>
<td>Na <strong>pokladní doklad</strong>, zadejte text popisující transakci předmět. Tento text bude vytištěn na hotovostní doklad formulář zprávy.</td>
</tr>
<tr class="even">
<td>Datum dokumentu</td>
<td>Zadejte popis, číslo a datum primárního dokumentu, který je důvodem pro transakci (například sestavy záloh, faktury nebo objednávky).</td>
</tr>
<tr class="odd">
<td>Typ prodejního zástupce</td>
<td>Toto pole může mít následující hodnoty:
<ul>
<li><strong>Pracovník</strong> – <strong>reprezentativní</strong> vyhledávání obsahuje seznam zaměstnanců, pokud <strong>protiúčet</strong> je nastaveno na <strong>knihy</strong> nebo <strong>banky</strong>, nebo seznam protistrany, kontaktní osoby, pokud <strong>protiúčet</strong> je nastaveno na <strong>zákazníka</strong> nebo <strong>dodavatele</strong>. Zástupci nastavení, přejděte na <strong>základní</strong>&gt;<strong>nastavení</strong>&gt;<strong>kontakty</strong>&gt;<strong>kontaktní osoby</strong>.</li>
<li><strong>Ostatní</strong> - <strong>reprezentativní</strong> vyhledávání obsahuje seznam jiných klientů. Nastavení přijímače, které nejsou uvedeny v <strong>zákazníci</strong> nebo <strong>dodavatele</strong> tabulky, přejděte na <strong>financí</strong>&gt;<strong>přijímače</strong>. Tento typ je k dispozici pouze pro Lotyšsko. ( <strong>CSELatvia</strong> by měl být povolen konfigurační klíč.)</li>
<li><strong>Dodavatel</strong> – <strong>zástupce</strong> vyhledávání obsahuje seznam dodavatelů. Chcete-li nastavit dodavatele, přejděte na <strong>závazků</strong>&gt;<strong>dodavatele</strong>.</li>
<li><strong>Zákazník</strong> – <strong>zástupce</strong> vyhledávání obsahuje seznam zákazníků. Nastavení zákazníků, přejděte na <strong>pohledávek</strong>&gt;<strong>zákazníci</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Zástupce</td>
<td>Vyberte zástupce typu, který je uveden v <strong>reprezentativní typ</strong> pole.</td>
</tr>
<tr class="odd">
<td>Jméno osoby</td>
<td>Toto pole je vyplněno automaticky na základě <strong>protiúčet</strong> a <strong>zástupce</strong> pole. Tato informace bude odrážet tiskové formuláře pro pokladní doklady.</td>
</tr>
<tr class="even">
<td>Průkaz totožnosti</td>
<td>Toto pole je vyplněno automaticky na základě průkazu totožnosti dat kontaktní osoby (zástupce). Pokud <strong>typ protiúčtu</strong> pole je nastavena na <strong>držitele zálohy</strong>a <strong>protiúčet</strong> pole je nastavena na číslo zaměstnance, peněžní příjmy a výdaje lze provést z nebo zaměstnanci. V tomto případě <strong>průkaz totožnosti</strong> vyplněno automaticky pomocí dat z průkazu totožnosti <strong>zaměstnance</strong> tabulka (<strong>účtování zaměstnanců</strong>&gt;<strong>tabulky zaměstnanců</strong>).</td>
</tr>
<tr class="odd">
<td>Účel</td>
<td>V <strong>účel</strong> tabulky, definujte jeden nebo více kódů místa určení částky transakce. Vyberte kód místa určení v <strong>účel</strong> pole a zadejte vysvětlení <strong>textu transakce</strong> pole. V <strong>částka</strong> zadejte částku v měně transakce. <strong>%</strong> Pole zobrazuje v procentech, poměru cílovou částku, která má celkovou částku transakce.</td>
</tr>
<tr class="even">
<td>Zůstatek</td>
<td>Zbývající částka, která je vypočtena. Všimněte si, že celá transakce částka musí být přiřazeny kódy místa určení.</td>
</tr>
<tr class="odd">
<td>Úřední osoby</td>
<td>Na <strong>úředníci</strong> karta, zadejte názvy a názvy pro odpovědné osoby: ředitel, hlavní účetní a pokladní. <strong>Pozici</strong> hodnoty jsou určeny nastavením úředníků na <strong>Obecné</strong> a <strong>knihy</strong> karty <strong>úředníci</strong> stránky (<strong>základní</strong>&gt;<strong>nastavení</strong>&gt;<strong>kontakty</strong>&gt;<strong>úředníci</strong>).</td>
</tr>
<tr class="even">
<td>Záloha</td>
<td>Toto políčko zaškrtněte v případě, že transakce je záloha.</td>
</tr>
<tr class="odd">
<td>Účetní profil</td>
<td>Zadejte účetní profil pro pokladní účet. Ve výchozím nastavení se používá účetní profil, který je určen v parametry řízení hotovosti a banky.</td>
</tr>
<tr class="even">
<td>Účetní profil protiúčtu</td>
<td>Vybrané protiúčtu zadejte účetní profil.</td>
</tr>
<tr class="odd">
<td>Celková částka</td>
<td>V <strong>celková částka</strong> skupinu polí v dolní části stránky, <strong>Reimb</strong> poli se zobrazí součet, který se vypočte pro všechny hotovostní refundační doklady, které jsou zadány v aktuálním deníku a <strong>Disb</strong> pole zobrazí součet pro všechny hotovostní výdajové doklady.</td>
</tr>
</tbody>
</table>

Při kontrole položky deníku, v podokně akcí klepněte na **ověřit**.

## <a name="daily-cash-operations-via-a-general-journal"></a>Denní pokladní operace prostřednictvím finančního deníku
Chcete-li vytvořit platební transakce prostřednictvím finančního deníku, přejděte na **financí**&gt;**položky deníku**&gt;**hlavní deníky**a vytvořte nový deník. V podokně akcí klepněte na tlačítko **řádky**. Přidat nový řádek a zadejte následující informace.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Pole</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Datum</td>
<td>Zadejte datum pro transakce.</td>
</tr>
<tr class="even">
<td>Typ účtu</td>
<td>Vyberte <strong>drobné hotovosti</strong>.</td>
</tr>
<tr class="odd">
<td>Účet</td>
<td>Vyberte číslo pokladní účet.</td>
</tr>
<tr class="even">
<td>Text transakce</td>
<td>Zadejte vysvětlující text transakce.</td>
</tr>
<tr class="odd">
<td>Debet kredit</td>
<td>Zadejte částku pokladního dokladu v jednom z těchto polí:
<ul>
<li><strong>MD</strong> – toto pole použít k registraci přijatou hotovost a hotovostní refundační doklad.</li>
<li><strong>Dal</strong> – toto pole slouží k evidenci výdajů hotovost a hotovostní výdajový doklad.</li>
</ul></td>
</tr>
<tr class="even">
<td>Typ protiúčtu protiúčet</td>
<td>Vyberte číslo účtu posun a typ protiúčtu.</td>
</tr>
<tr class="odd">
<td>Měna</td>
<td>Vyberte kód pro měnu transakce.</td>
</tr>
</tbody>
</table>

Na **fakturace** kartu, můžete zadat účetní profily pro vybraný účet a protiúčet. Pokud registrované transakce je záloha, vyberte **zálohy** políčko na **platební** kartu. V **reprezentativní** skupina, vyplňte pole, stejně jako u řádků deníku dokladů pro tisk na **platební** sestavy. Při kontrole položky deníku, v podokně akcí klepněte na **ověřit**.

## <a name="cash-transaction-approval-and-posting"></a>Schválení hotovostní transakce a zaúčtování
Pro hotovostní transakce mohou být použity následující stavy: **žádný**, **potvrzeno**, **schváleno**, a **byl odmítnut**. A **použít stav potvrzení** parametr **schválení** s náhledem **platební** tab na **řízení hotovosti a banky**&gt;**nastavení**&gt;**parametry řízení hotovosti a banky** umožňuje aktivovat další dva stavy: **potvrzeno** a **odmítnut**. Potvrzení je vhodné, když jsou vydávány pokladních dokladů a hotovostních příjmů a výdajů, které jsou sdíleny mezi dva zaměstnanci: účetní a pokladní. **Resetovat stav** funkce změní stav aktuální transakce. **Schválené** se stane **potvrzeno**, a **potvrzeno** se stane **žádný**. Pokladního deníku položky lze upravit pouze pokud je stav **žádný**. Hotovostní transakce mohou být odmítnuty pouze v případě, že je status transakce **potvrzeno**. Odmítnut platební dokumenty jsou k dispozici na **deník registrace pokladních dokladů** sestavy, ale neprojeví **pokladní knihy** sestavy. K potvrzení transakce, vyberte odpovídající list deníku a klepněte na tlačítko **doklady schválení**&gt;**potvrzení**. Číslo objednávky je generována podle určené číselné řady. Stav transakce se změní na **potvrzeno**, a již můžete upravit řádek deníku. Pokladní zůstatek účtu se nezmění. Pokladní doklad odmítnout, klepněte na tlačítko **doklady schválení**&gt;**odmítnout**. Tato možnost je k dispozici pouze pro dokumenty, které mají **potvrzeno** stav. Schválit transakce, vyberte odpovídající list deníku a klepněte na tlačítko **doklady schválení**&gt;**schválit**. **Schváleno** stav znamená, že peněžní prostředky byly přijaty nebo použito. Zůstatek hotovosti se změní. Platební transakce lze zaúčtovat. Zrušit **schváleno** stavu a obnovit stav na **žádný**, klepněte na tlačítko **doklady schválení**&gt;**resetovat stav**. Schválit pouze hotovostní transakce mohou být zaúčtovány. Deník zaúčtujete klepnutím na **účtování**&gt;**účtování**.

## <a name="print-a-cash-order"></a>Tisk pokladního dokladu
Tisk pokladního dokladu, vyberte řádek list deníku a v podokně akcí klepněte na tlačítko **tisk**&gt;**pokladní sestava objednávka**. Systém generuje tiskové formuláře pro hotovostní refundační doklad nebo hotovostní výdajový doklad, podle toho, zda je zadána částka v **MD** pole nebo **Dal** pole pro vybraný řádek:

-   Pokud je částka v **MD** pole: pokladní refundační doklad
-   Pokud je částka v **Dal** pole: Pokladní výdajový doklad

Stvrzenka řádky deníku, které mají **potvrzeno**, **schváleno**, nebo **odmítnut** stav lze vytisknout. Můžete také vytisknout pokladní dokladů objednávek na **řízení hotovosti a banky**&gt;**Inquires a zprávy o**&gt;**pokladní doklad**.

## <a name="periodic-tasks"></a>Periodické úlohy
Následující úkoly lze provést na **řízení hotovosti a banky**&gt;**pravidelné úlohy**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Periodická úloha</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Zkontrolovat limit salda</td>
<td>Kontrola zůstatku účtu vybrané hotovosti v určený den a zobrazit výsledek v informační zpráva. Výpočet zůstatku lze počítat pouze schválené transakce. Transakce, které jsou označeny jako <strong>pro mezd</strong> nejsou považovány za.</td>
</tr>
<tr class="even">
<td>Přepočet salda hotovosti</td>
<td>Pomocí této úlohy a ujistěte se, že umístit zůstatky hlavní knihy pro pokladní účty Zůstatek hotovosti.</td>
</tr>
<tr class="odd">
<td>Vytvoření výpisu hotovosti (pro pouze Polsko)</td>
<td>Vytvořit <strong>platební</strong> sestavy. <strong>Platební</strong> číslo sestavy je generována v závislosti na číselné řadě, která je nastavena pro <strong>číslo zprávy</strong>. V dialogovém okně pole pro úkol, v <strong>datum</strong>, zadejte poslední datum, pro které platební transakce musí být započítán pro <strong>platební</strong> sestavy. Použití <strong>filtr</strong> v pracovat <strong>záznamy mají být zahrnuty</strong> kartu a zadejte další kritéria omezující výběr hotovostních transakcí. Tato kritéria mohou zahrnovat čísla platební účet a kódy měn. V <strong>vytvořit</strong> vyberte uživatele, který je zodpovědný za vytváření sestav. Chcete-li zobrazit <strong>platební</strong> sestavu, která je vytvořena pomocí <strong>pokladní sestavy</strong> tlačítka <strong>pokladní účty</strong> stránky.</td>
</tr>
<tr class="even">
<td>Hotovost - Exchange nastavení FIFO a LIFO (pro pouze Polsko)</td>
<td>Výpočet kurzových rozdílů na polské normy. Použití <strong>filtr</strong> pracovat na <strong>záznamy mají být zahrnuty</strong> kartu a zadejte pro spuštění úlohy pro pokladní účet. Vyberte <strong>přepočet</strong> políčko, chcete-li provést úplný přepočet rozdílu úprava exchange pro všechna otevřená období. Zde je způsob výpočtu kurzových rozdílů při první, první ze skladu (FIFO) a poslední, první ze skladu (LIFO) metod:
<ul>
<li><strong>Metoda FIFO č.</strong> – systém vyhledá transakci výdaje, který má starší datum transakce (číslo menší objednávky) a vyrovná se příjmová transakce, která má starší datum transakce (číslo menší objednávky).</li>
<li><strong>Metoda LIFO</strong> – systém vyhledá transakci výdaje, který má pozdější datum transakce (větší číslo objednávky) a vyrovná se příjmová transakce, která obsahuje novější datum transakce (větší číslo objednávky).</li>
</ul>
Vyrovnaná částka se projeví v <strong>vyrovnání měny</strong> v <strong>platební transakce</strong> stránky. Pokud je úprava kursového rozdílu, částka se projeví v <strong>částka vyrovnání kurzových rozdílů</strong> pole a transakce <strong>rozdíl směnného kurzu</strong> typ dokumentu je generována v <strong>platební transakce</strong> tabulky. Účty hlavní knihy pro transakce zisků a ztrát, které jsou nastaveny v <strong>měny</strong> tabulka (<strong>finanční zisk</strong> a <strong>finanční ztráta směnného kurzu</strong>).</td>
</tr>
<tr class="odd">
<td>Přecenění cizí měny – hotovost</td>
<td>Použijte tento úkol dostatečný zůstatek ve výchozí měně vykazování dnem, kdy jsou zadány operace v cizích měnách. Použití <strong>filtr</strong> pracovat na <strong>záznamy mají být zahrnuty</strong> kartu a zadejte pro spuštění úlohy pro pokladní účet. V dialogovém okně úkol použít <strong>z měny</strong> a <strong>na měnu</strong> polí k zadání měny transakce. Systém porovná částky v měně, která byla převedena pomocí směnného kurzu ke zvolenému datu částku ve výchozí měně. Rozdíl mezi oběma částkami (s výjimkou předchozí vyrovnání kurzových rozdílů) je vypočítané kurzových rozdílů. Tato úloha vytvoří schválené platební transakce <strong>vyrovnání kurzových rozdílů</strong> typu. Transakce hlavní knihy, je vytvořen pomocí účtu hlavní knihy pro pokladní a účet hlavní knihy, který je určen v <strong>nerealizovaný zisk</strong> nebo <strong>Nerealizovaná ztráta</strong> v <strong>měny</strong> tabulka.</td>
</tr>
</tbody>
</table>

## <a name="inquiries-and-reports"></a>Dotazy a sestavy
| Dotaz nebo sestava                             | popis                                                                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zobrazení transakcí v hotovosti                        | Řádku listu deníku použít **dotazy** tlačítka v podokně akcí zobrazit transakce hlavní knihy, zůstatek hotovosti a dalších informací.                                                                                  |
| Hotovostní transakce                              | Přejít na **řízení hotovosti a banky**&gt;**dotazy a sestavy**&gt;**platební transakce** Chcete-li zobrazit platební transakce. Použití **filtr** funkce, chcete-li určit další kritéria pro omezení výběru hotovostní transakce. |
| Deník registrace (pro Estonsko, Rusko) | Sestava na **řízení hotovosti a banky**&gt;**dotazy a sestavy**&gt;**deník registrace** odráží všechny hotovostní refundační a hotovostní výdajové doklady, které byly vydány.                                   |
| Pokladní kniha (pro Lotyšsko, Litva, Rusko)     | Sestava na **řízení hotovosti a banky**&gt;**dotazy a sestavy**&gt;**pokladní kniha sestavy** odráží skutečné peněžní fond pohyby (příjmy a výdaje).                                                            |






