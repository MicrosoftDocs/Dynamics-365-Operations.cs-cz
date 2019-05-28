---
title: Párování faktur závazků
description: Párování faktur závazků je procesem párování informací na faktuře dodavatele, nákupní objednávce a příjemce produktu.
author: abruer
manager: AnnBe
ms.date: 02/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 27361
ms.assetid: 9f3dace7-05d8-4974-8f85-aca2e224876c
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74a1f7e16064a954bb22dc233a77bf28747f7f11
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509261"
---
# <a name="accounts-payable-invoice-matching"></a>Párování faktur závazků

[!include [banner](../includes/banner.md)]

Párování faktur závazků je procesem párování informací na faktuře dodavatele, nákupní objednávce a příjemce produktu.

Při párování dokumentů jsou rozdíly mezi těmito dokumenty označovány jako odchylky v párování. Odlišnosti v párování se porovnávají s odchylkami, které jsou zadány. Pokud odchylka párování překračuje tolerované procento nebo částku, zobrazí se na stránce Faktura dodavatele a na stránce Historie faktur a podrobnosti párování odpovídající ikona. 

Zadáte například nákupní objednávku s jedním řádkem obsahujícím 1 000 baterií v ceně 1,00 za kus. Nákupní objednávka je schválena a odeslána dodavateli. Dodavatel odešle 1 000 baterií a vy vložíte příjemku produktu na 1 000 baterií v ceně 1,00 za kus. Skladová cena těchto baterií je aktualizována prostřednictvím zadané ceny. 

Obdržíte fakturu na 1 000 baterií s cenou 1,10 za kus. Vaše zásady právnické osoby pro tuto kategorii položek povolují 5procentní toleranci čisté jednotkové ceny. Cena 1,05 by byla přijatelná, ale cena 1,10 přijatelná není. Při zadávání údajů z faktury je identifikována odchylka párování cen a fakturu je možné uložit do doby, než dojde k vyřešení odchylky.

Můžete použít následující typy párování faktur závazků:

-   Párování součtů faktur – párování celkových částek na faktuře s celkovými částkami na nákupní objednávce. Tento typ párování faktur zahrnuje nejmenší množství podrobností, takže ho můžete použít k vytvoření ovládacích prvků, které zaměstnancům minimalizují čas potřebný ke kontrole informací o párování faktur.
-   Dvoucestné párování – páruje informace o ceně na faktuře s informacemi o ceně na nákupní objednávce.
-   Třícestné párování – páruje informace o ceně na faktuře s informacemi o ceně na nákupní objednávce. Také páruje informace o množství na faktuře s informacemi o množství na příjemkách produktů, které jsou vybrány pro fakturu.
-   Párování nákladů – páruje informace o nákladech (částky) na faktuře s informacemi o nákladech (částky) na nákupní objednávce.

> [!NOTE]
> Ostatní typy ověření faktury lze provést pomocí zásad faktur dodavatele. 

Dvoucestné s třícestné párování vždy páruje informace o ceně podle jednotkové ceny. Tyto zásady párování můžete nakonfigurovat rovněž tak, aby párovaly informace o ceně podle celkové ceny.
-   Párování čisté jednotkové ceny – párování informací o ceně pro dvoucestné nebo třícestné párování porovnáním čisté jednotkové ceny pro jednotlivé řádky na faktuře s odpovídající čistou jednotkovou cenou na nákupní objednávce. Čistá jednotková cena je určována podle tohoto vzorce: čistá částka na řádku / množství na řádku.
-   Párování celkové ceny – párování informací o ceně pro dvoucestné nebo třícestné párování porovnáním čisté ceny (celkové ceny) pro jednotlivé řádky na faktuře s odpovídající čistou částkou na nákupní objednávce. Čistá částka je určována podle tohoto vzorce: *(jednotková cena \* množství na řádku) + náklady na řádku − slevy na řádku*. Při párování celkové ceny podle procent, systém porovnává hodnoty pomocí měny transakce. Při párování celkové ceny podle částky, systém porovnává hodnoty pomocí zúčtovací měny.

Výpočet párování faktur se obvykle provádí automaticky při úpravě faktur dodavatele na stránce Faktura dodavatele. Případně lze párování faktur provést podle potřeby. Párování faktur na vyžádání je pro právnickou osobu řízeno parametrem Automaticky aktualizovat stav záhlaví faktury na kartě Ověření faktury na stránce Parametry závazků. Párování faktur lze provést také v rámci proces kontroly faktury. Výsledky párování faktur si můžete zobrazit na stránce Faktura dodavatele a na stránkách souvisejících s párováním faktur.

## <a name="invoice-totals-matching"></a> Párování součtu faktur
Párování součtu faktur můžete použít k ověření toho, zda se celkové částky na faktuře neodlišují od očekávaných částek o větší než přijatelnou odchylku. Šest součtů je porovnáno na stránce Shodné podrobnosti o celkových součtech faktur (viz následující tabulka). Pokud je přípustná tolerance pro párování součtů faktur 20 %, je za odchylku párování považována 100% odchylka pro částku celkové slevy.

| Pole Celkem    | Skutečný součet faktury | Očekávaný součet faktury | Odchylka v % | Stav párování |
|----------------|----------------------|------------------------|---------------------|--------------|
| Zůstatek        | 495,00               | 495,00                 | 0 %                  | Úspěšné       |
| Celková sleva | 0,00                 | 9,90                   | 100 %                | Nezdařilo se       |
| Náklady        | 64,90                | 64,90                  | 0 %                  | Úspěšné       |
| DPH      | 139,98               | 137,50                 | 2 %                  | Úspěšné       |
| Zaokrouhlení      | 0,00                 | 0,00                   | 0 %                  | Úspěšné       |
| Fakturovaná částka | 699,88               | 687,50                 | 2 %                  | Úspěšné       |

Párování součtu faktur je pro právnickou osobu řízeno přepínačem Párování součtu faktur na stránce Parametry závazků. Párování je provedeno na očekávaných součtech faktur a skutečných součtech faktur. Očekávané součty faktur jsou vypočítány na základě informací o cenách, nákladech a DPH na nákupní objednávce a na základě množství na faktuře.

## <a name="two-way-price-totals-matching"></a> Dvoucestné párování celkových cen na fakturách
Dvoucestné párování použijte k ověření toho, zda odchylka mezi informacemi o ceně na nákupní objednávce a faktuře jsou v rámci přípustné tolerance. Můžete porovnat informace o ceně pro čistou částku na každém řádku faktury a všechny čekající a dříve zaúčtované řádky faktury s čistou částkou na odpovídajícím řádku nákupní objednávky. Tento úkon se nazývá párování celkových cen. 

Párování celkových cen může být založeno na procentu, částce nebo na procentu a částce. 

Pokud je specifikována celková procentní tolerance nákupní ceny, porovná se pět polí (viz následující tabulka). Vzhledem k tomu, že celková procentní tolerance nákupní ceny činí 10 %, celková odchylky ceny 50 % představuje odchylku párování.

| Stav párování | Čistá částka faktury | Očekávaná čistá částka | Celková hodnota nespárované nákupní ceny (částka odchylky) | Celková procentuální hodnota nespárované nákupní ceny (procento odchylky) | Procento tolerance celkové nákupní ceny |
|--------------|--------------------|---------------------|--------------------------------------------------|-----------------------------------------------------------------|----------------------------------------|
| Úspěšné       | 105,00 USD             | 100,00              | 5,00                                             | 5 %                                                              | 10 %                                    |
| Nezdařilo se       | 150,00             | 100,00              | 50,00                                            | 50 %                                                             | 10 %                                    |

Pokud je specifikována celková tolerance částky nákupní ceny, porovná se pět polí (viz následující tabulka). Vzhledem k tomu, že celková tolerance částky nákupní ceny činí 100,00, částka celkové odchylky ceny 105,00 představuje odchylku párování.

| Stav párování | Čistá částka faktury | Očekávaná čistá částka | Celková hodnota nespárované nákupní ceny (částka odchylky) | Celková hodnota nespárovaných nákupních cen v zúčtovací měně (částka odchylky) | Tolerance celkové nákupní ceny |
|--------------|--------------------|---------------------|--------------------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Úspěšné       | 150,00             | 100,00              | 50,00                                            | 50,00                                                                   | 100,00                         |
| Nezdařilo se       | 205,00             | 100,00              | 105,00 USD                                           | 105,00 USD                                                                  | 100,00                         |

Pokud je párování celkových cen nastaveno procentuální tolerancí a částkou odchylky (někdy označovanou jako částku, kterou nelze překročit), při vyhodnocování toho, zda má řádek odchylku párování, se použijí obě tolerance. Jestliže procento nebo částka překračuje toleranci, jak je uvedeno v řádcích 150,00 a 205,00 v následující tabulce, má řádek odchylku párování.

| Stav párování | Čistá částka faktury | Očekávaná čistá částka | Celková procentuální hodnota nespárované nákupní ceny (procento odchylky) | Procento tolerance celkové nákupní ceny | Celková hodnota nespárovaných nákupních cen v zúčtovací měně (částka odchylky) | Tolerance celkové nákupní ceny |
|--------------|--------------------|---------------------|-----------------------------------------------------------------|----------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Úspěšné       | 105,00 USD             | 100,00              | 5 %                                                              | 10 %                                    | 5,00                                                                    | 100,00                         |
| Nezdařilo se       | 150,00             | 100,00              | 50 %                                                             | 10 %                                    | 50,00                                                                   | 100,00                         |
| Nezdařilo se       | 205,00             | 100,00              | 105 %                                                            | 10 %                                    | 105,00 USD                                                                  | 100,00                         |

Dvoucestné párování je pro právnickou osobu řízeno hodnotou v poli Zásady párování řádků na stránce Parametry závazků. V závislosti na výběru v poli Povolit přepsání zásad párování můžete na stránce Zásady párování zvolit dvoucestné párování pro určitého dodavatele, položku nebo kombinaci položky a dodavatele a na stránce Nákupní objednávka pro konkrétní nákupní objednávku.

Párování celkových cen je pro právnickou osobu řízeno polem Párování celkových cen na stránce Parametry závazků. Na této stránce jsou uvedeny také celková procentní tolerance a částka tolerance nákupní ceny (částka, kterou nelze překročit).

## <a name="two-way-net-unit-price-matching"></a> Dvoucestné párování čisté jednotkové ceny
Dvoucestné párování použijte k ověření toho, zda odchylka mezi informacemi o ceně na nákupní objednávce a faktuře jsou v rámci přípustné tolerance. Můžete porovnat informace o ceně pro jednotkovou cenu každé položky na faktuře. Tento úkon se nazývá párování čistých jednotkových cen. 

Devět částek řádku je porovnáno na stránce Podrobnosti o párování faktur (viz následující tabulka). Pokud je přípustná tolerance ceny pro párování čistých jednotkových cen 10 %, 22,61% odchylka pro čistkou jednotkovou cenu je považována za odchylku párování.

| Pole řádku                    | Hodnota faktury | Hodnota nákupní objednávky | Odchylka v % | Stav párování |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Jednotková cena                    | 55,40         | 55,38                | 0 %                  | Úspěšné       |
| Cenová jednotka                    | 1,00          | 1,00                 | 0 %                  | Úspěšné       |
| Nákupní poplatky          | 50,00         | 0,00                 | 100 %                | Nezdařilo se       |
| Sleva                      | 0,00          | 0,00                 | 0 %                  | Úspěšné       |
| Procento slevy              | 0,00          | 0,00                 | 0 %                  | Úspěšné       |
| Víceřádková sleva            | 0,00          | 0,00                 | 0 %                  | Úspěšné       |
| Procenta víceřádkové slevy | 0,00          | 0,00                 | 0 %                  | Úspěšné       |
| Čistá částka                    | 271,60        | 221,52               | 22,61 %              | Nezdařilo se       |
| Čistá jednotková cena                | 67,9000       | 55,3800              | 22,61 %              | Nezdařilo se       |

Dvoucestné párování je pro právnickou osobu řízeno hodnotou v poli Zásady párování řádků na stránce Parametry závazků. V závislosti na výběru v poli Povolit přepsání zásad párování můžete na stránce Zásady párování zvolit dvoucestné párování pro určitého dodavatele, položku nebo kombinaci položky a dodavatele a na stránce Nákupní objednávka pro konkrétní nákupní objednávku. 

Párování čistých jednotkových cen je pro právnickou osobu řízeno polem Povolit ověření párování faktur na stránce Parametry závazků. Procentní tolerance čisté jednotkové ceny pro položky, skupiny položek, dodavatele, skupiny dodavatelů, kombinace položek a dodavatelů nebo pro právnickou osobu lze konfigurovat na stránce Tolerance ceny.

## <a name="two-way-price-totals-matching-and-net-unit-price-matching"></a> Dvoucestné párování celkových cen a párování čistých jednotkových cen
Párování celkových cen a párování čistých jednotkových cen můžete použít společně. Tento příklad vychází z následující konfigurace:

-   Tolerance čisté jednotkové ceny pro položku Jednotka USB je 10 %.
-   Tolerance párování celkové ceny pro právnickou osobu je 15 % nebo 500,00.

Nákupní objednávka obsahuje následující řádek.

| Číslo zboží | Množství | Jednotková cena | Čistá částka |
|-------------|----------|------------|------------|
| Jednotka USB   | 1 000    | 10,00      | 10 000,00  |

Jsou vloženy tři faktury (viz následující tabulka). Existuje odchylka párování faktury pro Fakturu 3, protože odchylka 1 880,00 překračuje celkovou toleranci částky nákupní ceny 500,00. U párování celkových cen zahrnuje čistá částka na faktuře kromě faktury, s níž právě pracujete, také všechny dříve zaúčtované faktury.

| Číslo zboží          | Množství | Jednotková cena | Čistá částka | Shoda ceny | Párování celkových cen |
|----------------------|----------|------------|------------|-------------|-------------------|
| Faktura 1: Jednotka USB | 800      | 10,80      | 8 640,00   | Úspěšné      | Úspěšné            |
| Faktura 2: Jednotka USB | 100      | 10,80      | 1 080,00   | Úspěšné      | Úspěšné            |
| Faktura 3: Jednotka USB | 200      | 10,80      | 2 160,00   | Úspěšné      | Nezdařilo se            |
| Celkem                |          |            | 11 880,00  |             |                   |

## <a name="three-way-matching"></a>Třícestné párování

Třícestné párování použijte k ověření toho, zda odchylka mezi informacemi o ceně na nákupní objednávce a na faktuře spadá do přijatelné tolerance a zda množství na faktuře odpovídá množství na příslušných příjemkách produktů.

Na stránce Podrobnosti o párování faktur jsou porovnány stejné částky řádku jako u dvoucestného párování. Kromě toho se množství na faktuře spáruje s přijatým množstvím na příjemce produktu. Pokud se množství na faktuře liší od množství na spárované příjemce produktu, dojde k chybě párování množství.

| Pole řádku                    | Hodnota faktury | Hodnota nákupní objednávky | Odchylka v % | Stav párování |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Jednotková cena                    | 55,40         | 55,38                | 0 %                  | Úspěšné       |
| Cenová jednotka                    | 1,00          | 1,00                 | 0 %                  | Úspěšné       |
| Nákupní poplatky          | 50,00         | 0,00                 | 100 %                | Nezdařilo se       |
| Sleva                      | 0,00          | 0,00                 | 0 %                  | Úspěšné       |
| Procento slevy              | 0,00          | 0,00                 | 0 %                  | Úspěšné       |
| Víceřádková sleva            | 0,00          | 0,00                 | 0 %                  | Úspěšné       |
| Procenta víceřádkové slevy | 0,00          | 0,00                 | 0 %                  | Úspěšné       |
| Čistá částka                    | 271,60        | 221,52               | 22,61 %              | Nezdařilo se       |
| Čistá jednotková cena                | 67,9000       | 55,3800              | 22,61 %              | Nezdařilo se       |

| Pole řádku                     | Hodnota faktury | Stav párování |
|--------------------------------|---------------|--------------|
| Fakturované množství               | 4,00          |              |
| Celkový počet spárovaných příjemek produktů | 0,00          | Nezdařilo se       |

Třícestné párování je pro právnickou osobu řízeno hodnotou v poli Zásady párování řádků na stránce Parametry závazků. V závislosti na výběru v poli Povolit přepsání zásad párování můžete na stránce Zásady párování zvolit třícestné párování pro určitého dodavatele, položku nebo kombinaci položky a dodavatele a na stránce Nákupní objednávka pro konkrétní nákupní objednávku.

## <a name="charges-matching"></a> Párování nákladů
Párování nákladů můžete použít k ověření toho, zda se částky nákladů neodlišují od očekávaných částek o větší než přijatelnou procentní odchylku. Na stránce Porovnat hodnoty nákladů – faktura: se porovnají celkové částky pro každý kód nákladů, který je použit na faktuře a nákupní objednávce (viz následující tabulka). Pokud je přípustná tolerance pro kódy nákladů 25 %, je za odchylku párování považována 99 999 999 999,99% odchylka pro kód nákladů na licence.

> [!NOTE] 
> Procentní odchylka 99 999 999 999,99 % znamená, že očekávaná částka na základě nákupní objednávky je nulová a skutečná částka na faktuře je kladná hodnota. 

| Stav párování nákladů | Kód nákladů faktury | Skutečná celková počítaná hodnota | Očekávaná celková počítaná hodnota | Částka odchylky | Odchylka v % | Procento tolerance |
|----------------------|----------------------|-------------------------------|---------------------------------|-----------------|---------------------|----------------------|
| Nezdařilo se               | Licence              | 25                            | 0                               | 25              | 99 999 999 999,99 %  | 25 %                  |
| Úspěšné               | Dopravné              | 200                           | 200                             | 0               | 0 %                  | 25 %                  |
| Nezdařilo se               | Urychleně zpracovat             | 4                             | 2                               | 2               | 100 %                | 25 %                  |

Párování nákladů je pro právnickou osobu řízeno přepínačem Párování nákladů na stránce Parametry závazků. Procentuální tolerance odchylek pro náklady můžete nastavit na stránce Tolerance nákladů.

> [!NOTE]
> Párování nákladů se provádí jen u kódů nákladů, pro které je přepínač Porovnat hodnotu nákupní objednávky s hodnotou faktury na stránce Kód nákladů aktivován.

## <a name="related-functionality"></a> Související funkce
Faktury dodavatele bývají často založeny na příjemkách produktu, které představují skutečné dodávky, namísto na nákupních objednávkách. Částky faktur se někdy neshodují s částkami nákupních objednávek a dodané množství se někdy neshoduje s fakturovaným množstvím. Správu těchto informací si můžete usnadnit těmito způsoby:
-   Na základě příjemek produktů vytvořte fakturu dodavatele. K fakturám se automaticky navrhnou příjemky produktu a vy budete moci zvolit, které příjemky produktu se mají použít. V případě potřeby je možné vybrat také konkrétní položky na řádcích příjemky produktu z více nákupních objednávek.
-   Zobrazte a schvalte rozdíly mezi fakturovaným množstvím na faktuře a obdrženým množstvím na příjemce produktu. Pokud existuje rozdíl, můžete fakturu uložit a později ji spárovat s jinou příjemkou produktu nebo změnit fakturované množství, aby odpovídalo přijatému množství.
-   Zadejte částky faktur, které nebyly zahrnuty na původní nákupní objednávce, aby se informace na faktuře shodovaly s fakturou přijatou od dodavatele. Můžete porovnat náklady pro nákupní objednávky s náklady pro faktury. V případě potřeby lze přidat na faktury náklady a přidělit je jednotlivým řádkům faktury.
-   Zobrazte a schvalte odchylky párování cen mezi čistou jednotkovou cenou na faktuře a čistou jednotkovou cenou na nákupní objednávce. Pro právnické osoby, dodavatele a položky je možné nastavit procentuální tolerance ceny. Pokud se částka na řádku faktury dodavatele nenachází v přijatelné toleranci ceny, můžete fakturu uložit, dokud nedojde ke schválení jejího zaúčtování nebo dokud neobdržíte od dodavatele opravu.

Další informace naleznete v tématu [Zásady třícestného párování](three-way-matching-policies.md) a [Nastavení ověřování párování faktur závazků](tasks/set-up-accounts-payable-invoice-matching-validation.md). 




