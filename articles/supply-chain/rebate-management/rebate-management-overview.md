---
title: Přehled modulu správy rabatu
description: Toto téma poskytuje přehled modulu správy rabatů pro Microsoft Dynamics 365 Supply Chain Management.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 136e528093e6e73ffe090cea0c02a4cdbf787c5efc3d9c0664869c995a682daa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720245"
---
# <a name="rebate-management-module-overview"></a>Přehled modulu správy rabatu

[!include [banner](../includes/banner.md)]

Můžete použít modul **Správa rabatů** k vytváření smluv, nabídek nebo dohod mezi vaším podnikem a jeho zákazníky nebo dodavateli, takže můžete vypočítat rabaty, odpočty a autorské poplatky. Správa rabatu sleduje a udržuje transakce rabatu a odpočtu na centrálním místě, kde je uživatelé mohou efektivně vytvářet, kontrolovat a zpracovávat.

Správa rabatů podporuje vytváření, údržbu a zpracování *rabatů*. Rabat je vrácení části kupní ceny prodávajícím nebo kupujícím. Rabaty jsou obvykle založeny na nákupu konkrétního množství nebo hodnoty zboží během určitého období. Na rozdíl od slev se rabaty provádějí až po úplné fakturaci částky nákupu.

Správa rabatů také podporuje *odpočty*. Odpočet je kompenzace, odměna nebo poplatek, který se platí buď za licenci, nebo za oprávnění používat duševní vlastnictví, jako je značka, autorské právo nebo patent, nebo za oprávnění používat účelně přírodní zdroj, jako je například rybaření, lov nebo těžba. Odpočty se obvykle počítají jako procento z výnosu nebo zisku z realizovaného použití. Čím více se duševní vlastnictví nebo přírodní zdroj používá, tím větší je odpočet, který se realizuje.

Správa rabatu navíc podporuje *autorské poplatky* zákazníka. Autorské poplatky jsou platby, které jedna strana provádí nabyvateli licence nebo franšízantovi za právo používat majetek.

Správa rabatů umožňuje definovat účetní profily pro dodávky, slevy a odpisy. Dále lze definovat účtování pro konkrétního zákazníka nebo dodavatele. Tímto způsobem lze nabídky, které se nevztahují na všechny scénáře zákazníků nebo dodavatelů, sledovat prostřednictvím účtování.

Transakce rabatů se generují automaticky na základě metody výpočtu, která je vybrána a naplánována v dávkových úlohách. Dále můžete nastavit pracovní postupy pro správu, kontrolu a schvalování dohod.

## <a name="basis-calculation"></a>Výpočet základu

Rabaty zákazníků, autorské poplatky zákazníků a rabaty prodejců mohou používat jiný základ, v závislosti na vašich obchodních požadavcích:

- Rabaty zákazníků mohou být založeny na prodejních objednávkách, dodacích listech nebo fakturách.
- Autorské poplatky zákazníků mohou být založeny na prodejních objednávkách, dodacích listech nebo zaplacených fakturách.
- Rabaty dodavatele mohou být založeny na nákupních objednávkách nebo prodejních objednávkách. Mohou být vypočítány na základě produktů, které jsou zakoupeny od dodavatele rabatu a prodány zákazníkům prostřednictvím prodejních faktur.

## <a name="flexible-calculations"></a>Flexibilní výpočty

Období pro výpočet rabatu jsou k dispozici jak u nabídek zákazníků, tak u nabídek dodavatelů. Období výpočtu definuje délku nabídky, frekvenci výpočtu a období výpočtu. Rabaty lze časově rozlišit na základě množství nebo částky prodejní objednávky kvalifikovaných produktů během období rabatu.

Pro každý výpočet dohody lze nastavit kterékoli z následujících období:

- Faktura
- Den
- Týden
- Měsíc
- Čtvrtletí
- Rok
- Přizpůsobené období
- Jakýkoli násobek některého z dříve uvedených období

Výpočet lze použít na jednotlivé zákazníky a produkty, skupiny zákazníků a produktů nebo na všechny zákazníky a produkty. Rabaty, které mají více řádků podrobností, mohou mít různá kvalifikační období. Období dodávek a nároků se mohou lišit. Například dodávky lze zpracovávat každý den, zatímco nároky se zpracovávají jednou za měsíc.

Rabaty lze konfigurovat na základě mnoha různých parametrů. Mohou být například konfigurovány jako procento, sazba nebo pevná částka. Existují čtyři hlavní metody výpočtu:

- Kroková
- Kumulativní
- Postupná
- Celková hodnota

Výsledky výpočtu rabatu lze snížit také o jiné rabaty, v závislosti na tom, zda je rabat nastaven tak, aby se počítal na základě čisté částky.

Na straně dodavatele mohou rabaty, které jsou založené na prodejních objednávkách, vypočítat cenu na základě pravidla FIFO, nejnovější nákupní ceny, průměrné nákupní ceny nebo prodejní ceny.

## <a name="rebate-target-transactions"></a>Cílové transakce rabatu

Výstupy, které nabídka rabatu nebo dohoda generuje, mohou být finanční nebo položkové.

Finanční výstupy jsou určeny typem platby, který je přiřazen ke smlouvě z účetního profilu. Tyto výstupy mohou zahrnovat deníky odpočtů zákazníků, volné faktury a faktury dodavatele. Pro účely auditu zahrnují cílové transakce finančních rabatů odkaz na původní dohodu o rabatu.

Výstupy položek vytvářejí bezplatnou prodejní objednávku položky pro rabaty zákazníků a nákupní objednávku pro rabaty dodavatele. Cílové transakce rabatu položky obsahují možnosti pro určení, která odkaz na rabat by měl být zadán na bezplatné prodejní objednávce nebo nákupní objednávce položky.

## <a name="accurate-rebate-calculations"></a>Přesné výpočty rabatů

Kombinace přidružených nabídek, četnost výpočtů, základ výpočtu a vybraná metoda výpočtu určuje přesnost výpočtů rabatů. K časovému rozlišení zaúčtovaných a nárokovaných hodnot lze použít dodávky rabatů.

Zřizování lze spravovat denně, týdně, měsíčně nebo podle vlastního období. Funkce však může alokovat nebo vyplatit slevu nebo obdržet její platbu v jakékoli definované frekvenci, která je stejně dlouhá nebo delší než frekvence poskytování. Odpis používá stejnou frekvenci jako rabat. Uživatelé mohou kdykoli během vyplacení snadno upravit plán nebo částky plateb.

Uživatelé již nemusí řešit nabídky nebo dodávky ve dvou krocích. Dodávky a odpisy se zaúčtují přímo do hlavní knihy. Navíc lze automaticky vytvářet dobropisy. Existuje tedy úplná integrace se závazky a pohledávkami. Během zpracování výpočty mohou zohlednit slevy na vyrovnání, zaplacené faktury, obchodní slevy a stávající dobropisy, aby bylo zajištěno přesné vypočítání částek a hodnot.

Když se vypočítají rabaty, proces vytvoří transakce, které lze zkontrolovat, než dojde k zaúčtování. Samostatný proces zaúčtuje transakce správy rabatů. Deník, dobropis nebo debetní transakci lze poté vytvořit během zaúčtování do navrhovaných transakcí. Pro zajištění souladu, účinnosti a transparentnosti lze získat výkazy a výpisy transakcí.

## <a name="guaranteed-royalty-payments"></a>Zaručené platby autorských poplatků

Ve správě rabatů umožňuje automatické generování plateb rychlé a snadné vypořádání autorských poplatků, i když platí garantovaná minima.

## <a name="maximizing-spend-versus-rebates"></a>Maximální útrata a rabaty

Dodavatele a produkty lze seskupit podle území a lze poskytnout různé nabídky v závislosti na zemi nebo oblasti transakce. Když uživatelé vyberou produkty, mohou definovat zahrnuté položky a počet položek, které budou použity rabatu.
