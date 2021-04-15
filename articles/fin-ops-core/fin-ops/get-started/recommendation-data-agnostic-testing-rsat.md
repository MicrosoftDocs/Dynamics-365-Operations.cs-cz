---
title: Agnostické testování dat pomocí Regression Suite Automation Tool
description: V tomto tématu jsou popsána doporučení pro agnostické testování dat pomocí Regression Suite Automation Tool.
author: kfend
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 120a88790b7cdb6a8cfcf97cbafeced4685384f2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744656"
---
# <a name="data-agnostic-testing-using-the-regression-suite-automation-tool"></a>Agnostické testování dat pomocí Regression Suite Automation Tool

[!include [banner](../includes/banner.md)]

Zatímco ověření funkčnosti aplikace ERP nemůže být plně agnostické, existuje několik fází a přístupů k testování. Tyto fáze testování zahrnují:  

- Rámec SysTest
- Rámec ATL
- Regression Suite Automation Tool (RSAT)

[![Zkušební pyramida klasifikace](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)

## <a name="overview"></a>Přehled
-   **Rámec SysTest** – rámec SysTest je spolehlivý pro zapisování testů jednotek. Vzhledem k tomu, že testy jednotek obvykle testují metodu nebo funkci, měly by vždy být agnostické podle dat a záviset pouze na vstupních datech, která jsou poskytována jako součást testu.
-   **Rámec ATL** – společnost Microsoft má rámec ATL, který je abstrakcí na rámec SysTest Framework a zajišťuje, že jsou funkce testování funkčnosti mnohem jednodušší a spolehlivější. Tento rámec by měl být použit k zápisu testů komponent nebo testů jednoduchých integrací.
-   **RSAT** – RSAT se používají pro testy integrace a testy obchodních cyklů. Testy obchodních cyklů, nazývané také regresní testy, jsou závislé na existujících datech. Tyto testy se však mohou stát datově agnostickými, pokud je třeba zvážit další faktory. 

    - o Tam, kde jsou testy jednotek a testy součástí nízké úrovně a mohou být plně datově agnostické (nezávisle na existující datové sadě), obchodní cyklus nebo testy regresního ověření jsou závislé na některých existujících datech. Mezi tato data patří nastavení, nastavení konfigurace (parametry) a hlavní data (odběratel, dodavatelé, položky atd.), ale nikdy neexistují data transakcí. Zkontrolujte, zda v průběhu testu nebyly některé z nich změněny, že jsou v rámci konečného testu vráceny zpět.
    - Vyberte hlavní data na základě určitých kritérií namísto výběru konkrétního záznamu. Chcete-li například vybrat položku na základě hodnot dimenzí a dostupnosti zásob, filtrujte seznam produktů s těmito hodnotami, vyberte první položku a zkopírujte číslo, které bude použito pro budoucí testy. Jedná-li se o jednoduchý řádek hlavní datové položky, jako je například odběratel, dodavatel nebo položka, lze jej vytvořit jako součást automatizace a použít v budoucích testech pomocí zřetězení. 
    - o Zadejte jedinečné identifikátory, jako například čísla faktur, pomocí číselné řady nebo pomocí funkcí Microsoft Excel jako = =TEXT(NOW(),"yyyymmddhhmm"). Tato funkce zadá jedinečné číslo každou minutu, což umožňuje sledovat, kdy k akci došlo. Lze je použít pro proměnné, jako jsou například čísla příjemek produktů a čísla faktur dodavatele. Tyto testy znovu pracují se stejnou databází i znovu, aniž by bylo nutné provést obnovení.
    - Vždy nastavte **režim úprav** prostředí na **čtení** nebo **úprava** jako první testovací případ, protože výchozí volba je **Auto**. Možnosti **Auto** vždy používají předchozí nastavení a mohou být příčinou nespolehlivých testů. 
 
    [![Stránka Možnosti, karta Výkon](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)
 
    - Proveďte ověření až poté, co filtrujete určitou transakci namísto obecného ověřování. Například pro počet záznamů můžete filtrovat číslo transakce nebo datum transakce tak, aby ověření vyloučilo všechny ostatní transakce. 
    - Pokud kontrolujete zůstatek odběratele nebo kontrolu rozpočtu, nejprve hodnotu uložte a poté přidejte hodnotu transakce pro ověření očekávaného výsledku namísto ověření pevné očekávané hodnoty. 
 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]