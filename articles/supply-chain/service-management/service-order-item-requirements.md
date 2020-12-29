---
title: Požadavků na položku servisní objednávky
description: Pokud pro objednávku služeb potřebujete rezervovat konkrétní zboží, můžete vytvořit požadavky na skladovou položku.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8866d8a4d6ad879f2c43b470af98457cb7c75721
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423499"
---
# <a name="service-order-item-requirements"></a>Požadavků na položku servisní objednávky   

[!include [banner](../includes/banner.md)]


Můžete vytvářet objednávky služeb ke sledování a řízení služeb, které poskytujete odběratelům. Pokud pro objednávku služeb potřebujete rezervovat konkrétní zboží, můžete vytvořit požadavky na skladovou položku. Požadavek na položku může být okamžitě spotřebován ze skladu nebo může spustit výrobní zakázku zboží.

Použitím požadavků zboží namísto transakcí zboží můžete naplánovat dodávku těsně před vlastním použitím zboží, vytvořit prodejní objednávku, zahrnout zboží do rámce obchodní smlouvy nebo zahrnout požadavek na zboží do provozního plánování.

Požadavky zboží pro objednávky služeb jsou zpracovávány prostřednictvím projektu. Chcete-li vytvořit pro objednávku služeb požadavek zboží, objednávka musí být přiřazena k projektu.

Pokud je pro servisní zakázku vytvořen požadavek na položku, lze jej zobrazit v okně **Projekt** v rámci jednotlivé servisní zakázky nebo prostřednictvím formuláře **Prodejní objednávka**.

## <a name="view-an-item-requirement-from-a-service-order"></a>Zobrazení požadavku na položku ze servisní zakázky

1.  Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.

2.  Klikněte na **Expedice** a pak kliknutím na **Požadavek na položku** otevřete formulář **Požadavky na položku**.

3.  Klepněte na kartu **Projekt** a zkontrolujte, zda jsou v poli **Servisní zakázka** uvedeny servisní zakázky požadavků zboží.

## <a name="delete-service-orders-with-item-requirements"></a>Odstranění servisních zakázek s požadavky na položky

Pokud je pro určitou servisní zakázku vytvořen požadavek na položku, nelze danou servisní zakázku odstranit. Požadavek na servisní zakázku je nutné nejprve odstranit a teprve poté lze odstranit i servisní zakázku.

1.  Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.

2.  Klikněte na **Expedice** a pak kliknutím na **Požadavek na položku** otevřete formulář **Požadavky na položku**. V tomto formuláři jsou všechny požadavky na zboží, které jsou pro danou servisní zakázku vytvořeny.

3.  Vyberte řádek požadavku na zboží, který má být odebrán, a klepněte na možnost **Odstranit**.

- nebo -

1.  Klikněte na **Řízení a účetnictví projektů** \> **Společné** \> **Projekty** \> **Všechny projekty**.

2.  Otevřete projekt se servisní zakázkou, v níž je vytvořen požadavek na zboží.

3.  Ve formuláři **Projekty**, v pravém podokně, klikněte na možnost **požadavky položky**. Zobrazí se formulář **Požadavky položky** se seznamem požadavků na položky asociovanými s vybraným projektem.

4.  Vyberte řádek požadavku na zboží, který má být odebrán, a klepněte na možnost **Odstranit**.

## <a name="see-also"></a>Viz také

[Požadavky položky (formulář)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))

