---
title: Mezipodnikové účetnictví pro centralizované platby
description: Toto téma popisuje vyrovnání pro centralizované platby v aplikaci Microsoft Dynamics 365 Finance.
author: abruer
ms.date: 08/02/2018
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "222414"
- intro-internal
ms.assetid: 610f6858-0f37-4d0f-8c68-bab5a971ef4a
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d00455d36b4350deffdd0bccb5529ce9e69a7cc
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982220"
---
# <a name="settlement-overview-for-centralized-payments"></a>Mezipodnikové účetnictví pro centralizované platby

[!include [banner](../includes/banner.md)]

Organizace zahrnující více právnických osob mohou vytvářet a spravovat platby pomocí jedné právnické osoby, která zpracovává všechny platby. Tento způsob vylučuje nutnost zadávat stejné transakce do několika právnických osob a šetří čas tím, že zjednodušuje proces návrhů plateb, proces vyrovnání, úpravy otevřených a uzavřených transakcí u centralizovaných plateb. 

Když je u jedné právnické osoby zadána platba odběratele nebo dodavatele a je vyrovnána s fakturou zadanou v jiné právnické osobě, pro každou právnickou osobu se automaticky vygeneruje použitelné vyrovnání a kreditní a debetní transakce. Pro každou kombinaci faktury a platby v transakci je vytvořen záznam vyrovnání. Každému záznamu vyrovnání je přiřazeno nové číslo dokladu, které je založeno na číselné řadě platebních dokladů zadané na stránce **Parametry pohledávek** pro odběratele a na stránce **Parametry závazků** pro dodavatele. 

Pokud dojde ke generování dalších záznamů vyrovnání pro platební slevy, přecenění cizí měny, haléřové rozdíly, přeplatky nebo nedoplatky, bude jim přiřazeno pozdější z dat platby nebo transakce faktury. Pokud k vyrovnání dojde po zaúčtování platby, bude pro záznamy vyrovnání použito datum zaúčtování vyrovnání zadané na stránce **Vyrovnání otevřených transakcí**.

## <a name="posting-types-transaction-types-and-default-descriptions"></a>Typy zaúčtování, typy transakcí a výchozí popisy

Mezipodnikové vyrovnání transakcí dokladu používá typ zaúčtování vyrovnání mezipodnikového odběratele a typy transakcí vyrovnání mezipodnikového dodavatele. Informace pro typ transakce můžete nastavit na stránce **Výchozí popisy**. 

Pro vyrovnání v rámci jedné společnosti a mezi společnostmi jsou k dispozici následující typy transakcí:

-   Vyrovnání
-   Platební sleva
-   Přecenění cizí měny (zahrnuje realizované a nerealizované přecenění cizí měny)
-   Haléřový rozdíl
-   Přeplatek nebo nedoplatek

Výchozí popis můžete definovat také pro mezipodnikové doklady vyrovnání.

## <a name="currency-exchange-gains-or-losses"></a>Zisky nebo ztráty směnného kurzu

Směnný kurz používaný pro transakce odběratele nebo dodavatele je uložen spolu s příslušnou transakcí. Realizované zisky nebo ztráty směnných kurzů jsou účtovány právnické osobě faktury nebo platby v závislosti na možnosti vybrané v poli **Zaúčtovat kurzový zisk nebo ztrátu** na stránce **Mezipodnikové účetnictví** pro právnickou osobu platby. V následujících příkladech jsou uvedeny tyto měny:
-   Zúčtovací měna platby: EUR
-   Zúčtovací měna faktury: USD
-   Měna transakce platby: DKK
-   Měna transakce faktury: CAD

### <a name="currency-calculations"></a>Kalkulace měny

Při vyrovnání faktury zadané v rámci jedné právnické osoby s platbou zadanou v rámci jiné právnické osoby dojde k převodu měny transakce platby (DKK) ve třech krocích:
1.  Převod na zúčtovací měnu platby (EUR) podle směnných kurzů právnické osoby faktury platných k datu platby.
2.  Převod na zúčtovací měnu faktury (USD).
3.  Převod na měnu transakce faktury (CAD) podle směnných kurzů od právnické osoby faktury.

Proces převodu používá směnné kurzy platné k datu platby. Pokud se výsledná částka platby v měně transakce faktury (CAD) shoduje s částkou na faktuře (CAD), faktura je považována za zcela zaplacenou. 

Po otevření stránky **Vyrovnat otevřené transakce** z deníku plateb, kam nebyla zadána částka platby, je částka k vyrovnání vypočtena na základě faktur vybraných k vyrovnání na stránce **Vyrovnat otevřené transakce**. Částka k vyrovnání je převedena ve třech krocích:
1.  Převod na zúčtovací měnu faktury (USD) podle směnných kurzů společnosti právnické osoby platných k datu platby.
2.  Převod na zúčtovací měnu platby (EUR) podle směnných kurzů společnosti právnické osoby platných k datu platby.
3.  Převod na měnu transakce platby (DKK).

Výsledná částka platby je při zavření stránky **Vyrovnat otevřené transakce** přenesena do řádek deníku plateb.

### <a name="posting-for-gain-or-loss-because-of-different-accounting-currencies"></a>Zaúčtování zisku nebo ztráty kvůli různým účtovacím měnám

Pokud existuje kurzový zisk nebo ztráta, je zaúčtován zisk nebo ztráta právnické osobě, která je zadaná v poli **Zaúčtovat kurzový zisk nebo ztrátu** na stránce **Mezipodnikovém účetnictví** pro právnickou osobu platby. Částka zisku nebo ztráty je převedena na zúčtovací měnu právnické osoby, kde byla zaúčtována, podle směnného kurzu definovaného pro danou právnickou osobu.

## <a name="cash-discounts"></a>Platební slevy

Platební slevy generované během procesu vyrovnání mezi společnostmi jsou účtovány právnické osobě faktury nebo platby v závislosti na možnosti vybrané v poli **Zaúčtovat platební slevu** na stránce **Mezipodnikové účetnictví** pro právnickou osobu platby. Pro právnickou osobu faktury je generována odpovídající transakce vyrovnání.

## <a name="overpayments-and-underpayments"></a>Přeplatky a nedoplatky

Tolerance přeplatků nebo nedoplatků a haléřových rozdílů jsou u přeplatků určovány na základě právnické osoby platby a u nedoplatků jsou určovány na základě právnické osoby faktury. Používaný účet je určen nastavením v poli **Správa platební slevy** na stránce **Parametry pohledávek** pro odběratele a **Správa platební slevy** na stránce **Parametry závazků** pro dodavatele.

-   Pokud má nastavení správy platební slevy hodnotu Specifické, nebo pokud má toto nastavení hodnotu Nespecifické a odpovídající platební sleva je zaúčtována pro jinou právnickou osobu než přeplatek, bude použit automatický účet pro platební slevu odběratele, platební slevu dodavatele nebo haléřový rozdíl v účtovací měně. Tyto účty můžete specifikovat tyto účty na stránce **Účty pro automatické transakce**.
-   Pokud má nastavení správy platební slevy hodnotu Neurčeno a platební sleva je zaúčtována pro stejnou právnickou osobu jako přeplatek (právnická osoba platby je shodná s právnickou osobou faktury), dojde k úpravě účtu platební slevy. Pokud došlo například k vyrovnání faktury s částkou 100,00 a s možnou platební slevou 3,00 pomocí platby ve výši 98,00, dojde k úpravě účtu platební slevy o částku 1,00. Čistá částka slevy je 2.00.
-   Pokud má nastavení správy platební slevy hodnotu Neurčeno, dojde k zaúčtování platební slevy pro stejnou právnickou osobu jako přeplatek, přeplatek nebo nedoplatek je vyrovnán s více fakturami s platebními slevami a účet platební slevy je pro poslední fakturu upraven.

Pokud má výběr správy platební slevy hodnotu Neurčeno, dojde k použití pravidel vyrovnání neurčené platby pouze v následujících situacích:
-   Existuje přeplatek.
-   Přeplatek je vyrovnán jednou nebo více fakturami s platební slevou.
-   Platební sleva je zaúčtována pro stejnou právnickou osobu jako přeplatek.

Ve všech ostatních případech jsou přeplatky či nedoplatky zaúčtovány na automatický účet pro platební slevu odběratele. platební slevu dodavatele nebo haléřový rozdíl v zúčtovací měně.

## <a name="sales-tax"></a>DPH
Transakce DPH zůstávají v právnické osobě, kde byly původně zaúčtovány. 

Pokud byla DPH zaúčtována pro zálohu, vyrovnání mezi společnostmi danou DPH pro zálohu v právnické osobě zálohy stornuje. Daně u právnické osoby faktury zůstávají v právnické osobě faktury.

## <a name="financial-dimensions"></a>Finanční dimenze
U plateb odběratelů transakce počátečního a koncového data splatnosti v právnické osobě platby používají finanční dimenze uhrazené platby určené pro součtový účet vyrovnávaných pohledávek. V právnické osobě faktury transakce počátečního a koncového data splatnosti používají finanční dimenze uhrazené faktury určené pro součtový účet vyrovnávaných závazků. 

U plateb dodavatelů transakce počátečního a koncového data splatnosti v právnické osobě platby používají finanční dimenze uhrazené platby určené pro součtový účet vyrovnávaných závazků. V právnické osobě faktury transakce počátečního a koncového data splatnosti používají finanční dimenze uhrazené faktury určené pro součtový účet vyrovnávaných závazků.

## <a name="withholding-tax"></a>Srážková daň
Účet dodavatele, který je přidružený k faktuře, slouží k určení, zda se má vypočítat srážkovou daň. Pokud se srážková daň používá, je vypočteno v právnické osobě, která je přidružená k faktuře. Pokud právnické osoby používají různé měny, použije se směnný kurz z právnické osoby, která je přidružená k faktuře.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]