---
title: "Odchozí proces"
description: "Toto téma obsahuje přehled odchozího procesu v modulu Řízení zásob."
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: f2cae64263769b5168d2bb9614d6388b42e23b49
ms.contentlocale: cs-cz
ms.lasthandoff: 12/14/2017

---

# <a name="outbound-process"></a>Odchozí proces

[!INCLUDE [banner](../includes/banner.md)]

Toto téma obsahuje přehled odchozího procesu v modulu Řízení zásob.

## <a name="output-orders"></a>Výstupní objednávky

Výstupní objednávky se používají k propojení řádků prodejní objednávky a řádků převodního příkazu s odchozími procesy výdeje, které používají výdejky.

Pokud jsou dodací listy generovány buď z prodejních objednávek nebo převodních příkazů, budou automaticky vytvořeny výstupní objednávky a dodávky. Výdejka má vztah jedna ku jedné s dodávkou. Dodávku převodního příkazu nebo dodací list prodejní objednávky lze zpracovat z dodávky. 

Následující diagram znázorňuje přehled procesu výstupních objednávek. 

[![Přehled procesu výstupních objednávek](./media/outbound-order.png)](./media/outbound-order.png)

Můžete nastavit výstupní pravidla určující způsob, jak má program zpracovat odchozí proces. Tato pravidla můžete použít ke kontrole procesu dodávky. Pravidla můžete použít obzvláště ke kontrole toho, během které fáze procesu lze odeslat dodávku. Následující nastavení určují způsob zpracování odchozích procesů.

## <a name="picking-route-status-for-sales-and-transfer-orders"></a>Stav postupu výdeje pro prodejní objednávky a převodní příkazy 

Přejděte na **Pohledávky** \> **Nastavení** \> **Parametry pohledávek** a poté na kartě **Aktualizace** vyberte hodnotu v poli **Stav postupu výdeje**.

[![Pole stav postupu výdeje pro prodejní objednávky](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)

Pokud je pole **Stav postupu výdeje** nastaveno na **Dokončeno**, dojde k procesu výdeje automaticky jako součásti procesu generování výdejek. Pokud je pole nastaveno na **Aktivováno**, řádky výdejky musíte aktualizovat ručně.

Stejné nastavení se vztahuje k převodním příkazům. Přejděte na **Řízení zásob** \> **Nastavení** \> **Parametry řízení zásob a skladu** a poté na kartě **Přeprava** vyberte hodnotu v poli **Stav postupu výdeje**.

[![Pole stav postupu výdeje pro převodní příkazy](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)

## <a name="end-output-inventory-orders"></a>Ukončení výstupních skladových objednávek

Přejděte na **Řízení zásob** \> **Nastavení** \> **Parametry řízení zásob a skladu** a poté na kartě **Obecné** nastavte možnost **Ukončit výstupní skladovou objednávku**.

[![Možnost Ukončit výstupní skladovou objednávku](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)

Když pracovníci ve skladu snižují množství výdejky, budou z expedice odebrána odpovídající množství oskladové objednávky. Při aktualizaci výdejky v určitý okamžik se zbývající množství vykáže zpět do objednávky, pokud je možnost **Ukončit výstupní skladovou objednávku** nastavena na **Ano**. Pokud je možnost **Ukončit výstupní skladovou objednávku** nastavena na **Ne**, zbývající množství se zachová jako otevřené množství výstupní objednávky a je nutné ho přidat do nové výdejky jako součást funkce **Otevřené výstupní objednávky**. 

[![Příkaz Otevřít výstupní objednávky v nabídce funkcí](./media/open-output-order.png)](./media/open-output-order.png)

[![Nabídka funkcí na stránce Otevřít výstupní objednávky](./media/open-output-order-function.png)](./media/open-output-order-function.png)

## <a name="reduce-quantity"></a>Snížit množství

Třetí parametr, který můžete použít jako součást procesu generování výdejek, je parametr **Snížit množství**. Nastavení tohoto parametru se používá spolu s nastavením **Rezervace**, které spustí proces rezervace jako součást uvolnění do skladu.

[![Parametr Snížit množství](./media/reduce-quantity.png)](./media/reduce-quantity.png)

## <a name="example-of-an-outbound-process-for-a-sales-order"></a>Příklad odchozího procesu pro prodejní objednávku

V tomto příkladu je prodejní objednávka pro dvě položky. Během generování seznamu výdejek zvolte parametr **Snížit množství**. Tím uvolníte a vytvoříte řádky výdeje pouze pro dostupné zásoby na skladě. Výdej musí být nahlášen pomocí procesu registrace výdejek (**Stav postupu výdeje** = **Aktivováno**).

Zásoby. které nebyly ještě rezervovány, se zarezervují během generování výdejek. Nedostupné zásoby lze buď odebrat z prodejní objednávky nebo uvolnit do skladu pro pozdější odchozí zpracování, až budou zásoby k dispozici pro výdej.

[![Aktualizace výdejky](./media/update-picking-list.png)](./media/update-picking-list.png)

Jakmile byly vyskladněny všechny řádků výdeje na stránce **Registrace výdejky**, přidružená dodávka je dokončena. Poté lze inicializovat proces pro dodací listy prodejní objednávky na základě vyskladněných zásob.

[![Aktualizace odchozích dodávek](./media/outbound-shipments.png)](./media/outbound-shipments.png)

