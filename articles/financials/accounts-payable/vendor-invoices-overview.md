---
title: "Přehled faktur dodavatele"
description: "V tomto článku jsou obecné informace o fakturách dodavatele. Faktury dodavatele jsou požadavky na zaplacení za přijaté produkty a služby. Faktury dodavatele mohou představovat účet za průběžné služby nebo mohou být založeny na nákupních objednávkách specifického zboží a služeb."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1982e495f740d6061b9574aa9f40f38180e8d110
ms.openlocfilehash: 4c27b5a8ab1a7aeab31b48937dcaf4a86d798689
ms.contentlocale: cs-cz
ms.lasthandoff: 08/03/2017

---

# <a name="vendor-invoices-overview"></a>Přehled faktur dodavatele

[!include[banner](../includes/banner.md)]


V tomto článku jsou obecné informace o fakturách dodavatele. Faktury dodavatele jsou požadavky na zaplacení za přijaté produkty a služby. Faktury dodavatele mohou představovat účet za průběžné služby nebo mohou být založeny na nákupních objednávkách specifického zboží a služeb. 

<a name="vendor-invoices"></a>Faktury dodavatele
---------------

Faktura dodavatele z nákupní objednávky je faktura, která je vytvořena při přijetí produktů nebo služeb podle nákupní objednávky, kterou jste uskutečnili s dodavatelem. Faktura dodavatele obsahuje hlavičku a jeden nebo více řádků se zbožím nebo službami. Faktura dodavatele představuje konec cyklu nákupní objednávky, příjemky produktu a faktury dodavatele. 

Ačkoliv jsou některé faktury dodavatele propojeny s nákupní objednávkou, mohou faktury dodavatele obsahovat také řádky, které neodpovídají řádkům nákupní objednávky. Můžete vytvořit také faktury dodavatele, které nejsou přidruženy k žádné nákupní objednávce. Tyto faktury dodavatele mohou představovat probíhající služby, jako například provozní účet, takže při jejich přidání nemusíte odkazovat na nákupní objednávku. 

Je několik způsobů, jak zadat fakturu dodavatele:

-   Registr faktur dodavatele umožňuje rychle zadat faktury, které neodkazují na nákupní objednávky, abyste mohli určovat časově rozlišené výdaje. Pomocí deníku schválení faktur dodavatelů můžete tyto faktury vybrat a zaúčtovat je do zůstatku dodavatele a časové rozlišení tak stornovat.
-   Deník faktur dodavatele slouží k rychlému zadání faktur, které neodkazují na nákupní objednávku, v jediném kroku.
-   Spolu s evidencí faktur dodavatele slouží registr faktur dodavatele k rychlému zadání faktur, které mají mít časově rozlišené výdaje. Přidružené nákupní objednávky můžete později otevřít k zaúčtování faktury na účet výdajů.
-   Stránky **Otevřít faktury dodavatele** a **Nevyřízené faktury dodavatele** slouží k vytváření faktur dodavatele z potvrzených nákupních objednávek.

V následující diskusi naleznete více informací o použití stránek **Otevřít faktury dodavatele** nebo **Nevyřízené faktury dodavatele** k vytvoření faktury dodavatele z nákupní objednávky.

## <a name="understanding-invoice-line-quantities"></a>Princip množství na řádcích faktury
Při otevření faktury dodavatele ze související nákupní objednávky se řádky faktury vytvoří z nákupní objednávky. Dle výchozího nastavení se množství převezme z množství na příjemce produktu. Můžete však použít některé z následujících výchozích chování:

-   **Množství nynějšího příjmu** – tuto možnost použijte pro částečné dodávky. Výchozí hodnota v poli **Množství** se převezme z pole s množstvím **Přijmout nyní** na nákupní objednávce.
-   **Objednané množství** – tuto možnost použijte pro úplné dodávky. Výchozí hodnota v poli **Množství** se převezme z pole s množstvím **Objednáno** na nákupní objednávce.
-   **Registrované množství** – tuto možnost použijte, pokud položka vyžaduje registraci (určuje se na stránce **Skupiny modelů položek**. Výchozí hodnota v poli **Množství** je fyzické upravené množství, které bylo zaregistrováno.
-   **Množství v příjemce produktu** – tuto možnost použijte, pokud pro danou objednávku již byla přijata příjemka produktu. Výchozí hodnota v poli **Množství** se převezme z celkového množství dostupných příjemek produktu.
-   **Registrované množství a služby** – tuto možnost použijte, pokud byla množství registrována v deníku doručených položek pro položky na skladě nebo položky, které nejsou na skladě. Tato možnost zahrnuje také služby bez ohledu na to, zda jsou registrovány.

Používá-li vaše právnická osoba párování faktur, můžete si zobrazit výsledky párování množství ve sloupci **Spárování množství v příjemce produktu**. K zobrazení výsledků párování množství můžete použít také příkaz nabídky **Podrobnosti o párování** na kartě **Kontrola**.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Přidání řádku, který nebyl v nákupní objednávce
Do faktury dodavatele můžete přidat nový řádek, který nebyl na nákupní objednávce. Je nutné vybrat číslo položky nebo kategorii zásobování. Poté lze na řádek přidat množství, ceny a částky. Řádek bude zahrnut pouze v zásadách párování pro součty faktur.

## <a name="submitting-a-vendor-invoice-for-review"></a>Odeslání faktury dodavatele ke kontrole
Vaše organizace může využívat workflowy ke správě procesu kontroly faktur dodavatele. Hlavička faktury, řádek faktury, nebo obojí může vyžadovat přezkoumání pracovního postupu. Ovládací prvky workflowu se použijí pro hlavičku nebo řádek podle toho, která část byla před kliknutím na ovládací prvek aktivní. Namísto tlačítka **Zaúčtovat** se zobrazí tlačítko **Odeslat**, které slouží k odeslání faktury dodavatele do procesu kontroly.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Spárování faktur dodavatele s příjemkami produktu
Podle potřeby můžete zadávat a ukládat informace o fakturách dodavatele a porovnat řádky faktury s řádky příjemky produktu. Také můžete spárovat částečná množství pro řádek. 

Fakturu dodavatele lze vytvořit na základě řádkových položek příjemek produktu, které byly přijaty k dnešnímu datu, a to i tehdy, když všechny položky určité nákupní objednávky nebyly dosud přijaty. Tuto možnost můžete využít například tehdy, když dodavatel zasílá jednou za měsíc fakturu, ve které jsou uvedeny všechny jím odeslané dodávky v daném měsíci. Každá příjemka produktu představuje částečnou nebo úplnou dodávku položek uvedených v nákupní objednávce. 

Při zaúčtování faktury je množství v poli **Zůstatek faktury** u každé položky aktualizováno celkovým počtem přijatého množství z vybraných příjemek produktu. Pokud bude množství **Zůstatek faktury** i množství **Zbývá dodat** pro všechny položky na nákupní objednávce nulové (0), stav nákupní objednávky se změní na hodnotu **Fakturováno**. Pokud množství v poli **Zůstatek faktury** není nulové (0), stav nákupní objednávky se nezmění a k této objednávce je možné zadat další faktury.

Tato možnost předpokládá, že pro nákupní objednávku byla zaúčtována alespoň jedna příjemka produktu. Faktura dodavatele je založena na těchto příjemkách produktu a odráží na nich uvedená množství. Finanční údaje pro fakturu jsou založeny na údajích zadaných při zaúčtování faktury.

Více informací naleznete v tématu [Zaznamenání faktury dodavatele a spárování s přijatým množstvím](../accounts-receivable/tasks/record-vendor-invoice-match-against-received-quantity.md)

## <a name="working-with-multiple-invoices"></a>Práce s více fakturami

Můžete pracovat s více fakturami současně a zaúčtovat je všechny najednou. Pokud je nutné vytvořit více faktur, použijte stránku **Nevyřízené faktury dodavatele**. Potřebujete-li zaúčtovat a vytisknout více faktur dodavatele, použijte stránku deníku pro schvalování faktur. Když používáte deník pro schvalování faktur, musí být pro nákupní objednávku zaúčtována alespoň jedna příjemka produktu a faktura pro nákupní objednávku musí být zaúčtována do registru faktur. Finanční informace pro fakturu pocházejí z faktury zaúčtované do registru.


Další informace naleznete zde: 

 - [Nastavení zásad faktur dodavatele](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md) 

 - [Zadání dat faktury do závazků s použitím faktury dodavatele](tasks/key-invoice-data-ap-system-vendor-invoice.md)
 
 - [Zadání dat faktury do závazků s použitím deníku schválení](tasks/key-invoice-data-into-ap-system-approval-journal.md)
  
 - [Zadání dat faktury do systému závazků s použitím evidence faktur](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
 
 - [Zaznamenání faktury dodavatele do deníku faktur](tasks/record-vendor-invoice-invoice-journal.md)

