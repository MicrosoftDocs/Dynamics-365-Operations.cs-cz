---
title: Integrace Dynamics 365 Supply Chain Management (správa majetku) s Dynamics 365 Guides
description: Toto téma vysvětluje, jak integrovat modul správy majetku do produktu Microsoft Dynamics 365 Supply Chain Management s Dynamics 365 Guides, aby bylo možné využít příručky smíšené reality ve vašich každodenních pracovních a servisních pracovních postupech.
author: kamaybac
manager: tfehr
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: ae26012d236a44bfa0c8453bdc660671ddee82a4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000277"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a>Integrace Dynamics 365 Supply Chain Management (správa majetku) s Dynamics 365 Guides

Toto téma vysvětluje, jak integrovat modul **Správa majetku** do produktu Microsoft Dynamics 365 Supply Chain Management s Dynamics 365 Guides, aby bylo možné využít příručky smíšené reality ve vašich každodenních pracovních a servisních pracovních postupech. Pokud je průvodce přiřazen k pracovnímu příkazu Správa majetku, pracovník, který otevře kontrolní seznam údržby objednávky v mobilní aplikaci Supply Chain Management (Dynamics 365), uvidí, že je průvodce k dispozici. Pracovník pak může průvodce najít a otevřít v aplikaci Dynamics 365 Guides HoloLens.

## <a name="prerequisites"></a>Předpoklady

Před připojením průvodců k pracovním příkazům správy aktiv musíte splnit tyto předpoklady:

- [Nastavení Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) verze 10.0.9 nebo novější.
- [Zapnutí duálního zápisu pro aplikace Supply Chain Management](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).
- [Zapnutí testovací verze](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) pro funkci **MRGuidesFeature**. (Pro produkční prostředí musíte nejprve odeslat lístek na podporu, aby byl váš klient přidán do skupiny testovací verze.)
- [Zapněte následující konfigurační klíče](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) na stránce **Konfigurace licence**:

    - Správa majetku \> Smíšená realita správy majetku
    - Smíšená realita \> Průvodce smíšenou realitou

- [Nastavení Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) verze 200.0.0.96 nebo novější.

## <a name="use-dynamics-365-guides-with-asset-management"></a>Použití Dynamics 365 Guides se správou majetku

Chcete-li průvodce přiřadit, použijte řádek kontrolního seznamu údržby ve správě aktiv. Přidružení můžete vytvořit pomocí šablony kontrolního seznamu údržby, typu úlohy údržby nebo pracovní objednávky, protože všechny tři obsahují řádky kontrolního seznamu údržby. Můžete ušetřit čas pomocí šablony, protože šablona může být spojena se všemi typy úloh údržby, které ji používají. Například průvodce, který je spojen s typem úlohy údržby, je automaticky spojen se všemi pracovními příkazy, které specifikují daný typ úlohy. Na druhé straně průvodce, který je přímo spojen s pracovním příkazem, existuje pouze pro tento pracovní příkaz.

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a>Přiřazení průvodce šabloně kontrolního seznamu údržby

Chcete-li přiřadit průvodce k šabloně kontrolního seznamu údržby, postupujte takto.

1. Vytvořte průvodce pomocí aplikací Dynamics 365 Guides PC a HoloLens. Další informace o vytvoření průvodce naleznete v následujících tématech:

    - [Vytvoření průvodce pomocí aplikace PC](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [Umístění hologramů pomocí aplikace HoloLens](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. V aplikaci Supply Chain Management [vytvořte šablonu kontrolního seznamu údržby](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).
1. Přiřaďte průvodce, kterého jste vytvořili, k řádce kontrolního seznamu údržby v nové šabloně kontrolního seznamu údržby:

    1. Na pevné záložce **Řádky kontrolního seznamu údržby** vyberte řádek, se kterým chcete průvodce spojit.
    1. Na pevné záložce **Přidružení průvodci** vyberte **Přidat průvodce**.

        ![Přiřazení průvodce řádku kontrolního seznamu údržby](media/am-guides-integration-add-guide.png "Přiřazení průvodce řádku kontrolního seznamu údržby")

    1. V poli **Název** vyberte průvodce a poté vyberte **Uložit**.

        ![Výběr průvodce v poli Název](media/am-guides-integration-select-guide.png "Výběr průvodce v poli Název")

1. Přidružení šablony kontrolního seznamu údržby typu úlohy:

    1. [Vytvořte typ úlohy údržby](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) nebo vyberte existující typ úlohy údržby.
    1. V podokně akcí vyberte **Výchozí typ úlohy údržby**.

        ![Tlačítko Výchozí hodnoty typu práce údržby](media/am-guides-integration-job-defaults.png "Tlačítko Výchozí hodnoty typu práce údržby")

    1. Vytvořte řádek a vyberte **Uložit**.

        ![Vytvoření řádku](media/am-guides-integration-add-line.png "Vytvoření řádku")

    1. V podokně akcí klikněte na možnost **Kontrolní seznam údržby**.

        ![Tlačítko Kontrolní seznamy údržby](media/am-guides-integration-maintenance-checklist.png "Tlačítko Kontrolní seznamy údržby")

    1. Na pevné záložce **Řádky kontrolního seznamu údržby** přidejte řádek a poté změňte hodnotu pole **Typ** na **Šablona**.

        ![Změna hodnoty typu](media/am-guides-integration-checklist-lines.png "Změna hodnoty typu")

    1. Na pevné záložce **Podrobnosti řádku** v poli **Šablona** vyberte šablonu, s níž jste průvodce spojili, a vyberte **Uložit**.

        ![Výběr šablony](media/am-guides-integration-checklist-line-details.png "Výběr šablony")

1. [Vytvořte pracovní příkaz](work-orders/manually-created-workorders.md#create-work-order) a poté vyberte typ úlohy údržby, který používá šablonu kontrolního seznamu údržby, s níž jste průvodce spojili. Průvodce je automaticky přiřazen k pracovnímu příkazu.

    ![Výběr typu úlohy údržby](media/am-guides-integration-create-work-order.png "Výběr typu úlohy údržby")

1. Podívejte se na průvodce, který je spojen s pracovním příkazem a zaměstnanci:

    1. Otevřete [Mobilní pracovní prostor Správa majetku](asset-management-mobile-workspace.md) pro přístup k pracovnímu příkazu.
    1. [Otevřete kontrolní seznam údržby](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) pro pracovní příkaz.
    1. Vyberte řádek kontrolního seznamu k zobrazení souvisejícího průvodce.

        ![Průvodce spojený s řádkem kontrolního seznamu](media/am-guides-integration-show-guide.png "Průvodce spojený s řádkem kontrolního seznamu")

    1. Otevřete průvodce v aplikaci HoloLens.

        ![Otevřete průvodce v aplikaci HoloLens](media/am-guides-integration-hololens-select.png "Otevření průvodce v aplikaci HoloLens")

> [!NOTE]
> Průvodce můžete také přiřadit přímo do kontrolního seznamu údržby pracovního příkazu nebo typu úlohy.

> [!IMPORTANT]
> Existuje známý problém, že když přiřadíte šablonu kontrolního seznamu údržby k výchozímu typu úlohy údržby, průvodce, který je propojen se šablonou, se nezobrazí na pevné záložce **Přidružení průvodci** stránky **Výchozí typ úlohy údržby**. Průvodce se však zobrazí poté, co se daný typ úlohy použije na pracovní příkaz na pevné záložce **Přidružení průvodci**.

## <a name="see-also"></a>Viz také

- [Přehled dvojitého zápisu](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [Přehled správy majetku](index.md)
