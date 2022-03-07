---
title: Správa pokladní hotovosti pro Commerce pro východní Evropu
description: Toto téma popisuje, jak nastavit a používat funkce správy hotovosti v aplikaci Commerce pro východní Evropu.
author: epopov
manager: annbe
ms.date: 10/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: b7c7c63083dceebe73bfa04169a0b2da3228c8b1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407597"
---
# <a name="petty-cash-management-for-commerce-for-eastern-europe"></a>Správa pokladní hotovosti pro Commerce pro východní Evropu

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o východoevropské lokalizaci specifické pro oblast obchodu.

V souladu s požadavky na účtování ve východní Evropě můžete nastavit operace pro pokladní účty pro automatizaci procesů pro příjemky, pokladní doklady a výpisy hotovosti. Více informací naleznete v části [(EEUR) Nastavení parametrů pro správu hotovosti](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/eeur-set-up-parameters-for-cash-management).

Maloobchodní prodejci mohou přijímat různé typy plateb za výrobky a služby, které prodávají. I když jsou hotovostní platby nejčastěji používaným typem platby, maloobchodní prodejci mohou také přijímat platby ve formě šeků, karet nebo kuponů. V maloobchodním pokladním místě (POS) jsou hotovost, doklady o platbě kartou a ostatní platby zpracovány n pokladně.

Pomocí správy hotovosti v aplikaci Commerce můžete provádět následující akce:

- Vytvoření pokladního účtu pro vybraný způsob platby pro každý obchod.
- Použít deníky hotovosti k zaúčtování hotovostních transakcí a plateb zákazníků přijímaných v Retail POS.
- Sdružení transakcí v řádku výkazu při zaúčtování výkazu. Můžete sdružovat odvody do trezoru, odvody do banky, transakce dokladu, odebírat transakce odvodu, transakce s plovoucí položkou, příjmové transakce, výdajové transakce, platby odběratelů, prodejní transakce a návratové transakce.

Všechny transakce, které se uskutečňují v POS, jsou zaúčtovány pomocí deníku hlavní knihy. Pokladní deníky plateb, deníky plateb odběratelů a hlavní deníky můžete používat k vytvoření a zaúčtování výkazů. Více informací naleznete v části [Vytvoření, výpočet a zaúčtování výkazů pro maloobchod](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/create-calculate-post-statement-retail-store).

Na stránce **Zaúčtované výkazy** v podokně akcí můžete provést následující:

- Přejděte na **Dotazy \> Deník plateb v hotovosti** pro přístup k deníkům plateb v hotovosti souvisejícím s výkazem.
- Přejděte na **Dotazy \> Hlavní deník** pro přístup k deníkům hlavní knihy, které se vztahují k výkazu jinému, než jsou platby odběratele a platby v hotovosti.

## <a name="set-up-for-cash-management-for-pos"></a>Nastavení správy hotovosti pro POS

Následující postup nastavení je nutné dokončit před použitím řízení hotovosti:

- Nastavení metody platby pro každý typ platby, kterou přijímá prodejce na stránce **Metody platby**. Pro zaúčtování transakcí v POS můžete použít různé metody platby. Další informace o metodách platby naleznete v tématu [Metody platby](https://docs.microsoft.com/dynamics365/unified-operations/retail/payment-methods).
- Nastavení parametrů pro hotovostní operace.
- Nastavení metody platby pro platby v hotovosti v obchodě.

### <a name="set-up-parameters-for-cash-operations"></a>Nastavení parametrů pro hotovostní operace

Můžete nastavit parametry pro vytvoření a zaúčtování hotovostních transakcí v Commerce. K zaúčtování transakcí v POS můžete použít pokladní deníky a deníky plateb odběratelů nebo hlavní deníky. Lze seskupit transakce, které mají stejné vlastnosti při zaúčtování výkazu.

1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry obchodu**. V levém podokně klikněte na **Zaúčtování**.
2. V oblasti **Zaúčtování** na pevné záložce **Agregace** nastavte možnost **Úhrada – odebrat/plovoucí** na **Ano** pro agregaci odebrání transakcí úhrad nebo transakcí plovoucí položky, které jsou přidruženy k řádku výkazu při zaúčtování výkazu. Transakce odebrání úhrady je vytvořena při výběru hotovosti ze zásuvky s hotovostí POS. Transakce plovoucí položky je vytvořena při vložení hotovosti do zásuvky s hotovostí POS.
3. Aktivujte jednotlivé parametry uvedené níže pro seskupení transakcí, které jsou přidruženy k řádku výkazu při zaúčtování výkazu:

    - **Odvod do banky** – Souhrnné bankovní transakce.
    - **Odvod do trezoru** – Souhrnné transakce trezoru.
    - **Transakce příjmů/výdajů** – Souhrnné transakce příjmů nebo transakce výdajů.
    - **Transakce dokladu** – Souhrnné transakce dokladu.
    - **Platby odběratele** – Souhrnné platby odběratele.
    - **Prodeje a vrácení** – Souhrnné transakce prodeje a vrácení.

4. Na pevné záložce **Platby** zvolte výchozí název deníku pro následující možnosti:

    - **Deník plateb odběratele** - Tento deník se používá k zaúčtování plateb odběratele.
    - **Deník plateb v hotovosti** - Tento deník se používá k zaúčtování plateb v hotovosti.
    - **Hlavní deník** – Tento deník se používá k zaúčtování jiných transakcí než hotovostních plateb a plateb odběratele.

### <a name="set-up-a-payment-method-for-cash-payments-in-a-store"></a>Nastavení metody platby pro platby v hotovosti v obchodě

Následující postup slouží k nastavení metody platby pro platby v hotovosti v obchodě.

1. Přejděte na **Retail a Commerce \> Kanály \> Obchody \> Všechny obchody**.
2. Na stránce se seznamem **Všechny obchody** vyberte obchod, pro který chcete nastavit platební metodu.
3. Na panelu akcí na kartě **Nastavení** ve skupině **Nastavení** klikněte na možnost **Metody platby**.
4. Na stránce **Metody platby** vytvořte nebo vyberte metodu platby.
5. Na pevné záložce **Zaúčtování** ve skupině polí **Účet** v poli **Typ účtu** vyberte **Pokladní účet**.

    > [!NOTE]
    > Můžete vybrat **Pokladní účet** v poli **Typ účtu** pouze tehdy, pokud zvolíte **Normální** nebo **Úhrady odebrat/plovoucí** v poli **Funkce**.

6. V poli **Číslo účtu** vyberte číslo hotovostního účtu pro metodu platby.
7. Ve skupině polí **Úhrada - odebrat/plovoucí** v poli **Protiúčet** vyberte protiúčet pro zaúčtování odebrané úhrady nebo transakce odvodu pro metodu platby.

> [!NOTE]
> Je nutné nastavit protiúčty jak pro metodu platby pro úhrady hotovosti, tak pro odebrání úhrady nebo metodu platby plovoucí položky pro obchod. Tím se vytvoří vyrovnané položky hlavní knihy pro odebrání úhrady nebo transakce plovoucí položky.
