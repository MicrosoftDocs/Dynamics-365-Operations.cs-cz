---
title: "Centralizované platby pohledávek"
description: "Organizace zahrnující více právnických osob mohou vytvářet a spravovat platby pomocí jedné právnické osoby, která zpracovává všechny platby. Proto není nutné zadat stejné transakce pro více právnických osob. Tento článek uvádí příklady, které znázorňují zpracování zaúčtování pro centralizované platby v různých scénářích."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c5a09eedd1dd12b7f5343953b16f9f0b210213d7
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="centralized-payments-for-accounts-receivable"></a>Centralizované platby pohledávek

[!include[banner](../includes/banner.md)]


Organizace zahrnující více právnických osob mohou vytvářet a spravovat platby pomocí jedné právnické osoby, která zpracovává všechny platby. Proto není nutné zadat stejné transakce pro více právnických osob. Tento článek uvádí příklady, které znázorňují zpracování zaúčtování pro centralizované platby v různých scénářích.

Organizace zahrnující více právnických osob mohou vytvářet a spravovat platby pomocí jedné právnické osoby, která zpracovává všechny platby. Proto není nutné zadat stejné transakce pro více právnických osob. Kromě toho organizace ušetří čas, jelikož je zjednodušen proces návrhů plateb, vyrovnání a úpravy otevřených a uzavřených transakcí pro centralizované platby. 

V organizaci s centralizovanými platbami existuje mnoho právnických osob pro operace a každá provozní právnická osoba spravuje své vlastní pohledávky. Platby pro všechny provozní právnické osoby jsou přijímány jednou právnickou osobou, která se nazývá právnická osoba platby. Během procesu vyrovnání jsou generovány odpovídající kreditní a debetní transakce. Můžete určit, která právnická osoba v organizaci přijímá transakce realizovaného zisku nebo realizované ztráty a také způsob, jakým mají být zpracovány transakce platebních slev, které souvisejí s centralizovanou platbou. 

Následující příklady ilustrují způsob zaúčtování při různých scénářích. U všech těchto příkladů se předpokládá následující konfigurace:

-   Právnické osoby jsou Fabrikam, Fabrikam East a Fabrikam West. Platby odběratele jsou zadávány do společnosti Fabrikam.
-   Pole **Zaúčtovat platební slevu** na stránce **Mezipodnikové účetnictví** je nastaveno na hodnotu **Právnická osoba faktury**.
-   Pole **Zaúčtovat zisk nebo ztrátu směnného kurzu** na stránce **Mezipodnikové účetnictví** je nastaveno na hodnotu **Právnická osoba platby**.
-   Odběratel Northwind Traders je u každé právnické osoby nastaven jako odběratel. Odběratelé z různých právnických osob jsou označení jako stejný odběratel, protože mají stejný identifikátor globálního adresáře.

| ID adresáře | Účet odběratele | Název              | Právnická osoba  |
|-----------------|------------------|-------------------|---------------|
| 4050            | 4000             | Northwind Traders | Fabrikam      |
| 4050            | 4000             | Northwind Traders | Fabrikam-východ |
| 4050            | 10000            | Northwind Traders | Fabrikam-západ |

## <a name="example-1-customer-payment-of-invoice-from-another-legal-entity"></a>Příklad 1: Odběratel platí fakturu od jiné právnické osoby
Společnost Fabrikam obdrží platbu ve výši 600,00 od odběratele číslo 4000 – Northwind Traders. Platba je vyrovnána s otevřenou fakturou odběratelského účtu číslo 4000 ve společnosti Fabrikam-východ.

### <a name="invoice-is-posted-in-fabrikam-east-for-customer-4000"></a>Zaúčtování faktury vystavené odběrateli číslo 4000 ve společnosti Fabrikam-východ.

| Účet                             | Částka Má dáti | Částka Dal |
|-------------------------------------|--------------|---------------|
| Pohledávky (Fabrikam-východ) | 600,00       |               |
| Tržby (Fabrikam-východ)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Příjem a zaúčtování platby od odběratele číslo 4000 ve společnosti Fabrikam.

| Účet                        | Částka Má dáti | Částka Dal |
|--------------------------------|--------------|---------------|
| Peníze (Fabrikam)                | 600,00       |               |
| Pohledávky (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Úhrada přijatá společností Fabrikam je vyrovnána s fakturou společnosti Fabrikam-východ.

**Účetnictví společnosti Fabrikam**

| Účet                         | Částka Má dáti | Částka Dal |
|---------------------------------|--------------|---------------|
| Pohledávky (Fabrikam)  | 600,00       |               |
| Závazky Fabrikam-východ (Fabrikam) |              | 600,00        |

**Účetnictví společnosti Fabrikam-východ**

| Účet                             | Částka Má dáti | Částka Dal |
|-------------------------------------|--------------|---------------|
| Pohledávky Fabrikam (Fabrikam-východ)   | 600,00       |               |
| Pohledávky (Fabrikam-východ) |              | 600,00        |

## <a name="example-2-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Příklad 2: Odběratel platí fakturu od jiné právnické osoby s platební slevou
Společnost Fabrikam obdrží platbu 580,00 na účet odběratele 4000 – Northwind Traders. Společnost Fabrikam East má otevřenou fakturu pro dodavatele 4000. Na faktuře je k dispozici platební sleva 20,00. Platba je vyrovnána s otevřenými fakturami společnosti Fabrikam-východ. Platební sleva je zaúčtována právnické osobě, která vystavila fakturu, což je Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Zaúčtování faktury vystavené odběrateli číslo 4000 ve společnosti Fabrikam-východ. Jedná se o odběratele společnosti Fabrikam-východ.

| Účet                             | Částka Má dáti | Částka Dal |
|-------------------------------------|--------------|---------------|
| Pohledávky (Fabrikam-východ) | 600,00       |               |
| Tržby (Fabrikam-východ)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Příjem a zaúčtování platby od odběratele číslo 4000 ve společnosti Fabrikam. Jedná se o odběratele společnosti Fabrikam.

| Účet                        | Částka Má dáti | Částka Dal |
|--------------------------------|--------------|---------------|
| Peníze (Fabrikam)                | 600,00       |               |
| Pohledávky (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Úhrada přijatá společností Fabrikam je vyrovnána s fakturou společnosti Fabrikam-východ.

**Účetnictví společnosti Fabrikam**

| Účet                         | Částka Má dáti | Částka Dal |
|---------------------------------|--------------|---------------|
| Pohledávky (Fabrikam)  | 580,00       |               |
| Závazky Fabrikam-východ (Fabrikam) |              | 580,00        |

**Účetnictví společnosti Fabrikam-východ**

| Účet                             | Částka Má dáti | Částka Dal |
|-------------------------------------|--------------|---------------|
| Pohledávky Fabrikam (Fabrikam-východ)   | 580,00       |               |
| Pohledávky (Fabrikam-východ) |              | 580,00        |
| Platební sleva (Fabrikam-východ)       | 20,00        |               |
| Pohledávky (Fabrikam-východ) |              | 20,00         |

## <a name="example-3-customer-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-gain"></a>Příklad 3: Odběratel platí fakturu od jiné právnické osoby s realizovaným kurzovým ziskem
Společnost Fabrikam obdrží platbu ve výši 600,00 eur (EUR) pro odběratele číslo 4000, což je Northwind Traders. Platba je vyrovnána s otevřenou fakturou odběratele číslo 4000 ve společnosti Fabrikam-východ. Během procesu vyrovnání je generovaná transakce kurzového zisku.

-   Směnný kurz z eur (EUR) na americké dolary (USD) k datu faktury: 1,2062
-   Kurz EUR/USD k datu platby: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Zaúčtování faktury vystavené odběrateli číslo 4000 ve společnosti Fabrikam-východ. Jedná se o odběratele společnosti Fabrikam-východ.

| Účet                             | Částka Má dáti            | Částka Dal           |
|-------------------------------------|-------------------------|-------------------------|
| Pohledávky (Fabrikam-východ) | 600,00 EUR tj. 723,72 USD |                         |
| Tržby (Fabrikam-východ)               |                         | 600,00 EUR tj. 723,72 USD |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Příjem a zaúčtování platby od odběratele číslo 4000 ve společnosti Fabrikam. Jedná se o odběratele společnosti Fabrikam.

| Účet                        | Částka Má dáti            | Částka Dal           |
|--------------------------------|-------------------------|-------------------------|
| Peníze (Fabrikam)                | 600,00 EUR tj. 736,62 USD |                         |
| Pohledávky (Fabrikam) |                         | 600,00 EUR tj. 736,62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Úhrada přijatá společností Fabrikam je vyrovnána s fakturou společnosti Fabrikam-východ.

**Účetnictví společnosti Fabrikam**

| Účet                         | Částka Má dáti            | Částka Dal           |
|---------------------------------|-------------------------|-------------------------|
| Pohledávky (Fabrikam)  | 600,00 EUR tj. 736,62 USD |                         |
| Závazky Fabrikam-východ (Fabrikam) |                         | 600,00 EUR tj. 736,62 USD |
| Závazky Fabrikam-východ (Fabrikam) | 0 EUR / 12,90 USD    |                         |
| Kurzové zisky (Fabrikam)        |                         | 0 EUR / 12,90 USD    |

**Účetnictví společnosti Fabrikam-východ**

| Účet                             | Částka Má dáti            | Částka Dal           |
|-------------------------------------|-------------------------|-------------------------|
| Pohledávky Fabrikam (Fabrikam-východ)   | 600,00 EUR tj. 736,62 USD |                         |
| Pohledávky (Fabrikam-východ) |                         | 600,00 EUR tj. 736,62 USD |
| Pohledávky (Fabrikam-východ) | 0 EUR / 12,90 USD    |                         |
| Pohledávky Fabrikam (Fabrikam-východ)   |                         | 0 EUR / 12,90 USD    |

## <a name="example-4-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-gain"></a>Příklad 4: Odběratel platí fakturu od jiné právnické osoby s platební slevou a realizovaným kurzovým ziskem
Společnost Fabrikam zaúčtuje úhradu otevřené faktury společnosti Fabrikam-východ od odběratele číslo 4000 – Northwind Traders (odběratel společnosti Fabrikam). Na faktuře je uvedena platební sleva a je vygenerována transakce DPH. Platba je vyrovnána s otevřenou fakturou společnosti Fabrikam-východ. Během procesu vyrovnání je generovaná transakce kurzového zisku. Platební sleva je zaúčtována u právnické osoby, která vystavila fakturu (Fabrikam East), a kurzový zisk je zaúčtován u právnické osoby platby (Fabrikam).

-   Kurz EUR/USD k datu faktury: 1,2062
-   Kurz EUR/USD k datu platby: 1,2277

### <a name="free-text-invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-customer-4000"></a>Zaúčtování volné faktury pro odběratele 4000 a generování daňové transakce ve společnosti Fabrikam-východ.

| Účet                             | Částka Má dáti            | Částka Dal           |
|-------------------------------------|-------------------------|-------------------------|
| Pohledávky (Fabrikam-východ) | 638,22 EUR tj. 769,82 USD |                         |
| Tržby (Fabrikam-východ)               |                         | 600,00 EUR tj. 723,72 USD |
| DPH – prodej (Fabrikam East)           |                         | 38,22 EUR tj. 46,10 USD   |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Příjem a zaúčtování platby od odběratele číslo 4000 ve společnosti Fabrikam.

| Účet                        | Částka Má dáti            | Částka Dal           |
|--------------------------------|-------------------------|-------------------------|
| Peníze (Fabrikam)                | 626,22 EUR tj. 768,81 USD |                         |
| Pohledávky (Fabrikam) |                         | 626,22 EUR tj. 768,81 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Úhrada přijatá společností Fabrikam je vyrovnána s fakturou společnosti Fabrikam-východ.

**Účetnictví společnosti Fabrikam**

| Účet                         | Částka Má dáti            | Částka Dal           |
|---------------------------------|-------------------------|-------------------------|
| Pohledávky (Fabrikam)  | 626,22 EUR tj. 768,81 USD |                         |
| Závazky Fabrikam-východ (Fabrikam) |                         | 626,22 EUR tj. 768,81 USD |
| Závazky Fabrikam-východ (Fabrikam) | 0 EUR / 13,46 USD    |                         |
| Kurzové zisky (Fabrikam)        |                         | 0 EUR / 13,46 USD    |

**Účetnictví společnosti Fabrikam-východ**

| Účet                             | Částka Má dáti            | Částka Dal           |
|-------------------------------------|-------------------------|-------------------------|
| Pohledávky Fabrikam (Fabrikam-východ)   | 626,22 EUR tj. 768,81 USD |                         |
| Pohledávky (Fabrikam-východ) |                         | 626,22 EUR tj. 768,81 USD |
| Pohledávky (Fabrikam-východ)  | 0 EUR / 13,46 USD    |                         |
| Pohledávky Fabrikam (Fabrikam-východ)   |                         | 0 EUR / 13,46 USD    |
| Platební sleva (Fabrikam-východ)       | 12,00 EUR tj. 14,47 USD   |                         |
| Pohledávky (Fabrikam-východ) |                         | 12,00 EUR tj. 14,47 USD   |

## <a name="example-5-customer-credit-note-with-primary-payment"></a>Příklad 5: Odběratelský dobropis s hlavní platbou.
Společnost Fabrikam obdrží platbu ve výši 75,00 od odběratele číslo 4000 – Northwind Traders. Platba je vyrovnána s otevřenou fakturou vystavenou společností Fabrikam-západ odběrateli číslo 10000 a otevřeným dobropisem od odběratele číslo 4000 (odběratel společnosti Fabrikam-východ). Tato platba je vybrána jako hlavní platba na stránce **Vyrovnat transakce**.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Zaúčtování faktury vystavené odběrateli číslo 10000 ve společnosti Fabrikam-západ.

| Účet                             | Částka Má dáti | Částka Dal |
|-------------------------------------|--------------|---------------|
| Pohledávky (Fabrikam-západ) | 100,00       |               |
| Tržby (Fabrikam-západ)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Zaúčtování dobropisu ve společnosti Fabrikam-východ pro odběratele číslo 4000.

| Účet                             | Částka Má dáti | Částka Dal |
|-------------------------------------|--------------|---------------|
| Prodejní vratky (Fabrikam-východ)       | 25,00        |               |
| Pohledávky (Fabrikam-východ) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Zaúčtování přijaté platby ve společnosti Fabrikam od odběratele číslo 4000.

| Účet                        | Částka Má dáti | Částka Dal |
|--------------------------------|--------------|---------------|
| Peníze (Fabrikam)                | 75,00        |               |
| Pohledávky (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Platba přijatá společností Fabrikam je vyrovnaná s fakturou společnosti Fabrikam-západ a dobropisem společnosti Fabrikam-východ.

**Účetnictví společnosti Fabrikam**

| Účet                           | Částka Má dáti | Částka Dal |
|-----------------------------------|--------------|---------------|
| Pohledávky Fabrikam-východ (Fabrikam) | 25,00        |               |
| Pohledávky (Fabrikam)    |              | 25,00         |
| Pohledávky (Fabrikam)    | 100,00       |               |
| Závazky Fabrikam-západ (Fabrikam)   |              | 100,00        |

**Účetnictví společnosti Fabrikam-východ**

| Účet                             | Částka Má dáti | Částka Dal |
|-------------------------------------|--------------|---------------|
| Pohledávky (Fabrikam-východ) | 25,00        |               |
| Závazky Fabrikam (Fabrikam-východ)     |              | 25,00         |

**Účetnictví společnosti Fabrikam-západ**

| Účet                             | Částka Má dáti | Částka Dal |
|-------------------------------------|--------------|---------------|
| Pohledávky Fabrikam (Fabrikam-západ)   | 100,00       |               |
| Pohledávky (Fabrikam-západ) |              | 100,00        |

## <a name="example-6-customer-credit-note-without-primary-payment"></a>Příklad 6: Odběratelský dobropis bez hlavní platby.
Společnost Fabrikam obdrží platbu ve výši 75,00 od odběratele číslo 4000 – Northwind Traders. Platba je vyrovnána s otevřenou fakturou vystavenou společností Fabrikam-západ odběrateli číslo 10000 a otevřeným dobropisem od odběratele číslo 4000 (odběratel společnosti Fabrikam-východ). Tato platba není vybrána jako hlavní platba na stránce **Vyrovnat transakce**.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Zaúčtování faktury vystavené odběrateli číslo 10000 ve společnosti Fabrikam-západ.

| Účet                             | Částka Má dáti | Částka Dal |
|-------------------------------------|--------------|---------------|
| Pohledávky (Fabrikam-západ) | 100,00       |               |
| Tržby (Fabrikam-západ)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Zaúčtování dobropisu ve společnosti Fabrikam-východ pro odběratele číslo 4000.

| Účet                             | Částka Má dáti | Částka Dal |
|-------------------------------------|--------------|---------------|
| Prodejní vratky (Fabrikam-východ)       | 25,00        |               |
| Pohledávky (Fabrikam-východ) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Zaúčtování přijaté platby ve společnosti Fabrikam od odběratele číslo 4000.

| Účet                        | Částka Má dáti | Částka Dal |
|--------------------------------|--------------|---------------|
| Peníze (Fabrikam)                | 75,00        |               |
| Pohledávky (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Platba přijatá společností Fabrikam je vyrovnaná s fakturou společnosti Fabrikam-západ a dobropisem společnosti Fabrikam-východ.

**Účetnictví společnosti Fabrikam**

| Účet                         | Částka Má dáti | Částka Dal |
|---------------------------------|--------------|---------------|
| Pohledávky (Fabrikam)  | 75,00        |               |
| Závazky Fabrikam-západ (Fabrikam) |              | 75,00         |

**Účetnictví společnosti Fabrikam-východ**

| Účet                              | Částka Má dáti | Částka Dal |
|--------------------------------------|--------------|---------------|
| Pohledávky (Fabrikam-východ)  | 25,00        |               |
| Závazky Fabrikam-západ (Fabrikam-východ) |              | 25,00         |

**Účetnictví společnosti Fabrikam-západ**

| Účet                                | Částka Má dáti | Částka Dal |
|----------------------------------------|--------------|---------------|
| Pohledávky Fabrikam (Fabrikam-západ)      | 75,00        |               |
| Pohledávky (Fabrikam-západ)    |              | 75,00         |
| Pohledávky Fabrikam-východ (Fabrikam-západ) | 25,00        |               |
| Pohledávky (Fabrikam-západ)    |              | 25,00         |






