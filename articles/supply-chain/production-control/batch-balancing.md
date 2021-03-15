---
title: Vyvážení dávky
description: Toto téma popisuje proces vyvážení dávky.
author: johanhoffmann
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8c1f52239b2050425c37a8130507e689b29205a8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966548"
---
# <a name="batch-balancing"></a>Vyvážení dávky

[!include [banner](../includes/banner.md)]

Toto téma popisuje podporu procesu vyvážení dávky.

Další informace naleznete ve [videu o vyvážení dávky](https://www.youtube.com/watch?v=4SNLWsU9KyI&feature=youtu.be).

V procesu vyvážení dávky se množství látek pro použití ve výrobní dávce vypočítá z koncentrace aktivních látek ve vybraných výrobních dávkách.

## <a name="products-that-have-an-active-ingredient"></a>Produkty, které mají aktivní látku

Produkt lze definovat podle jeho koncentrace aktivní látky. Aktivní látka produktu je modelována pomocí atributu dávky specifické pro produkt, který má minimální hodnotu, maximální hodnotu a cílovou úroveň.

Cílová úroveň atributu dávky představuje odhadované procento aktivní látky v produktu. Minimální a maximální hodnoty představují přijatelnou odchylku od cílové úrovně. Lze je použít například jako přijatelnou toleranci pro dávky na příjemce produktu.

Produkt může mít pouze jeden aktivní látku. Chcete-li určit aktivní látku produktu, je nutné nejprve definovat atribut dávky specifický pro produkt. Poté přiřaďte atribut jako základní atribut produktu.

Na úrovni produktu musíte rovněž upřesnit způsob, jakým chcete zaznamenat úroveň aktivní látky pro dávku produktu: buď jako součást procesu nákupní příjemky nebo jako součást procesu objednávky kvality.

Chcete-li přidružit základní atribut k produktu, je nutné následující nastavení:

- Produkt musí být řízen dávkou. Aby byl produkt řízen dávkou, musíte přiřadit k produktu skupinu sledovací dimenze, která má aktivní dimenze dávky.

- Atribut, který označuje úrovně látky musí být definován jako atribut dávky specifický pro produkt.

Vyhledání a úprava skutečné hodnoty aktivní látky pro dávku:
1. Přejděte na **Řízení zásob \> Dotazy a sestavy \> Sledovací dimenze \> dávky**.
1. Vyberte číslo šarže z mřížky.
1. V podokně akcí otevřete kartu **Zobrazení** a poté vyberte **Atributy dávky zásob**.

## <a name="ingredient-types-and-how-they-interact-in-the-batch-balancing-process"></a>Typy látek a způsob jejich interakce v procesu vyvážení dávky

Vytvořený řádek receptury může mít jeden z těchto typů látky:

- None
- Aktivní
- Kompenzování
- Vyplňující osoba

Zbývající část tohoto oddílu obsahuje příklady fungování každého typu látky. Příklady jsou založeny na následující receptuře, která má celkovou velikost dávky 100 litrů.

| Typ látky | Č. položky | Množství řádku receptury | Jednotka |
|---|---|---|---|
| None | A | 20 | Litr |
| Aktivní | mld. | 30 | Litr |
| Kompenzování | K | 10 | Litr |
| Vyplňující osoba | D | 40 | Litr |

Následující tabulka poskytuje přehled výsledků každého příkladu.

| Č. položky | Typ látky | Odhadované množství | Vyvážené množství | Aktivní množství | Jednotka | Základní hodnota |
|---|---|---|---|---|---|---|
| A | None | 20 | 20 | | Litr | |
| D | Aktivní | 30 | 25.71 | 9:00 | Litr | 30.00 |
| K | Kompenzování | 10 | 14.72 | | Litr | |
| D | Vyplňující osoba | 40 | 39.57 | | Litr | |

### <a name="active-ingredients"></a>Aktivní látky

Při přidání produktu se základním atributem do řádku receptury se na produkt odkazuje jako na *aktivní látku* receptury. Dávkové objednávky, které mají receptury obsahující aktivní látky, lze použít pro proces vyvážení dávky. U každé látky v receptuře odhaduje proces vyvážení dávky množství, které je zapotřebí k vyrobení produktu. Odhad množství vychází z koncentrace aktivních látek ve vybraných dávkách.

#### <a name="active-ingredient-example"></a>Příklad aktivní látky

Látka B má základní atribut X a cílovou úroveň 30. Je obsažena v receptuře, která vyžaduje 30 litrů látky B na každých 100 litrů produktu. Je vytvořena dávková objednávka s velikostí dávky 100 litrů. Je zahájena dávková objednávka a během procesu vyvážení dávky uživatel vybere dávku látky B s úrovní obsahu 35. Vzhledem k tomu, že je úroveň obsahu vyšší než cílová úroveň 30, je vyvážené množství látky B sníženo pomocí poměru hodnoty obsahu na cílovou úroveň dávky, která je vynásobena odhadovaným množstvím. Výpočet vyváženého množství vypadá takto:

(30 ÷ 35) x 30 litrů = 25,71 litrů.

### <a name="none-ingredients"></a>Žádné látky

Pokud použijete proces vyvážení dávky, když je **typ látky** *Žádná*, odhadované množství a vyvážené množství řádku receptury v dávkové objednávce je stejné.

#### <a name="none-ingredient-example"></a>Příklad žádné látky

Látka A je přiřazena k látce typu *Žádná* a přidána k receptuře pro dokončený produkt. Receptura vyžaduje 10 litrů látky A na každých 100 litrů dokončeného produktu. Když dávková objednávka vyžaduje 200 litrů, vyvážené množství látky i odhadované množství látky A se vypočítá na 20 litrů.

### <a name="compensating-ingredients"></a>Kompenzační látky

Kompenzační látka může buď vykompenzovat nebo doplnit účinek aktivní látky v produktu. Proto množství spotřebované kompenzační látky závisí na obsahu produktu:

- **Opačný efekt** – Je-li množství aktivní látky větší než předpokládané, je nutné přidat méně kompenzační látky.

- **Doplňkový efekt** – Je-li množství aktivní látky nižší než předpokládané, je nutné přidat více kompenzační látky.

Vztah mezi aktivní látkou a doplňkovou látkou se nastavuje na stránce **Princip kompenzace**.

Chcete-li nastavit vztahy mezi látkami, postupujte podle následujících kroků:

1. Vyberte **Řízení informací o produktech \> Kusovníky a receptury \> Receptury**.
1. Otevřete řádek vzorce a poté vyberte **Látky** pro otevření stránky **Princip kompenzace**.
1. Vyberte řádek, který představuje princip kompenzace, a poté vyberte aktivní látku ke kompenzaci.

V principu kompenzace také zadáte kladný nebo záporný kompenzační koeficient, kterým určíte, o kolik se bude kompenzovat a zda princip bude opačný nebo doplňkový. Kladný koeficient označuje doplňkový efekt a záporný koeficient označuje opačný efekt.

#### <a name="compensating-ingredient-example"></a>Příklad kompenzační látky

Látka B je aktivní látkou se základním atributem X a cílovou úrovní 30. Je obsažena v receptuře, která vyžaduje 30 litrů látky B na každých 100 litrů produktu. Látka C je kompenzační látka a její množství 10 je zahrnuto ve stejné receptuře. Kompenzační koeficient 1,1 je nastaven pro princip kompenzace. Proto vyvážené množství kompenzační látka bude sníženo o rozdíl mezi vyváženým množstvím aktivní látky a odhadovaným požadovaným množstvím vynásobeným 1,1.

V tomto příkladu bylo vypočítáno typ látky *Aktivní* vyvážené množství požadované aktivní látky 25,71 a odhadované požadované množství bylo vypočítáno na 30. V tomto případě se vypočítá vyvážené množství kompenzační látky takto:

1. Rozdíl mezi odhadovaným a vyváženým množstvím se určí takto:  
    25,71 – 30 = –4,29

1. Výsledek je pak vynásoben kompenzačním koeficientem:  
    4,29 × 1,10 = –4,72

1. Odhadované kompenzační množství bude sníženo o –4,72 k určení vyváženého kompenzačního množství:  
    10 – (–4,72) = 14,72

Vzhledem k tomu, že 1,10 je kladný kompenzační koeficient, má tento princip kompenzace doplňkový efekt. V takovém případě je aktivní látka koncentrovanější než se předpokládalo. Je tudíž zapotřebí více kompenzační látka.

### <a name="filler-ingredients"></a>Pomocné látky

*Pomocná látka* je neutrální látka, která se používá k dosažení požadovaného výstupního množství dokončeného produktu. Úpravy množství pomocné látky se vypočítají podle odchylek v aktivní látce a kompenzační látce ve srovnání se standardním množstvím.

#### <a name="filler-ingredient-example"></a>Příklad pomocné látky

Připravili jste recepturu produktu, který zahrnuje látky A, B, C a D pro velikost receptury 100 litrů. Vypočítali jste vyvážené množství všech typů látek, kromě typu látky *Pomocná látka*, který je použit na jednom řádku.
Vyvážené množství pomocné látky se počítá jako rozdíl mezi velikostí dávky 100 litrů a součtem látek A, B a C:

100 – (20 + 25,71 + 14,72) = 39,57

## <a name="the-batch-balancing-process"></a>Proces vyvážení dávky

Proces vyvážení dávky se provádí ze stránky **Vyvážení dávky**.
Zvolte **Řízení nákladů \> Dávkové objednávky** a poté na kartě **Proces** zvolte **Vyvážení dávky**. Vyvážení dávky je k dispozici pro dávkové objednávky, které mají stav **Zahájeno**.

Obecně platí, že vyvážení dávky lze použít pro dávkové objednávky, pokud má receptura alespoň jeden řádek receptury s **typem látky** *Aktivní*. (Ohledně výjimky k tomuto pravidlu nahlédněte do části "Dávkové objednávky, které nejsou použitelné pro vyvážení dávky" dále v tomto tématu)

Proces vyvážení dávky může být rozdělen do dvou dílčích procesů:

1. Látky pro vyvážení dávky
1. Potvrzení a uvolnění receptury

### <a name="balance-batch-ingredients"></a>Látky pro vyvážení dávky

V dílčím procesu látek pro vyvážení dávky se množství látek pro použití ve výrobní dávce vypočítá na základě zvolených dávek, které mají aktivní látky. Pravidlem je, že výpočet lze dokončit pouze tehdy, pokud existuje plná disponibilita všech látek. Nelze vyvážit pouze část dávky, když je dávková objednávka nastavena k výrobě.

> [!NOTE]
> Nelze uložit výpočte a poté dokončit proces vyvážení dávky později. Pokud zavřete stránku **Vyrovnání dávky**, je nutné opakovat výpočet pro dokončení procesu.

### <a name="confirm-and-release-the-formula"></a>Potvrzení a uvolnění receptury

Poté, co byla vypočtena množství látek, můžete potvrdit a uvolnit recepturu. Proces uvolnění se liší v závislosti na tom, zda jsou produkty povoleny pro procesy správy skladu:

- Pokud je produkt povolen pro procesy správy skladu, je řádek receptury uvolněn do skladu podle zásad pro procesy správy skladu. Řádek receptury je uvolněn v množstvích, která odpovídají vyrovnaným množstvím, a je uvolněn pro určité dávky vybraných pro aktivní látky.

    > [!NOTE]
    > Řádky receptury je možné uvolnit do skladu pouze jako součást procesu vyvážení dávky. I když existují další možnosti pro uvolnění materiálu pro výrobu do skladu, tyto možnosti nelze použít pro řádky receptury.

- Pokud není produkt povolen pro procesy správy skladu, je vytvořena výrobní výdejka pro produkt, když potvrdíte a uvolníte recepturu.

Do jedné receptury můžete kombinovat produkty, které jsou povoleny pro procesy správy skladu, a produkty, které nejsou povoleny pro procesy správy skladu. Když jsou v jedné receptuře zahrnuty dva typy produktů, jsou uvolněny do skladu produkty, které jsou povoleny pro procesy správy skladu. U produktů, které nejsou povoleny pro procesy správy skladu, je vytvořena výrobní výdejka, když potvrdíte a uvolníte recepturu.

### <a name="batch-orders-that-arent-applicable-for-batch-balancing"></a>Dávkové objednávky, které nejsou použitelné pro vyvážení dávky

Existují dvě výjimky z pravidla, že dávkové objednávky lze použít pro vyvážení dávky, a to, pokud má receptura alespoň jeden řádek receptury s **typem látky** *Aktivní*.

1. Pokud receptura obsahuje aktivní látku produktu, který je povolen pro procesy správy skladu, ale je číslo dávky je pod umístěním v hierarchii rezervací, není dávková objednávka použitelná pro vyvážení dávky.
1. Pokud se měrná jednotka vzorce liší od měrné jednotky inventáře aktivní látky, dávkové pořadí není použitelné pro vyvážení dávky.

Dávková objednávka, která není použitelná pro vyvážení dávky, prochází pravidelným cyklem procesu pro dávkové objednávky.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]