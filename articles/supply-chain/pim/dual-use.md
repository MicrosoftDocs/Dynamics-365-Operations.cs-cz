---
title: Zboží dvojího užití
description: Toto téma vysvětluje, jak sledovat výrobky, které jsou identifikovány jako zboží dvojího užití, ukládat čísla certifikátů pro každý relevantní produkt a zemi určení a tisknout platná čísla certifikátů na příslušné faktury, dodací listy a / nebo prodejní objednávky.
author: dasani-madipalli
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COODualUseCerts, COORules, COODualUseCountries
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 15e8696b2bfa9f1df3cecd2d98b9ad2f6c5d6000
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829467"
---
# <a name="dual-use-goods"></a>Zboží dvojího užití

[!include [banner](../includes/banner.md)]

Zboží dvojího užití je obvykle zboží, které má civilní i vojenské použití. Například chemická látka může být použita jako hnojivo nebo výbušnina. Mnoho zemí má zvláštní předpisy, které se vztahují na vývoz, dovoz a přepravu zboží dvojího užití. Proto je důležité, aby společnosti, které se podílejí na mezinárodním obchodu se zbožím dvojího užití, sledovaly různé politiky a certifikáty.

Funkce dvojího užití pomáhá společnostem sledovat výrobky, které jsou identifikovány jako zboží dvojího užití, ukládat čísla certifikátů pro každý relevantní produkt a zemi určení a tisknout platná čísla certifikátů na příslušné faktury, dodací listy a / nebo prodejní objednávky. Pomáhá zajistit, aby při dodání vašich produktů vždy obsahovaly aktuální certifikáty.

Představte si následující scénář:

1. Stránka **Nastavení země dvojího užití** ve vašem systému označuje, že zásilky do Francie vyžadují certifikaci.
2. Stránka **Vydané podrobnosti o produktu** pro produkt X-100 naznačuje, že se jedná o zboží dvojího užití. Kód, kategorie, skupina a režim společně označují klasifikaci kontroly vývozu, do které produkt patří.
3. Stránka **Certifikáty dvojího užití** obsahuje certifikát pro produkt X-100, když je dodáván do Francie. Platnost tohoto certifikátu vyprší 1. ledna 2020.
4. 17. června 2020 vytvoříte prodejní objednávku pro zákaznickou společnost se sídlem ve Francii a objednávka zahrnuje produkt X-100.
5. Při uložení prodejní objednávky systém určí následující informace:

    1. Zahrnuje objednávka nějaké výrobky, které jsou zboží dvojího užití?
    2. Pokud objednávka zahrnuje zboží dvojího užití, vyžaduje země určení osvědčení o dvojím použití?
    3. Pokud země vyžaduje certifikáty dvojího užití, existuje platný certifikát pro každé zboží dvojího užití pro cílovou zemi?

6. Objednávka zahrnuje produkt X-100, produkt je dodáván do Francie a pro produkt existuje francouzský certifikát. Platnost certifikátu však vypršela. Proto se zobrazí následující upozornění: „Certifikáty dvojího užití pro jednu nebo více položek dvojího užití v této prodejní objednávce nejsou platné. Chcete pokračovat s potvrzením?“

Toto téma vysvětluje, jak nakonfigurovat všechna nastavení, která jsou nutná pro nastavení zboží dvojího užití, a podporovat tento scénář.

## <a name="define-dual-use-requirements-for-each-relevant-country"></a>Definujte požadavky na dvojí použití pro každou příslušnou zemi

Různé země mají různé požadavky na zboží dvojího užití. Používáte stránku **Nastavení země s dvojím použitím** pro sledování zemí, které vyžadují a nevyžadují certifikát. Informace, které zde zadáte, se při vytváření prodejních objednávek kontrolují a budete vyzváni, abyste zadali požadované certifikace.

Chcete-li nastavit informace o požadavcích dvojího užití pro různé země, postupujte takto.

1. Přejděte na **Správa informací o produktu \> Nastavení \> Shoda výrobků \> Výrobky dvojího užití \> Nastavení země s dvojím použitím**.
2. Vyberte existující nastavení země, které chcete upravit, nebo vyberte **Nový** v podokně akcí a vytvořte nové nastavení země.
3. Nastavte následující hodnoty pro vybranou nebo novou zemi.

    | Pole | popis |
    |---|---|
    | Země / oblast | Vyberte zemi, pro kterou sledujete požadavky. |
    | Je vyžadován certifikát | Zaškrtněte toto políčko u zemí, které vyžadují certifikaci pro zboží dvojího užití. Vymažte to pro země, které tuto certifikaci nevyžadují. |

## <a name="create-dual-use-categories"></a>Vytvoření kategorií dvojího užití

Zboží s dvojím použitím musí být často roztříděno podle svého klasifikačního čísla pro kontrolu vývozu (ECCN). ECCN je alfanumerický kód, který kategorizuje položky na základě faktorů, jako je komodita a technologie. Stránka **Kategorie dvojího užití** vám pomůže vytvořit seznam kategorií, které používáte pro účely vytváření přehledů.

Chcete-li kategorie dvojího užití, postupujte následujícím způsobem.

1. Přejděte na **Správa informací o produktu \> Nastavení \> Shoda výrobků \> Výrobky dvojího užití \> Kategorie dvojího použití**.
2. Vyberte existující kategorii, kterou chcete upravit, nebo vyberte **Nový** v podokně akcí a vytvořte novou kategorii.
3. Nastavte následující hodnoty pro vybranou nebo novou kategorii.

    | Pole | popis |
    |---|---|
    | Kód dvojího použití | Zadejte úplný kód ECCN (například *3A001*).|
    | Kategorie dvojího použití | Zadejte část kódu ECCN kategorie obchodního seznamu (CCL). Například pro kód ECCN *3A001*, tato hodnota je *3*. |
    | Skupina dvojího použití | Zadejte část kódu ECCN pro skupinu produktů. Například pro kód ECCN *3A001*, tato hodnota je *A*. |
    | Režim dvojího použití | Zadejte kód režimu pro tuto položku. Tento kód uvádí důvod, proč je položka klasifikována jako zboží dvojího užití. Například pro kód ECCN *3A001*, tato hodnota je *001*. |

## <a name="apply-dual-use-categories-to-products"></a>Použití produktů dvojího užití na produkty

Chcete-li produkt identifikovat jako zboží dvojího užití a použít pro něj kategorii dvojího užití, postupujte takto.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Vyberte nebo vytvořte produkt a otevřete jeho stránku **Podrobnosti o uvolněném produktu**.
1. Na pevné záložce **Zahraniční obchod** nastavte **Výrobky dvojího užití** na **Ano** pro identifikaci současného produktu jako zboží dvojího užití.
1. Nastavte pole **Kód pro dvojí použití** na kód, který se vztahuje na aktuální produkt. (Tento kód jste definovali na stránce **Kategorie dvojího užití**.)

Toto nastavení je zkontrolováno při vytváření prodejní objednávky.

## <a name="set-up-dual-use-certificates"></a>Nastavení certifikátů dvojího použití

Používáte stránku **Certifikáty dvojího použití** pro nastavení a správu požadovaných certifikátů dvojího užití pro každý produkt a zemi. Můžete sledovat podrobnosti každého certifikátu, například zemi a datum platnosti. Můžete také nastavit možnosti pro určení, kde by se tyto informace měly tisknout. Tyto informace mohou být například vytištěny na faktuře, na dodacím listě nebo na prodejní objednávce. Toto nastavení je zkontrolováno při vytváření prodejní objednávky.

1. Přejděte na **Správa informací o produktu \> Nastavení \> Shoda výrobků \> Výrobky dvojího užití \> Certifikáty dvojího použití**.
2. Vyberte existující certifikát, který chcete upravit, nebo vyberte **Nový** v podokně akcí a vytvořte nový certifikát.
3. Proveďte následující hodnoty pro vybraný nebo nový certifikát.

    | Pole | popis |
    |---|---|
    | Č. položky | Vyberte číslo položky zboží dvojího užití, na které se tento certifikát vztahuje. |
    | Země / oblast | Cílová země nebo region, kde musíte tento certifikát použít. |
    | Číslo certifikátu | Číslo, které se objeví na certifikátu vydaném prodejci nebo zákazníkovi. |
    | Platný | Vyberte první datum, kdy je aktuální certifikát platný.|
    | Vypršení platnosti | Vyberte poslední datum, kdy je aktuální certifikát platný. |
    | Vytisknout na fakturu | Zaškrtněte toto políčko, chcete-li vytisknout číslo certifikátu na fakturách, které jsou adresovány konkrétní zemi během zadaného časového období. |
    | Vytisknout na dodacím listu | Zaškrtněte toto políčko, chcete-li vytisknout číslo certifikátu na dodacích listech, které jsou adresovány konkrétní zemi během zadaného časového období. |
    | Vytisknout na prodejní objednávku | Zaškrtněte toto políčko, chcete-li vytisknout číslo certifikátu na prodejních objednávkách, které jsou adresovány konkrétní zemi během zadaného časového období. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]