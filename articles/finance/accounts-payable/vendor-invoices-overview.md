---
title: Přehled faktur dodavatele
description: V tomto tématu jsou obecné informace o fakturách dodavatele. Faktury dodavatele jsou požadavky na zaplacení za přijaté produkty a služby. Faktury dodavatele mohou představovat účet za průběžné služby nebo mohou být založeny na nákupních objednávkách specifického zboží a služeb.
author: abruer
manager: AnnBe
ms.date: 07/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b9708c37f10cd08e6b98167fe24d9ae0380c3dac
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772161"
---
# <a name="vendor-invoices-overview"></a>Přehled faktur dodavatele

[!include [banner](../includes/banner.md)]

V tomto tématu jsou obecné informace o fakturách dodavatele. Faktury dodavatele jsou požadavky na zaplacení za přijaté produkty a služby. Faktury dodavatele mohou představovat účet za průběžné služby nebo mohou být založeny na nákupních objednávkách specifického zboží a služeb.

## <a name="vendor-invoices"></a>Faktury dodavatele

Faktura dodavatele z nákupní objednávky je faktura, která je vytvořena při přijetí produktů nebo služeb podle nákupní objednávky, kterou jste uskutečnili s dodavatelem. Faktura dodavatele obsahuje hlavičku a jeden nebo více řádků se zbožím nebo službami. Faktura dodavatele představuje konec cyklu nákupní objednávky, příjemky produktu a faktury dodavatele.

Ačkoliv jsou některé faktury dodavatele propojeny s nákupní objednávkou, mohou faktury dodavatele obsahovat také řádky, které neodpovídají řádkům nákupní objednávky. Můžete vytvořit také faktury dodavatele, které nejsou přidruženy k žádné nákupní objednávce. Tyto faktury dodavatele mohou představovat probíhající služby, jako například provozní účet, takže při jejich přidání nemusíte odkazovat na nákupní objednávku.

Je několik způsobů, jak zadat fakturu dodavatele:

- Registr faktur dodavatele umožňuje rychle zadat faktury, které neodkazují na nákupní objednávky, abyste mohli určovat časově rozlišené výdaje. Pomocí deníku schválení faktur dodavatelů můžete tyto faktury vybrat a zaúčtovat je do zůstatku dodavatele a časové rozlišení tak stornovat.
- Deník faktur dodavatele slouží k rychlému zadání faktur, které neodkazují na nákupní objednávku, v jediném kroku.
- Spolu s evidencí faktur dodavatele slouží registr faktur dodavatele k rychlému zadání faktur, které mají mít časově rozlišené výdaje. Přidružené nákupní objednávky můžete později otevřít k zaúčtování faktury na účet výdajů.
- Stránky **Otevřít faktury dodavatele** a **Nevyřízené faktury dodavatele** slouží k vytváření faktur dodavatele z potvrzených nákupních objednávek.

V následující diskusi naleznete více informací o použití stránek **Otevřít faktury dodavatele** nebo **Nevyřízené faktury dodavatele** k vytvoření faktury dodavatele z nákupní objednávky.

## <a name="understanding-invoice-line-quantities"></a>Princip množství na řádcích faktury

Při otevření faktury dodavatele ze související nákupní objednávky se řádky faktury vytvoří z nákupní objednávky. Dle výchozího nastavení se množství převezme z množství na příjemce produktu. Můžete však použít některé z následujících výchozích chování:

- **Množství nynějšího příjmu** – tuto možnost použijte pro částečné dodávky. Výchozí hodnota v poli **Množství** se převezme z množství určeného v poli **Přijmout nyní** na nákupní objednávce.
- **Objednané množství** – tuto možnost použijte pro úplné dodávky. Výchozí hodnota v poli **Množství** se převezme z množství určeného v poli **Objednáno** na nákupní objednávce.
- **Registrované množství** – tuto možnost použijte, pokud položka vyžaduje registraci (určuje se na stránce **Skupiny modelů položek**. Výchozí hodnota v poli **Množství** je fyzické upravené množství, které bylo zaregistrováno.
- **Množství v příjemce produktu** – tuto možnost použijte, pokud pro danou objednávku již byla přijata příjemka produktu. Výchozí hodnota v poli **Množství** se převezme z celkového množství dostupných příjemek produktu.
- **Registrované množství a služby** – tuto možnost použijte, pokud byla množství registrována v deníku doručených položek pro položky na skladě nebo položky, které nejsou na skladě. Tato možnost zahrnuje také služby bez ohledu na to, zda jsou registrovány.

Používá-li vaše právnická osoba párování faktur, můžete si zobrazit výsledky párování množství ve sloupci **Spárování množství v příjemce produktu**. K zobrazení výsledků párování množství můžete použít také tlačítko **Podrobnosti o párování** na kartě podokna akcí **Kontrola**.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Přidání řádku, který nebyl v nákupní objednávce

Do faktury dodavatele můžete přidat řádek, který nebyl na nákupní objednávce. Je nutné vybrat číslo položky nebo kategorii zásobování. Poté lze na řádek přidat množství, ceny a částky. Řádek bude zahrnut pouze v zásadách párování pro součty faktur.

## <a name="submitting-a-vendor-invoice-for-review"></a>Odeslání faktury dodavatele ke kontrole

Vaše organizace může využívat workflowy ke správě procesu kontroly faktur dodavatele. Hlavička faktury, řádek faktury, nebo obojí může vyžadovat přezkoumání pracovního postupu. Ovládací prvky workflow se použijí na záhlaví nebo řádek podle toho, která část byla před zvolením ovládacího prvku aktivní. Namísto tlačítka **Zaúčtovat** se zobrazí tlačítko **Odeslat**, které slouží k odeslání faktury dodavatele do procesu kontroly.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Spárování faktur dodavatele s příjemkami produktu

Podle potřeby můžete zadávat a ukládat informace o fakturách dodavatele a porovnat řádky faktury s řádky příjemky produktu. Také můžete spárovat částečná množství pro řádek.

Fakturu dodavatele lze vytvořit na základě řádkových položek příjemek produktu, které byly přijaty do dnešního data, a to i tehdy, když všechny položky určité nákupní objednávky nebyly dosud přijaty. Tuto možnost můžete využít například tehdy, když dodavatel zasílá jednou za měsíc fakturu pokrývající všechny jím odeslané dodávky v daném měsíci. Každá příjemka produktu představuje částečnou nebo úplnou dodávku položek uvedených v nákupní objednávce.

Při zaúčtování faktury je množství v poli **Zůstatek faktury** u každé položky aktualizováno celkovým počtem přijatého množství z vybraných příjemek produktu. Pokud bude množství **Zůstatek faktury** i množství **Zbývá dodat** pro všechny položky na nákupní objednávce nulové (0), stav nákupní objednávky se změní na hodnotu **Fakturováno**. Pokud množství v poli **Zůstatek faktury** není nulové (0), stav nákupní objednávky se nezmění a k této objednávce je možné zadat další faktury.

Tato možnost předpokládá, že pro nákupní objednávku byla zaúčtována alespoň jedna příjemka produktu. Faktura dodavatele je založena na těchto příjemkách produktu a odráží na nich uvedená množství. Finanční údaje pro fakturu jsou založeny na údajích zadaných při zaúčtování faktury.

Více informací naleznete v tématu [Zaznamenání faktury dodavatele a spárování s přijatým množstvím](../accounts-receivable/tasks/record-vendor-invoice-match-against-received-quantity.md)

## <a name="working-with-multiple-invoices"></a>Práce s více fakturami

Můžete pracovat s více fakturami současně a zaúčtovat je všechny najednou. Pokud je nutné vytvořit více faktur, použijte stránku **Nevyřízené faktury dodavatele**. Potřebujete-li zaúčtovat a vytisknout více faktur dodavatele, použijte deník pro schvalování faktur. Když používáte deník pro schvalování faktur, musí být pro nákupní objednávku zaúčtována alespoň jedna příjemka produktu a faktura pro nákupní objednávku musí být zaúčtována do registru faktur. Finanční informace pro fakturu pocházejí z faktury zaúčtované do registru.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>Obnovení faktur dodavatele, které se používají

Když se používá faktura dodavatele, nemůže být upravena jiným uživatelem. Stav faktury však může někdy znamenat, že se faktura používá, i když není aktivně upravována. Aplikace například mohla přestat odpovídat, když byla faktura upravována, nebo uživatel může nechtěně nechat otevřenou fakturu v aplikaci.

Můžete použít stránku **Obnovit faktury dodavatel** pro obnovení nebo uvolnění faktur dodavatele, které byly používány déle než čtyři hodiny, aby mohly být upraveny. Můžete otevřít tuto stránku z navigace **Periodická úloha** nebo dlaždice v pracovním prostoru **Záznam faktury dodavatele**. Po obnovení faktury bude k dispozici pro úpravy na stránce **Faktura dodavatele**.

Na stránku **Obnovit faktury dodavatele** budete mít přístup pouze v případě, že vám je přiděleno funkční oprávnění zabezpečení **Obnovit používané faktury dodavatele**. Kromě toho musí být zapnutý parametr **Povolit obnovení faktury dodavatele** na stránce **Parametry závazků**.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>Resetování stavu workflow pro faktury dodavatele z Bez možnosti obnovy na Koncept

Instance workflow, která byla zastavena kvůli neobnovitelné chybě, bude míst stav workflow **Bez možnosti obnovy**. Pokud je stav faktury dodavatele **Bez možnosti obnovy**, můžete ho obnovit do stavu **Koncept** výběrem možnosti **Obnovit**. Poté můžete upravit fakturu dodavatele. Tato funkce je k dispozici, pokud je zapnutý parametr **Resetovat stav konceptu workflow faktury dodavatele** na stránce **Správa funkcí**.

Na stránce **Historie workflowu** můžete resetovat stav workflow na **Koncept**. Tuto stránku můžete otevřít **Faktury dodavatele** nebo z navigace **Obecné > Dotazy > Workflow**. Chcete-li obnovit stav workflow na **Koncept**, vyberte možnost **Obnovit**. Stav workflow můžete také resetovat na koncept výběrem akce **Obnovit** na stránce **Faktura dodavatele** nebo **Čekající faktury dodavatele**. Po resetování stavu workflow na **Koncept** bude k dispozici pro úpravy na stránce **Faktura dodavatele**.



## <a name="additional-resources"></a>Další zdroje

- [Nastavení zásad faktur dodavatele](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [Zadání dat faktur do systému závazků pomocí faktury dodavatele](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [Zadání dat faktury do závazků s použitím deníku schválení](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [Zadání dat faktury do systému závazků s použitím evidence faktur](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [Zaznamenání faktury dodavatele do deníku faktur](tasks/record-vendor-invoice-invoice-journal.md)
