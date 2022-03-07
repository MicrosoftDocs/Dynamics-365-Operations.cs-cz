---
title: Požadavky na položku servisní objednávky
description: Toto téma popisuje způsob vytvoření požadavku na položku pro servisní zakázku.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae211cb24e3ed0e9e54643448ee378a20658ad89
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573194"
---
# <a name="service-order-item-requirements"></a>Požadavky na položku servisní objednávky

[!include [banner](../includes/banner.md)]

Můžete vytvářet objednávky služeb ke sledování a řízení služeb, které poskytujete odběratelům. Pokud pro objednávku služeb potřebujete rezervovat konkrétní zboží, můžete vytvořit požadavky na skladovou položku. Požadavek na položku může být okamžitě spotřebován ze skladu nebo může spustit výrobní zakázku zboží.

Použitím požadavků zboží namísto transakcí zboží můžete naplánovat dodávku těsně před vlastním použitím zboží, vytvořit prodejní objednávku, zahrnout zboží do rámce obchodní smlouvy nebo zahrnout požadavek na zboží do provozního plánování.

Požadavky zboží pro objednávky služeb jsou zpracovávány prostřednictvím projektu. Chcete-li vytvořit pro objednávku služeb požadavek zboží, objednávka musí být přiřazena k projektu.

Pokud je pro servisní zakázku vytvořen požadavek na položku, lze jej zobrazit v okně **Projekt** v rámci jednotlivé servisní zakázky nebo prostřednictvím formuláře **Prodejní objednávka**.

## <a name="view-an-item-requirement-from-a-service-order"></a>Zobrazení požadavku na položku ze servisní zakázky

1. Přejděte na **Správa servisu** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.
1. Vyberte **Expedice** a pak vybráním možnosti **Požadavek na položku** otevřete formulář **Požadavky na položku**.
1. Vyberte kartu **Projekt** a zkontrolujte, zda jsou v poli **Servisní zakázka** uvedeny servisní zakázky požadavků zboží.

## <a name="delete-service-orders-with-item-requirements"></a>Odstranění servisních zakázek s požadavky na položky

Pokud je pro určitou servisní zakázku vytvořen požadavek na položku, nelze danou servisní zakázku odstranit. Požadavek na servisní zakázku je nutné nejprve odstranit a teprve poté lze odstranit i servisní zakázku.

1. Přejděte na **Správa servisu** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.
1. Vyberte **Expedice** a pak vybráním možnosti **Požadavek na položku** otevřete formulář **Požadavky na položku**. V tomto formuláři jsou všechny požadavky na zboží, které jsou pro danou servisní zakázku vytvořeny.
1. Vyberte řádek požadavku na zboží, který má být odebrán, a pak vyberte **Odstranit**.

- nebo -

1. Přejděte na **Řízení a účetnictví projektů** \> **Společné** \> **Projekty** \> **Všechny projekty**.
1. Otevřete projekt se servisní zakázkou, v níž je vytvořen požadavek na zboží.
1. Ve formuláři **Projekty**, vyberte v pravém podokně možnost **Požadavky na položky**. Zobrazí se formulář **Požadavky položky** se seznamem požadavků na položky asociovanými s vybraným projektem.
1. Vyberte řádek požadavku na zboží, který má být odebrán, a pak vyberte **Odstranit**.

## <a name="see-also"></a>Viz také

[Požadavky položky (formulář)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))



[!INCLUDE[footer-include](../../includes/footer-banner.md)]