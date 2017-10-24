---
title: "Platby částečných částek odběratelem"
description: "Odběratelé někdy provedou platbu, která je nižší než částka faktury. Tento článek popisuje různé možnosti pro zvládnutí této situace. Dostupné možnosti závisí na daných obchodních požadavcích a konfiguraci."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13011
ms.assetid: 20423a2d-6997-4e1c-a596-a77016600071
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6e4fac197e75b80609486be7ea7c50c4b48beeb7
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="customer-payments-for-a-partial-amount"></a>Platby částečných částek odběratelem

[!include[banner](../includes/banner.md)]


Odběratelé někdy provedou platbu, která je nižší než částka faktury. Tento článek popisuje různé možnosti pro zvládnutí této situace. Dostupné možnosti závisí na daných obchodních požadavcích a konfiguraci.

<a name="partial-payment-with-no-discount"></a>Částečná platba beze slevy
--------------------------------

Odběratelé mohou provést částečnou úhradu, protože u sebe právě nemají dostatek hotovosti k zaplacení faktury v plném rozsahu, nebo protože došlo k nesrovnalosti ohledně položky na faktuře. V takovém případě lze fakturu uhradit částečnou platbou. Faktura zůstane otevřená a bude na ní uveden zůstatek.

## <a name="discount-amounts"></a>Částky slev
Můžete zákazníkům nabídnout platební slevu za úhradu faktury před datem splatnosti. Například zadáte fakturu na částku 100,00, která určuje 2% platební slevu, pokud bude faktura zaplacena do 10 dní. Doba splatnosti dle podmínek je 30 dnů. Pokud obdržíte platbu ve výši 98,00 do 10 dnů, zadáte platbu částky 98,00. Poté, jakmile bude faktura označena pro vyrovnání, bude platební sleva přijata automaticky.

## <a name="partial-payments-with-cash-discounts"></a>Částečné platby s platebními slevami
Když zákazník provede částečnou úhradu, může plánovat uskutečnění další částečné platby k úplnému vyrovnání faktury. Chcete-li aplikovat hotovostní slevu za částečnou platbu, je nutné nastavit možnost  **Vypočítat platební slevy pro částečné platby** na hodnotu **Ano** na stránce **Parametry pohledávek**. 

Například můžete nabídnout platební slevu 2 %, pokud bude faktura proplacena do 10 dnů po vydání. Je zaúčtována faktura na 100,00. Pokud obdržíte platbu ve výši 49,00 do 10 dnů, zadáte částku Dal ve výši 49,00 do deníku plateb. Při vyrovnání částečné platby na stránce **Vyrovnat transakce**, hodnota **1,00** se zobrazí v poli **Částka platební slevy k přijetí**. Částka slevy je zaúčtována na účet platební slevy. 

> [!NOTE] 
> Pokud zadáte částečnou platbu a ponecháte úplnou fakturovanou částku v poli **Částka k vyrovnání**, pole **Částka platební slevy k přijetí** bude automaticky přepočítáno při zaúčtování transakcí.

## <a name="credit-notes-with-discounts"></a>Dobropisy se slevami
Pokud odběratel vrátí některé položky na faktuře, můžete vydat dobropis. Jestliže byla v rámci původní faktury přijata platební sleva, musí být dobropis pro odběratele snížen o platební slevu, která byla přijata odběratelem. Pokud je možnost **Vypočítat platební slevy pro dobropisy** nastavena na hodnotu **Ano** na stránce **Parametry pohledávek**, sleva je automaticky vypočtena pro dobropis. 

Například je mohli nabídnout platební podmínky specifikující platební slevu 2 %, pokud bude faktura proplacena do 10 dnů po vydání. Byla zaúčtována faktura na 100,00 a odběratel přijal platební slevu. Pokud odběratel vrátí zboží a vystavíte mu dobropis, můžete zadat dobropis na -100,00. Při prohlížení dobropisu na stránce **Vyrovnat otevřené transakce** se zobrazí částka **98,00** v poli **Částka k vyrovnání** a částka **-2,00** v poli **Částka platební slevy**. Částka slevy je zaúčtována na účet platební slevy.

## <a name="overpaymentunderpayment-amounts"></a>Částky přeplatku nebo nedoplatku
Když odběratel uskuteční platbu, může stále existovat velmi malá částka, která ještě musí být vyrovnána. Například můžete odběrateli fakturovat částku 1 000,00 a odběratel zaplatí 999,90. Je-li zůstatek nižší než částka zadaná pro přeplatky nebo nedoplatky na stránce **Parametry pohledávek**, rozdíl se automaticky zaúčtuje na účet hlavní knihy pro přeplatky a nedoplatky.

## <a name="full-settlement"></a>Úplné vyrovnání
Odběratelé mohou provést částečnou platbu, kde se zbývající částka nezaplatí, ale je větší než částka nedoplatku, který je uveden na stránce **Parametry závazků**. Pokud chcete označit fakturu jako zcela vyrovnanou, můžete použít možnost **Úplné vyrovnání** na stránce **Vyrovnání transakce**. (Funkci úplného vyrovnání lze povolit pomocí konfiguračního klíče.) Například bude faktura zaúčtována na částku 1 000,00 a odběratel provede platbu ve výši 990,00. Dohodli jste se, že odběratel nemusí zaplatit zbývající částku 10. Po označení faktury pro vyrovnání můžete také označit výběr **Úplné vyrovnání**. Faktura bude poté považována za úplně vyrovnanou. Rozdíl 10,00 je zaúčtován na účet pro platební slevy jako částka dodatečné platební slevy.


Další informace naleznete v tématu [Vložení platby odběratele](tasks/deposit-customer-payments.md).

