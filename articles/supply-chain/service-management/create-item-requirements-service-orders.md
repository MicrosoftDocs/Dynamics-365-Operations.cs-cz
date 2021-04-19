---
title: Vytvoření požadavků položky pro servisní zakázky
description: Pokud pro objednávku služeb potřebujete rezervovat konkrétní zboží, můžete vytvořit požadavky na skladovou položku.
author: ShylaThompson
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 650d02d2160757d9629e4deb1e9217c85e9d01df
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831619"
---
# <a name="create-item-requirements-for-service-orders"></a>Vytvoření požadavků položky pro servisní zakázky 

[!include [banner](../includes/banner.md)]


Můžete vytvářet objednávky služeb ke sledování a řízení služeb, které poskytujete odběratelům. Pokud pro objednávku služeb potřebujete rezervovat konkrétní zboží, můžete vytvořit požadavky na skladovou položku. Požadavek na položku může být okamžitě spotřebován ze skladu nebo může spustit výrobní zakázku zboží.

Použitím požadavků zboží namísto transakcí zboží můžete naplánovat dodávku těsně před vlastním použitím zboží, vytvořit prodejní objednávku, zahrnout zboží do rámce obchodní smlouvy nebo zahrnout požadavek na zboží do provozního plánování.

Požadavky zboží pro objednávky služeb jsou zpracovávány prostřednictvím projektu. Chcete-li vytvořit pro objednávku služeb požadavek zboží, objednávka musí být přiřazena k projektu. Po vytvoření požadavku na položku pro servisní zakázku můžete zobrazit požadavek na položku ve formuláři **Projekty** pro vybraný projekt.

## <a name="create-an-item-requirement-for-a-service-order"></a>Vytvoření požadavku položky pro servisní zakázku

1.  Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.

2.  Vyberte servisní zakázku, pro kterou chcete vytvořit požadavek na položky.

3.  V **podokně akcí** na kartě **Expedice** klikněte na **Požadavek na položku**.

4.  Ve formuláři **Požadavky na položku** zadejte informace pro požadovanou položku. Další informace o daných polích ve formuláři lze najít v tématu [Požadavky na položku (formulář)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Vytvoření požadavku položky pro servisní smlouvu

1.  Klikněte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy**.

2.  Otevřete servisní smlouvu, pro kterou chcete vytvořit požadavek na položky.

3.  Na pevné záložce **Řádky** kliknutím na tlačítko **Přidat** vytvořte nový řádek.

4.  V poli **Typ transakce** vyberte **Položka**.

5.  V poli **Nastavení položky** vyberte **Požadavek na položku**.

6.  V poli **Číslo položky** vyberte položku, která je vyžadována pro servisní smlouvu.

7.  Na pevné záložce **podrobnosti řádku** na kartě **dimenze produktu** v poli **pracoviště** vyberte skladové pracoviště pro položku.

8.  Chcete-li vytvořit servisní zakázku z řádku smlouvy, na pevné záložce **Řádky** klepněte na možnost **Vytvořit servisní příkazy** a poté zadejte relevantní informace do formuláře **Vytvořit servisní příkazy**. 


## <a name="see-also"></a>Viz také

[Automatické vytvoření servisních zakázek](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]