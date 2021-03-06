---
title: Vytvoření nové zakázky na doplnění stavu zásob dodávky
description: Tto téma vysvětluje, jak vytvořit objednávku doplnění stavu zásob dodávky, kde můžete sledovat očekávanou dodávku od dodavatele do skladu dodávky.
author: sherry-zheng
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0d2030277e0810bebef9356136b0e11effc6d5b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834018"
---
# <a name="create-a-consignment-replenishment-order"></a>Vytvoření nové zakázky na doplnění stavu zásob dodávky

[!include [banner](../../includes/banner.md)]

Tto téma vysvětluje, jak vytvořit objednávku doplnění stavu zásob dodávky, kde můžete sledovat očekávanou dodávku od dodavatele do skladu dodávky. Také ukazuje, jak zaznamenávat příjem produktů tak, aby byla zásoba dodávky registrována jako zásoby na skladě ve vlastnictví dodavatele. Tuto proceduru obvykle provádí zásobovací pracovník. Tohoto průvodce můžete použít s ukázkových dat společnosti USMF. Tento postup je určen pro funkci, která byla přidána do Dynamics 365 for Operations, verze 1611.

## <a name="create-a-consignment-replenishment-order"></a>Vytvoření nové zakázky na doplnění stavu zásob dodávky
1. V navigačním podokně přejděte na **Moduly > Zásobování a zdroje > Stav zásob dodávky > Zakázky na doplnění stavu zásob dodávky**.
2. Zvolte **Nové**.
3. V poli **Účet dodavatele** vyberte dodavatele **US-104** (musíte vybrat dodavatele, který je zaregistrován jako vlastník na stránce **Vlastníci zásob**). 
4. Vyberte **OK**.
5. Vyberte **Přidat řádek**.
6. Do pole **Číslo položky** zadejte `M9211CI` (je nutné vybrat položku, která je nastavena pro zásoby dodávky).
7. Zadejte číslo do pole **Množství**.
8. Zadejte datum do pole **Požadované datum dodání**. Požadované a potvrzené datum používá modul MRP pro očekávané přijetí zboží.  
9. Zadejte datum do pole **Potvrzené datum dodání**.
10. Rozbalte sekci **Podrobnosti řádku**.
11. Vyberte kartu **Dimenze zásob**.
12. Chcete-li zobrazit vlastníka v poli **Vlastník dimenze zásob**, aktualizujte stránku. Dodavatel US-104 je nyní uveden jako vlastník.  

## <a name="check-the-inventory-transaction-status"></a>Zkontrolujte stav transakce zásob.
1. Vyberte **skladový model**.
2. Vyberte **Transakce**.
3. Všimněte si, že pole **Příjemka** je nastaveno na **Objednáno** v požadovaném řádku.  
4. Zavřete stránku.

## <a name="receive-items"></a>Přijmout položky
1. Vyberte **Příjemka produktu**.
2. Zadejte hodnotu do pole **Externí příjemka produktu**.
3. Do pole **Množství** zadejte číslo, které je nižší než číslo, které je zde uvedeno. 
4. Vyberte **OK**.

## <a name="check-the-on-hand-inventory"></a>Zkontrolujte množství na skladě.
1. Vyberte **skladový model**.
2. Vyberte **Na skladě**.
3. Vyberte **Přehled**. Položky, které byly přijaty jako zásoby dodávky ve vlastnictví dodavatele, jsou k dispozici na skladě. Zbývající množství na objednávce doplnění stavu zásob dodávky je uvedeno v poli **Celkem objednáno**.  
4. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]