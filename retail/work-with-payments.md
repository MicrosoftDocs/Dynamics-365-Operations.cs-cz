---
title: "Platební metody v kontaktním středisku"
description: "Toto téma popisuje různé platební metody, které lze použít v telefonickém centru v aplikaci Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 07cb1bcb3870b96e34f7f6725fe5b7da32628fde
ms.contentlocale: cs-cz
ms.lasthandoff: 06/20/2017

---

# <a name="payment-methods-in-a-call-center"></a>Platební metody v kontaktním středisku

[!include[banner](includes/banner.md)]


Toto téma popisuje různé platební metody, které lze použít v telefonickém centru v aplikaci Dynamics 365 for Retail.

V telefonickém centrech lze použít také metody platby, které se používají u jiných kanálů, jako například pro hotovost, šeky, kreditní karty a dárkové poukazy. Po nastavení způsobu platby pro kontaktní středisko se pro uživatele kontaktního střediska tento způsob zobrazí jako jedna z možností v části **Platby** na stránce **Prodejní objednávka**. Dále můžete nastavit kupóny pro nabízení slev odběratelům při objednávání prostřednictvím kontaktního střediska vaší organizace. Kupóny mohou být pevná částka slevy nebo procento ceny položky nebo celkové částky objednávky. Například kupón částky může nabízet odběratelům slevu 75,00, když odběratele tratí 750,00 nebo více. Můžete vytvořit různé typy kupónů, nastavit nadřazené a podřízené kupóny a kupóny kopírovat nebo anulovat. Pomocí možností v následující tabulce vytvoříte kupóny.

|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Atribut**             | Do pole **Umořovací sazba** zadejte očekávanou umořovací sazbu kupónu v procentech a pak vyberte, zda kupón je kupón pro jednorázové použití, bude vydán automaticky znovu nebo je specifický pro odběratele.                                                                                                                                                                                                                                                                                                                                                                                       |
| **Platné**                 | V polích **Počáteční datum** a **Konečné datum** zadejte data prvního a posledního dne, kdy je kupón platný.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Zahrnout/vyloučit pravidla** | V polích **Katalogy** a **Položky** vyberte, zda jsou v kupónu zahrnuty nebo vyloučeny nějaké katalogy nebo zboží. Vyberete-li možnost **Zahrnout** nebo **Vyloučit**, klepněte na tlačítko **Nastavit**, vyberte **Zahrnout/vyloučit katalogy** nebo **Zahrnout/vyloučit produkty** a zadejte informace o katalogu nebo položce. Vyberete-li v těchto polích **Žádný**, všechny katalogy nebo položky jsou součástí kupónu.                                                                                                                                                                                                                          |
| **Různé**         | Pokud tento kupón nelze použít společně s dalšími slevami, označte pole **Výhradní**. Pak v poli **Původ** vyberte místo pro použití kupónu. Jedná-li se o kupón výrobce, zaškrtněte políčko **Kupón výrobce**.                                                                                                                                                                                                                                                                                                                                                                |
| **Budoucí kupón**         | Je-li tento kupón přiřazen ostatním kupónům jako nadřazený kupón, zaškrtněte políčko **Nadřazený kupón**. Má-li být tento kupón přidružen jako podřízený kupón s existujícím kupónem, vyberte nadřazený kupón v poli **ID nadřazeného kupónu**. Můžete například vytvořit kupón nadcházející jarní katalog. Všechny ostatní kupóny, které vytvoříte pro jarní katalog, budou podřízené kupóny kupónu jarního katalogu. Podřízené kupóny mohou zahrnovat 20% slevu pro objednávky nových odběratelů, 10% slevu nově vydané položky nebo slevu 95,00 z objednávek za nejméně 1000,00. |

Pokud odešlete platbu platební kartou na stránce **Prodejní objednávka** a zobrazí se zpráva oznamující, že karta nebyla autorizována, lze ověření zpracovat ručně. Můžete schválit, odmítnout nebo znovu odeslat transakci platební pomocí stránky **Správa autorizací**. Pomocí stránky Parametry kontaktního střediska můžete konfigurovat další možnosti zpracování platby:

-   Blokování šeků umožňuje pracovníkům finančního oddělení zpracování objednávek, které byly blokovány, protože byl použit šek jako způsob platby, a mezní hodnota kontroly šeků byla překročena. Blokování je možné ručně uvolnit, nebo jeho platnost automaticky vyprší na konci nakonfigurovaného období.
-   Můžete nastavit prahové hodnoty, kdy při jejich přesažení budou refundace prostřednictvím šeku nebo platebních karet vyžadovat ruční schválení. Částka, která přesahuje prahovou částku, je přidána do fronty na schválení. Po schválení refundace je možné fakturovat prodejní vratku.





