---
title: Přehled odchozího procesu
description: Tento článek obsahuje přehled odchozího procesu v modulu Řízení zásob.
author: yufeihuang
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "274363"
- intro-internal
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 4e3c97862858e219d98b4ef9a81b52c6ab1623ab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852469"
---
# <a name="outbound-process-overview"></a>Přehled odchozího procesu

[!include [banner](../includes/banner.md)]

Tento článek obsahuje přehled odchozího procesu v modulu Řízení zásob.

## <a name="output-orders"></a>Výstupní objednávky

Výstupní objednávky se používají k propojení řádků prodejní objednávky a řádků převodního příkazu s odchozími procesy výdeje, které používají výdejky.

Pokud jsou dodací listy generovány buď z prodejních objednávek nebo převodních příkazů, budou automaticky vytvořeny výstupní objednávky a dodávky. Výdejka má vztah jedna ku jedné s dodávkou. Dodávku převodního příkazu nebo dodací list prodejní objednávky lze zpracovat z dodávky. 

Následující diagram znázorňuje přehled procesu výstupních objednávek. 

[![Přehled procesu výstupních objednávek.](./media/outbound-order.png)](./media/outbound-order.png)

Můžete nastavit výstupní pravidla určující způsob, jak má program zpracovat odchozí proces. Tato pravidla můžete použít ke kontrole procesu dodávky. Pravidla můžete použít obzvláště ke kontrole toho, během které fáze procesu lze odeslat dodávku. Následující nastavení určují způsob zpracování odchozích procesů.

## <a name="picking-route-status-for-sales-and-transfer-orders"></a>Stav postupu výdeje pro prodejní objednávky a převodní příkazy 

Přejděte na **Pohledávky** \> **Nastavení** \> **Parametry pohledávek** a poté na kartě **Aktualizace** vyberte hodnotu v poli **Stav postupu výdeje**.

[![Pole stav postupu výdeje pro prodejní objednávky.](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)

Pokud je pole **Stav postupu výdeje** nastaveno na **Dokončeno**, dojde k procesu výdeje automaticky jako součásti procesu generování výdejek. Pokud je pole nastaveno na **Aktivováno**, řádky výdejky musíte aktualizovat ručně.

Stejné nastavení se vztahuje k převodním příkazům. Přejděte na **Řízení zásob** \> **Nastavení** \> **Parametry řízení zásob a skladu** a poté na kartě **Přeprava** vyberte hodnotu v poli **Stav postupu výdeje**.

[![Pole stav postupu výdeje pro převodní příkazy.](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)

## <a name="end-output-inventory-orders"></a>Ukončení výstupních skladových objednávek

Přejděte na **Řízení zásob** \> **Nastavení** \> **Parametry řízení zásob a skladu** a poté na kartě **Obecné** nastavte možnost **Ukončit výstupní skladovou objednávku**.

[![Možnost Ukončit výstupní skladovou objednávku.](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)

Když pracovníci ve skladu snižují množství výdejky, budou z expedice odebrána odpovídající množství oskladové objednávky. Při aktualizaci výdejky v určitý okamžik se zbývající množství vykáže zpět do objednávky, pokud je možnost **Ukončit výstupní skladovou objednávku** nastavena na **Ano**. Pokud je možnost **Ukončit výstupní skladovou objednávku** nastavena na **Ne**, zbývající množství se zachová jako otevřené množství výstupní objednávky a je nutné ho přidat do nové výdejky jako součást funkce **Otevřené výstupní objednávky**. 

[![Příkaz Otevřít výstupní objednávky v nabídce funkcí.](./media/open-output-order.png)](./media/open-output-order.png)

[![Nabídka funkcí na stránce Otevřít výstupní objednávky.](./media/open-output-order-function.png)](./media/open-output-order-function.png)

## <a name="reduce-quantity"></a>Snížit množství

Třetí parametr, který můžete použít jako součást procesu generování výdejek, je parametr **Snížit množství**. Nastavení tohoto parametru se používá spolu s nastavením **Rezervace**, které spustí proces rezervace jako součást uvolnění do skladu.

[![Parametr Snížit množství.](./media/reduce-quantity.png)](./media/reduce-quantity.png)

## <a name="example-of-an-outbound-process-for-a-sales-order"></a>Příklad odchozího procesu pro prodejní objednávku

V tomto příkladu je prodejní objednávka pro dvě položky. Během generování seznamu výdejek zvolte parametr **Snížit množství**. Tím uvolníte a vytvoříte řádky výdeje pouze pro dostupné zásoby na skladě. Výdej musí být nahlášen pomocí procesu registrace výdejek (**Stav postupu výdeje** = **Aktivováno**).

Zásoby. které nebyly ještě rezervovány, se zarezervují během generování výdejek. Nedostupné zásoby lze buď odebrat z prodejní objednávky nebo uvolnit do skladu pro pozdější odchozí zpracování, až budou zásoby k dispozici pro výdej.

[![Aktualizace výdejky.](./media/update-picking-list.png)](./media/update-picking-list.png)

Jakmile byly vyskladněny všechny řádků výdeje na stránce **Registrace výdejky**, přidružená dodávka je dokončena. Poté lze inicializovat proces pro dodací listy prodejní objednávky na základě vyskladněných zásob.

[![Aktualizace odchozích dodávek.](./media/outbound-shipments.png)](./media/outbound-shipments.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]