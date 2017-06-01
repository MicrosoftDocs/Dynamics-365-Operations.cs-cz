---
title: "Zálohové faktury pro východní Evropu"
description: "Zálohová faktura je dokument, který vytvoříte pro odběratele nebo dodavatele. Zálohová faktura uvádí částku, která musí být předplacena na prodejní objednávce. Toto téma obsahuje informace o zálohových fakturách pro východní Evropu."
author: ShylaThompson
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Operations, Core
ms.custom: 272643
ms.assetid: 00072155-f3d1-4d09-b848-5c086cac0891
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: epopov
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 948124526f5718d783b1ecd80462701610734f82
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="advance-invoices-for-eastern-europe"></a>Zálohové faktury pro východní Evropu

[!include[banner](../includes/banner.md)]


Zálohová faktura je dokument, který vytvoříte pro odběratele nebo dodavatele. Zálohová faktura uvádí částku, která musí být předplacena na prodejní objednávce. Toto téma obsahuje informace o zálohových fakturách pro východní Evropu.

Funkce zálohové faktury umožňuje provádět následující činnosti:

-   Vydání zálohových faktur odběratelům a sledování stavu těchto zálohových faktur (**Otevřené**, **Částečně zaplacené** nebo **Uzavřené**).
-   Zaúčtování transakcí zálohové faktury a transakcí daně z přidané hodnoty (DPH) (pouze pro Polsko).
-   Generování řádků deníku plateb automaticky v závislosti na zálohové faktuře.
-   Propojení záloh přijatých od odběratelů k zálohovým fakturám (před nebo po zaúčtování zálohy).
-   Změna zaúčtování DPH do zaúčtované zálohy (tj. převést zálohu na platbu nebo platbu na zálohu, nebo změnit datum zaúčtování, sazby daně nebo částky).
-   Vytvořte daňový doklad pro dodávku podléhající DPH (pouze pro Českou republiku).

## <a name="advance-invoices-for-poland"></a>Zálohové faktury pro Polsko
Polské společnosti přijímající zálohy musí vytvořit fakturu pro platbu záloh pro odběratele. Tato zálohová faktura je zaúčtována do hlavní knihy a je to povinný dokument pro daňové účely DPH. Daň, která se vypočítává na zálohové faktuře, musí být nahlášena finančnímu úřadu. Při provádění konečného prodeje zboží by měla zálohová faktura být zadána na prodejní faktuře. Celková částka prodeje musí obsahovat zálohy. Při zaúčtování prodejní faktury bude vyrovnaná zálohová faktura stornována. Původní zálohová faktura bude vyrovnána se stornem zálohové faktury.

## <a name="set-up-accounts-receivable-for-advance-invoices"></a>Nastavení parametrů modulu Pohledávky pro zálohové faktury
Na stránce **Parametry závazků** na kartě **Aktualizovat** určete následující parametry.

|Pevná záložka|Parametr|popis|
|------|----------|------------|
|Zálohová faktura  |Účetní profil|Vyberte účetní profil, který chcete používat pro zálohovou fakturaci (pouze Polsko). **Důležité:** Pro Českou republiku a Maďarsko nejsou zálohové faktury považovány za účetní nebo daňové doklady a nejsou zaúčtovány do hlavní knihy. Proto byste měli toto pole pro tyto země ponechat prázdné, aby se zabránilo zaúčtování zálohových faktur do hlavní knihy.
|
|Zálohová faktura  |Vypnuto|protiúčet        |Vyberte výchozí protiúčet pro použití s rozšířenou fakturací.|
|Zálohová faktura  |Skupina prodejní daně        |Vyberte skupinu DPH, která má být použita, když se pro zálohovou fakturaci vypočítává DPH:|
|Zálohová faktura  |Storno jako oprava |Toto políčko zaškrtněte, pokud storno zálohové faktury má být považováno za opravu.|
|Zálohová faktura  |Stornovat k datu faktury|Zaškrtnutím tohoto políčka zajistíte stornování zálohy k datu zaúčtování faktury.|
|Platba          |Více dat zálohy|Vyberte některou z následujících možností: **přijmout**, **upozornění**, nebo **chyba**.|
|Platba          |Neshoda data          |Vyberte některou z následujících možností: **přijmout**, **upozornění**, nebo **chyba**.|
|Platba          |Neshoda částky        |Vyberte některou z následujících možností: **přijmout**, **upozornění**, nebo **chyba**.|
|Platba          |Propojení na zaúčtovanou zálohovou fakturu|Vyberte některou z následujících možností: **přijmout**, **upozornění**, nebo **chyba**.|
|Platba          |(CZE), (POL) Zpracování záloh|Vyberte **Upřesnit**.|

Na kartě **Číselné řady** nastavte číselné řady pro následující reference:

-   Daňový doklad
-   Daňový dobropis
-   Zálohová faktura
-   Dobropis zálohové faktury
-   Storno zálohové faktury
-   Doklad zálohové faktury
-   Doklad dobropisu zálohové faktury
-   Doklad stornování zálohové faktury

## <a name="create-a-customer-advance-invoice"></a>Vytvoření zálohové faktury odběratele
Klikněte na **Pohledávky** &gt; **Běžné** &gt; **Zálohové faktury** &gt; **Všechny zálohové faktury**. Chcete-li vytvořit novou zálohovou fakturu, v podokně akcí na kartě **Zálohová faktura** klikněte na **Zálohová faktura**. Zadejte požadovanou informaci a poté klikněte na možnost **Zaúčtovat** k zaúčtování zálohové faktury. Zálohová faktura může mít některý z následujících stavů: **Otevřená**, **Částečně zaplacená** nebo **Uzavřená**. Stav zálohové faktury, která byla zaúčtována, můžete ručně změnit. Klepněte na tlačítko **stav**a poté na stránce **Změnit stav zálohové faktury** stránky v poli **Nový stav** vyberte nový stav zálohové faktury. **Poznámka:** Kdykoli můžete změnit stav zálohové faktury. Nelze zpracovat uzavřené zálohové faktury v transakcích. **Poznámka:** Pro Polsko jsou zálohové faktury vygenerovány, pokud nastavíte účetní profil pro zálohové faktury v parametrech pohledávek. K zobrazení transakcí, které byly zaúčtovány, na stránce **Zálohová faktura** klepněte na **Doklad**.

## <a name="vat-on-advance-invoices"></a>DPH na zálohových fakturách
Společnosti musí zaznamenat DPH při platbách záloh od odběratelů, i když prodej nebyl dokončen. Pokud chcete zaúčtovat DPH ze zálohy, můžete přidat řádek, který obsahuje specifikace DPH do zálohové faktury. Zálohová faktura může mít několik řádků a řádky mohou obsahovat specifikace DPH, které jsou převzaty z řádků prodejní objednávky. Proto lze zaúčtovat DPH ze zálohy přísně v souladu s řádky prodejní objednávky. **Poznámka:** specifikace DPH budou zkopírovány do zálohové faktury řádky pouze v případě, že je hodnota v poli **typ daně** na stránce **Kódy DPH** nastavena na **Standardní daň DPH** nebo **Snížená DPH**. Jinak je řádek zkopírován do zálohové faktury, jako by částka DPH byla 0 (nula).

## <a name="link-an-advance-invoice-to-a-sales-order-or-a-free-text-invoice"></a>Propojení zálohové faktury s prodejní objednávkou nebo volnou fakturou
Každou zálohovou fakturu lze spojit pouze s jednou prodejní objednávkou nebo fakturou s volným textem najednou. Můžete také změnit přidružení stávající zálohové faktury s jinou prodejní objednávkou nebo fakturou s volným textem za předpokladu, že žádné zálohy nejsou spojeny se zálohovou fakturou. Pokud chcete provést propojení zálohové faktury s prodejní objednávkou, na stránce **Všechny zálohové faktury** vyberte zálohovou fakturu. V podokně akcí klepněte na tlačítko **Zálohová faktura**a klepněte na tlačítko **Prodejní objednávka**. Potom vyberte prodejní objednávku k propojení se zálohovou fakturou a klepněte na tlačítko **OK**. Pokud chcete provést propojení faktury s volným textem s prodejní objednávkou, na stránce **Všechny zálohové faktury** vyberte zálohovou fakturu. V podokně akcí klepněte na tlačítko **Zálohová faktura**a klepněte na tlačítko **Faktura s volným textem**. Potom vyberte fakturu s volným textem k propojení se zálohovou fakturou a klepněte na tlačítko **OK**.

## <a name="create-a-customer-advance-invoice-from-a-sales-order"></a>Vytvoření zálohové faktury odběratele z prodejní objednávky
Vytvořte novou prodejní objednávku nebo vyberte stávající. Klepněte na tlačítko **Faktura** a potom na tlačítko **Generovat** &gt; **Zálohová faktura**. Na stránce **Vytvořit zálohovou fakturu** nastavte následující pole.

| Pole                                           | popis                                                                                                                                                                                                                               |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Procento                                         | Zadejte procento zálohy pro prodejní objednávku.                                                                                                                                                                             |
| Protiúčet                                  | Vyberte výchozí protiúčet pro použití s rozšířenou fakturací.                                                                                                                                                                         |
| Aktualizace objednávky                                    | Vyberte některou z následujících možností: **Vše**, **Dodat nyní**, **Vyskladněno**, **Dodací list** nebo **Vyskladněné množství a produkty mimo sklad**. Částka zálohové faktury se vypočítá na základě částky prodejní objednávku pro položky. |
| Zaúčtovat DPH                                        | Určete, zda se má DPH zaúčtovat při zaúčtování zálohové faktury.                                                                                                                                                                      |
| Datum zaúčtování DPH                                   | Upřesněte datum zaúčtování DPH.                                                                                                                                                                                                         |
| Účetní profil se zálohovým dokladem deníku | Zadejte účetní profil pro zálohu.                                                                                                                                                                                           |
| Vytvořit daňový doklad                             | Určete, zda se má vytvořit daňový doklad.                                                                                                                                                                                         |

> [!POZNÁMKA} Pro Polsko jsou zálohové faktury vygenerovány, pokud nastavíte účetní profil pro zálohové faktury v parametrech pohledávek.

## <a name="create-a-customer-advance-invoice-from-a-free-text-invoice"></a>Vytvoření zálohové faktury odběratele z faktury s volným textem
Vytvořte fakturu s volným textem nebo vyberte stávající fakturu s volným textem. Na kartě **Faktury** v části **Nová** klepněte na položku **Zálohová faktura**. pak můžete vytvořit novou zálohovou fakturu, která bude spojená s fakturou s volným textem. **Poznámka:** Pro Polsko jsou zálohové faktury vygenerovány, pokud nastavíte účetní profil pro zálohové faktury v parametrech pohledávek.

## <a name="print-an-advance-invoice"></a>Tisk zálohové faktury
Pokud chcete vytisknout zálohovou fakturu, na stránce **Zálohová faktura** klepněte na možnost **Vytisknout**. Pro Polsko můžete vytisknout dokument zálohové faktury fiskálního dokumentu. Vyberte možnost při zaúčtování zálohových faktur. Pro Polsko zahrnuje rozvržení prodejní faktury a dokumentů faktur s volným textem následující informace o vyrovnanou zálohové faktury

-   Číslo zálohové faktury
-   Datum zálohové faktury
-   Částka bez DPH, Částka DPH, částka včetně DPH a Měna
-   Procento daně

Souhrn částek DPH musí obsahovat **daň ze zálohové faktury**. Částka, která je splatná, by měla být snížena o částku zálohové faktury.

## <a name="create-a-payment-proposal-from-an-advance-invoice"></a>Vytvoření návrhu platby ze zálohové faktury
Můžete generovat řádky deníku plateb automaticky v závislosti na zálohové faktuře. Při vytváření nového deníku plateb na stránce **Deník plateb** vyberte možnost **Zálohový doklad deníku** a klepněte na tlačítko **Řádky**. Na stránce **Doklad deníku** můžete kliknout na možnosti **Návrh platby** &gt; **Návrh platby ze zálohové faktury**, abyste otevřeli formulář návrhu platby ze zálohových faktur. Informace jako například účetní profil a skupiny DPH jsou převzaty ze zálohové faktury. **Poznámka:** Nové zálohy budou automaticky propojeny se zálohovými fakturami, pokud budou zaškrtnuta políčka **Propojení záloh** a **Změna stavu** na stránce **Vytvořit návrh platby ze zálohových faktur**.

## <a name="link-a-prepayment-to-an-advance-invoice"></a>Připojení zálohy k zálohové faktuře
Pokud chcete propojit zálohu se zálohovou fakturou z deníku plateb, otevřete deník plateb, vyberte řádek, který obsahuje zálohu, a klepněte na tlačítko **Funkce** &gt; **Propojit se zálohovými fakturami**. Pokud chcete propojit zálohu se zálohovou fakturou ze stránky **Transakce odběratele**, klikněte na **Všichni odběratelé** &gt; **Odběratel** &gt; **Transakce**. Vyberte deník plateb, vyberte řádek, který má zálohu, a klikněte na **Funkce** &gt; **Propojit se zálohovými fakturami**.

## <a name="link-an-advance-invoice-to-a-prepayment"></a>Připojení zálohové faktury k záloze
Pokud chcete provést propojení zálohové faktury s řádkem zálohy, na stránce **Všechny zálohové faktury** vyberte zálohovou fakturu. V podokně akcí klepněte na tlačítko **Zálohová faktura**a klepněte na tlačítko **Záloha**. Potom vyberte řádek zálohy k propojení se zálohovou fakturou a klepněte na tlačítko **OK**.

## <a name="advance-invoice-credit-note"></a>Dobropis zálohové faktury
-   (POL) Pokud chcete zálohovou fakturu zrušit, můžete vytvořit dobropis zálohové faktury a zaúčtovat jej do hlavní knihy.
-   Pokud chcete vytvořit dobropis, můžete vytvořit novou zálohovou fakturu a klikknout na tlačítko **Dobropis**. Poté můžete vybrat zálohovou fakturu ke zrušení.
-   Můžete také vytvořit dobropis prodejní faktury s vyrovnáním zálohové faktury.
-   Rozložení faktur dobropisu zálohové faktury obsahuje informace o řádcích před a po opravě.
-   (POL) Po zaúčtování dobropisu zálohové faktury se vytvářejí transakce hlavní knihy.

## <a name="cze-tax-documents"></a>(CZE) Daňové doklady
Pro Českou republiku můžete vytvořit daňový doklad, který je založen na informacích o záloze pro doručení podléhající DPH. Můžete vytvořit, vytvořit a zobrazit nebo vytvořit a vytisknout daňový doklad ze stránky zálohy. Klepněte na tlačítko **Funkce** &gt; **Daňový doklad**a vyberte jednu z možností. Daňový doklad obsahuje podrobné informace o DPH jako například typ DPH, hodnotu a základ v zúčtovací měně a měně transakce.

## <a name="set-up-accounts-payable-for-advance-invoices"></a>Nastavení parametrů modulu Závazky pro zálohové faktury
Na stránce **Parametry závazků** na kartě **Číselné řady** určete číselnou řadu pro zálohové faktury.

## <a name="create-a-vendor-advance-invoice"></a>Tvorba zálohové faktury dodavatele
Můžete ručně vytvořit zálohovou fakturu. Případně může být nová zálohová faktura založena na stávající nákupní objednávce.

## <a name="manually-create-a-vendor-advance-invoice"></a>Ruční tvorba zálohové faktury dodavatele
Klikněte na **Závazky** &gt; **Běžné** &gt; **Zálohové faktury** &gt; **Všechny zálohové faktury**. Chcete-li vytvořit novou zálohovou fakturu, v podokně akcí na kartě **Zálohová faktura** klikněte na **Zálohová faktura**. Potom zadejte požadovanou informaci a poté klikněte na možnost **Zaúčtovat** k zaúčtování zálohové faktury. Zálohová faktura může mít některý z následujících stavů: **Otevřená**, **Částečně zaplacená** nebo **Uzavřená**. Stav zálohové faktury, která byla zaúčtována, můžete ručně změnit. Klepněte na tlačítko **stav**a poté na stránce **Změnit stav zálohové faktury** stránky v poli **Nový stav** vyberte nový stav zálohové faktury. **Poznámka:** Kdykoli můžete změnit stav zálohové faktury. Nelze zpracovat uzavřené zálohové faktury v transakcích. **Poznámka:** specifikace DPH budou zkopírovány do zálohové faktury řádky pouze v případě, že je hodnota v poli **typ daně** na stránce **Kódy DPH** nastavena na **Standardní daň DPH** nebo **Snížená DPH**. Jinak je řádek zkopírován do zálohové faktury, jako by částka DPH byla 0 (nula).

## <a name="link-an-advance-invoice-to-a-purchase-order"></a>Propojení zálohové faktury s nákupní objednávkou
Každou zálohovou fakturu lze spojit pouze s jednou nákupní objednávkou nebo fakturou s volným textem najednou. Můžete také změnit přidružení stávající zálohové faktury k jiné nákupní objednávce za předpokladu, že žádné zálohy nejsou spojeny se zálohovou fakturou. Pokud chcete provést propojení zálohové faktury s nákupní objednávkou, na stránce **Všechny zálohové faktury** vyberte zálohovou fakturu. V podokně akcí klepněte na tlačítko **Zálohová faktura**a klepněte na tlačítko **Nákupní objednávka**. Potom vyberte nákupní objednávku k propojení se zálohovou fakturou a klepněte na tlačítko **OK**.

## <a name="create-a-vendor-advance-invoice-from-a-purchase-order"></a>Vytvoření zálohové faktury dodavatele z nákupní objednávky
Vytvořte nákupní objednávku nebo vyberte stávající nákupní objednávku. Klepněte na tlačítko **Faktura** a potom na tlačítko **Generovat** &gt; **Zálohová faktura**. Na stránce **Vytvořit zálohovou fakturu** nastavte následující pole.

| Pole                                           | popis                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Procento                                         | Zadejte procento zálohy pro nákupní objednávku.                                                         |
| Aktualizovat nákup                                 | Vyberte některou z následujících možností: Částka zálohové faktury se vypočítá na základě částky nákupní objednávky pro položky. |
| Účetní profil se zálohovým dokladem deníku | Zadejte účetní profil pro zálohu.                                                                          |







