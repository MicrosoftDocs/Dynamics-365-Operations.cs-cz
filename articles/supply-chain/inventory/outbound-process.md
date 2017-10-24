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
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 9c09a7bd314bb9005eb0b6c69d7cccad1c30cfdb
ms.openlocfilehash: 7b395cab2184f8f9f3f50a7a595c6ed782645323
ms.contentlocale: cs-cz
ms.lasthandoff: 10/04/2017

---

# <a name="outbound-process"></a>Odchozí proces

[!include[banner](../includes/banner.md)]

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

V některých případech nelze některé položky na skladě vydat jako součást procesu výdejek. Může dojít například k takové situaci, že pracovník skladu sníží množství na řádcích výdeje a zpracuje výdejku. Pokud je možnost **Ukončit výstupní skladovou objednávku** nastavena na **Ano**, zbývající nevyskladněné množství je nahlášeno zpět na úroveň objednávky. Pokud je možnost nastavena na **ne**, zbývající nevyskladněné množství je zachováno jako otevřené množství výstupní objednávky. V takovém případě množství zůstanou uvolněná do skladu a je nutné je přidat na novou výdejku jako součást funkce **Otevřít výstupní objednávky**.

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

