---
title: "Centralizované platby pro závazky"
description: "Organizace zahrnující více právnických osob mohou vytvářet a spravovat platby pomocí jedné právnické osoby, která zpracovává všechny platby. Proto stejné platby není nutné zadat pro více právnických osob. Tento článek uvádí příklady, které znázorňují zpracování zaúčtování pro centralizované platby v různých scénářích."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14341
ms.assetid: 7bd02e32-2416-4ac6-8a60-85525267fdb7
ms.search.region: Global
ms.author: Shiva.Pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 23541bb2d82b552cdc9e0ada4aa4ec473f498d0b
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017

---

# <a name="centralized-payments-for-accounts-payable"></a>Centralizované platby pro závazky

[!include[banner](../includes/banner.md)]


Organizace zahrnující více právnických osob mohou vytvářet a spravovat platby pomocí jedné právnické osoby, která zpracovává všechny platby. Proto stejné platby není nutné zadat pro více právnických osob. Tento článek uvádí příklady, které znázorňují zpracování zaúčtování pro centralizované platby v různých scénářích.

Organizace zahrnující více právnických osob mohou vytvářet a spravovat platby pomocí jedné právnické osoby, která zpracovává všechny platby. Proto stejné platby není nutné zadat pro více právnických osob. Kromě toho organizace šetří čas, protože je zjednodušen proces plateb.

V organizaci s centralizovanými platbami existuje mnoho právnických osob pro operace a každá provozní právnická osoba spravuje své vlastní faktury dodavatele. Platby pro všechny provozní právnické osoby jsou generovány jednou právnickou osobou, která se nazývá právnická osoba platby. Během procesu vyrovnání jsou generovány odpovídající kreditní a debetní transakce. Můžete určit, která právnická osoba v organizaci přijímá transakce realizovaného zisku nebo realizované ztráty a také jak mají být zpracovány transakce platebních slev, které souvisejí s platbou mezi společnostmi. 

Následující příklady ilustrují způsob zaúčtování při různých scénářích. U všech těchto příkladů se předpokládá následující konfigurace:

-   Právnické osoby jsou Fabrikam, Fabrikam East a Fabrikam West. Platby provádí společnost Fabrikam.
-   Pole **Zaúčtovat platební slevu** na stránce **Mezipodnikové účetnictví** je nastaveno na hodnotu **Právnická osoba faktury**.
-   Pole **Zaúčtovat zisk nebo ztrátu směnného kurzu** na stránce **Mezipodnikové účetnictví** je nastaveno na hodnotu **Právnická osoba platby**.
-   Dodavatel Fourth Coffee je nastaven jako dodavatel u každé právnické osoby. Dodavatelé z různých právnických osob jsou označení jako stejný dodavatel, protože mají stejný identifikátor globálního adresáře.

| ID adresáře | Účet dodavatele | Název          | Právnická osoba  |
|--------------|----------------|---------------|---------------|
| 1050         | 3004           | Fourth Coffee | Fabrikam      |
| 1050         | 100            | Fourth Coffee | Fabrikam-východ |
| 1050         | 3004           | Fourth Coffee | Fabrikam-západ |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a>Příklad 1: Platba faktury dodavatele od jiné právnické osoby
Společnost Fabrikam East má otevřenou fakturu pro účet dodavatele 100, Fourth Coffee. Společnost Fabrikam zadá a zaúčtuje platbu na účet dodavatele Fabrikam 3004, Fourth Coffee. Platba je poté vyrovnána s otevřenou fakturou.

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a>Faktura je zaúčtována ve společnosti Fabrikam East pro účet 100 dodavatele

| Účet                          | Částka Má dáti | Částka Dal |
|----------------------------------|--------------|---------------|
| Výdaje (Fabrikam East)          | 600,00       |               |
| Závazky (Fabrikam East) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Platba je generována a zaúčtována ve společnosti Fabrikam pro účet 3004 dodavatele

| Účet                     | Částka Má dáti | Částka Dal |
|-----------------------------|--------------|---------------|
| Závazky (Fabrikam) | 600,00       |               |
| Hotovost (Fabrikam)             |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Platba společnosti Fabrikam je vyrovnána s fakturou společnosti Fabrikam East

**Zaúčtování společnosti Fabrikam**

| Účet                           | Částka Má dáti | Částka Dal |
|-----------------------------------|--------------|---------------|
| Splatná částka od společnosti Fabrikam East (Fabrikam) | 600,00       |               |
| Závazky (Fabrikam)       |              | 600,00        |

**Zaúčtování společnosti Fabrikam East**

| Účet                          | Částka Má dáti | Částka Dal |
|----------------------------------|--------------|---------------|
| Závazky (Fabrikam East) | 600,00       |               |
| Závazky Fabrikam (Fabrikam-východ)  |              | 600,00        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Příklad 2: Platba faktury dodavatele od jiné právnické osoby s platební slevou
Společnost Fabrikam East má otevřenou fakturu pro účet dodavatele 100, Fourth Coffee. Faktura umožňuje hotovostní slevu ve výši 20,00. Společnost Fabrikam zadá a zaúčtuje platbu ve výši 580,00 pro dodavatele Fabrikam 3004, Fourth Coffee. Platba je vyrovnána s otevřenými fakturami společnosti Fabrikam-východ. Platební sleva je zaúčtována právnické osobě, která vystavila fakturu, což je Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Faktura je zaúčtována ve společnosti Fabrikam East pro dodavatele Fabrikam East 100

| Účet                          | Částka Má dáti | Částka Dal |
|----------------------------------|--------------|---------------|
| Výdaje (Fabrikam East)          | 600,00       |               |
| Závazky (Fabrikam East) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Platba je generována a zaúčtována ve společnosti Fabrikam pro dodavatele Fabrikam 3004

| Účet                     | Částka Má dáti | Částka Dal |
|-----------------------------|--------------|---------------|
| Závazky (Fabrikam) | 580,00       |               |
| Hotovost (Fabrikam)             |              | 580,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Platba společnosti Fabrikam je vyrovnána s fakturou společnosti Fabrikam East

**Zaúčtování společnosti Fabrikam**

| Účet                           | Částka Má dáti | Částka Dal |
|-----------------------------------|--------------|---------------|
| Splatná částka od společnosti Fabrikam East (Fabrikam) | 580,00       |               |
| Závazky (Fabrikam)       |              | 580,00        |

**Zaúčtování společnosti Fabrikam East**

| Účet                          | Částka Má dáti | Částka Dal |
|----------------------------------|--------------|---------------|
| Závazky (Fabrikam East) | 580,00       |               |
| Splatná částka pro společnost Fabrikam (Fabrikam East)  |              | 580,00        |
| Závazky (Fabrikam East) | 20,00        |               |
| Platební sleva (Fabrikam-východ)    |              | 20,00         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a>Příklad 3: Platba dodavatele faktury od jiné právnické osoby s realizovanou ztrátou směnného kurzu
Společnost Fabrikam East má otevřenou fakturu pro účet dodavatele 100, Fourth Coffee. Společnost Fabrikam zadá a zaúčtuje platbu pro dodavatele Fabrikam 3004, Fourth Coffee. Platba je vyrovnána s otevřenými fakturami společnosti Fabrikam East. Během procesu vyrovnání je poté vygenerována transakce ztráty směnného kurzu.

-   Směnný kurz z eura (EUR) na americké dolary (USD) k datu faktury: 1,2062
-   Kurz EUR/USD k datu platby: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Faktura je zaúčtována ve společnosti Fabrikam East pro dodavatele Fabrikam East 100

| Účet                          | Částka Má dáti            | Částka Dal           |
|----------------------------------|-------------------------|-------------------------|
| Výdaje (Fabrikam East)          | 600,00 EUR / 723,72 USD |                         |
| Závazky (Fabrikam East) |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Platba je generována a zaúčtována ve společnosti Fabrikam pro dodavatele Fabrikam 3004

| Účet                     | Částka Má dáti            | Částka Dal           |
|-----------------------------|-------------------------|-------------------------|
| Závazky (Fabrikam) | 600,00 EUR / 736,62 USD |                         |
| Hotovost (Fabrikam)             |                         | 600,00 EUR / 736,62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Platba společnosti Fabrikam je vyrovnána s fakturou společnosti Fabrikam East

**Zaúčtování společnosti Fabrikam**

| Účet                           | Částka Má dáti            | Částka Dal           |
|-----------------------------------|-------------------------|-------------------------|
| Splatná částka od společnosti Fabrikam East (Fabrikam) | 600,00 EUR / 736,62 USD |                         |
| Závazky (Fabrikam)       |                         | 600,00 EUR / 736,62 USD |
| Realizovaná ztráta (Fabrikam)          | 0,00 EUR / 12,90 USD    |                         |
| Splatná částka od společnosti Fabrikam East (Fabrikam) |                         | 0,00 EUR / 12,90 USD    |

**Zaúčtování společnosti Fabrikam East**

| Účet                          | Částka Má dáti            | Částka Dal           |
|----------------------------------|-------------------------|-------------------------|
| Závazky (Fabrikam East) | 600,00 EUR / 736,62 USD |                         |
| Splatná částka pro společnost Fabrikam (Fabrikam East)  |                         | 600,00 EUR / 736,62 USD |
| Splatná částka pro společnost Fabrikam (Fabrikam East)  | 0,00 EUR / 12,90 USD    |                         |
| Závazky (Fabrikam East) |                         | 0 EUR / 12,90 USD    |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a>Příklad 4: Platba dodavatele faktury od jiné právnické osoby s platební slevou a realizovanou ztrátou směnného kurzu
Společnost Fabrikam East má otevřenou fakturu pro účet dodavatele 100, Fourth Coffee. Na faktuře je uvedena platební sleva a je vygenerována transakce DPH. Společnost Fabrikam zaúčtuje platbu pro dodavatele Fabrikam 3004, Fourth Coffee. Platba je vyrovnána s otevřenou fakturou společnosti Fabrikam-východ. Během procesu vyrovnání je poté vygenerována transakce ztráty směnného kurzu. Platební sleva je zaúčtována u právnické osoby faktury (Fabrikam East) a ztráta směnného kurzu je zaúčtována u právnické osoby platby (Fabrikam).

-   Kurz EUR/USD k datu faktury: 1,2062
-   Kurz EUR/USD k datu platby: 1,2277

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a>Faktura je zaúčtována a je vygenerována transakce ve společnosti Fabrikam East pro účet dodavatele 100

| Účet                          | Částka Má dáti            | Částka Dal           |
|----------------------------------|-------------------------|-------------------------|
| Výdaje (Fabrikam East)          | 564,07 EUR / 680,38 USD |                         |
| DPH (Fabrikam East)        | 35,93 EUR / 43,34 USD   |                         |
| Závazky (Fabrikam East) |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Platba je generována a zaúčtována ve společnosti Fabrikam pro účet dodavatele 3004

| Účet                     | Částka Má dáti            | Částka Dal           |
|-----------------------------|-------------------------|-------------------------|
| Závazky (Fabrikam) | 588,72 EUR / 722,77 USD |                         |
| Hotovost (Fabrikam East)        |                         | 588,72 EUR / 722,77 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Platba společnosti Fabrikam je vyrovnána s fakturou společnosti Fabrikam East

**Zaúčtování společnosti Fabrikam**

| Účet                           | Částka Má dáti            | Částka Dal           |
|-----------------------------------|-------------------------|-------------------------|
| Splatná částka od společnosti Fabrikam East (Fabrikam) | 588,72 EUR / 722,77 USD |                         |
| Závazky (Fabrikam)       |                         | 588,72 EUR / 722,77 USD |
| Realizovaná ztráta (Fabrikam)          | 0,00 EUR / 12,66 USD    |                         |
| Splatná částka od společnosti Fabrikam East (Fabrikam) |                         | 0,00 EUR / 12,66 USD    |

**Zaúčtování společnosti Fabrikam East**

| Účet                          | Částka Má dáti            | Částka Dal           |
|----------------------------------|-------------------------|-------------------------|
| Závazky (Fabrikam East) | 588,72 EUR / 722,77 USD |                         |
| Splatná částka pro společnost Fabrikam (Fabrikam East)  |                         | 588,72 EUR / 722,77 USD |
| Splatná částka pro společnost Fabrikam (Fabrikam East)   | 0,00 EUR / 12,66 USD    |                         |
| Závazky (Fabrikam East) |                         | 0,00 EUR / 12,66 USD    |
| Závazky (Fabrikam East) | 11,28 EUR / 13,61 USD   |                         |
| Hotovostní sleva (Fabrikam East)    |                         | 11,28 EUR / 13,61 USD   |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a>Příklad 5: Dobropis dodavatele s primární platbou
Společnost Fabrikam vygeneruje platbu ve výši 75,00 pro účet dodavatele 3004, Fourth Coffee. Platba bude vyrovnána s použitím otevřené faktury pro účet 3004 dodavatele Fabrikam West a otevřeného dobropisu pro účet 100 dodavatele Fabrikam East. Tato platba je vybrána jako hlavní platba na stránce **Vyrovnat transakce**.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Faktura je zaúčtována pro společnost Fabrikam West pro účet dodavatele 3004

| Účet                          | Částka Má dáti | Částka Dal |
|----------------------------------|--------------|---------------|
| Výdaje (Fabrikam West)          | 100,00       |               |
| Závazky (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Dobropis je zaúčtován pro společnost Fabrikam East pro účet dodavatele 100

| Účet                          | Částka Má dáti | Částka Dal |
|----------------------------------|--------------|---------------|
| Závazky (Fabrikam East) | 25,00        |               |
| Vratky (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Platba je zaúčtována pro společnost Fabrikam pro účet dodavatele 3004

| Účet                     | Částka Má dáti | Částka Dal |
|-----------------------------|--------------|---------------|
| Závazky (Fabrikam) | 75,00        |               |
| Hotovost (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Platba společnosti Fabrikam je vyrovnána s fakturou Fabrikam West a dobropisem Fabrikam East

**Zaúčtování společnosti Fabrikam**

| Účet                           | Částka Má dáti | Částka Dal |
|-----------------------------------|--------------|---------------|
| Závazky (Fabrikam)       | 25,00        |               |
| Splatná částka pro společnost Fabrikam East (Fabrikam)   |              | 25,00         |
| Splatná částka od společnosti Fabrikam West (Fabrikam) | 100,00       |               |
| Závazky (Fabrikam)       |              | 100,00        |

**Zaúčtování společnosti Fabrikam East**

| Účet                           | Částka Má dáti | Částka Dal |
|-----------------------------------|--------------|---------------|
| Splatná částka od společnosti Fabrikam (Fabrikam East) | 25,00        |               |
| Závazky (Fabrikam East)  |              | 25,00         |

**Zaúčtování pro společnost Fabrikam West**

| Účet                          | Částka Má dáti | Částka Dal |
|----------------------------------|--------------|---------------|
| Závazky (Fabrikam West) | 100,00       |               |
| Splatná částka pro společnost Fabrikam (Fabrikam West)  |              | 100,00        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a>Příklad 6: Dobropis dodavatele bez primární platby
Společnost Fabrikam vygeneruje platbu ve výši 75,00 pro účet dodavatele 3004, Fourth Coffee. Platba bude vyrovnána s použitím otevřené faktury pro účet 3004 dodavatele Fabrikam West a otevřeného dobropisu pro účet 100 dodavatele Fabrikam East. Tato platba není vybrána jako hlavní platba na stránce **Vyrovnat transakce**.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Faktura je zaúčtována pro společnost Fabrikam West pro účet dodavatele 3004

| Účet                          | Částka Má dáti | Částka Dal |
|----------------------------------|--------------|---------------|
| Výdaje (Fabrikam West)          | 100,00       |               |
| Závazky (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Dobropis je zaúčtován pro společnost Fabrikam East pro účet dodavatele 100

| Účet                          | Částka Má dáti | Částka Dal |
|----------------------------------|--------------|---------------|
| Závazky (Fabrikam East) | 25,00        |               |
| Vratky (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Platba je zaúčtována pro společnost Fabrikam pro účet dodavatele 3004

| Účet                     | Částka Má dáti | Částka Dal |
|-----------------------------|--------------|---------------|
| Závazky (Fabrikam) | 75,00        |               |
| Hotovost (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Platba společnosti Fabrikam je vyrovnána s fakturou Fabrikam West a dobropisem Fabrikam East

**Zaúčtování společnosti Fabrikam**

| Účet                           | Částka Má dáti | Částka Dal |
|-----------------------------------|--------------|---------------|
| Splatná částka od společnosti Fabrikam West (Fabrikam) | 75,00        |               |
| Závazky (Fabrikam)       |              | 75,00         |

**Zaúčtování společnosti Fabrikam East**

| Účet                                | Částka Má dáti | Částka Dal |
|----------------------------------------|--------------|---------------|
| Splatná částka od společnosti Fabrikam West (Fabrikam East) | 25,00        |               |
| Závazky (Fabrikam East)       |              | 25,00         |

**Zaúčtování pro společnost Fabrikam West**

| Účet                              | Částka Má dáti | Částka Dal |
|--------------------------------------|--------------|---------------|
| Závazky (Fabrikam West)     | 75,00        |               |
| Splatná částka pro společnost Fabrikam (Fabrikam West)      |              | 75,00         |
| Závazky (Fabrikam West)     | 25,00        |               |
| Splatná částka pro společnost Fabrikam East (Fabrikam West) |              | 25,00         |






