---
title: Pokladní hotovost pro východní Evropu a Rusko
description: Tento článek uvádí informace o funkci pokladní hotovosti, která umožňuje uživatelům v Estonsku, Litvě, České republice, Maďarsku, Lotyšku, Polsku a Rusku provádět hotovostní operace v systému.
author: AdamTrukawka
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: atrukawk
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 268504
ms.search.form: RCashBalance, RCashCountStatementForm, RCashPosting, RCashRemainLimit, RCashReportJour_PL, RCashTable, RCashTableBalance, RCashTableCredLimit, RCashTableLastRevaluation, RCashTableTransactions, RCashTrans
ms.openlocfilehash: d66e76f6d432b02c24997b76fe93797828a33c93
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267677"
---
# <a name="petty-cash-for-eastern-europe-and-russia"></a>Pokladní hotovost pro východní Evropu a Rusko

[!include [banner](../includes/banner.md)]

Tento článek uvádí informace o funkci pokladní hotovosti, která umožňuje uživatelům v Estonsku, Litvě, České republice, Maďarsku, Lotyšku, Polsku a Rusku provádět hotovostní operace v systému.

Funkci pokladní hotovosti můžete používat k automatizaci provozů pro příjmy a výdaje v hotovosti, vytváření primárních dokumentů a tisku souvisejících sestav. Funkce pokladní hotovosti umožňuje provádět následující operace:

-   Účtovat příjmy a výdaje dostupných finančních aktiv.
-   Vytvářet a ukládat běžné hotovostní formuláře: hotovostní refundační doklady, hotovostní výdajové doklady a deník registrace pokladních dokladů.
-   Určovat maximální peněžní částky, která je povolena pro operace se zákazníky, dodavateli atd.
-   Vyjadřovat hotovostní operace v různých měnách v systému.
-   Převádět částky pokladních operací v cizích měnách na zúčtovací měnu, a zajistit tak účetní vykazování.
-   Generovat sestavu **pokladní hotovosti** a sestavu pokladníka.

## <a name="prerequisites"></a>Předpoklady
Před použitím funkce pokladní hotovosti je nutné provést následující požadované úkoly:

-   Nastavit účty hotovostní zálohy.
-   Nastavit účetní profily pro hotovost.
-   Nastavit číselné řady pro číslování hotovostních dokladů.
-   Nastavit výchozí hodnoty a parametry pro parametry pokladny a banky.
-   Nastavit názvy hotovostních deníků v hlavní knize.

### <a name="set-up-cash-accounts"></a>Nastavit účty hotovostní zálohy.

Pokud chcete nastavit hotovost, otevřete složku **Pokladna a banka** &gt; **Bankovní účty** &gt; **Pokladní účty** a zadejte následující informace.

| Pole                 | popis                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| Hotovost                  | Zadejte kód pro označení pokladního účtu (hotovost).                                                                    |
| Jméno                  | Zadejte popis pokladního účtu.                                                                             |
| Měna              | Vyberte výchozí kód měny pro hotovostní transakce.                                                              |
| Skupina číselné řady | Pokud se musí číslování pokladních dokladů lišit od číslování, které je určeno v parametrech, zadejte kód. |
| Více měn       | Zaškrtněte toto políčko k povolení měn, které se liší od zúčtovací měny k zaúčtování.                     |
| Záporná hotovost         | Zaškrtněte toto políčko, pokud chcete povolit záporné peněžní zůstatky v jakékoliv měně.                                               |

Pokud chcete nastavit pravidla pro kontrolu zůstatku na pokladním účtu, vyberte pokladní účet a poté v podokně akcí na kartě **Pokladní účet** klepněte ve skupině **Limit zůstatku** na **Limit zůstatku**. Zadejte následující informace.

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
<li><strong>Zúčtovací měna</strong> – použijte základní firemní kód měny.</li>
<li><strong>Označená měna</strong> – použijte kód měny, který se liší od základního firemního kódu měny.</li>
</ul></td>
</tr>
<tr class="even">
<td>Měna</td>
<td>Pokud jste vybrali <strong>Označená měna</strong> v poli <strong>Typ měny</strong>, vyberte kód měny. Toto pole není k dispozici, pokud jste vybrali <strong>Zúčtovací měna</strong> v poli <strong>Typ měny</strong>.</td>
</tr>
<tr class="odd">
<td>Typ limitu zůstatku</td>
<td>Vyberte jednu z dostupných hodnot:
<ul>
<li><strong>Maximální</strong> – Nemělo by být povoleno, aby zůstatek v hotovosti překročil částku <strong>limitu zůstatku</strong> pro pokladní účet (horní mez).</li>
<li><strong>Minimální</strong> – Nemělo by být povoleno, aby zůstatek v hotovosti klesl pod částku <strong>limitu zůstatku</strong> pro pokladní účet (dolní mez).</li>
</ul></td>
</tr>
<tr class="even">
<td>Zkontrolovat limit salda</td>
<td>Vyberte, co se má dít během procesu schvalování pokladních dokladů, jestliže je překročena částka pro <strong>Limit zůstatku</strong> pro pokladní účet:
<ul>
<li><strong>Přijmout</strong> – Limit je možné překročit.</li>
<li><strong>Upozornění:</strong> – Limit může být překročen, ale uživatel obdrží zprávu s upozorněním. Pokladní doklad je potvrzen nebo schválen.</li>
<li><strong>Chyba</strong> – Limit není možné překročit. Uživatel obdrží chybovou zprávu a pokladní doklad není potvrzen nebo schválen.</li>
</ul>
Další informace o procesu schvalování pokladních dokladů naleznete v části &quot;Schvalování platebních transakcí a zaúčtování&quot; dále v tomto článku.</td>
</tr>
<tr class="odd">
<td>Limit salda</td>
<td>Zadejte limit zůstatku na pokladním účtu. Částka by měla být v měně, kterou jste zadali.</td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-posting-profiles"></a>Nastavení účetních profilů pro hotovost

Účetní profily pro hotovost definují zaúčtování do hlavní knihy. Chcete-li nastavit účetní profil pro hotovost, přejděte na položky **Pokladna** **a banka** &gt; **Nastavení** &gt; **Účetní profily pro hotovost** a vyberte nebo vytvořte účetní profil. Zadejte následující informace.

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
<td>Vyberte, zda se účetní profil týká konkrétního pokladního účtu všech pokladních účtů:
<ul>
<li><strong>Tabulka</strong> – Pokud je řádek účetního profilu pro pokladní účet, tento řádek slouží k zaúčtování hotovostní transakce.</li>
<li><strong>Všechny</strong> – neexistuje žádný řádek účetního profilu pro pokladní účet.</li>
</ul></td>
</tr>
<tr class="even">
<td>Hotovost</td>
<td>Pokud jste vybrali <strong>Tabulka</strong> v poli <strong>Platné pro</strong>, zadejte pokladní účet. Toto pole zůstane prázdné, pokud jste vybrali <strong>Vše</strong> v poli <strong>Platné pro</strong>.</td>
</tr>
<tr class="odd">
<td>Účet hlavní knihy</td>
<td>Zadejte číslo účtu hlavní knihy, který chcete použít jako souhrnný účet pro pokladní účet.</td>
</tr>
</tbody>
</table>

### <a name="set-up-number-sequences-for-cash-documents"></a>Nastavení číselných řad pro pokladní doklady

Chcete-li nastavit číselné řady pro pokladní doklady, přejděte na **Pokladna a banka** &gt; **Nastavení** &gt; **Parametry pokladny a banky**. Na kartě **Číselná řada** zadejte kódy číselných řad pro tyto doklady: **Hotovostní refundační doklady**, **Hotovostní výdajové doklady**, **Opravný hotovostní doklad**, **Vyrovnání kurzových rozdílů** a **Číslo výpisu hotovosti**.

### <a name="set-up-default-values-for-cash-and-bank-management-parameters"></a>Nastavení výchozích hodnot a parametrů pro parametry pokladny a banky

Chcete-li nastavit výchozí hodnoty pro parametry Pokladna a banka pro funkci pokladní hotovosti, přejděte na **Pokladna a banka** &gt; **Nastavení** &gt; **Parametry pokladny a banky**. Na kartě **Hotovost** zadejte následující informace:

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
<td>Vyberte výchozí pokladní účet v denících.</td>
</tr>
<tr class="even">
<td>Účtování hotovosti</td>
<td>Zadejte výchozí účetní profil pro hotovost, který se používá, pokud není zadán žádný jiný účetní profil.</td>
</tr>
<tr class="odd">
<td>Kontrola použitých dokladů</td>
<td>Vyberte, co se stane, pokud budou při kontrole čísla pokladního dokladu nalezena duplicitní čísla:
<ul>
<li>Zamítnout duplikaci</li>
<li>Zamítnout kopie v rámci fiskálního roku</li>
<li>Akceptovat duplicity</li>
<li>Upozornit v případě duplicit</li>
</ul></td>
</tr>
<tr class="even">
<td>Zkontrolovat limit operací</td>
<td>Určete, co se stane při překročení limitu pro operace s protistranami:
<ul>
<li><strong>Přijmout</strong> – Limit je možné překročit.</li>
<li><strong>Upozornění:</strong> – Limit může být překročen, ale uživatel obdrží zprávu s upozorněním. Operace je zaúčtována.</li>
<li><strong>Chyba</strong> – Limit není možné překročit. Uživatel obdrží chybovou zprávu a operace není zaúčtována.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Metoda ověření</td>
<td>Vyberte metodu ověření, která slouží ke kontrole množství překročení limitu pro operace:
<ul>
<li><strong>Operace</strong> – ověření se provádí na transakci</li>
<li><strong>Dohoda</strong> – ověření se provádí na transakci, která má specifikovanou dohodu s protistranou.</li>
</ul></td>
</tr>
<tr class="even">
<td>Limit operací</td>
<td>Zadejte maximální částku povolenou pro operace, které mají protistrany v hotovosti.</td>
</tr>
<tr class="odd">
<td>Zaúčtování k dřívějšímu datu</td>
<td>Zaškrtněte toto políčko pro povolení peněžních transakcí, které mají být zaúčtovány před posledním datem peněžní transakce.</td>
</tr>
<tr class="even">
<td>Dimenze</td>
<td>Zadejte rozměry v polích <strong>Kód oddělení</strong>, <strong>Analytický kód</strong> a <strong>Účel kódu</strong>. Tyto informace se projeví ve formuláři Tisk pokladních dokladů.</td>
</tr>
<tr class="odd">
<td>Použít stav potvrzení</td>
<td>Toto políčko zaškrtněte, pokud chcete během procesu schvalování pokladních dokladů použít další stav, <strong>Potvrzeno</strong>. (Další informace naleznete v části &quot;Schválení a zaúčtování platebních transakcí&quot;.)</td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-journal-names-in-general-ledger"></a>Nastavení názvů hotovostních deníků v hlavní knize

Chcete-li vytvořit deník pro zaúčtování platební transakce, přejděte na **Hlavní kniha** &gt; **Nastavení deníku** &gt; **Názvy deníku** a vytvořte nový záznam. V poli **Typ deníku** zadejte **Hotovost**. Definujte další výchozí parametry deníku podle potřeby.

## <a name="daily-cash-operations-via-a-slip-journal"></a>Denní pokladní operace prostřednictvím deníku dokladů
Chcete-li vytvořit pokladní doklad prostřednictvím deníku dokladu, přejděte na **Řízení hotovosti a banky** &gt; **Platební transakce** &gt; **Deník** a vytvořte nový deník. V podokně akcí klikněte na **Řádky**. Přidejte nový řádek a zadejte následující informace.

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
<td>Vyberte pokladní účet. Ve výchozím nastavení je pokladní účet specifikován podle parametrů Hotovost a řízení banky.</td>
</tr>
<tr class="odd">
<td>popis</td>
<td>Zadejte vysvětlující text pro použití s transakcí.</td>
</tr>
<tr class="even">
<td>Má dáti Dal</td>
<td>Zadejte částku pokladního dokladu do jednoho z těchto polí:
<ul>
<li><strong>Má Dáti</strong> – toto pole slouží k registraci přijaté hotovosti a hotovostního refundačního dokladu.</li>
<li><strong>Dal</strong> – toto pole slouží k registraci přijaté hotovosti a hotovostního refundačního dokladu.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Typ protiúčtu Protiúčet</td>
<td>Vyberte typ a číslo protiúčtu.</td>
</tr>
<tr class="even">
<td>Měna</td>
<td>Vyberte kód měny pro transakci.</td>
</tr>
<tr class="odd">
<td>Doklad</td>
<td>Toto pole je vyplněno automaticky na základě nastavení deníku.</td>
</tr>
<tr class="even">
<td>Číslo objednávky</td>
<td>Pokud není nastavena žádná číselná řada pro pokladní účet, toto pole je vyplněno automaticky na základě číselné řady, která je určena v parametrech. V tomto poli můžete podle potřeby ručně zadat číslo objednávky. Aby se zabránilo nekonzistentnímu číslování pokladních dokladů, platí následující kontrola: číslo pokladního dokladu, který má starší datum operace, nemůže být vyšší než číslo pokladního dokladu, které má pozdější datum operace. Pokud tuto kontrolu nepožadujete, zaškrtněte políčko <strong>Zaúčtování k dřívějšímu datu</strong> v parametrech pokladny a banky.</td>
</tr>
<tr class="odd">
<td>Stav schválení</td>
<td>Stav první transakce je <strong>Žádný</strong>. Informace o tom, jak nastavit stav transakce, naleznete v části &quot;Schválení a zaúčtování platebních transakcí&quot;.</td>
</tr>
<tr class="even">
<td>Typ dokumentu</td>
<td>Toto pole na kartě <strong>Pokladní doklad</strong> kartu je vyplněno automaticky na základě množství, které jste zadali pro pokladní doklad:
<ul>
<li><strong>Hotovostní refundační doklad</strong> – tato hodnota se používá, pokud jste zadali množství do pole <strong>Má Dáti</strong> pro pokladní účet.</li>
<li><strong>Hotovostní výdajový doklad</strong> – tato hodnota se používá, pokud jste zadali množství do pole <strong>Dal</strong> pro pokladní účet.</li>
<li><strong>Oprava</strong> – zadali jste zápornou částku do pole <strong>Má Dáti</strong> nebo <strong>Dal</strong> pro pokladní účet.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skupina prodejní daně</td>
<td>Zadejte skupinu DPH pro výpočet daní z operace.</td>
</tr>
<tr class="even">
<td>Skupina DPH zboží</td>
<td>Zadejte skupinu DPH položky pro výpočet daní z operace.</td>
</tr>
<tr class="odd">
<td>Důvod</td>
<td>Na kartě <strong>Pokladní doklad</strong> zadejte text popisující předmět transakce. Tento text bude vytištěn na formuláři zprávy o hotovostním dokladu.</td>
</tr>
<tr class="even">
<td>Datum dokumentu</td>
<td>Zadejte popis, číslo a datum primárního dokladu, který je důvodem pro transakci (například sestavy záloh, faktura nebo objednávka).</td>
</tr>
<tr class="odd">
<td>Typ prodejního zástupce</td>
<td>Toto pole může mít následující hodnoty:
<ul>
<li><strong>Pracovník</strong> – vyhledávací hodnota <strong>Zástupce</strong> obsahuje seznam zaměstnanců, pokud je hodnota v poli <strong>Protiúčet</strong> nastavena na <strong>Hlavní kniha</strong> nebo <strong>Banka</strong>, nebo seznam kontaktních osob protistrany, pokud je v poli <strong>Protiúčet</strong> nastavena hodnota <strong>Zákazník</strong> nebo <strong>Dodavatel</strong>. Při nastavování zástupců přejděte na <strong>Základní</strong> &gt; <strong>Nastavení</strong> &gt; <strong>Kontakty</strong> &gt; <strong>Kontaktní osoba</strong>.</li>
<li><strong>Ostatní</strong> – vyhledávací hodnota <strong>Zástupce</strong> obsahuje seznam jiných klientů. Pokud chcete nastavit příjemce, kteří nejsou uvedeni v tabulce <strong>Zákazníci</strong> nebo <strong>Dodavatelé</strong>, přejděte na <strong>Hlavní kniha</strong> &gt; <strong>Příjemci</strong>. Tento typ je dostupný pouze pro Lotyšsko. (Měl by být povolen klíč konfigurace <strong>CSELatvia</strong>.)</li>
<li><strong>Dodavatel</strong> – vyhledávací hodnota <strong>Zástupce</strong> obsahuje seznam dodavatelů. Při nastavování dodavatelů přejděte na položky <strong>Závazky</strong> &gt; <strong>Dodavatelé</strong>.</li>
<li><strong>Zákazník</strong> – vyhledávací hodnota <strong>Zástupce</strong> obsahuje seznam zákazníků. Při nastavování zákazníků přejděte na položky <strong>Pohledávky</strong> &gt; <strong>Zákazníci</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Zástupce</td>
<td>Vyberte zástupce typu, který je uveden v poli <strong>Typ zástupce</strong>.</td>
</tr>
<tr class="odd">
<td>Jméno osoby</td>
<td>Toto pole je vyplněno automaticky na základě hodnot v poli <strong>Protiúčet</strong> a <strong>Zástupce</strong>. Tyto informace se projeví ve formuláři pro tisk pokladních dokladů.</td>
</tr>
<tr class="even">
<td>Průkaz totožnosti</td>
<td>Toto pole je vyplněno automaticky na základě dat průkazu totožnosti kontaktní osoby (zástupce). Pokud je hodnota v poli <strong>Typ protiúčtu</strong> nastavena na <strong>Držitel zálohy</strong> a hodnota v poli <strong>Protiúčet</strong> pole je nastavena na číslo zaměstnance, lze od zaměstnance nebo pro něho provést peněžní příjmy a výdaje. V tomto případě je pole <strong>Průkaz totožnosti</strong> vyplněno automaticky s využitím dat z průkazu totožnosti z tabulky <strong>Zaměstnanec</strong> (<strong>účtování zaměstnanců</strong> &gt; <strong>Tabulka zaměstnanců</strong>).</td>
</tr>
<tr class="odd">
<td>Účel</td>
<td>V tabulce <strong>Účel</strong> definujte jeden nebo více kódů místa určení částky transakce. Vyberte kód místa určení v poli <strong>Účel</strong> a zadejte vysvětlení do pole <strong>Text transakce</strong>. Do pole <strong>Částka</strong> zadejte částku v měně transakce. V poli <strong>Procento%</strong> se zobrazuje poměr cílové částky k celkové částce transakce vyjádřený v procentech.</td>
</tr>
<tr class="even">
<td>Zůstatek</td>
<td>Zbývající částka, která je vypočtena. Všimněte si, že celá částka transakce musí být přiřazena ke kódům místa určení.</td>
</tr>
<tr class="odd">
<td>Úřední osoby</td>
<td>Na kartě <strong>Úředníci</strong> zadejte názvy a názvy pro odpovědné osoby: ředitel, hlavní účetní a pokladní. Hodnoty <strong>Pozice</strong> jsou určeny nastavením úředníků na kartě <strong>Obecné</strong> a <strong>Hlavní kniha</strong> stránky <strong>Úředníci</strong> (<strong>Základní</strong> &gt; <strong>Nastavení</strong> &gt; <strong>Kontakty</strong> &gt; <strong>Úředníci</strong>).</td>
</tr>
<tr class="even">
<td>Záloha</td>
<td>Toto políčko zaškrtněte, pokud je daná transakce zálohová.</td>
</tr>
<tr class="odd">
<td>Účetní profil</td>
<td>Zadejte krátký název hotovostního účtu. Ve výchozím nastavení se používá účetní profil, který je určen v parametrech pokladny a banky.</td>
</tr>
<tr class="even">
<td>Účetní profil protiúčtu</td>
<td>Zadejte profil zaúčtování vybraného protiúčtu.</td>
</tr>
<tr class="odd">
<td>Celková částka</td>
<td>Ve skupině polí <strong>Celková částka</strong> v dolní části stránky je v poli <strong>Refundace</strong> uveden součet, který se vypočte pro všechny hotovostní refundační doklady, které jsou zadány v aktuálním deníku, a v poli <strong>Úhr.</strong> se zobrazuje součet pro všechny hotovostní výdajové doklady.</td>
</tr>
</tbody>
</table>

Při kontrole položky deníku v podokně akcí klepněte na **Ověřit**.

## <a name="daily-cash-operations-via-a-general-journal"></a>Denní pokladní operace prostřednictvím hlavního deníku
Chcete-li vytvořit platební transakce prostřednictvím hlavního deníku, přejděte na **Hlavní kniha** &gt; **Položky deníku** &gt; **Hlavní deníky** a vytvořte nový deník. V podokně akcí klikněte na **Řádky**. Přidejte nový řádek a zadejte následující informace.

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
<td>Vyberte <strong>Pokladní hotovost</strong>.</td>
</tr>
<tr class="odd">
<td>Účet</td>
<td>Vyberte číslo pokladního účtu.</td>
</tr>
<tr class="even">
<td>Text transakce</td>
<td>Zadejte vysvětlující text pro použití s transakcí.</td>
</tr>
<tr class="odd">
<td>Má dáti Dal</td>
<td>Zadejte částku pokladního dokladu do jednoho z těchto polí:
<ul>
<li><strong>Má Dáti</strong> – toto pole slouží k registraci přijaté hotovosti a hotovostního refundačního dokladu.</li>
<li><strong>Dal</strong> – toto pole slouží k registraci přijaté hotovosti a hotovostního refundačního dokladu.</li>
</ul></td>
</tr>
<tr class="even">
<td>Typ protiúčtu Protiúčet</td>
<td>Vyberte typ a číslo protiúčtu.</td>
</tr>
<tr class="odd">
<td>Měna</td>
<td>Vyberte kód měny pro transakci.</td>
</tr>
</tbody>
</table>

Na kartě **Fakturace** můžete zadat účetní profily pro vybraný účet a protiúčet. Pokud je registrovaná transakce placením zálohy, vyberte zaškrtávací políčko **Zálohy** na kartě **Platba**. Ve skupině polí **Zástupce** vyplňte pole stejně jako u řádků deníku dodacích listů, které chcete vytisknout v sestavě **Hotovost**. Při kontrole položky deníku v podokně akcí klepněte na **Ověřit**.

## <a name="cash-transaction-approval-and-posting"></a>Schválení a zaúčtování hotovostní transakce
Pro hotovostní transakce mohou být použity následující stavy: **žádný**, **potvrzeno**, **schváleno** a **odmítnuto**. Parametr **použít stav potvrzení** na pevné záložce **Schválení** karty **Hotovost** v okně **Pokladna a banka** &gt; **Nastavení** &gt; **Parametry pokladny a banky** umožňuje aktivovat další dva stavy: **Potvrzeno** a **Odmítnuto**. Potvrzení je vhodné, když jsou vydávány pokladní doklady a hotovostní příjmy a výdaje, které jsou sdíleny mezi dvěma zaměstnanci: účetní a pokladní. Funkce **Resetovat stav** změní stav aktuální transakce. Z možnosti **Schválené** se stane **potvrzeno** a z možnosti **potvrzeno** se stane **žádný**. Položky pokladního deníku lze upravit, pouze pokud je stav **žádný**. Hotovostní transakce mohou být odmítnuty pouze v případě, že je stav transakce **potvrzeno**. Odmítnuté platební doklady jsou k dispozici v sestavě **Deník registrace pokladních dokladů**, ale neprojeví se v sestavě **Pokladní kniha**. K potvrzení transakce vyberte odpovídající řádek deníku dokladů a klepněte na tlačítko **Schválení dokumentů** &gt; **potvrzení**. Číslo objednávky je generováno podle určené číselné řady. Stav transakce se změní na **potvrzeno** a již nemůžete upravit řádek deníku. Pokladní zůstatek účtu se nezmění. Pokud chcete pokladní doklad odmítnout, klepněte na tlačítko **Schválení dokumentů** &gt; **odmítnout**. Tato možnost je k dispozici pouze pro dokumenty, které mají stav **potvrzeno**. Ke schválení transakce vyberte odpovídající řádek deníku dokladů a klepněte na tlačítko **Schválení dokumentů** &gt; **Schválit**. Stav **Schváleno** znamená, že peněžní prostředky byly přijaty nebo použity. Zůstatek hotovosti se změní. Platební transakci lze zaúčtovat. Pokud chcete zrušit stav **schváleno** obnovit stav na **žádný**, klepněte na tlačítko **schválení dokumentů** &gt; **resetovat stav**. Zaúčtovat lze pouze schválené hotovostní transakce. Když chcete zaúčtovat deník, klepněte na **Zaúčtovat** &gt; **Zaúčtovat**.

## <a name="print-a-cash-order"></a>Tisk platební slevy
Pokud chcete vytisknout pokladní doklad, vyberte řádek deníku dokladů a v podokně akcí klepněte na tlačítko **tisk** &gt; **Sestava pokladního dokladu**. Systém generuje tiskový formulář pro hotovostní refundační doklad nebo hotovostní výdajový doklad, podle toho, zda je zadána částka v poli **MD** nebo **Dal** pro vybraný řádek:

-   Pokud je částka v poli **MD**: pokladní refundační doklad
-   Pokud je částka v poli **Dal**: hotovostní výdajový doklad

Řádky deníku dokladů, které mají stav **potvrzeno**, **schváleno** nebo **odmítnuto** lze vytisknout. Můžete také vytisknout pokladní doklady objednávek na v **řízení hotovosti a banky** &gt; **Dotazy a sestavy** &gt; **Pokladní doklad**.

## <a name="periodic-tasks"></a>Periodické úlohy
Následující úkoly lze provést v okně **Řízení hotovosti a banky** &gt; **Pravidelné úlohy**.

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
<td>Zkontrolujte zůstatek na vybraném hotovostním účtu v určený den a zobrazte výsledek v informační zprávě. Ve výpočtu zůstatku lze počítat pouze schválené transakce. Transakce, které jsou označeny jako <strong>pro mzdy</strong> nejsou zohledněny.</td>
</tr>
<tr class="even">
<td>Přepočet salda hotovosti</td>
<td>Pomocí této úlohy se ujistěte, že zůstatky hlavní knihy pro pokladní účty odpovídají zůstatku hotovosti.</td>
</tr>
<tr class="odd">
<td>Vytvoření výpisu hotovosti (pro pouze Polsko)</td>
<td>Vytvořte sestavu <strong>hotovosti</strong>. Číslo sestavy <strong>hotovosti</strong> se generuje na základě číselné řady nastavené pro <strong>číslo sestavy</strong>. V dialogovém okně pole pro úkol, v poli <strong>Datum</strong>, zadejte poslední datum, pro které by měla být započítána platební transakce pro <strong>platební</strong> sestavu. Pomocí funkce <strong>filtr</strong> na kartě <strong>Záznamy pro zahrnutí</strong> zadejte další kritéria omezující výběr hotovostních transakcí. Tato kritéria mohou zahrnovat čísla platebního účtu a kódy měn. V poli <strong>Vytvořit podle</strong> vyberte uživatele, který bude za vytvoření sestavy zodpovědný. Chcete-li zobrazit <strong>platební</strong> sestavu, která je vytvořená, použijte tlačítko <strong>Pokladní sestavy</strong> na stránce <strong>Pokladní účty</strong>.</td>
</tr>
<tr class="even">
<td>Hotovost – vyrovnání kurzových rozdílů FIFO a LIFO (pouze Polsko)</td>
<td>Vypočítejte úpravu směnného kurzu dle polské normy. Pomocí funkce <strong>filtr</strong> na kartě <strong>Záznamy pro zahrnutí</strong> zadejte platební účet, pro který chcete úlohu použít. Zaškrtněte políčko <strong>Přepočet</strong>, chcete-li provést úplný přepočet rozdílu úpravy směnného kurzu pro všechna otevřená období. Zde je způsob úpravy kurzových rozdílů při použití metody FIFO a LIFO:
<ul>
<li><strong>Metoda FIFO</strong> – systém vyhledá výdajovou transakci, která má starší datum transakce (menší číslo objednávky) a vyrovná se s příjmovou transakcí, která má starší datum transakce (menší číslo objednávky).</li>
<li><strong>Metoda LIFO</strong> – systém vyhledá výdajovou transakci, která má pozdější datum transakce (větší číslo objednávky) a vyrovná se s příjmovou transakcí, která má pozdější datum transakce (větší číslo objednávky).</li>
</ul>
Vyrovnaná částka se projeví v poli <strong>Měna vyrovnání</strong> na stránce <strong>Platební transakce</strong>. Pokud existuje rozdíl v úpravě směnného kurzu, částka se projeví v poli <strong>Částka úpravy směnného kurzu</strong> a vygeneruje se typ dokumentu <strong>Rozdíl směnného kurzu</strong> v tabulce <strong>Platební transakce</strong>. Účty hlavní knihy pro transakce zisků a ztrát jsou nastaveny v tabulce <strong>Měna</strong> (<strong>finanční zisk</strong> a <strong>finanční ztráta směnného kurzu</strong>).</td>
</tr>
<tr class="odd">
<td>Přecenění cizí měny – hotovost</td>
<td>Použijte tento úkol pro zajištění dostatečného zůstatku ve výchozí měně v den vykazování, kdy jsou zadány operace v cizích měnách. Pomocí funkce <strong>filtr</strong> na kartě <strong>Záznamy pro zahrnutí</strong> zadejte platební účet, pro který chcete úlohu použít. V dialogovém okně pro úkol použijte pole <strong>Z měny</strong> a <strong>Na měnu</strong> polí k zadání měn transakce. Systém porovná částky v měně, která byla převedena pomocí směnného kurzu ke zvolenému datu částku ve výchozí měně. Rozdíl mezi oběma částkami (s výjimkou předchozího vyrovnání kurzových rozdílů) je vypočítaný kurzový rozdíl. Tato úloha vytvoří schválenou platební transakci typu <strong>vyrovnání kurzových rozdílů</strong>. Transakce hlavní knihy je vytvořena pomocí účtu hlavní knihy pro hotovost a účtu hlavní knihy, který je zadán v poli <strong>Nerealizovaný zisk</strong> nebo <strong>Nerealizovaná ztráta</strong> v tabulce <strong>Měna</strong>.</td>
</tr>
</tbody>
</table>

## <a name="inquiries-and-reports"></a>Dotazy a sestavy

| Dotaz nebo sestava                             | popis                                                                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zobrazení hotovostních transakcí                        | Pro řádek listu deníku použijte tlačítko **dotazy** v podokně akcí k zobrazení transakcí hlavní knihy, zůstatek hotovosti a dalších informací.                                                                                  |
| Hotovostní transakce                              | Pokud chcete zobrazit platební transakce, přejděte na **řízení hotovosti a banky** &gt; **Dotazy a sestavy** &gt; **Platební transakce**. Pomocí funkce **Filtr** na kartě Záznamy pro zahrnutí zadejte další kritéria omezující výběr hotovostních transakcí. |
| Registrační deník (pro Estonsko, Rusko) | Sestava v okně **řízení hotovosti a banky** &gt; **dotazy a sestavy** &gt; **deník registrace** odráží všechny hotovostní refundační a hotovostní výdajové doklady, které byly vydány.                                   |
| Pokladní kniha (pro Lotyšsko, Litvu, Rusko)     | Sestava v okně **řízení hotovosti a banky** &gt; **dotazy a sestavy** &gt; **pokladní kniha sestavy** odráží skutečné peněžní fond pohyby (příjmy a výdaje).                                                            |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
