---
title: Integrace fiskální služby (ESR)
description: Toto téma obsahuje informace o integraci fiskální služby pro Rakousko a Českou republiku.
author: Anasyash
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CashRegister_W
audience: Application user
ms.reviewer: kfend
ms.search.region: Austria, Czech Republic
ms.author: Anasyash
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: b34ea77f8a522bad4f8d9161a069d048503aeb11
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003058"
---
# <a name="fiscal-service-esr-integration"></a>Integrace fiskální služby (ESR)

[!include [banner](../includes/banner.md)]

V Rakousku musí být všechny platby v hotovosti podepsány externím zařízením nebo službou, a musí být bezpečně uloženy. V České republice musí být platby v hotovosti odeslány na vládní portál pro fiskální podpis. V obou zemích musí být vystavena hotovostní účtenka s vytištěným podpisem.

K podpoře těchto požadavků specifických pro tyto země vám aplikace Dynamics 365 Finance umožňuje integraci s fiskální službou třetí strany, která splňuje specifické požadavky pro řízení hotovostních plateb v různých zemích nebo oblastech.

> [!NOTE]
> Předpokládá se, že fiskální služba třetích stran splňuje všechny další právní požadavky specifické pro zemi týkající se zaregistrovaných transakcí. Jste zodpovědni za správné nastavení a správu finanční služby.

## <a name="available-configurations"></a>Dostupné konfigurace

Formáty hotovostní účtenky, XML požadavek na fiskální službu a XML odezva z fiskální služby, jsou nastaveny jako konfigurace elektronického výkaznictví, které jsou uloženy v knihovně sdíleného majetku v aplikaci Microsoft Dynamics Lifecycle Services. K dispozici jsou následující konfigurace.

| Název konfigurace | Popis konfigurace | Komentář | Konfigurační soubor elektronického výkaznictví ve sdílené knihovně majetku LCS |
|---|---|---|---|
| **Model hotovostní účtenky** | | **Datový model pro formát hotovostní účtenky** | **Hotovostní příjemka Model.version.1.xml** |
| Formát hotovostní příjemky | | Základní formát pro hotovostní příjemku | Hotovostní příjemka Format.version.1.1.xml |
| Formát hotovostní příjemky (AT) | | Formát pro hotovostní příjemku v Rakousku (Tento formát zahrnuje \[QR kód\].) | Hotovostní příjemka Format (AT).version.1.1.1.xml |
| Formát hotovostní příjemky (CZ) | | Formát pro hotovostní příjemku v České republice (Tento formát zahrnuje ID obchodních prostor \[BP\].) | Hotovostní příjemka Format (CZ).version.1.1.1.xml |
| **Model registrační pokladny** | | **Datový model pro integraci registrační pokladny** | **Registrační pokladna Model.version.1.xml** |
| Příklad ESR požadavku | Příklad požadavku jedné příjemky EFSTA | Základní formát pro vzorový XML požadavek na fiskální službu EFSTA (Tento formát lze použít v Rakousku). | ESR požadavek example.version.1.1.xml |
| Příklad ESR požadavku (CZ) | Příklad ESR požadavku pro Českou republiku | Formát pro vzorový XML požadavek na fiskální službu EFSTA v České republice | ESR požadavek example (CZ).version.1.1.1.xml |
| Příklad ESR odezvy | Příklad ESR odezvy | Základní formát pro vzorovou XML odezvu na fiskální službu EFSTA (Tento formát lze použít v Rakousku). | ESR odezva example.version.1.1.xml |
| Příklad ESR odezvy (CZ) | Příklad ESR odezvy pro Českou republiku | Formát pro vzorovou XML odezvu na fiskální službu EFSTA v České republice | ESR odezva example (CZ).version.1.1.1.xml |

## <a name="setup"></a>Nastavení

### <a name="cash-registers"></a>Registrační pokladny

Každá registrační pokladna musí být nastavena pro komunikaci s fiskální sloužbou. Můžete nastavit registrační pokladny na stránce **Regstrační pokladny** (**Pohledávky** &gt; **Nastavení** &gt; **Registrační pokladny** &gt; **Registrační pokladny**). Následující tabulka podává další informace o požadovaném nastavení.

<table>
<thead>
<tr>
<th>Nastavení</th>
<th>Podrobnosti</th>
<th>Další informace</th>
</tr>
</thead>
<tbody>
<tr>
<td>Nastavení registrační pokladny</td>
<td>Zadejte adresu URL registrační pokladny, název instance Microsoft Azure Key Vault a název třídy.</td>
<td><ul>
<li><strong>URL adresa registrační pokladny</strong> – Zadejte adresu URL fiskální služby.
<p><strong>Upozornění:</strong> Služby třetích stran nebo jiné služby, které zde nakonfigurujete, nevyžadují certifikaci, a nemusí splňovat standardy společnosti Microsoft týkající se ochrany osobních údajů. Měli byste ověřit dokumentaci týkající se ochrany osobních údajů každé služby a kontaktovat poskytovatele každé služby, abyste se dozvěděli více informací o úrovni shody, kterou každá služba poskytuje. Jste sami zodpovědní za to, že se ujistíte, zda tyto služby splňují vaše bezpečnostní, ochranné a právní standardy. Odpovědnost za používání těchto služeb je pouze na vás. Společnost Microsoft vám nedává žádné výslovné záruky, garance ani podmínky. Důrazně doporučujeme používat pouze služby, které poskytují zabezpečené a autorizované připojení (to znamená služby, které používají protokol HTTPS).</p>
</li>
<li><strong>Název úložiště klíčů</strong> – Je-li fiskální služba přístupná na zabezpečeném připojení (to znamená, že adresa URL začíná https://), je třeba nastavit certifikáty a správně je uložit na obou stranách (aplikace Finance a fiskální služba třetí strany). V tomto poli vyberte název instance Azure Key Vault, kde je uložen certifikát aplikace Finance. Další informace naleznete v tématu <a href="https://support.microsoft.com/help/4040305/setting-up-a-key-vault-client">Nastavení klienta Azure Key Vault</a>.</li>
<li><strong>Název třídy</strong> – Vyberte třídu, kde jsou implementována specifika integrace s fiskální službou. Dostupná třída je <strong>CashRegisterProcessingEFSTA_W</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>Konfigurace</td>
<td>Pro každou registrační pokladnu vyberte formáty elektronického výkaznictví, které se použijí k tisku účtenek, odesílání požadavků do fiskální služby a přijímání odezvy od fiskální služby. Zvolené formáty elektronického výkaznictví musí odpovídat primární adrese právnické osoby.</td>
<td>Například pro formát účtenky vyberte <strong>Formátu hotovostní příjemky (AT)</strong> pro Rakousko a <strong>Formát hotovostní příjemky (CZ)</strong> pro Českou republiku.

Pokud formát nemůžete najít v seznamu, můžete stáhnout poslední elektronické formáty z LCS. Další informace viz <a href="https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs">Stažení konfigurace elektronického vykazování ze služby Lifecycle Services</a>.</td>
</tr>
<tr>
<td>Nastavení certifikátu registrační pokladny</td>
<td>Povolte použití certifikátů podepsaných svým držitelem.</td>
<td>
<ul>
<li><strong>Použít certifikát podepsaný svým držitelem</strong> – Nastavte tuto možnost na <strong>Ano</strong>, pokud budete používat certifikáty vygenerované a podepsané svým držitelem, které nelze přidat do seznamu důvěryhodných certifikátů.</li>
<li><strong>Kryptografický otisk certifikátu registrační pokladny</strong> – Zadejte kryptografický otisk certifikátu podepsaného svým držitelem, který je uložen ve fiskální službě a který bude použit k ověření certifikátu fiskální služby.</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="cash-register-locations"></a>Umístění registračních pokladen

Můžete nastavit umístění registrační pokladny na stránce **Umístění registrační pokladny** (**Pohledávky** &gt; **Nastavení** &gt; **Registrační pokladny** &gt; **Umístění registrační pokladny**).

#### <a name="prerequisites-for-the-czech-republic"></a>Předpoklady pro Českou republiku

Před nastavením umístění registrační pokladny pro právnickou osobu, která má svou primární adresu v České republice, postupujte takto.

1. Vytvořte typ daňové registrace pro ID podnikových prostor výběrem **Správa organizace** &gt; **Globální adresář** &gt; **Typy registrace** &gt; **Typy registrace**.

    Tento typ registrace by měl být omezen na **Organizace**.

2. Přidružte typ registrace ke kategorii registrace **ID podnikových prostor**:

    1. Zvolte **Správa organizace** &gt; **Globální adresář** &gt; **Typy registrace** &gt; **Kategorie registrace**.
    2. Vyberte typ registrace, který jste vytvořili dříve, a pak v poli **Kategorie registrace** vyberte **ID podnikových prostor**.

3. Přidružte ID podnikových prostor k adrese provozní jednotky, která bude použita pro umístění registrační pokladny.

    1. Zvolte **Správa organizace** &gt; **Obecné** &gt; **Organizace** &gt; **Interní organizace**.
    2. Vyberte organizaci pro přidružení k ID provozních prostor.
    3. Na pevné záložce **Adresy** vyberte **Další možnosti** &gt; **Rozšířené**.
    4. Na pevné záložce **ID registrace** vyberte **Přidat**.
    5. Vyberte typ registrace, který jste vytvořili dříve.
    6. Zadejte registrační číslo.

### <a name="create-cash-register-terminals"></a>Vytvoření terminálů registračních pokladen

Můžete vytvořit terminály registrační pokladny, které budou k dispozici pro umístění, a poté přiřadit registrační pokladny k terminálu na stránce **Terminály registrační pokladny** (**Pohledávky** &gt; **Nastavení** &gt; **Registrační pokladny** &gt; **Terminály registrační pokladny**).

### <a name="assign-the-user-to-a-person"></a>Přiřazení uživatele k osobě

Uživatel, který bude operátorem registrační pokladny a bude moct zaznamenávat hotovostní transakce, které jsou zaregistrovány v registrační pokladně, musí být přiřazen k osobě. Můžete přiřadit uživatele k osobě výběrem možnosti **Správa systému** &gt; **Uživatelé**.

### <a name="set-up-cash-register-operators"></a>Nastavit operátory registrační pokladny

Můžete nastavit operátory registrační pokladny, přiřadit je k umístění registrační pokladny a přiřadit výchozí terminál pomocí volby **Pohledávky** &gt; **Nastavení** &gt; **Registrační pokladna** &gt; **Operátoř registrační pokladny**.

### <a name="set-up-methods-of-payment-that-require-fiscal-registration"></a>Nastavení metody platby, která vyžaduje fiskální registraci

Můžete nastavit metody platby, které musí být registrovány v registrační pokladně. Zvolte **Pohledávky** &gt; **Nastavení** &gt; **Registrační pokladny** &gt; **Metody platby registrační pokladny** a poté nastavte následující pole.

| Pole | popis |
|---|---|
| Metoda platby | Vyberte metodu platby, která musí být registrována v registrační pokladně a odeslána fiskální službě. |
| Registrovat výši daně | Zaškrtnutím políčka označíte, že částky daně vztahující se k částce platby v hotovosti, musí být registrovány ve fiskální službě. |

#### <a name="important-notices"></a>Důležitá oznámení

V následujících situacích mohou být částky daně, které se vztahují k částce platby, spolehlivě identifikovány ze zaúčtovaných transakcí:

- Pro hotovostní platbu, která je automaticky zaúčtována při zaúčtování faktury platby na dobírku (podmínky platby na dobírku). V tomto případě jsou odeslané částky daně shodné jako částky daně vytvořené zaúčtováním faktury.
- Pro hotovostní zálohu, která je ručně zaúčtována z deníku plateb odběratele při výpočtu částky DPH a zaúčtování z deníku plateb. (Částky daně zaúčtované ze zálohy jsou vždy odeslány, bez ohledu na nastavení zaškrtávacího políčka **Registrovat výši daně**.)

Poraďte se s místním finančním úřadem ohledně určení požadavků pro registraci výše daně související s hotovostní platbou v registrační pokladně. Je třeba rozdělit způsoby platby podle potřeby.

V následujících situacích nemohou být částky daně, které se vztahují k částce platby, spolehlivě identifikovány ze zaúčtovaných transakcí:

- Pro hotovostní zálohu, která je ručně zaúčtována z deníku plateb odběratele a vyrovnána proti předchozí zaúčtované faktuře obsahující zaúčtovanou částku daně.

Pokud je metoda platby registrační pokladny nakonfigurována pro registraci částky daně, konkrétní distribuční logika částky vypočítá přibližnou výši daně, na základě částky platby v tomto scénáři.

V těchto případech se zobrazí správné částky daně pouze v zaúčtované faktuře, která je vyrovnána. Obraťte se na místní finanční úřady k určení správné metody pro odeslání fakturovaných částek daně ke kontrole finančního úřadu pro tyto situace.

### <a name="create-terms-of-payment-for-a-cod-scenario"></a>Vytvoření platebních podmínek pro scénáře platby na dobírku

Když lze přijmout hotovostní platbu při zaúčtování faktury, můžete vytvořit platební podmínky, které majíplatební metodu **Platba na dobírku**. Vyberte **Pohledávky** &gt; **Platba** &gt; **Platební podmínky** a poté nastavte následující pole.

| Pole | popis |
|---|---|
| Způsob platby | Zvolte **Platba na dobírku**. |
| Platba v hotovosti | Nastavte možnost na **Ano** pro vytvoření automatické platební transakce. |
| Hotovost | Vyberte účet hlavní knihy, který se používá k zaúčtování plateb v hotovosti, které jsou generovány automaticky. |

## <a name="example"></a>Příklad

Tato část vás provede následujícími obchodními procesy a používá fiskální službu [EFSTA](https://public.efsta.net/efr/) jako příklad:

- Po zaúčtování platby v hotovosti, která podléhá registraci, je vytvořena transakce registrační pokladny obsahující data, která je třeba podepsat. Tato transakce je potom odeslána, v určeném XML formátu, fiskální službě k registraci.
- Od fiskální služby obdržíte odezvu. Tato odezva má podpis a fiskální kódy, které fiskální služba generuje podle pravidel specifických pro zemi/oblast. Tato odezva je uložena ve finanční transakci registrační pokladny.
- Hotovostní příjemka je vytištěna. Tato účtenka obsahuje data transakce, podpis a fiskální kódy.

### <a name="register-an-automatically-posted-cod-payment-for-a-free-text-invoice-and-print-a-cash-receipt"></a>Registrace automaticky zaúčtované platby na dobírku pro volnou fakturu a tisk hotovostní příjemky

1. Zvolte **Pohledávky** &gt; **Volné faktury** &gt; **Všechny volné faktury**.
2. Vytvořte volnou fakturu. Více informací naleznete v tématu [Vytvoření volných faktur](../accounts-receivable/create-free-text-invoice-new.md). 
3. Na pevné záložce **Platba** vyberte metodu platby, která je nastavena jako metoda platby pro registrační pokladnu.
4. Vyberte platební podmínky, které jsou nastaveny pro platbu na dobírku.
5. Zvolte **Zaúčtovat**.
6. V dialogovém okně **Zaúčtovat volnou fakturu** proveďte následující kroky:

    1. Na pevné záložce **Parametry** vyberte zaškrtávací políčko **Vytisknout účtenku** pro tisk hotovostní příjemky po zaúčtování faktury.
    2. Na pevné záložce **Registrační pokladna** zkontrolujte umístění terminálu, registrační pokladnu a kódy operátora. Kód terminálu je automaticky vyplněn z pole **Výchozí terminál registrační pokladny** na stránce **Operátoři registrační pokladny**. Změňte kód terminálu pouze v případě, když je přijata hotovostní platba na jiném terminálu registrační pokladny, než který je k dispozici pro aktuálního operátora.
    3. Vyberte **OK**.

7. Zkontrolujte hotovostní příjemku, která je vygenerována pro zaúčtovanou fakturu. Ve výchozím nastavení je vygenerovaná hotovostní příjemka k dispozici jako soubor. Více informací o nastavení jiných cílových umístění, která můžete použít pro hotovostní příjemky, naleznete v tématu [Místa určení elektronického výkaznictví](../../dev-itpro/analytics/electronic-reporting-destinations.md).


### <a name="register-an-automatically-posted-cod-payment-for-a-sales-order-invoice-and-print-a-cash-receipt"></a>Registrace automaticky zaúčtované platby na dobírku pro fakturu prodejní objednávky a tisk hotovostní příjemky

1. Zvolte **Pohledávky** &gt; **Objednávky** &gt; **Všechny prodejní objednávky**.
2. Vytvořte prodejní objednávku. Další informace naleznete v tématu [Vytvoření prodejních objednávek](../../supply-chain/sales-marketing/tasks/create-sales-orders.md).
3. Na pevné záložce **Cena a sleva** vyberte metodu platby, která je nastavena jako metoda platby pro registrační pokladnu.
4. V poli **Platba** vyberte podmínky platby nastavené pro platbu na dobírku.
5. Zvolte **Faktura** &gt; **Faktura**.
6. Na pevné záložce **Parametry** nastavte možnost **Vytisknout účtenku** na **Ano** pro tisk hotovostní příjemky po zaúčtování faktury.
7. Na pevné záložce **Registrační pokladna** zkontrolujte umístění terminálu, registrační pokladnu a kódy operátora. Změňte informace podle potřeby. Kód terminálu je automaticky vyplněn z pole **Výchozí terminál registrační pokladny** na stránce **Operátoři registrační pokladny**. Změňte kód terminálu pouze v případě, když je přijata hotovostní platba na jiném terminálu registrační pokladny, než který je k dispozici pro aktuálního operátora.

### <a name="register-a-customer-payment-from-the-customer-payment-journal-and-print-a-cash-receipt"></a>Registrace platby odběratele z deníku plateb odběratele a tisk hotovostní příjemky

1. Vyberte **Pohledávky** &gt; **Deníky** &gt; **Platby** &gt; **Deník plateb** pro otevření deníku plateb odběratele. (Nebo můžete vybrat **Hlavní kniha** &gt; **Deníky** &gt; **Hlavní deník** pro otevření hlavního deníku.)
2. Vytvořte řádky deníku s hotovostní platbou odběratele.
3. Na kartě **Platba** vyberte metodu platby, která je nastavena jako metoda platby pro registrační pokladnu.
4. Zvolte zaškrtávací políčko **Zálohový doklad deníku**, pokud je platbou záloha.
5. Na kartě **Platba** zkontrolujte umístění terminálu, registrační pokladnu a kódy operátora. Změňte informace podle potřeby. Kód terminálu je automaticky vyplněn z pole **Výchozí terminál registrační pokladny** na stránce **Operátoři registrační pokladny**. Změňte kód terminálu pouze v případě, když je přijata hotovostní platba na jiném terminálu registrační pokladny, než který je k dispozici pro aktuálního operátora.
6. Vyberte **Zaúčtovat** &gt; **Zaúčtovat**.
7. Vyberte **Tisk** &gt; **Hotovostní příjemka** pro tisk příjemky obsahující fiskální kódy.

### <a name="register-a-customer-payment-from-the-slip-journal-and-print-a-cash-order-that-includes-cash-receipt-information-czech-republic-only"></a>Registrace platby odběratele z deníku dokladu a tisk hotovostního dokladu obsahujícího informace o hotovostní příjemce (pouze Česká republika)

1. Vyberte **Pokladna a banka** &gt; **Deníky** &gt; **Deník dokladů**.
2. Vytvořte řádky deníku s hotovostní platbou odběratele.
3. Na kartě **Platba** zkontrolujte pole v části **Registrační pokladna**. Kód terminálu je automaticky vyplněn z pole **Výchozí terminál registrační pokladny** na stránce **Operátoři registrační pokladny**. Změňte kód terminálu pouze v případě, když byla přijata hotovostní platba na jiném terminálu registrační pokladny. 
4. Vyberte **Schválení dokumentů** &gt; **Schválit**. Číslo hotovostního dokladu je přiřazeno k platbě.
5. Vyberte **Zaúčtovat** &gt; **Zaúčtovat**.
6. Vyberte **Tisk** &gt; **Hotovostní doklad** pro tisk hotovostního dokladu obsahujícího fiskální kódy.

### <a name="cancel-a-payment"></a>Zrušení platby

Pokud bylo zaregistrováno číslo hotovostní příjemky pro platbu v registrační pokladně a pak jste zrušili platbu, bude ve stejné registrační pokladně zaregistrováno nové číslo hotovostní příjemky. Hotovostní příjemka zrušení platby obsahuje stejné částky jako původní příjemka, ale částky mají záporné znaménko.

1. Otevřete stránku **Transakce odběratele**:

    1. Zvolte **Pohledávky** &gt; **Odběrateléi** &gt; **Všichni odběratelé**.
    2. Vyberte odběratele.
    3. V podokně akcí zvolte **Odběratel** &gt; **Transakce**.

2. Vyberte platební transakci ke zrušení.
3. Zvolte **Stornovat** &gt; **Zrušení platby**.
3. Zadejte požadované informace a poté vyberte **OK** pro vytvoření transakce zrušení platby a přejdete zpět na stránku **Transakce odběratele**.
4. Vyberte novou transakci zrušení platby a poté vyberte **Tisk** &gt; **Hotovostní příjemka** pro tisk hotovostní příjemky obsahující fiskální kódy.

### <a name="review-cash-register-fiscal-transactions-and-resend-a-transaction-to-the-cash-register"></a>Zkontrolovat fiskální transakce registrační pokladny a znovu odešlete transakci do registrační pokladny.

Můžete zkontrolovat hotovostní platby, které byly zaregistrovány, a vytisknout znovu původní hotovostní příjemku nebo ji zkopírovat pomocí volby **Tisk** v možnostech **Pohledávky** &gt; **Dotazy** &gt; **Fiskální transakce registrační pokladny**.

Zákon popisuje výjimky, se kterými by měla fiskální služba správně zacházet. Pokud nebyla hotovostní platba úspěšně zaregistrována z důvodu, které nesouvisí s jednou z těchto výjimek, obdržíte chybové hlášení po zaúčtování hotovostní platby. Transakce registrační pokladny, která má stav **Vytvořeno**, bude k dispozici na stránce **Fiskální transakce registrační pokladny**. Musíte opravit problémy a ručně opětovné odeslat vytvořené hotovostní transakce do registrační pokladny. V opačném případě nelze vytisknout hotovostní příjemku obsahující fiskální kódy. Pokud je hotovostní platba správně zaregistrována, má stav **Registrováno**.

V následující tabulce jsou popsána pole pro platební transakce registrační pokladny.

<table>
<thead>
<tr>
<th>Pole</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr>
<td>Registrační pokladna</td>
<td>ID registrační pokladny.</td>
</tr>
<tr>
<td>ID transakce</td>
<td>ID transakce v registrační pokladně. Tato hodnota je přijata z fiskální služby.</td>
</tr>
<tr>
<td>Adresa URL registrační pokladny</td>
<td>Adresa URL místa fiskální služby.</td>
</tr>
<tr>
<td>Stav</td>
<td>Stav transakce. Používají se následující hodnoty:
<ul>
<li><strong>Vytvořeno</strong> – Byla zaúčtována platební transakce, ale nebyla zaregistrována.</li>
<li><strong>Registrováno</strong> – Byla zaúčtována platební transakce a byla zaregistrována. (Jinými slovy, odeslali jste platební transakci do fiskální služby a obdrželi jste odezvu s fiskálními kódy.)</li>
</ul></td>
</tr>
<tr>
<td>(CZ/Česká republika) Offline</td>
<td>Indikátor, že platební transakce byla zaregistrována offline (povolená výjimka) a byl přijat PKP (kód podpisu).</td>
</tr>
<tr>
<td>Terminál</td>
<td>Kód terminálu registrační pokladny.</td>
</tr>
<tr>
<td>Operátor</td>
<td>Kód operátora registrační pokladny.</td>
</tr>
<tr>
<td>Doklad</td>
<td>Číslo dokladu zaúčtované hotovostní transakce.</td>
</tr>
<tr>
<td>Datum</td>
<td>Datum transakce.</td>
</tr>
<tr>
<td>Číslo příjemky</td>
<td>Číslo hotovostní příjemky.</td>
</tr>
<tr>
<td>Datum a čas transakce</td>
<td>Datum a čas registrované transakce. Tato hodnota je přijata z fiskální služby.</td>
</tr>
<tr>
<td>Částka na účtence</td>
<td>Částka platby.</td>
</tr>
<tr>
<td>Měna</td>
<td>Měna platby.</td>
</tr>
<tr>
<td>Jméno</td>
<td>Název fiskálního kódu přijatého z fiskální služby. Lze použít následující hodnoty:
<ul>
<li><strong>Info</strong> – Další informace</li>
<li>(AT/Rakousko) <strong>Kód</strong> – Podpis</li>
<li>(AT/Rakousko) <strong>Odkaz</strong> – Odkaz závislý na podpisu</li>
</ul>
</td>
</tr>
<tr>
<td>Štítek</td>
<td>Popisek fiskálního kódu přijatého z fiskální služby. Lze použít následující hodnoty:
<ul>
<li>(CZ/Česká republika) <strong>FIK</strong> – Fiskální identifikační kód</li>
<li>(CZ/Česká republika) <strong>BKP</strong> – Bezpečnostní kód</li>
<li>(CZ/Česká republika) <strong>PKP</strong> – Kód popdisu (Tento kód se vrací v případě registrace offline.)</li>
</ul>
</td>
</tr>
<tr>
<td>Hodnota</td>
<td>Hodnota fiskálního kódu přijatého z fiskální služby.</td>
</tr>
<tr>
<td>Hodnota</td>
<td>Procento registrované daně.</td>
</tr>
<tr>
<td>Částka prodejní daně</td>
<td>Částka registrované daně.</td>
</tr>
<tr>
<td>Hrubá částka</td>
<td>Částka reghistrované platby.</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]