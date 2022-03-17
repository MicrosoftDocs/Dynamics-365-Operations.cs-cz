---
title: Přehled faktur dodavatele
description: V tomto tématu jsou obecné informace o fakturách dodavatele.
author: abruer
ms.date: 02/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b54a60ac3b1868ea7cc5ed88d5a31203b4bd29d3
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358410"
---
# <a name="vendor-invoices-overview"></a>Přehled faktur dodavatele

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


V tomto tématu jsou obecné informace o fakturách dodavatele. Faktury dodavatele jsou požadavky na platbu za produkty a služby. Faktury dodavatele mohou představovat účet za průběžné služby nebo mohou být založeny na nákupních objednávkách specifického zboží a služeb.

## <a name="vendor-invoices"></a>Faktury dodavatele

Faktura dodavatele z nákupní objednávky je vytvořena při přijetí produktů nebo služeb podle nákupní objednávky, kterou jste uskutečnili s dodavatelem. Faktura dodavatele obsahuje hlavičku a jeden nebo více řádků se zbožím nebo službami. Faktura dodavatele představuje konec cyklu nákupní objednávky, příjemky produktu a faktury dodavatele.

Ačkoliv jsou některé faktury dodavatele propojeny s nákupní objednávkou, mohou faktury dodavatele obsahovat také řádky, které neodpovídají řádkům nákupní objednávky. Můžete vytvořit také faktury dodavatele, které nejsou přidruženy k žádné nákupní objednávce. Tyto faktury dodavatele mohou představovat probíhající služby, například fakturu za služby. Když přidáte probíhající službu, nemusíte odkazovat na nákupní objednávku.

Je několik způsobů, jak zadat fakturu dodavatele:

- Registr faktur dodavatele umožňuje rychle zadat faktury, které neodkazují na nákupní objednávky, abyste mohli určovat časově rozlišené výdaje. Pomocí deníku schválení faktur dodavatelů můžete tyto faktury vybrat a zaúčtovat je do zůstatku dodavatele a časové rozlišení tak stornovat.
- Deník faktur dodavatele slouží k rychlému zadání faktur, které neodkazují na nákupní objednávku, v jediném kroku.
- Spolu s evidencí faktur dodavatele slouží registr faktur dodavatele k rychlému zadání faktur, které mají mít časově rozlišené výdaje. Přidružené nákupní objednávky můžete později otevřít k zaúčtování faktury na účet výdajů.
- Stránky **Otevřít faktury dodavatele** a **Nevyřízené faktury dodavatele** slouží k vytváření faktur dodavatele z potvrzených nákupních objednávek.

V následující diskusi naleznete více informací o použití stránek **Otevřít faktury dodavatele** nebo **Nevyřízené faktury dodavatele** k vytvoření faktury dodavatele z nákupní objednávky.

## <a name="understanding-invoice-line-quantities"></a>Princip množství na řádcích faktury

Při otevření faktury dodavatele ze související nákupní objednávky systém vytvoří řádky faktury z nákupní objednávky. Dle výchozího nastavení systém převezme množství z příjemky produktu. Můžete však použít některé z následujících výchozích chování:

- **Množství nynějšího příjmu** – tuto možnost použijte pro částečné dodávky. Výchozí hodnota v poli **Množství** bude nastavena na množství určené v poli **Přijmout nyní** na nákupní objednávce.
- **Objednané množství** – tuto možnost použijte pro úplné dodávky. Výchozí hodnota v poli **Množství** bude nastavena na množství určené v poli **Objednáno** na nákupní objednávce.
- **Registrované množství** – tuto možnost použijte, pokud položka vyžaduje registraci určuje se na stránce **Skupiny modelů položek**. Výchozí hodnota v poli **Množství** je fyzické upravené množství, které bylo zaregistrováno.
- **Množství v příjemce produktu** – tuto možnost použijte, pokud pro danou objednávku již byla přijata příjemka produktu. Výchozí hodnota v poli **Množství** je celkové množství dostupných příjemek produktu.
- **Registrované množství a služby** – tuto možnost použijte, pokud byla množství registrována v deníku doručených položek pro položky na skladě nebo položky, které nejsou na skladě. Tato možnost zahrnuje také služby bez ohledu na to, zda jsou registrovány.

Používá-li vaše právnická osoba párování faktur, můžete si zobrazit výsledky párování množství ve sloupci **Spárování množství v příjemce produktu**. K zobrazení výsledků párování množství můžete použít také tlačítko **Podrobnosti o párování** na kartě podokna akcí **Kontrola**.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Přidání řádku, který nebyl v nákupní objednávce

Do faktury dodavatele můžete přidat řádek, který nebyl na nákupní objednávce. Je nutné vybrat číslo položky nebo kategorii zásobování. Poté lze na řádek přidat množství, ceny a částky. Řádek bude zahrnut pouze v zásadách párování pro součty faktur.

## <a name="submitting-a-vendor-invoice-for-review"></a>Odeslání faktury dodavatele ke kontrole

Vaše organizace může využívat workflowy ke správě procesu kontroly faktur dodavatele. Hlavička faktury, řádek faktury, nebo obojí může vyžadovat přezkoumání pracovního postupu. Ovládací prvky workflow se použijí na záhlaví nebo řádek podle toho, která část byla před zvolením ovládacího prvku aktivní. Namísto tlačítka **Zaúčtovat** se tlačítko **Odeslat** odesílá faktury dodavatele do procesu kontroly.

### <a name="preventing-invoice-from-being-submitted-to-workflow"></a>Zabránění odeslání faktury do workflowu 

Následuje několik způsobů, jak lze zabránit odeslání faktury do workflowu.

- **Celková částka faktury a zaregistrovaná celková částka se neshodují.** Osoba, která předložila fakturu, obdrží upozornění, že součty nejsou stejné. Výstraha poskytuje příležitost opravit zůstatky před opětovným odesláním faktury do workflow. Tato funkce je k dispozici, pokud je zapnutý parametr **Zabránit odeslání do workflowu, když liší celková částka faktury a registrovaná celková částka** na stránce **Správa funkcí**. 
- **Faktura obsahuje nepřidělené náklady.** Osoba, která odeslala fakturu, obdrží výstrahu, že faktura obsahuje nepřidělené částky, takže může opravit fakturu před opětovným odesláním do workflowu. Tato funkce je k dispozici, pokud je zapnutý parametr **Zabránit odeslání do workflowu, když existují nepřidělené částky na faktuře dodavatele** na stránce **Správa funkcí**.
- **Faktura obsahuje stejné číslo faktury jako jiná zaúčtovaná faktura.** Osoba, která odeslala fakturu, obdrží zprávu s oznámením, že byla nalezena faktura s duplicitním číslem. Duplicitní číslo lze opravit před opětovným odesláním faktury do pracovního postupu. Tato výstraha se zobrazí, pokud je parametr **Zkontrolovat použité číslo faktury** v závazcích nastaven na **Zamítnout duplikaci**. Tato funkce je k dispozici , pokud je zapnutý parametr **Zabránit odeslání do workflowu, pokud číslo faktury již existuje na zaúčtované faktuře a systém není nastaven, aby přijímal duplicitní čísla faktur** na stránce **Správa funkcí**.
- **Faktura obsahuje řádek, kde je množství faktury menší než shodné množství příjmu produktu.** Osoba, která předloží fakturu nebo se pokusí zaúčtovat, obdrží zprávu, že množství není stejné. Zpráva poskytuje příležitost opravit hodnoty před opětovným odesláním faktury do workflow. Tato funkce je k dispozici, pokud je parametr **Blokovat účtování a odesílání faktur dodavatele do pracovního postupu** na stránce **Správa funkcí** zapnuty a parametr **Blokovat zveřejňování a odesílání do pracovního postupu** na stránce **Parametry závazků** je zapnutý.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Spárování faktur dodavatele s příjemkami produktu

Podle potřeby můžete zadávat a ukládat informace o fakturách dodavatele a porovnat řádky faktury s řádky příjemky produktu. Také můžete spárovat částečná množství pro řádek.

Fakturu dodavatele lze vytvořit na základě řádkových položek příjemek produktu, které byly přijaty do dnešního data, a to i tehdy, když všechny položky určité nákupní objednávky nebyly dosud přijaty. Tuto možnost můžete využít například tehdy, když dodavatel zasílá jednou za měsíc fakturu pokrývající všechny jím odeslané dodávky v daném měsíci. Každá příjemka produktu představuje částečnou nebo úplnou dodávku položek uvedených v nákupní objednávce.

Když je faktura ve workflow, schvalovatel může aktualizovat množství faktur tak, aby odpovídala hodnotě v poli **Product-receipt-quantity-to-match**. Chcete-li tak učinit, vyberte funkci **Aktualizovat množství faktur tak, aby odpovídala množství příjemek ve workflow** v pracovním prostoru **Správa funkcí** a vyberte **Povolit**. Pokud schvalovatel v procesu pracovního postupu odstranil všechny shody ze všech příjemek z řádku faktury, řádek faktury bude odstraněn. Pokud tato funkce není povolena, množství faktur se u faktur ve workflow neaktualizuje.

Při zaúčtování faktury je množství v poli **Zůstatek faktury** u každé položky aktualizováno celkovým počtem přijatého množství z vybraných příjemek produktu. Pokud bude množství **Zůstatek faktury** i množství **Zbývá dodat** pro všechny položky na nákupní objednávce nulové (0), stav nákupní objednávky se změní na hodnotu **Fakturováno**. Pokud množství v poli **Zůstatek faktury** není nulové (0), stav nákupní objednávky se nezmění a k této objednávce je možné zadat další faktury.

Tato možnost předpokládá, že pro nákupní objednávku byla zaúčtována alespoň jedna příjemka produktu. Faktura dodavatele je založena na těchto příjemkách produktu a odráží na nich uvedená množství. Finanční údaje pro fakturu jsou založeny na údajích zadaných při zaúčtování faktury.

Více informací naleznete v tématu [Zaznamenání faktury dodavatele a spárování s přijatým množstvím](../accounts-payable/tasks/record-vendor-invoice-match-against-received-quantity.md)

## <a name="configure-an-automated-task-for-vendor-invoice-workflow-to-post-the-vendor-invoice-using-a-batch-job"></a>Konfigurace automatizované úlohy pro workflow faktury dodavatele za účelem zaúčtování faktury dodavatele pomocí dávkové úlohy

Můžete přidat automatizovanou úlohu zaúčtování do workflowu faktury dodavatele, aby byly faktury zpracovány v dávce. Zaúčtování faktur v dávce umožňuje pokračovat v procesu workflowu, aniž by bylo nutné čekat na dokončení zaúčtování, což zlepšuje celkový výkon všech úloh odeslaných do workflowu.

Chcete-li zaúčtovat fakturu dodavatele v dávce, zapněte na stránce **Správa funkcí** parametr **Dávkové zaúčtování faktur dodavatele**. Workflowy faktur dodavatele jsou konfigurovány přechodem na **Závazky > Nastavení > Workflowy závazků**.

V editor workflowů se nachází úloha **Zaúčtovat faktury dodavatele pomocí dávky** bez ohledu na to, zda je povolen parametr funkce **Dávkové zaúčtování faktur dodavatele**. Není-li parametr funkce povolen, faktura obsahující úlohu **Zaúčtovat faktury dodavatele pomocí dávky** nebude zpracována v rámci workflowu, dokud není parametr povolen. Úloha **Zaúčtovat faktury dodavatele pomocí dávky** nesmí být použita ve stejném workflowu jako automatizovaná úloha **Zaúčtovat faktury dodavatele**. Kromě toho úloha **Zaúčtovat faktury dodavatele pomocí dávky** by měla být posledním prvkem v konfiguraci workflowu.

Můžete zadat počet faktur, které mají být zahrnuty do dávky, a počet hodin, jak dlouho se má čekat před přeplánováním dávky, pomocí nastavení **Závazky > Nastavení > Parametry závazků > Faktura > Worflow faktury**. 

## <a name="working-with-multiple-invoices"></a>Práce s více fakturami

Můžete pracovat s více fakturami současně a zaúčtovat je všechny najednou. Pokud je nutné vytvořit více faktur, použijte stránku **Nevyřízené faktury dodavatele**. Potřebujete-li zaúčtovat a vytisknout více faktur dodavatele, použijte **Deník pro schvalování faktur**. Když používáte **deník pro schvalování faktur**, musí být pro nákupní objednávku zaúčtována alespoň jedna příjemka produktu a faktura pro nákupní objednávku musí být zaúčtována do registru faktur. Finanční informace pro fakturu pocházejí z faktury zaúčtované do registru.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>Obnovení faktur dodavatele, které se používají

Když se používá faktura dodavatele, nemůže být upravena jiným uživatelem. Stav faktury však může někdy znamenat, že se faktura používá, i když není aktivně upravována. Aplikace například mohla přestat odpovídat, když byla faktura upravována, nebo uživatel může nechtěně nechat otevřenou fakturu v aplikaci.

Můžete použít stránku **Obnovit faktury dodavatel** pro obnovení nebo uvolnění faktur dodavatele, které byly používány déle než čtyři hodiny, aby mohly být upraveny. Můžete otevřít tuto stránku z navigace **Periodická úloha** nebo dlaždice v pracovním prostoru **Záznam faktury dodavatele**. Po obnovení faktury bude k dispozici pro úpravy na stránce **Faktura dodavatele**.

Na stránku **Obnovit faktury dodavatele** budete mít přístup pouze v případě, že vám je přiděleno funkční oprávnění zabezpečení **Obnovit používané faktury dodavatele**. Kromě toho musí být zapnutý parametr **Povolit obnovení faktury dodavatele** na stránce **Parametry závazků**.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>Resetování stavu workflow pro faktury dodavatele z Bez možnosti obnovy na Koncept

Instance workflow, která byla zastavena kvůli neobnovitelné chybě, bude míst stav workflow **Bez možnosti obnovy**. Pokud je stav faktury dodavatele **Bez možnosti obnovy**, můžete ho obnovit do stavu **Koncept** výběrem možnosti **Obnovit**. Poté můžete upravit fakturu dodavatele. Tato funkce je k dispozici, pokud je zapnutý parametr **Resetování stavu workflowu pro faktury dodavatele z Bez možnosti obnovy na Koncept** na stránce **Správa funkcí**.

Na stránce **Historie workflowu** můžete resetovat stav workflow na **Koncept**. Tuto stránku můžete otevřít **Faktury dodavatele** nebo z navigace **Obecné > Dotazy > Workflow**. Chcete-li obnovit stav workflow na **Koncept**, vyberte možnost **Obnovit**. Stav workflow můžete také resetovat na koncept výběrem akce **Obnovit** na stránce **Faktura dodavatele** nebo **Čekající faktury dodavatele**. Po resetování stavu workflow na **Koncept** bude k dispozici pro úpravy na stránce **Faktura dodavatele**.

## <a name="viewing-the-invoice-total-on-the-pending-vendor-invoices-page"></a>Zobrazení celkové fakturované částky na stránce Čekající faktury dodavatele

Celkovou fakturovanou částku můžete zobrazit na stránce **Čekající faktury dodavatele** povolením parametru **Zobrazit součet faktur na seznamu čekajících faktur dodavatele vyřízení** na stránce **Parametry závazků**. 

## <a name="vendor-open-transactions-report"></a>Sestava otevřených transakcí dodavatelů

Sestava **Otevřené transakce dodavatele** poskytuje podrobné informace o otevřených transakcích pro každého dodavatele k datu, které zadáte. Tato sestava se často používá během auditního postupu pro ověření zůstatků mezi transakcemi v knize dodavatelů a transakcemi na účtu hlavní knihy.

Pro každou transakci obsahuje sestava následující údaje:

- Číslo faktury
- Datum transakce
- Číslo dokladu
- Částka transakce v měně transakce a účetní měně
- Kreditní zůstatek v měně transakce a účetní měně
- Debetní zůstatek v měně transakce a účetní měně
- Částka mezisoučtu v zúčtovací měně
- Datum splatnosti platby

### <a name="filter-the-data-on-the-report"></a>Filtrování dat v sestavě

Při generování sestavy **Otevřené transakce dodavatele** jsou k dispozici následující výchozí parametry. Slouží k filtrování dat, která se zobrazí v sestavě.

- **Vyloučit budoucí vypořádání** – Toto zaškrtávací políčko zaškrtněte, chcete-li vyloučit transakce, které jsou vypořádány po datu zadaném do pole **Otevřené transakce za**.
- **Otevřené transakce za** – Zadejte datum pro zahrnutí transakcí, které jsou k tomuto datu otevřené. Pokud nezadáte datum, toto pole je nastaveno na maximální datum. (Maximální datum je nejzazší datum, které systém přijme, 31. prosince 2154.) Ve výchozím nastavení bude toto pole při příštím spuštění sestavy nastaveno jako poslední datum, které do něj bylo zadáno.

Můžete použít filtry pod polem **Záznam k zahrnutí** pro další omezení transakčních dat, která jsou zahrnuta ve zprávě.

## <a name="additional-resources"></a>Další prostředky

- [Nastavit zásady faktur dodavatele](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [Zadání dat faktur do systému závazků pomocí faktury dodavatele](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [Zadání dat faktury do závazků s použitím deníku schválení](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [Zadání dat faktury do systému závazků s použitím evidence faktur](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [Zaznamenání faktury dodavatele do deníku faktur](tasks/record-vendor-invoice-invoice-journal.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
