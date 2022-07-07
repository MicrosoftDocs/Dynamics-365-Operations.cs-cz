---
title: Přidání adresy do servisní zakázky
description: Tento článek popisuje postup přidání adresy odběratele do servisní zakázky.
author: sorenva
ms.date: 06/15/2020
ms.topic: article
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c485c50bab7c2e945aa0f0fc0601008dcebd3328
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015718"
---
# <a name="add-an-address-to-a-service-order"></a>Přidání adresy do servisní zakázky

[!include [banner](../includes/banner.md)]

Tento článek popisuje postup přidání adresy odběratele do servisní zakázky. Při vytváření servisní zakázky se informace o adrese přenáší z projektu, ke kterému je servisní zakázka připojena. Pro odběratele, dodavatele, pracoviště, sklady, servisní zakázky a projekty však můžete vybrat alternativní umístění z adres, které jsou již zadány v aplikaci Microsoft Dynamics AX.

Můžete také vytvořit adresy nové. Ve výchozím stavu je nová adresa převedena do projektu. Můžete však zadat, aby nová adresa byla relevantní pouze pro tuto instanci služby. V takovém případě nová adresa do projektu převedena nebude.

## <a name="create-a-customer-address-for-a-service-order"></a>Vytvoření adresy zákazníka pro servisní zakázku

Pro přidání adresy do servisní zakázky postupujte takto:

1. Přejděte na **Správa servisu** \> **Servisní zakázky** \> **Servisní zakázky**.

1. Otevřete servisní zakázku, pro kterou chcete vytvořit adresu.

1. Otevřete kartu **Hlavička**.

1. Rozbalte pevnou záložku **Adresa** a poté vyberte **Přidat adresu** z panelu nástrojů pevné záložky.

1. Ve dialogu **Nová adresa** zadejte jedinečný název adresy a vyplňte zbývající pole. 

    > [!WARNING]
    > Zadáte-li stejný název, jaký používá existující adresa, informace zadané do zbývajících polí přepíší informace pro existující adresu.

1. Výběrem **OK** zkopírujete novou adresu do servisní zakázky.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Zadání alternativní adresy pro servisní zakázku

Pro přidání alternativní adresy do servisní zakázky postupujte takto:

1. Přejděte na **Správa servisu** \> **Servisní zakázky** \> **Servisní zakázky**.

1. Otevřete servisní zakázku, pro kterou chcete zadat alternativní adresu.

1. Otevřete kartu **Hlavička**.

1. Rozbalte pevnou záložku **Adresa** a poté vyberte **Další adresu** z panelu nástrojů pevné záložky.

1. V dialogu **Výběr adresy** vyberte **Servisní zakázky** z rozevíracího seznamu nad mřížkou.

1. Vyberte adresu a pak výběrem **OK** ji zkopírujete do servisní zakázky.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]