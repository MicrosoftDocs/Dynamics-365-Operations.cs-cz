---
title: "Výkazy maloobchodu"
description: "Toto téma popisuje způsob vytváření a zaúčtování výkazů."
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 9e88a8b22b73aca5c2cee6984ecad3c62e597102
ms.contentlocale: cs-cz
ms.lasthandoff: 01/04/2019

---

# <a name="retail-statements"></a>Výkazy maloobchodu

[!include [banner](includes/banner.md)]

V aplikaci Microsoft Dynamics 365 for Retail proces zaúčtování výkazů slouží k zaúčtování transakcí, které se mohou vyskytovat v Cloudovém pokladním místě (POS) nebo v Modern POS (MPOS).. Proces zaúčtování výkazu používá plán distribuce k vyžádání sady transakcí Retail POS do klienta centrály (HQ). Parametry, které jsou definovány na stránkách **Parametry maloobchodu** a **Obchody** se používají k výběru transakcí, které budou převedeny na jednotlivé výkazy.

Proces zaúčtování je znázorněn na následujícím obrázku. V tomto procesu jsou transakce, které jsou zaznamenány v POS, předávány klientovi pomocí modulu Maloobchodní plánovač. Po přijetí transakcí klientem můžete vytvářet, kalkulovat a zaúčtovávat výkazy transakce pro daný obchod.

[![Proces zaúčtování výpisu](./media/retail-statements.png)](./media/retail-statements.png)

## <a name="creating-and-posting-statements"></a>Vytváření a zaúčtovávání výkazů

Výkaz můžete vytvářet ručně nebo pomocí dávkových procesů, které jste nastavili ke spuštění v pravidelných intervalech během dne. V obou případech následující postup slouží k vytvoření a zaúčtování výkazů.

### <a name="create-the-statement"></a>Vytvoření výkazu

Tento krok identifikuje obchod, pro který je výkaz ručně vytvořen. Pokud konfigurujete dávkové zpracování, můžete vytvořit automaticky výkazy pro všechny obchody podle určeného plánu.

### <a name="calculate-the-statement"></a>Výpočet výkazu

V tomto kroku jsou vybrány řádky transakcí na základě kritérií, která jsou definovaná pro jednotlivé obchody na stránkách **Parametry maloobchodu** a **Obchody**. Na těchto stránkách definujete kritéria a určujete způsob výpočtu transakce. Chcete-li zobrazit seznam transakcí, které jsou zahrnuty do výkazu, dříve než začnete počítat výkaz, použijte stránku **Transakce**.

Výpočet výkazu používá tyto výkazy úhrad z registračních pokladen jako spočítanou částku. Případně můžete zadat spočítanou částku ručně. Výkaz ukazuje rozdíl mezi prodejní částkou transakce a skutečně spočítanou částkou u všech metod platby. Výkaz je zaúčtován tehdy, když rozdílová částka je menší než maximální vybraný rozdílu v zaúčtování definovaný pro obchod.

> [!NOTE]
> Proces výpočtu výkazu používá globální číselnou řadu.

Při výpočtu výkazu výpočet zahrnuje následující úkoly:

- Pro vybraný rozsah dat označte transakce, které nebyly zahrnuty do předchozího výpočtu výkazu pro vybrané období.
- Proveďte výpočet celkových částek, které byly uhrazeny ve vybraných transakcích. Výsledky jsou zobrazeny v řádcích výkazu v závislosti na metodě výkazu:

    - Je-li metoda výkazu **Součet**, bude vytvořen řádek pro každý způsob platby ve vybraných transakcích.
    - Je-li metoda výkazu **Zaměstnanci**, bude vytvořen řádek pro každý způsob platby v transakcích provedených vybraným zaměstnancem.
    - Je-li metoda výkazu **Terminál POS**, bude vytvořen řádek pro každý způsob platby v transakcích provedených vybranou pokladnou.
    - Je-li metoda výkazu **Směna**, bude vytvořen řádek pro každý způsob platby v transakcích provedených během směny.

Pokud je na stránce **Obchody** zaškrtnuto políčko **Rozdělit podle způsobu výpisu**, vytvoří se samostatný výpis na základě hodnoty vybrané v poli **Způsob výpisu**.

Pokud otevírací doba obchodu přesahuje po půlnoci, můžete nakonfigurovat zaúčtování výkazů podle konce pracovního dne namísto podle konce kalendářního dne.

Na stránce **Obchody** na pevné záložce **Výpis/uzávěrka** v poli **Konec pracovního dne** zadejte čas, kdy musí být zaznamenána poslední transakce, aby byla zahrnuta do výkazu pracovního dne. Zaškrtnutím políčka **Zaúčtovat jako pracovní den** budete účtovat transakce v rámci stejného pracovního dne. Při zaúčtování výkazu, transakcí které jsou zaznamenány do stejného pracovního dne lze vložit do stejné prodejní objednávky, i když se některé transakce objeví před půlnocí a jiné po půlnoci.

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a>Příklad: Zaúčtování výkazu pro pracovní den, který zasahuje do dvou kalendářních dní

Obchod je otevřen v 8:00 až 3:00 a je zaškrtnuto políčko **Zaúčtovat jako pracovní den** v konfiguraci obchodu. 31. května obchod eviduje transakce mezi 8:00 a půlnocí. Obchod zaznamená také transakce, které se uskutečnily v době mezi 12:01 až 3:00 1. června.

Při zaúčtování výkazu obchodu při ukončení pracovního dne, dojde k vygenerování prodejní objednávky obsahující všechny transakce, které byly zapsány v pracovní době mezi 8.00 a 3.00 dopoledne, přestože k transakcím došlo během dvou dnů, 31. května i 1. června.

Pokud je stejný obchod nakonfigurován bez zaškrtnutého políčka **Zaúčtovat pracovní den** pro stejný obchod, jsou generovány samostatné prodejní objednávky, když obchod zaúčtovává výkazy při ukončení pracovního dne. Jedna prodejní objednávka obsahuje transakce, které byly zaznamenány během pracovní doby od 8.00 do půlnoci 31. května, a druhá prodejní objednávka obsahuje transakce, které byly zaznamenány v pracovní době mezi 12:01 a 3:00 1. června.

> [!NOTE]
> Před vytvořením výkazů zavřete směny v určeném období.

### <a name="post-the-statement"></a>Zaúčtování výkazu

Při zaúčtování výkazu prodejní objednávky a faktury jsou vytvořeny pro maloobchodní prodej ve výkazu.

- Prodej cash and carry jsou agregován na jedné prodejní objednávce a fakturován pro výchozího odběratele, který je přiřazen k obchodu.
- Maloobchodní prodeje, pro které byl přidání odběratel do transakce v Microsoft Dynamics 365 for Retail POS, generují samostatné prodejní objednávky a faktury, jednu pro každého jedinečného odběratele.

Pro platby ve výkazu jsou automaticky vytvořeny deníky plateb a zásoby jsou automaticky aktualizovány pro obchod POS.

