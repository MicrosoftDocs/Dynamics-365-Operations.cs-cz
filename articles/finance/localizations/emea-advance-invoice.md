---
title: Zálohové faktury pro východní Evropu
description: Tento článek obsahuje informace o zálohových fakturách pro východní Evropu. Zálohová faktura je dokument, který vytvoříte pro odběratele nebo dodavatele. Zálohová faktura uvádí částku, která musí být předplacena na prodejní objednávce.
author: EvgenyPopovMBS
ms.date: 05/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 272643
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: epopov
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c722d8215c2b65e24008042c9a4d65bb419ad46a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886286"
---
# <a name="advance-invoices-for-eastern-europe"></a>Zálohové faktury pro východní Evropu

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o zálohových fakturách pro východní Evropu. Zálohová faktura je dokument, který vytvoříte pro odběratele nebo dodavatele. Zálohová faktura uvádí částku, která musí být předplacena na prodejní objednávce. 

> [!NOTE]
> Další možností je využít funkci zálohových faktur. Od Microsoft Dynamics 365 Finance verze 10.0.28, můžete tuto funkci použít, tím že přejdete na **Závazky** &gt; **Nastavení** &gt; **Parametry** &gt; **Hlavní kniha a DPH** a nastavíte možnost **Použít zálohovou fakturu** na pevné záložce **Zálohová faktura** na **Ano**. Více informací najdete v tématu [Zálohové faktury vs. zálohové platby](../accounts-payable/prepayments-invoices-vs-prepayments.md).

Funkce zálohové faktury umožňuje provádět následující činnosti:

- Vydání zálohových faktur odběratelům a sledování stavu těchto zálohových faktur (**Otevřené**, **Částečně zaplacené** nebo **Uzavřené**).
- *Pouze pro Polsko:* Zaúčtování transakcí zálohové faktury a transakcí daně z přidané hodnoty (DPH).
- Automatické generování řádků deníku plateb v závislosti na zálohové faktuře.
- Propojení záloh přijatých od odběratelů k zálohovým fakturám (před nebo po zaúčtování zálohy).
- Změna zaúčtování DPH do zaúčtované zálohy (tj. převést zálohu na platbu nebo platbu na zálohu, nebo změnit datum zaúčtování, sazby daně nebo částky).
- *Pouze pro Českou republiku:* Vytvořte daňový doklad pro dodávku podléhající DPH.

## <a name="advance-invoices-for-poland"></a>Zálohové faktury pro Polsko

Polské společnosti přijímající zálohy musí vytvořit fakturu pro platbu záloh pro odběratele. Tato zálohová faktura je zaúčtována do hlavní knihy a je to povinný dokument pro daňové účely DPH. Daň, která se vypočítává na zálohové faktuře, musí být nahlášena finančnímu úřadu.

Při provádění konečného prodeje zboží by měla zálohová faktura být zadána na prodejní faktuře. Celková částka prodeje musí obsahovat zálohy.

Při zaúčtování prodejní faktury je vyrovnaná zálohová faktura stornována. Původní zálohová faktura je vyrovnána se stornem zálohové faktury.

## <a name="set-up-accounts-receivable-for-advance-invoices"></a>Nastavení parametrů modulu Pohledávky pro zálohové faktury

1. Na stránce **Parametry pohledávek** na kartě **Aktualizace** na pevné záložce **Zálohová faktura** nastavte následující pole.

    | Pole | Popis |
    |-------|-------------|
    | Účetní profil | <p>*Pouze pro Polsko:* Vyberte účetní profil, který chcete používat pro zálohovou fakturaci.</p><p>**Důležité:** Pro Českou republiku a Maďarsko nejsou zálohové faktury považovány za účetní nebo daňové doklady a nejsou zaúčtovány do hlavní knihy. Proto byste měli toto pole pro tyto země ponechat prázdné, aby se zabránilo zaúčtování zálohových faktur do hlavní knihy.</p> |
    | Protiúčet | Vyberte protiúčet. |
    | Skupina DPH | Vyberte skupinu DPH, která má být použita, když se pro zálohovou fakturaci vypočítává DPH: |
    | Storno jako oprava | Toto políčko zaškrtněte, pokud storno zálohové faktury má být považováno za opravu. |
    | Stornovat k datu faktury | Zaškrtnutím tohoto políčka zajistíte stornování zálohy k datu zaúčtování faktury. |

1. Na pevné záložce **Platba** zadejte následující pole.

    | Pole | Popis |
    |-------|-------------|
    | Více dat zálohy | Vyberte **Přijmout**, **Varování** nebo **Chyba**. |
    | Neshoda data | Vyberte **Přijmout**, **Varování** nebo **Chyba**. |
    | Neshoda částky | Vyberte **Přijmout**, **Varování** nebo **Chyba**. |
    | Propojení na zaúčtovanou zálohovou fakturu | Vyberte **Přijmout**, **Varování** nebo **Chyba**. |
    | (CZE), (POL) Zpracování záloh | Vyberte **Upřesnit**. |

1. Na kartě **Číselné řady** nastavte číselné řady pro následující reference:

    - Daňový doklad
    - Daňový dobropis
    - Zálohová faktura
    - Dobropis zálohové faktury
    - Storno zálohové faktury
    - Doklad zálohové faktury
    - Doklad dobropisu zálohové faktury
    - Doklad stornování zálohové faktury

## <a name="create-a-customer-advance-invoice"></a>Vytvoření zálohové faktury odběratele

1. Přejděte na **Pohledávky** &gt; **Běžné** &gt; **Zálohové faktury** &gt; **Všechny zálohové faktury**.
1. V podokně akcí na kartě **Zálohová faktura** vyberte **Zálohová faktura** a vytvořte zálohovou fakturu.
1. Zadejte požadovanou informaci a poté vyberte **Zaúčtovat** k zaúčtování zálohové faktury.

Zálohová faktura může mít některý z následujících stavů: **Otevřená**, **Částečně zaplacená** nebo **Uzavřená**. Stav zálohové faktury, která byla zaúčtována, můžete ručně změnit. Vyberte **Stav** a poté na stránce **Změnit stav zálohové faktury** stránky v poli **Nový stav** vyberte nový stav zálohové faktury.

> [!NOTE]
> Kdykoli můžete změnit stav zálohové faktury. Nelze zpracovat uzavřené zálohové faktury v transakcích.
> 
> *Pouze pro Polsko:* Zálohové faktury jsou vygenerovány, pokud nastavíte účetní profil pro zálohové faktury v parametrech pohledávek. K zobrazení transakcí, které byly zaúčtovány, na stránce **Zálohová faktura** vyberte **Doklad**.

## <a name="vat-on-advance-invoices"></a>DPH na zálohových fakturách

Společnosti musí zaznamenat DPH při platbách záloh od odběratelů, i když prodej nebyl dokončen. Pokud chcete zaúčtovat DPH ze zálohy, můžete přidat řádek, který obsahuje specifikace DPH do zálohové faktury. Zálohová faktura může mít několik řádků a tyto řádky mohou obsahovat specifikace DPH, které jsou převzaty z řádků prodejní objednávky. Proto lze zaúčtovat DPH ze zálohy přísně v souladu s řádky prodejní objednávky.

> [!NOTE]
> Specifikace DPH budou zkopírovány do zálohové faktury řádky pouze v případě, že je hodnota v poli **Typ daně** na stránce **Kódy DPH** nastavena na **Standardní DPH** nebo **Snížená DPH**. Jinak jsou zkopírovány do řádků zálohové faktury, jako by částka DPH byla 0 (nula).

## <a name="link-an-advance-invoice-to-a-sales-order-or-a-free-text-invoice"></a>Propojení zálohové faktury s prodejní objednávkou nebo volnou fakturou

Každou zálohovou fakturu lze spojit pouze s jednou prodejní objednávkou nebo fakturou s volným textem najednou. Můžete také změnit přidružení stávající zálohové faktury s jinou prodejní objednávkou nebo fakturou s volným textem za předpokladu, že žádné zálohy nejsou spojeny se zálohovou fakturou.

Pro propojení zálohové faktury s prodejní objednávkou postupujte takto.

1. Na stránce **Všechny zálohové faktury** vyberte zálohovou fakturu.
1. V podokně akcí vyberte **Zálohová faktura** a pak vyberte **Prodejní objednávka**.
1. Vyberte prodejní objednávku k propojení se zálohovou fakturou a vyberte **OK**.

Pro propojení zálohové faktury s fakturou s volným textem postupujte takto.

1. Na stránce **Všechny zálohové faktury** vyberte zálohovou fakturu.
1. V podokně akcí vyberte **Zálohová faktura** a pak vyberte **Faktura s volným textem**.
1. Vyberte fakturu s volným textem k propojení se zálohovou fakturou a pak vyberte **OK**.

## <a name="create-a-customer-advance-invoice-from-a-sales-order"></a>Vytvoření zálohové faktury odběratele z prodejní objednávky

1. Vytvořte novou prodejní objednávku nebo vyberte stávající.
1. Vyberte **Faktura** a potom vyberte **Generovat** &gt; **Zálohová faktura**.
1. Na stránce **Vytvořit zálohovou fakturu** nastavte následující pole.

    | Pole | Popis |
    |-------|-------------|
    | Procento | Zadejte procento zálohy pro prodejní objednávku. |
    | Protiúčet | Vyberte výchozí protiúčet pro použití se zálohovou fakturací. |
    | Aktualizace objednávky | Vyberte **Vše**, **Dodat nyní**, **Vyskladněno**, **Dodací list** nebo **Vyskladněné množství a produkty mimo sklad**. Částka zálohové faktury se vypočítá na základě částky prodejní objednávku pro položky. |
    | Zaúčtovat DPH | Určete, zda se má DPH zaúčtovat při zaúčtování zálohové faktury. |
    | Datum zaúčtování DPH | Zadejte datum, kdy se má zaúčtovat DPH. |
    | Účetní profil se zálohovým dokladem deníku | Zadejte účetní profil pro zálohu. |
    | Vytvořit daňový doklad | Určete, zda se má vytvořit daňový doklad. |

> [!NOTE]
> *Pouze pro Polsko:* Zálohové faktury jsou vygenerovány, pokud nastavíte účetní profil pro zálohové faktury v parametrech pohledávek.

## <a name="create-a-customer-advance-invoice-from-a-free-text-invoice"></a>Vytvoření zálohové faktury odběratele z faktury s volným textem

1. Vytvořte fakturu s volným textem nebo vyberte stávající fakturu s volným textem.
1. Na kartě **Faktury** v části **Nová** vyberte **Zálohová faktura**.

    Nyní můžete vytvořit novou zálohovou fakturu, která bude spojená s fakturou s volným textem.

> [!NOTE]
> *Pouze pro Polsko:* Zálohové faktury jsou vygenerovány, pokud nastavíte účetní profil pro zálohové faktury v parametrech pohledávek.

## <a name="print-an-advance-invoice"></a>Tisk zálohové faktury

- Na stránce **Zálohová faktura** vyberte **Tisk**. 

*Pouze pro Polsko:* můžete vytisknout dokument zálohové faktury fiskálního dokumentu. Vyberte možnost při zaúčtování zálohových faktur.

*Pouze pro Polsko:* Rozvržení prodejní faktury a dokumentů faktur s volným textem následující informace o vyrovnané zálohové faktuře:

- Číslo zálohové faktury
- Datum zálohové faktury
- Částka bez DPH, Částka DPH, částka včetně DPH a Měna
- Procento daně

Souhrn částek DPH musí obsahovat pole **Daň ze zálohové faktury**. Částka, která je splatná, by měla být snížena o částku zálohové faktury.

## <a name="create-a-payment-proposal-from-an-advance-invoice"></a>Vytvoření návrhu platby ze zálohové faktury

Když generujete nový deník plateb, můžete automaticky generovat řádky deníku plateb v závislosti na zálohové faktuře.

1. Na stránce **Deník plateb** vyberte možnost **Zálohový doklad deníku** a pak vyberte **Řádky**.
1. Na stránce **Doklad deníku** vyberte možnosti **Návrh platby** &gt; **Návrh platby ze zálohové faktury**, abyste otevřeli formulář návrhu platby ze zálohových faktur. Informace jako například účetní profil a skupiny DPH jsou převzaty ze zálohové faktury.

> [!NOTE]
> Nové zálohy budou automaticky propojeny se zálohovými fakturami, pokud budou zaškrtnuta políčka **Propojení záloh** a **Změna stavu** na stránce **Vytvořit návrh platby ze zálohových faktur**.

## <a name="link-a-prepayment-to-an-advance-invoice"></a>Připojení zálohy k zálohové faktuře

Chcete-li propojit zálohu se zálohovou fakturou z deníku plateb, postupujte takto.

- Otevřete deník plateb, vyberte řádek, který má zálohu, a pak vyberte **Funkce** &gt; **Propojit se zálohovými fakturami**.

Chcete-li propojit zálohu se zálohovou fakturou ze stránky **Transakce odběratele**, postupujte takto.

1. Vyberte **Všichni zákazníci** &gt; **Zákazník** &gt; **Transakce**.
1. Vyberte deník plateb, vyberte řádek, který má zálohu, a vyberte **Funkce** &gt; **Propojit se zálohovými fakturami**.

## <a name="link-an-advance-invoice-to-a-prepayment"></a>Připojení zálohové faktury k záloze

Pro propojení zálohové faktury s řádkem zálohy postupujte takto.

1. Na stránce **Všechny zálohové faktury** vyberte zálohovou fakturu.
1. V podokně akcí vyberte **Zálohová faktura** a pak vyberte **Záloha**.
1. Vyberte řádek zálohy k propojení se zálohovou fakturou a pak vyberte **OK**.

## <a name="advance-invoice-credit-notes"></a>Dobropisy zálohových faktur

- *Pouze pro Polsko:* Pokud chcete zálohovou fakturu zrušit, můžete vytvořit dobropis zálohové faktury a zaúčtovat jej do hlavní knihy.
- Pokud chcete vytvořit dobropis, můžete vytvořit novou zálohovou fakturu a pak vybrat **Dobropis**. Poté můžete vybrat zálohovou fakturu ke zrušení.
- Můžete také vytvořit dobropis prodejní faktury s vyrovnáním zálohové faktury.
- Rozložení faktur dobropisu zálohové faktury obsahuje informace o řádcích před a po opravě.
- *Pouze pro Polsko:* Po zaúčtování dobropisu zálohové faktury se vytvářejí transakce hlavní knihy.

## <a name="tax-documents-for-the-czech-republic"></a>Daňové doklady pro Českou republiku

Pro Českou republiku můžete vytvořit daňový doklad, který je založen na informacích o záloze pro doručení podléhající DPH. Daňový doklad můžete vytvořit, vytvořit a zobrazit nebo vytvořit a vytisknout ze stránky zálohy tím, že vyberete **Funkce** &gt; **Daňový doklad** a poté vyberte jednu z možností. Daňový doklad obsahuje podrobné informace o DPH jako například typ DPH, hodnotu a základ v zúčtovací měně a měně transakce.

## <a name="set-up-accounts-payable-for-advance-invoices"></a>Nastavení parametrů modulu Závazky pro zálohové faktury

- Na stránce **Parametry závazků** na kartě **Číselné řady** určete číselnou řadu pro zálohové faktury.

## <a name="create-a-vendor-advance-invoice"></a>Tvorba zálohové faktury dodavatele

Můžete ručně vytvořit zálohovou fakturu. Případně může být nová zálohová faktura založena na stávající nákupní objednávce.

### <a name="manually-create-a-vendor-advance-invoice"></a>Ruční tvorba zálohové faktury dodavatele

1. Přejděte na **Závazky** &gt; **Běžné** &gt; **Zálohové faktury** &gt; **Všechny zálohové faktury**.
1. V podokně akcí na kartě **Zálohová faktura** vyberte **Zálohová faktura** a vytvořte zálohovou fakturu.
1. Zadejte požadovanou informaci a poté vyberte **Zaúčtovat** k zaúčtování zálohové faktury.

Zálohová faktura může mít některý z následujících stavů: **Otevřená**, **Částečně zaplacená** nebo **Uzavřená**. Stav zálohové faktury, která byla zaúčtována, můžete ručně změnit. Vyberte **Stav** a poté na stránce **Změnit stav zálohové faktury** stránky v poli **Nový stav** vyberte nový stav zálohové faktury.

> [!NOTE]
> Kdykoli můžete změnit stav zálohové faktury. Nelze zpracovat uzavřené zálohové faktury v transakcích.
>
> Specifikace DPH budou zkopírovány do zálohové faktury řádky pouze v případě, že je hodnota v poli **Typ daně** na stránce **Kódy DPH** nastavena na **Standardní DPH** nebo **Snížená DPH**. Jinak jsou zkopírovány do řádků zálohové faktury, jako by částka DPH byla 0 (nula).

### <a name="link-an-advance-invoice-to-a-purchase-order"></a>Propojení zálohové faktury s nákupní objednávkou

Každou zálohovou fakturu lze propojit pouze s jednou nákupní objednávkou najednou. Můžete také změnit přidružení stávající zálohové faktury k jiné nákupní objednávce za předpokladu, že žádné zálohy nejsou spojeny se zálohovou fakturou.

Pro propojení zálohové faktury s nákupní objednávkou postupujte takto.

1. Na stránce **Všechny zálohové faktury** vyberte zálohovou fakturu.
1. V podokně akcí vyberte **Zálohová faktura** a pak vyberte **Nákupní objednávka**.
1. Vyberte nákupní objednávku k propojení se zálohovou fakturou a pak vyberte **OK**.

### <a name="create-a-vendor-advance-invoice-from-a-purchase-order"></a>Vytvoření zálohové faktury dodavatele z nákupní objednávky

1. Vytvořte nákupní objednávku nebo vyberte stávající nákupní objednávku.
1. Vyberte **Faktura** a potom vyberte **Generovat** &gt; **Zálohová faktura**.
1. Na stránce **Vytvořit zálohovou fakturu** nastavte následující pole.

    | Pole | Popis |
    |-------|-------------|
    | Procento | Zadejte procento zálohy pro nákupní objednávku. |
    | Aktualizovat nákup | Vyberte možnost. Částka zálohové faktury se vypočítá na základě částky nákupní objednávky pro položky. |
    | Účetní profil se zálohovým dokladem deníku | Zadejte účetní profil pro zálohu. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
