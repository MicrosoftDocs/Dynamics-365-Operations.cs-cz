---
title: Vytvoření požadavků položky pro servisní zakázky
description: Toto téma popisuje způsob vytvoření požadavku na položku pro servisní zakázky.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a92843a82093826822ab9865e43fee07d65e94c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677807"
---
# <a name="create-item-requirements-for-service-orders"></a>Vytvoření požadavků položky pro servisní zakázky

[!include [banner](../includes/banner.md)]

Můžete vytvářet objednávky služeb ke sledování a řízení služeb, které poskytujete odběratelům. Pokud pro objednávku služeb potřebujete rezervovat konkrétní zboží, můžete vytvořit požadavky na skladovou položku. Požadavek na položku může být okamžitě spotřebován ze skladu nebo může spustit výrobní zakázku zboží.

Použitím požadavků zboží namísto transakcí zboží můžete naplánovat dodávku těsně před vlastním použitím zboží, vytvořit prodejní objednávku, zahrnout zboží do rámce obchodní smlouvy nebo zahrnout požadavek na zboží do provozního plánování.

Požadavky zboží pro objednávky služeb jsou zpracovávány prostřednictvím projektu. Chcete-li vytvořit pro objednávku služeb požadavek zboží, objednávka musí být přiřazena k projektu. Po vytvoření požadavku na položku pro servisní zakázku můžete zobrazit požadavek na položku ve formuláři **Projekty** pro vybraný projekt.

## <a name="create-an-item-requirement-for-a-service-order"></a>Vytvoření požadavku položky pro servisní zakázku

1. Přejděte na **Správa servisu** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.
1. Vyberte servisní zakázku, pro kterou chcete vytvořit požadavek na položky.
1. V **podokně akcí** na kartě **Expedice** vyberte **Požadavek na položku**.
1. Ve formuláři **Požadavky na položku** zadejte informace pro požadovanou položku. Další informace o daných polích ve formuláři lze najít v tématu [Požadavky na položku (formulář)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Vytvoření požadavku položky pro servisní smlouvu

1. Přejděte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy**.
1. Otevřete servisní smlouvu, pro kterou chcete vytvořit požadavek na položky.
1. Na záložce **Řádky** výběrem tlačítka **Přidat** vytvořte nový řádek.
1. V poli **Typ transakce** vyberte **Položka**.
1. V poli **Nastavení položky** vyberte **Požadavek na položku**.
1. V poli **Číslo položky** vyberte položku, která je vyžadována pro servisní smlouvu.
1. Na pevné záložce **podrobnosti řádku** na kartě **dimenze produktu** v poli **pracoviště** vyberte skladové pracoviště pro položku.
1. Chcete-li vytvořit servisní zakázku z řádku smlouvy, na pevné záložce **Řádky** vyberte možnost **Vytvořit servisní příkazy** a poté zadejte relevantní informace do formuláře **Vytvořit servisní příkazy**.

## <a name="see-also"></a>Viz také

[Automatické vytvoření servisních zakázek](create-service-orders-automatically.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
