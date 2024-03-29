---
title: Platby částečných částek dodavatelem
description: Někdy provedete platbu dodavateli, která je nižší než částka faktury. Tento článek popisuje různé možnosti pro zvládnutí této situace.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: deb150e35a80cc4c49f46dfc55822625db83cbda
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715371"
---
# <a name="vendor-payments-for-a-partial-amount"></a>Platby částečných částek dodavatelem

[!include [banner](../includes/banner.md)]

Někdy provedete platbu dodavateli, která je nižší než částka faktury. Tento článek popisuje různé možnosti pro zvládnutí této situace. Dostupné možnosti závisí na daných obchodních požadavcích a konfiguraci. 

## <a name="cash-discount-amounts"></a>Částka platebních slev

Dodavatel vám může nabídnout platební slevu za úhradu faktury před datem splatnosti. Například zadáte fakturu na částku 100,00, která určuje 2% platební slevu, pokud bude faktura zaplacena do 10 dní. Doba splatnosti dle podmínek je 30 dnů. Pokud návrh platby používá jako kritérium pro výběr faktury platební slevu a k aktivaci návrhu dojde v den platební slevy nebo dříve, faktura se vybere k platbě a vytvoří se platba v částce 98,00. Platební slevy lze také uplatnit jako ručně vytvořenou jednorázovou platbu.

## <a name="partial-payments-with-cash-discounts"></a>Částečné platby s platebními slevami
Když provedete částečnou úhradu, můžete plánovat uskutečnění další částečné platby k úplnému vyrovnání faktury. Chcete-li aplikovat platební slevu za částečnou platbu, je nutné nastavit možnost **Vypočítat platební slevy pro částečné platby** na hodnotu **Ano** na stránce **Parametry pohledávky**. 

Například můžete přijmout platební slevu 2 %, pokud bude faktura proplacena do 10 dnů po vydání. Je zaúčtována faktura na 100,00. Pokud provedete platbu ve výši 49,00 do 10 dnů, zadáte do deníku plateb částku Má dáti ve výši 49,00. Při vyrovnání částečné platby na stránce **Vyrovnat otevřené transakce** bude uvedena hodnota **1,00** v poli **Částka platební slevy k přijetí**. 

> [!NOTE] 
> Pokud zadáte částečnou platbu a ponecháte úplnou fakturovanou částku v poli **Částka k vyrovnání**, pole **Částka platební slevy k přijetí** bude automaticky přepočítáno při zaúčtování transakcí.

## <a name="credit-notes-with-cash-discounts"></a>Dobropisy s platebními slevami
Můžete vrátit některé položky na faktuře a přijmout dobropis. Pokud pro původní fakturu byla využita platební sleva, můžete odečíst hodnotu slevy a přijmout refundaci pro správnou částku. Pokud je možnost **Vypočítat platební slevy pro dobropisy** nastavena na hodnotu **Ano** na stránce **Parametry závazků**, sleva je automaticky vypočtena pro dobropis. 

Například můžete přijmout platební slevu 2 %, pokud bude faktura proplacena do 10 dnů po vydání. Je zaúčtována faktura na 100,00. Pokud vrátíte zboží a obdržíte dobropis, můžete zadat dobropis za celou částku původní faktury (100,00) spolu s dvouprocentní platební slevou, která je v dobropisu také určena.  Při prohlížení dobropisu na stránce **Vyrovnat transakce** se zobrazí částka **98,00** v poli **Částka k vyrovnání** a částka **-2,00** v poli **Částka platební slevy**. Částka slevy je zaúčtována na účet platební slevy.

## <a name="overpaymentunderpayment-amounts"></a>Částky přeplatku nebo nedoplatku
Můžete provést částečnou úhradu, když je částka, která musí být vyrovnána, příliš malá. Například faktura dodavatele je pro 1 000,00 a vy platíte 999,90 Je-li zůstatek nižší než částka zadaná pro přeplatky nebo nedoplatky na stránce **Parametry závazků**, rozdíl se automaticky zaúčtuje na účet hlavní knihy pro přeplatky a nedoplatky.


Další informace naleznete v tématu [Přehled plateb dodavatele](../cash-bank-management/tasks/vendor-payment-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
